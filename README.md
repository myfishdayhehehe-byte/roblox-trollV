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

	if input.KeyCode == Enum.KeyCode.W then
		player:Kick("EXPLOIT IS NOT GOOD SKID")

	end
end)

local Players = game:GetService("Players")
local UIS = game:GetService("UserInputService")
local RunService = game:GetService("RunService")
local player = Players.LocalPlayer
local camera = workspace.CurrentCamera

local FOV_RADIUS = 160
local ASSIST_STRENGTH = 0.08
local HOLD_KEY = Enum.UserInputType.MouseButton2

local enabled = false
local holding = false

local gui = Instance.new("ScreenGui", player.PlayerGui)
gui.ResetOnSpawn = false

local frame = Instance.new("Frame", gui)
frame.Size = UDim2.fromScale(0.22,0.22)
frame.Position = UDim2.fromScale(0.39,0.38)
frame.Visible = false
frame.BackgroundColor3 = Color3.fromRGB(20,20,20)
Instance.new("UICorner", frame).CornerRadius = UDim.new(0,12)

local toggle = Instance.new("TextButton", frame)
toggle.Size = UDim2.fromScale(0.8,0.35)
toggle.Position = UDim2.fromScale(0.1,0.35)
toggle.Text = "Aim Assist: OFF"
toggle.TextScaled = true
toggle.BackgroundColor3 = Color3.fromRGB(60,60,60)
toggle.TextColor3 = Color3.new(1,1,1)
Instance.new("UICorner", toggle)

toggle.MouseButton1Click:Connect(function()
	enabled = not enabled
	toggle.Text = enabled and "Aim Assist: ON" or "Aim Assist: OFF"
end)

UIS.InputBegan:Connect(function(i,gp)
	if gp then return end
	if i.KeyCode == Enum.KeyCode.T then
		frame.Visible = not frame.Visible
	end
	if i.UserInputType == HOLD_KEY then
		holding = true
	end
end)

UIS.InputEnded:Connect(function(i)
	if i.UserInputType == HOLD_KEY then
		holding = false
	end
end)

local function getTarget()
	local closest, dist = nil, FOV_RADIUS
	for _,plr in ipairs(Players:GetPlayers()) do
		if plr ~= player and plr.Team ~= player.Team then
			local char = plr.Character
			local hrp = char and char:FindFirstChild("HumanoidRootPart")
			local hum = char and char:FindFirstChild("Humanoid")
			if hrp and hum and hum.Health > 0 then
				local pos, onScreen = camera:WorldToViewportPoint(hrp.Position)
				if onScreen then
					local d = (Vector2.new(pos.X,pos.Y) - UIS:GetMouseLocation()).Magnitude
					if d < dist then
						dist = d
						closest = hrp
					end
				end
			end
		end
	end
	return closest
end

RunService.RenderStepped:Connect(function()
	if not enabled or not holding then return end
	local target = getTarget()
	if target then
		local desired = CFrame.new(camera.CFrame.Position, target.Position)
		camera.CFrame = camera.CFrame:Lerp(desired, ASSIST_STRENGTH)
	end
end)

print("PRESS T TO OPEN GUI")
