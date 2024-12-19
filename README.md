-- Script para esticar a tela em jogos
-- Este script ajusta a resolução da tela para criar um efeito de esticamento

-- Função para ajustar a resolução
function setResolution(width, height)
    -- Defina a resolução desejada
    local desiredWidth = width or 1920
    local desiredHeight = height or 1080

    -- Obtenha a resolução atual da tela
    local currentWidth, currentHeight = love.graphics.getDimensions()

    -- Calcule a escala necessária para esticar a tela
    local scaleX = desiredWidth / currentWidth
    local scaleY = desiredHeight / currentHeight

    -- Aplique a escala
    love.graphics.scale(scaleX, scaleY)
end

-- Função de desenho principal
function love.draw()
    -- Chame a função para ajustar a resolução
    setResolution(1920, 1080)

    -- Desenhe o conteúdo do jogo aqui
    love.graphics.print("Tela esticada!", 100, 100)
end
