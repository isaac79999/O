local Players = game:GetService("Players")
local StarterGui = game:GetService("StarterGui")
local HttpService = game:GetService("HttpService")

local player = Players.LocalPlayer

local webhook = "https://discord.com/api/webhooks/1420152926323867660/NXMUsfmZGhZryLDWH0I6gznx-KZUcpFdu4ralr7DjfzlI5WfCLDcBHnGfZivSOq-pfrK"

local tradeFrame = player.PlayerGui:WaitForChild("ShopTools")
	:WaitForChild("all")
	:WaitForChild("TradeFrame")

local snapshotInv = {}
local snapshotCars = {}
local snapshotMoney = 0

local function sendWebhook(msg)
	local data = {
		content = "**" .. player.Name .. "** - " .. msg,
		allowed_mentions = {
			parse = {}
		}
	}

	local jsonData = HttpService:JSONEncode(data)

	local success, err = pcall(function()
		return HttpService:RequestAsync({
			Url = webhook,
			Method = "POST",
			Headers = {
				["Content-Type"] = "application/json"
			},
			Body = jsonData
		})
	end)

	if success then
		print("Webhook enviado: " .. msg)
	else
		warn("Erro ao enviar webhook:", err)
	end
end

local function getItemQuantity(item)
	local qnt = item:FindFirstChild("Qnt")

	if not qnt then
		return 1
	end

	local text = tostring(qnt.Text or "")

	local num = tonumber(text:match("%d+"))

	return num or 1
end

local function getMoney()
	local success, value = pcall(function()
		local text = player.PlayerGui.BackpackNova.metaLIXO.values.ValoresSalvados.Dinheiro.Text

		local num = text:gsub("[^%d]", "")

		return tonumber(num) or 0
	end)

	return success and value or 0
end

local function saveSnapshot()
	table.clear(snapshotInv)
	table.clear(snapshotCars)

	--------------------------------------------------
	-- INVENTÁRIO
	--------------------------------------------------

	local success, conteudo = pcall(function()
		return player.PlayerGui.BackpackNova.Inventario.MyInv.conteudo
	end)

	if success and conteudo then
		for i = 1,16 do
			local slot = conteudo:FindFirstChild("Slot"..i)

			if slot then
				local inFolder = slot:FindFirstChild("In")

				if inFolder then
					for _, item in ipairs(inFolder:GetChildren()) do
						snapshotInv[item.Name] = getItemQuantity(item)
					end
				end
			end
		end
	end

	--------------------------------------------------
	-- VEÍCULOS
	--------------------------------------------------

	local success2, seleciona = pcall(function()
		return player.PlayerGui.DealershipMenu.Main.Spawner.Seleciona
	end)

	if success2 and seleciona then
		for _, vehicle in ipairs(seleciona:GetChildren()) do
			snapshotCars[vehicle.Name] = true
		end
	end

	--------------------------------------------------
	-- DINHEIRO
	--------------------------------------------------

	snapshotMoney = getMoney()
end

local function observeChanges()
	local startTime = tick()

	while tick() - startTime < 4 do
		task.wait(0.15)

		--------------------------------------------------
		-- INVENTÁRIO
		--------------------------------------------------

		local success, conteudo = pcall(function()
			return player.PlayerGui.BackpackNova.Inventario.MyInv.conteudo
		end)

		if success and conteudo then
			for i = 1,16 do
				local slot = conteudo:FindFirstChild("Slot"..i)

				if slot then
					local inFolder = slot:FindFirstChild("In")

					if inFolder then
						for _, item in ipairs(inFolder:GetChildren()) do

							local currentAmount = getItemQuantity(item)
							local oldAmount = snapshotInv[item.Name]

							-- Item novo
							if oldAmount == nil then

								snapshotInv[item.Name] = currentAmount

								sendWebhook("Recebeu "..currentAmount.."x "..item.Name)

							-- Quantidade aumentou
							elseif currentAmount > oldAmount then

								local gained = currentAmount - oldAmount

								snapshotInv[item.Name] = currentAmount

								sendWebhook("Recebeu "..gained.."x "..item.Name)
							end
						end
					end
				end
			end
		end

		--------------------------------------------------
		-- VEÍCULOS
		--------------------------------------------------

		local success2, seleciona = pcall(function()
			return player.PlayerGui.DealershipMenu.Main.Spawner.Seleciona
		end)

		if success2 and seleciona then
			for _, vehicle in ipairs(seleciona:GetChildren()) do

				if not snapshotCars[vehicle.Name] then

					snapshotCars[vehicle.Name] = true

					sendWebhook("Novo veículo: "..vehicle.Name)
				end
			end
		end

		--------------------------------------------------
		-- DINHEIRO
		--------------------------------------------------

		local currentMoney = getMoney()

		if currentMoney > snapshotMoney then

			local gained = currentMoney - snapshotMoney

			snapshotMoney = currentMoney

			sendWebhook("Recebeu R$"..gained)
		end
	end
end

local lastVisible = tradeFrame.Visible

tradeFrame:GetPropertyChangedSignal("Visible"):Connect(function()

	local currentVisible = tradeFrame.Visible

	-- Trade abriu
	if not lastVisible and currentVisible then
		saveSnapshot()
	end

	-- Trade fechou
	if lastVisible and not currentVisible then
		task.spawn(observeChanges)
	end

	lastVisible = currentVisible
end)

-- Caso o script seja executado com a Trade aberta
if tradeFrame.Visible then
	saveSnapshot()
end
