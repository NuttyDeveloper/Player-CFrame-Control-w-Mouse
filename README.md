local plr = game.Players.LocalPlayer
local Mouse = plr:GetMouse()
local Humanoid = plr.Character:WaitForChild("HumanoidRootPart")

game:GetService("RunService").RenderStepped:Connect(function()
    local mousePos = Vector3.new(Mouse.Hit.p.X, Humanoid.Position.Y, Mouse.Hit.p.Z)
    Humanoid.CFrame = CFrame.new(Humanoid.CFrame.p, mousePos)
end)
