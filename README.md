-- Script para Brookhaven no Roblox
-- ATENÇÃO: Use scripts apenas em servidores privados ou com permissão.

local player = game.Players.LocalPlayer
local character = player.Character or player.CharacterAdded:Wait()
local humanoid = character:WaitForChild("Humanoid")

-- Função para aumentar a velocidade
local function aumentarVelocidade(novaVelocidade)
    humanoid.WalkSpeed = novaVelocidade
    print("Velocidade aumentada para:", novaVelocidade)
end

-- Função para teleporte
local function teleporte(posicao)
    if character and character:FindFirstChild("HumanoidRootPart") then
        character.HumanoidRootPart.CFrame = CFrame.new(posicao)
        print("Teleportado para:", posicao)
    else
        warn("Não foi possível teleportar. Verifique o personagem.")
    end
end

-- Aumentar velocidade para 100
-- Você pode alterar o valor para o que desejar
print("Aumentando velocidade...")
aumentarVelocidade(100)

-- Teleporte para uma posição específica no mapa
-- Substitua os valores pelas coordenadas desejadas
local posicaoDesejada = Vector3.new(0, 10, 0)
print("Teleportando para a posição desejada...")
teleporte(posicaoDesejada)

-- Observação: Certifique-se de usar este script com responsabilidade e em ambientes permitidos.
