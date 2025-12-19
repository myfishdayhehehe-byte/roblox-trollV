--[[
⠀⠀⠀⣀⣀⣀⡀⠠⠤⠤⠤⠤⠤⠤⠤⠤⠤⠤⠤⢄⣀⣀⠀⠀⠀⠀⠀⠀⠀
⠀⢀⡞⠁⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠉⠑⠒⢄⠀⠀⠀
⠀⠈⡇⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠱⡀⠀
⠀⠀⠘⢎⢰⣄⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⢠⠇⠀
⠀⠀⠀⠀⢳⡈⠛⠂⠤⠤⠤⢀⣀⣀⣀⣀⣀⣀⣀⣀⡀⣀⣠⡀⠄⢠⠁⠀⠀
⠀⢀⣀⣤⡖⠉⠔⢢⡄⣀⣀⡀⠀⠀⠀⠀⠀⠀⠀⠀⠁⠀⠠⡇⣠⠋⠀⠀⠀
⠒⠛⠋⡟⠀⢀⠀⠀⠈⡥⠂⠈⠉⠍⠠⠐⠒⠂⠀⠠⠤⠤⠤⠃⢁⠀⠀⠀⠀
⠀⠀⠀⣇⠀⢸⠀⠀⠀⢇⢠⣀⣀⠀⠀⠀⠤⣀⠀⠀⠀⠀⠀⠀⠀⠑⡶⠀⠀
⠀⠀⠀⠈⠢⣠⠓⢤⡀⢀⡑⠛⠂⠀⠀⠀⢰⠈⠑⠰⠄⠠⡀⠀⠀⣄⠀⠀⠀
⠀⠀⠀⠀⣴⠋⠉⠝⠻⣿⡿⠛⠋⠩⠽⢿⣭⣿⣶⡄⠀⡼⠁⠀⠰⡹⡀⠀⠀
⠀⢠⠴⠛⡇⢸⠁⢊⠃⠆⠂⣤⠀⠀⠀⣤⢠⡬⢀⣣⡾⡴⠀⠀⠀⢷⡵⣄⠀
⠀⠀⠀⠀⠹⡀⠚⣬⣢⠀⠐⠀⠀⠀⠀⠀⠁⠘⠚⡳⣪⠀⢀⠀⠀⠀⣿⡌⡇
⠀⠀⠀⠀⠀⠈⠑⠋⠉⡑⠦⢄⣀⠶⠀⠀⣀⣠⢴⡿⠁⠀⣸⠃⠀⠀⠘⡇⠇
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠳⣦⠀⣈⠉⢻⣉⣿⣱⠿⣀⠀⡰⣗⠀⠀⠀⠀⢧⠇
⠀⠀⠀⠀⠀⠀⠀⠀⣐⣶⠶⠈⣟⢀⣊⠝⣁⣉⠶⠈⢹⡏⠾⣰⣀⡠⠖⠁⠀
⠀⠀⠀⠀⠀⠀⣴⢩⢹⡇⢠⣷⣾⣷⣿⢉⣁⣀⣀⢀⠼⢣⣤⣄⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠿⡑⢸⡇⢸⣿⣿⣿⣿⣷⣶⣿⣿⣿⠁⠀⣣⠮⠥⢷⡄⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠁⢸⡇⢸⣿⣿⠟⣿⣿⣿⣿⡿⠃⠀⢠⡏⣰⠃⠀⠘⣄⠀
⠀⠀⠀⠀⠀⠀⠀⢀⡸⣧⣌⡛⠁⠀⠿⠇⠿⠛⠁⠀⠀⣾⣩⠉⠀⠀⠀⠸⡆
⠀⠀⠀⠀⠀⠀⠀⠠⠤⣿⣿⣿⣿⣶⣶⣶⣦⣤⣤⣤⣸⡏⠁⠀⠀⠀⠀⠀⠀
⠀⠀⠀⠀⠀⠀⠀⠀⠀⠀⠉⠙⠛⠿⠭⠉⠛⠛⠛⠛⠛⠁⠀⠀⠀⠀⠀⠀⠀
]]
local UserInputService = game:GetService("UserInputService")
local Players = game:GetService("Players")

local player = Players.LocalPlayer

UserInputService.InputBegan:Connect(function(input, gameProcessed)
	-- gameProcessed is true if the player is typing in chat or a menu
	if gameProcessed then return end

	if input.KeyCode == Enum.KeyCode.T then
		player:Kick("SKID")
	end
end)
print("PRESS T TO OPEN GUI")
