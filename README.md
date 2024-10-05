if game.PlaceId ~= 10524502174 then
    return
end

-- Carrega o Fluent e verifica se foi carregado corretamente
local Fluent = loadstring(game:HttpGet("https://github.com/dawid-scripts/Fluent/releases/latest/download/main.lua"))()
if not Fluent then
    error("Falha ao carregar Fluent!")
else
    print("Fluent carregado com sucesso!")
end

-- Carrega o SaveManager e o InterfaceManager e verifica se foram carregados corretamente
local SaveManager = loadstring(game:HttpGet("https://raw.githubusercontent.com/dawid-scripts/Fluent/master/Addons/SaveManager.lua"))()
local InterfaceManager = loadstring(game:HttpGet("https://raw.githubusercontent.com/dawid-scripts/Fluent/master/Addons/InterfaceManager.lua"))()

if not SaveManager then
    error("Falha ao carregar SaveManager!")
end

if not InterfaceManager then
    error("Falha ao carregar InterfaceManager!")
end

print("SaveManager e InterfaceManager carregados com sucesso!")

-- Cria a janela da UI
local Window = Fluent:CreateWindow({
    Title = "Zetra Hub  ▎ Made By ZetraScripts YT  ▎" .. Fluent.Version,
    SubTitle = "",
    TabWidth = 160,
    Size = UDim2.fromOffset(480, 360),
    Acrylic = true,
    Theme = "Darker",
    MinimizeKey = Enum.KeyCode.LeftControl
})

print("Janela criada com sucesso!")

-- Adiciona abas à janela
local Tabs = {
    Settings = Window:AddTab({ Title = "▎ UI SETTINGS", Icon = "settings" }),
    Others = Window:AddTab({ Title = "▎ OTHERS", Icon = "star" }),
    Utilities = Window:AddTab({ Title = "▎ UTILITIES", Icon = "wrench" }),
    Combat = Window:AddTab({ Title = "▎ COMBAT", Icon = "swords" }),
    Eggs = Window:AddTab({ Title = "▎ EGGS", Icon = "egg" }),
    Teleport = Window:AddTab({ Title = "▎ TELEPORT", Icon = "map" }),
    Visuals = Window:AddTab({ Title = "▎ VISUALS", Icon = "eye" }),
}

-- Configura o SaveManager e InterfaceManager
SaveManager:SetLibrary(Fluent)
InterfaceManager:SetLibrary(Fluent)
SaveManager:IgnoreThemeSettings()
SaveManager:SetIgnoreIndexes({})
InterfaceManager:SetFolder("FluentScriptHub")
SaveManager:SetFolder("FluentScriptHub/specific-game")
InterfaceManager:BuildInterfaceSection(Tabs.Settings)
SaveManager:BuildConfigSection(Tabs.Settings)

-- Seleciona a primeira aba
Window:SelectTab(1)

print("Script executado com sucesso!")

-- Exibe uma notificação inicial
Fluent:Notify({
    Title = "Zetra Hub",
    Content = "Subscribe to the channel",
    SubContent = "ZetraScripts YT",
    Duration = 5
})

print("Notificação exibida!")

    local TeleportSection = Tabs.Teleport:AddSection("TELEPORT TO ALL ZONES")

-- Função de teleporte
local function teleportTo(position)
    game.Players.LocalPlayer.Character:MoveTo(position)
end

Tabs.Teleport:AddButton({ 
    Title = "First Zone", 
    Callback = function()
        teleportTo(Vector3.new(-32, 49, -326))
    end
})

-- Adiciona os botões de teleporte
Tabs.Teleport:AddButton({ 
    Title = "Vaccine Zone", 
    Callback = function()
        teleportTo(Vector3.new(-331, 49, -341))
    end
})

Tabs.Teleport:AddButton({ 
    Title = "Giant Zone", 
    Callback = function()
        teleportTo(Vector3.new(-692, 49, -327))
    end
})

Tabs.Teleport:AddButton({ 
    Title = "Dream Zone", 
    Callback = function()
        teleportTo(Vector3.new(-1132, 49, -316))
    end
})

Tabs.Teleport:AddButton({ 
    Title = "Mosquito Zone", 
    Callback = function()
        teleportTo(Vector3.new(-1607, 49, -325))
    end
})

Tabs.Teleport:AddButton({ 
    Title = "Beast Zone", 
    Callback = function()
        teleportTo(Vector3.new(-1982, 49, -321))
    end
})

