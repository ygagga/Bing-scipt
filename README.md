-- INÍCIO: Configuração Inicial
local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()

-- Criando a interface gráfica
local screenGui = Instance.new("ScreenGui")
local button = Instance.new("TextButton")

-- MEIO: Configuração da Interface Gráfica
screenGui.Parent = player:WaitForChild("PlayerGui")
button.Parent = screenGui
button.Text = "Mudar Cor"
button.Size = UDim2.new(0, 200, 0, 50)
button.Position = UDim2.new(0.5, -100, 0.5, -25)

-- Adicionando funcionalidade ao botão
button.MouseButton1Click:Connect(function()
    game.Workspace.CurrentCamera.BackgroundColor3 = Color3.new(math.random(), math.random(), math.random())
end)

-- Configurando a velocidade de movimento
character.Humanoid.WalkSpeed = 16 -- Velocidade padrão permitida

-- FIM: Finalização e Mensagem de Log
print("Script carregado com sucesso! Interface pronta para uso.")
