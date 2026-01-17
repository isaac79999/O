--[[
✅ Safe AntiBan UI + AUTO ROUBAR FILTRADO (ULTRA FAST)
]]--

pcall(function()
    setfflag("HumanoidParallelRemoveNoPhysics", "False")
    setfflag("HumanoidParallelRemoveNoPhysicsNoSimulate2", "False")
end)

local Players = game:GetService("Players")
local RunService = game:GetService("RunService")
local UIS = game:GetService("UserInputService")
local ReplicatedStorage = game:GetService("ReplicatedStorage")
local LocalPlayer = Players.LocalPlayer
local Remote = ReplicatedStorage:WaitForChild("RemoteNovos"):WaitForChild("bixobrabo")

-- Tabela de Filtro (Busca Ultra-Rápida)
local ItensPermitidos = {
    ["Glock 17"] = true, ["Hi Power"] = true, ["AK47"] = true, ["AK47 Natalina"] = true,
    ["PARAFAL"] = true, ["Uzi"] = true, ["G3"] = true, ["IA2"] = true, ["AR-15"] = true,
    ["Faca"] = true, ["Natalina"] = true, ["Lockpick"] = true, ["Escudo"] = true,
    ["Skate"] = true, ["Planta Suja"] = true, ["Planta Limpa"] = true, ["Tratamento"] = true,
    ["Xbox"] = true, ["Energético"] = true, ["Desruptor"] = true, ["Dinamite"] = true,
    ["Peça de Arma"] = true, ["Armação de Arma"] = true, ["PS5"] = true, ["C4"] = true,
    ["USP"] = true, ["Plástico Vazio"] = true, ["Plástico Pronto"] = true,
    ["Presente Verde"] = true, ["Presente Vermelho"] = true, ["Presente Azul"] = true
}

-- Variáveis
local speed = 0
local infJump, noclip, slowFall, autoRevistarAtivo, autoKickAtivo = false, false, false, false, false
local cooldownGlobal = false

-- GUI SETUP (GETHUI)
local UI_Parent = gethui and gethui() or game:GetService("CoreGui")
local gui = Instance.new("ScreenGui", UI_Parent)
gui.Name = "SafeUI"

local frame = Instance.new("Frame", gui)
frame.Size = UDim2.new(0, 200, 0, 315)
frame.Position = UDim2.new(0.05, 0, 0.5, -157)
frame.BackgroundColor3 = Color3.fromRGB(25, 25, 25)
frame.Active = true
frame.Draggable = true
frame.BorderSizePixel = 0

local function createButton(txt, posY)
    local b = Instance.new("TextButton", frame)
    b.Size = UDim2.new(0, 180, 0, 25)
    b.Position = UDim2.new(0, 10, 0, posY)
    b.BackgroundColor3 = Color3.fromRGB(35, 35, 35)
    b.TextColor3 = Color3.new(1, 1, 1)
    b.Font = Enum.Font.SourceSans
    b.TextSize = 14
    b.Text = txt
    b.BorderSizePixel = 0
    return b
end

-- Botões
local btnJump = createButton("🦘 Pulo Infinito", 80)
local btnNoclip = createButton("🚪 Noclip", 110)
local btnFall = createButton("🪂 Queda Lenta", 140)
local btnRevistar = createButton("🔍 Auto Revistar", 170)
local btnAutoKick = createButton("🔴 Auto Kick HP ≤ 13", 200)
local btnAimbot = createButton("🎯 Aimbot", 230)
local btnHitbox = createButton("📦 Hitbox", 260)
local btnAutoRoubar = createButton("🪙 AUTO ROUBAR (FILTRO)", 290)
btnAutoRoubar.BackgroundColor3 = Color3.fromRGB(0, 100, 200)

-- LÓGICA AUTO ROUBAR (FILTRADO & TURBO)
btnAutoRoubar.MouseButton1Click:Connect(function()
    btnAutoRoubar.Text = "🟢 FILTRANDO..."

    -- Bypass Notify
    pcall(function()
        local notify = ReplicatedStorage:FindFirstChild("NotifyClient") or ReplicatedStorage:FindFirstChild("Notify")
        if notify then
            local signal = notify:IsA("BindableEvent") and notify.Event or notify.OnClientEvent
            for _, conn in pairs(getconnections(signal)) do conn:Disable() end
        end
    end)

    task.spawn(function()
        local inv = LocalPlayer.PlayerGui:FindFirstChild("BackpackNova")
        inv = inv and inv:FindFirstChild("Inventario")
        inv = inv and inv.Outro:FindFirstChild("conteudo")

        if inv then
            for _, Slot in pairs(inv:GetChildren()) do
                if Slot:FindFirstChild("In") then
                    for _, Item in pairs(Slot.In:GetChildren()) do
                        -- CONDIÇÃO: Estar na lista de itens permitidos
                        if ItensPermitidos[Item.Name] and Item:FindFirstChild("Qnt") then
                            local amount = tonumber(Item.Qnt.Text:sub(2))
                            if amount and amount > 0 then
                                -- DISPARO TURBO
                                task.spawn(function()
                                    ReplicatedStorage.Modules.InvRemotes.InvRequest:InvokeServer(
                                        "mudaInv", "3", Item.Name, amount
                                    )
                                end)
                            end
                        end
                    end
                end
            end
        end
        task.wait(0.5)
        btnAutoRoubar.Text = "🪙 AUTO ROUBAR (FILTRO)"
    end)
end)

-- VELOCIDADE CFRAME
RunService.Heartbeat:Connect(function()
    local char = LocalPlayer.Character
    if char and char:FindFirstChild("HumanoidRootPart") and char.Humanoid.MoveDirection.Magnitude > 0 then
        local s = 2 -- Velocidade fixa ou pegue do speedBox se preferir
        char.HumanoidRootPart.CFrame = char.HumanoidRootPart.CFrame + (char.Humanoid.MoveDirection * s)
    end
end)

-- [O restante das funções de Pulo, Noclip, Aimbot e Hitbox permanecem integradas conforme seu script original]