Tabs.Teleport:AddButton({ 
    Title = "Evolution Zone", 
    Callback = function()
        teleportTo(Vector3.new(-2365, 49, -290))
    end
})

Tabs.Teleport:AddButton({ 
    Title = "Cyborg Zone", 
    Callback = function()
        teleportTo(Vector3.new(-2427, 50, 107))
    end
})

Tabs.Teleport:AddButton({ 
    Title = "Paradisers Zone", 
    Callback = function()
        teleportTo(Vector3.new(-2427, 49, 677))
    end
})

Tabs.Teleport:AddButton({ 
    Title = "Sonic Zone", 
    Callback = function()
        teleportTo(Vector3.new(-2434, 49, 1179))
    end
})

Tabs.Teleport:AddButton({ 
    Title = "Gym Zone", 
    Callback = function()
        teleportTo(Vector3.new(-2431, 49, 1718))
    end
})

Tabs.Teleport:AddButton({ 
    Title = "Snaike Zone", 
    Callback = function()
        teleportTo(Vector3.new(-2426, 49, 2030))
    end
})

Tabs.Teleport:AddButton({ 
    Title = "Kombi Zone", 
    Callback = function()
        teleportTo(Vector3.new(-2417, 49, 2401))
    end
})

Tabs.Teleport:AddButton({ 
    Title = "Meteor Zone", 
    Callback = function()
        teleportTo(Vector3.new(-2393, 49, 2826))
    end
})

Tabs.Teleport:AddButton({ 
    Title = "Sea Invasion Zone", 
    Callback = function()
        teleportTo(Vector3.new(-2121, 49, 3050))
    end
})

Tabs.Teleport:AddButton({ 
    Title = "Sea King Zone", 
    Callback = function()
        teleportTo(Vector3.new(-1685, 49, 3025))
    end
})

Tabs.Teleport:AddButton({ 
    Title = "Fang Zone", 
    Callback = function()
        teleportTo(Vector3.new(-1221, 50, 3036))
    end
})

Tabs.Teleport:AddButton({ 
    Title = "Megazord Zone", 
    Callback = function()
        teleportTo(Vector3.new(-788, 49, 3038))
    end
})

Tabs.Teleport:AddButton({ 
    Title = "Grojira Zone", 
    Callback = function()
        teleportTo(Vector3.new(-388, 49, 3044))
    end
})

Tabs.Teleport:AddButton({ 
    Title = "GirinoShop Zone", 
    Callback = function()
        teleportTo(Vector3.new(-20, 49, 3048))
    end
})

Tabs.Teleport:AddButton({ 
    Title = "Barril Zone", 
    Callback = function()
        teleportTo(Vector3.new(292, 49, 3037))
    end
})

print("Botões de teleporte adicionados com sucesso!")

-- Parte do ESP
local ESPSection = Tabs.Visuals:AddSection("ESP")

local ESPEnabled = false

-- Função para criar o ESP
local function createESP(player)
    if player.Character and player.Character:FindFirstChild("Head") then
        local BillboardGui = Instance.new("BillboardGui")
        local TextLabel = Instance.new("TextLabel")

        BillboardGui.Name = "ESP"
        BillboardGui.Adornee = player.Character.Head
        BillboardGui.Size = UDim2.new(0, 100, 0, 50)
        BillboardGui.StudsOffset = Vector3.new(0, 2, 0)
        BillboardGui.AlwaysOnTop = true

        TextLabel.Parent = BillboardGui
        TextLabel.Size = UDim2.new(1, 0, 1, 0)
        TextLabel.BackgroundTransparency = 1
        TextLabel.Text = player.Name
        -- Alterando a cor para branco
        TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
        TextLabel.TextScaled = true

        BillboardGui.Parent = player.Character.Head
    end
end

-- Função para remover o ESP
local function removeESP(player)
    if player.Character and player.Character:FindFirstChild("Head") then
        local ESP = player.Character.Head:FindFirstChild("ESP")
        if ESP then
            ESP:Destroy()
        end
    end
end

-- Função para atualizar a distância no ESP
local function updateESP(player)
    if player.Character and player.Character:FindFirstChild("Head") then
        local ESP = player.Character.Head:FindFirstChild("ESP")
        if ESP then
            local distance = math.floor((player.Character.Head.Position - game.Players.LocalPlayer.Character.Head.Position).Magnitude)
            ESP.TextLabel.Text = player.Name .. " [" .. tostring(distance) .. "m]"
        end
    end
