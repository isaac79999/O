--// SERVIÇOS
local Players = game:GetService("Players")
local RunService = game:GetService("RunService")
local ReplicatedStorage = game:GetService("ReplicatedStorage")

local player = Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()

player.CharacterAdded:Connect(function(char)
	character = char
end)

--// REMOTE
local InvRequest = ReplicatedStorage
	:WaitForChild("Modules")
	:WaitForChild("InvRemotes")
	:WaitForChild("InvRequest")

local ENABLED = false

--// UI
local gui = Instance.new("ScreenGui")
gui.Name = "FastAutoFarm"
gui.ResetOnSpawn = false
gui.Parent = player:WaitForChild("PlayerGui")

local frame = Instance.new("Frame")
frame.Size = UDim2.new(0,180,0,75)
frame.Position = UDim2.new(0.5,-90,0.6,0)
frame.BackgroundColor3 = Color3.fromRGB(30,30,30)
frame.Active = true
frame.Draggable = true
frame.Parent = gui

Instance.new("UICorner", frame).CornerRadius = UDim.new(0,12)

local toggle = Instance.new("TextButton")
toggle.Size = UDim2.new(1,-16,1,-16)
toggle.Position = UDim2.new(0,8,0,8)
toggle.BackgroundColor3 = Color3.fromRGB(45,45,45)
toggle.TextColor3 = Color3.new(1,1,1)
toggle.Font = Enum.Font.SourceSansBold
toggle.TextScaled = true
toggle.Text = "ATIVAR"
toggle.Parent = frame

Instance.new("UICorner", toggle).CornerRadius = UDim.new(0,10)

--// PEGAR TOOLS
local function getTools()
	local t = {}

	for _,v in ipairs(player.Backpack:GetChildren()) do
		if v:IsA("Tool") then
			t[#t+1] = v
		end
	end

	return t
end

--// SEGURAR 3 TOOLS
local function equip3()
	local tools = getTools()

	for i = 1,3 do
		local tool = tools[i]

		if tool then
			tool.Parent = character
		end
	end
end

--// LOOP ULTRA RÁPIDO
local connection

local function start()
	connection = RunService.Heartbeat:Connect(function()

		if not ENABLED then
			return
		end

		local backpackCount = 0
		local equippedCount = 0

		for _,v in ipairs(player.Backpack:GetChildren()) do
			if v:IsA("Tool") then
				backpackCount += 1
			end
		end

		for _,v in ipairs(character:GetChildren()) do
			if v:IsA("Tool") then
				equippedCount += 1
			end
		end

		-- SE NÃO TEM TOOL EQUIPADA
		if equippedCount <= 0 then

			-- PEGA 3
			if backpackCount < 3 then
				for i = 1,3 do
					task.spawn(function()
						pcall(function()
							InvRequest:InvokeServer(
								"janemseimais",
								"Cimento"
							)
						end)
					end)
				end
			else
				-- EQUIPA 3 AO MESMO TEMPO
				equip3()
			end
		end
	end)
end

local function stop()
	if connection then
		connection:Disconnect()
		connection = nil
	end
end

--// BOTÃO
toggle.MouseButton1Click:Connect(function()
	ENABLED = not ENABLED

	if ENABLED then
		toggle.Text = "DESATIVAR"
		toggle.BackgroundColor3 = Color3.fromRGB(0,170,0)

		start()
	else
		toggle.Text = "ATIVAR"
		toggle.BackgroundColor3 = Color3.fromRGB(45,45,45)

		stop()
	end
end)
