local TeleportService = game:GetService("TeleportService")
local Players = game:GetService("Players")

local player = Players.LocalPlayer
local placeId = game.PlaceId
local jobId = game.JobId

-- Função para rejoin na mesma instância
local function rejoin()
    TeleportService:TeleportToPlaceInstance(placeId, jobId, player)
end

-- Espera 2 segundos antes de rejoinar (pra garantir que o resto do script terminou)
task.delay(2, rejoin)