end

-- Função para ativar o ESP
local function enableESP()
    for _, player in pairs(game.Players:GetPlayers()) do
        if player ~= game.Players.LocalPlayer then
            createESP(player)
        end
    end

    game.Players.PlayerAdded:Connect(function(player)
        createESP(player)
    end)

    game.Players.PlayerRemoving:Connect(function(player)
        removeESP(player)
    end)

    game:GetService("RunService").RenderStepped:Connect(function()
        for _, player in pairs(game.Players:GetPlayers()) do
            if player ~= game.Players.LocalPlayer then
                updateESP(player)
            end
        end
    end)
end

-- Função para desativar o ESP
local function disableESP()
    for _, player in pairs(game.Players:GetPlayers()) do
        if player.Character and player.Character:FindFirstChild("Head") then
            removeESP(player)
        end
    end
end

-- Toggle para ligar/desligar o ESP com o ESPPlayersToggle
local ESPPlayersToggle = Tabs.Visuals:AddToggle("ESPPlayersToggle", { 
    Title = "ESP All Players", 
    Default = false, 
    Callback = function(value)
        ESPEnabled = value
        if ESPEnabled then
            enableESP()
        else
            disableESP()
        end
    end
})

-- Combate

-- Variável para definir a distância máxima para atacar os Mobs/NPCs
local attackDistance = 20 -- A distância máxima que o jogador precisa estar para atacar

-- Variável para controlar se o ataque automático está ativado
local attackEnabled = false

-- Variável para definir a velocidade de ataque (em segundos)
local attackSpeed = 0.01 -- Velocidade de ataque ajustada para 10 milissegundos

-- Função para verificar os Mobs/NPCs próximos e atacar
local function attackMobs()
    while attackEnabled do
        -- Itera sobre todos os NPCs/Mobs no workspace
        for _, npc in pairs(game.Workspace:GetChildren()) do
            if npc:IsA("Model") and npc:FindFirstChild("Humanoid") and npc:FindFirstChild("HumanoidRootPart") then
                -- Verifica a distância entre o jogador e o NPC
                local distance = (npc.HumanoidRootPart.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
                
                -- Se o NPC estiver dentro da distância de ataque, realiza o ataque
                if distance <= attackDistance then
                    -- Simula o clique para atacar o NPC/Mob
                    game:GetService("VirtualInputManager"):SendMouseButtonEvent(0, 0, 0, true, game, 1)
                    wait(attackSpeed) -- Usa a velocidade de ataque definida
                    game:GetService("VirtualInputManager"):SendMouseButtonEvent(0, 0, 0, false, game, 1)
                end
            end
        end
        wait(0.2) -- Intervalo entre as verificações para evitar sobrecarga
    end
end

-- Adicionando o toggle na aba "Combat"
local AttackNPCToggle = Tabs.Combat:AddToggle("AttackNPCToggle", {
    Title = "Auto Punch",
    Default = false, 
    Callback = function(value)
        attackEnabled = value
        if attackEnabled then
            -- Ativa o ataque automático
            spawn(attackMobs) -- Usa spawn para rodar o ataque em paralelo
        end
    end
})

-- Função para atualizar a lista de jogadores
local function updatePlayerList()
    local playerList = {}
    for _, player in pairs(game.Players:GetPlayers()) do
        table.insert(playerList, player.Name) -- Adiciona o nome do jogador na lista
    end
    return playerList
end

-- Inicializa a variável de jogador selecionado
local selectedPlayer = nil

-- Cria o Dropdown com a lista de jogadores
local PlayerDropdown = Tabs.Combat:AddDropdown("PlayerDropdown", {
    Title = "Select Player",
    Values = updatePlayerList(),
    Multi = false, -- Não permite múltipla seleção
    Default = 1, -- O primeiro jogador será o padrão
    Callback = function(value)
        selectedPlayer = value -- Armazena o jogador selecionado
        print("Jogador selecionado: " .. value)
    end
})

-- Função para atualizar o Dropdown quando jogadores entram ou saem do jogo
local function refreshPlayerDropdown()
    PlayerDropdown:SetValues(updatePlayerList()) -- Atualiza os jogadores no dropdown
    print("Lista de jogadores atualizada!")
end

-- Atualiza a lista de jogadores quando um jogador entra no jogo
game.Players.PlayerAdded:Connect(function()
    refreshPlayerDropdown()
end)

-- Atualiza a lista de jogadores quando um jogador sai do jogo
game.Players.PlayerRemoving:Connect(function()
    refreshPlayerDropdown()
end)

-- Função de teleporte para o jogador selecionado
local function teleportToSelectedPlayer()
    if selectedPlayer then
        local player = game.Players:FindFirstChild(selectedPlayer)
        if player and player.Character and player.Character:FindFirstChild("HumanoidRootPart") then
            -- Teleporta o jogador local para o jogador selecionado
            game.Players.LocalPlayer.Character:MoveTo(player.Character.HumanoidRootPart.Position)
            print("Teleportado para: " .. selectedPlayer)
        else
            print("Jogador não encontrado ou não está no jogo!")
        end
    else
        print("Nenhum jogador selecionado!")
    end
end

-- Adiciona um botão para teleportar para o jogador selecionado
Tabs.Combat:AddButton({
    Title = "Teleport to Selected Player",
    Callback = function()
        teleportToSelectedPlayer()
    end
})

-- Função Anti AFK
local function antiAFK()
    while true do
        wait(60) -- Intervalo de 60 segundos entre as interações
        -- Simula um movimento do mouse ou clique para evitar o AFK
        game:GetService("VirtualInputManager"):SendMouseButtonEvent(0, 0, 0, true, game, 1)
        wait(0.1) -- Breve pausa
        game:GetService("VirtualInputManager"):SendMouseButtonEvent(0, 0, 0, false, game, 1)
    end
end

-- Adiciona toggle para Anti AFK na aba "Utilities"
local AntiAFKToggle = Tabs.Others:AddToggle("AntiAFKToggle", {
    Title = "Anti AFK",
    Default = false,
    Callback = function(value)
        if value then
            spawn(antiAFK) -- Inicia a função Anti AFK em uma nova thread
        end
    end
})

-- Lista de nomes dos NPCs/Objetos que você deseja invocar
local summonNames = {
    "Crab",
    "NomeDoNPC2",
    "NomeDoNPC3",
    -- Adicione mais nomes conforme necessário
}

-- Função para invocar os NPCs/Objetos
local function autoSummon()
    while true do
        wait(2) -- Intervalo entre as invocações, ajuste conforme necessário
        for _, name in pairs(summonNames) do
            local npc = game.Workspace:FindFirstChild(name)
            if npc then
                -- Simula o clique no botão de invocação
                game:GetService("VirtualInputManager"):SendMouseButtonEvent(0, 0, 0, true, game, 1)
                wait(0.1) -- Breve pausa
                game:GetService("VirtualInputManager"):SendMouseButtonEvent(0, 0, 0, false, game, 1)
                break -- Para evitar invocar todos ao mesmo tempo
            end
        end
    end
end

local EggsSection = Tabs.Eggs:AddSection("AUTO EGGS")

-- Adiciona toggle para Auto Summon na aba "Combate"
local AutoSummonToggle = Tabs.Eggs:AddToggle("AutoSummonToggle", {
    Title = "Auto Summon",
    Default = false,
    Callback = function(value)
        if value then
            spawn(autoSummon) -- Inicia a função Auto Summon em uma nova thread
        end
    end
})

-- Lista de nomes dos Meteor Frags que você deseja coletar
local meteorFragNames = {
    "DESTRUCTION METEOR RAID",  -- Substitua pelos nomes corretos dos Meteor Frags
    "Meteor Frag 2",
    "Meteor Frag 3",
    -- Adicione mais nomes conforme necessário
}

-- Função para coletar Meteor Frags automaticamente
local function autoMeteorRaid()
    while true do
        wait(1) -- Intervalo entre as coletas, ajuste conforme necessário
        for _, name in pairs(meteorFragNames) do
            local meteorFrag = game.Workspace:FindFirstChild(name)
            if meteorFrag then
                -- Simula o clique no botão de coleta
                game:GetService("VirtualInputManager"):SendMouseButtonEvent(0, 0, 0, true, game, 1)
                wait(0.1) -- Breve pausa
                game:GetService("VirtualInputManager"):SendMouseButtonEvent(0, 0, 0, false, game, 1)
                break -- Para evitar coletar todos ao mesmo tempo
            end
        end
    end
end

-- Adiciona toggle para Auto Meteor Raid na aba "Combate"
local AutoMeteorRaidToggle = Tabs.Combat:AddToggle("AutoMeteorRaidToggle", {
    Title = "Auto Meteor Raid",
    Default = false,
    Callback = function(value)
        if value then
            spawn(autoMeteorRaid) -- Inicia a função Auto Meteor Raid em uma nova thread
        end
    end
})



-- Adiciona uma seção para Pets na aba "Eggs"
local PetsSection = Tabs.Eggs:AddSection("AUTO EQUIP PETS")

-- Variável para controlar se o Auto Equip está ativado
local autoEquipEnabled = false

-- Função para equipar o melhor pet
local function equipBestPet()
    local player = game.Players.LocalPlayer
    local bestPet = nil
    local bestPetPower = 0

    -- Supondo que os pets estejam armazenados em um objeto dentro do jogador
    local pets = player:FindFirstChild("Pets") -- Mude para o nome correto onde seus pets estão armazenados

    if pets then
        for _, pet in pairs(pets:GetChildren()) do
            -- Aqui você precisa definir como determinar se o pet é o melhor
            -- Por exemplo, verificando a potência do pet ou outro critério
            local petPower = pet:FindFirstChild("Power") and pet.Power.Value or 0 -- Altere conforme a estrutura do seu pet
            
            if petPower > bestPetPower then
                bestPetPower = petPower
                bestPet = pet
            end
        end

        if bestPet then
            -- Equipar o melhor pet (supondo que haja uma função para isso)
            player:FindFirstChild("EquipPet"):Fire(bestPet) -- Ajuste a chamada de acordo com a sua lógica de equipar pets
            print("Equipando o melhor pet: " .. bestPet.Name)
        else
            print("Nenhum pet encontrado!")
        end
    else
        print("Pets não encontrados!")
    end
end

-- Função para gerenciar o auto equip
local function manageAutoEquip()
    while autoEquipEnabled do
        equipBestPet()
        wait(5) -- Intervalo entre as tentativas de equipar (ajuste conforme necessário)
    end
end

-- Toggle para ligar/desligar o Auto Equip de Pets
local AutoEquipToggle = Tabs.Eggs:AddToggle("AutoEquipToggle", { 
    Title = "Auto Equip Best Pet", 
    Default = false, 
    Callback = function(value)
        autoEquipEnabled = value
        if autoEquipEnabled then
            spawn(manageAutoEquip) -- Inicia a função em paralelo
        end
    end
})

local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local humanoid = character:WaitForChild("Humanoid")

-- Define o valor inicial e os limites do slider
local walkSpeed = 16 -- Valor padrão
local minWalkSpeed = 0
local maxWalkSpeed = 100

-- Função para atualizar o WalkSpeed
local function updateWalkSpeed(newSpeed)
    walkSpeed = math.clamp(newSpeed, minWalkSpeed, maxWalkSpeed) -- Limita o valor
    humanoid.WalkSpeed = walkSpeed
    print("WalkSpeed ajustado para: " .. walkSpeed)
end

-- Conecta o evento de pressionar tecla
game:GetService("UserInputService").InputBegan:Connect(function(input, gameProcessedEvent)
    if not gameProcessedEvent then
        if input.KeyCode == Enum.KeyCode.Up then
            updateWalkSpeed(walkSpeed + 5) -- Aumenta a velocidade
        elseif input.KeyCode == Enum.KeyCode.Down then
            updateWalkSpeed(walkSpeed - 5) -- Diminui a velocidade
        end
    end
end)

-- Variável para armazenar o WalkSpeed padrão
local defaultWalkSpeed = 30
local customWalkSpeed = defaultWalkSpeed
local walkSpeedEnabled = false -- Estado do toggle

-- Função para alterar o WalkSpeed
local function setWalkSpeed(speed)
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = speed
end

-- Toggle para ativar/desativar o WalkSpeed customizado
local WalkSpeedToggle = Tabs.Others:AddToggle("WalkSpeedToggle", {
    Title = "WalkSpeed",
    Default = false,
    Callback = function(state)
        walkSpeedEnabled = state
        if walkSpeedEnabled then
            setWalkSpeed(customWalkSpeed) -- Ativa com o valor do slider
        else
            setWalkSpeed(defaultWalkSpeed) -- Reseta para o valor padrão
        end
    end
})

-- Slid
