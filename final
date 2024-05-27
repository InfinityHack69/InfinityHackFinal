local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()

OrionLib:MakeNotification({
	Name = "Loaded",
	Content = "Ready, Hack Version 1.2",
	Image = "rbxassetid://4483345998",
	Time = 5
})

local Window = OrionLib:MakeWindow({Name = "Super Toilet Brawl [Infinity Hack Beta 1.2]", HidePremium = false, SaveConfig = true, ConfigFolder = "OrionTest"})
local Tab = Window:MakeTab({
	Name = "Rage Functions",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

local Section = Tab:AddSection({
	Name = "Functions"
})
Tab:AddButton({
	Name = "Rage",
	Callback = function()
      		local args = {
    [1] = game:GetService("Players").LocalPlayer
}

game:GetService("ReplicatedStorage").Events.RemoteEvents.RageMode:FireServer(unpack(args))
  	end    
})

Tab:AddParagraph("Why doesn't it work?","It only works on those characters who have rage.")
Tab:AddParagraph("How to use it?","Accumulate rage on any character, then it will work.")

local Tab = Window:MakeTab({
	Name = "Player Functions",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

local Section = Tab:AddSection({
	Name = "Functions"
})
Tab:AddButton({
	Name = "Freeze",
	Callback = function()
      		game.Players.LocalPlayer.Character:WaitForChild("HumanoidRootPart").Anchored = true
  	end    
})

Tab:AddButton({
	Name = "UnFreeze",
	Callback = function()
      		game.Players.LocalPlayer.Character:WaitForChild("HumanoidRootPart").Anchored = false
  	end    
})

local CoolSlider = Tab:AddSlider({
	Name = "Speed",
	Min = 5,
	Max = 500,
	Default = 5,
	Color = Color3.fromRGB(255,255,255),
	Increment = 1,
	ValueName = "Speed",
	Callback = function(Value)
        game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = Value
	end    
})

local CoolSlider = Tab:AddSlider({
	Name = "Jump",
	Min = 50,
	Max = 500,
	Default = 50,
	Color = Color3.fromRGB(255,255,255),
	Increment = 1,
	ValueName = "Speed",
	Callback = function(Value)
        game.Players.LocalPlayer.Character.Humanoid.JumpPower = Value
	end    
})

Tab:AddButton({
	Name = "ClickTP",
	Callback = function()
      		local Plr = game:GetService("Players").LocalPlayer
local Mouse = Plr:GetMouse()
 
Mouse.Button1Down:connect(function()
if not game:GetService("UserInputService"):IsKeyDown(Enum.KeyCode.LeftControl) then return end
if not Mouse.Target then return end
Plr.Character:MoveTo(Mouse.Hit.p)
end)
--]]
    game:GetService("StarterGui"):SetCore("SendNotification",{
Title = "CTRL click tp",
Text = "Hold Ctrl then press click to a place you want to teleport to.",
Duration = 6,
    })
local speed = 100 -- set this lower to make it slower
local bodyvelocityenabled = true -- set this to false if you are getting kicked
 
local Imput = game:GetService("UserInputService")
local Plr = game.Players.LocalPlayer
local Mouse = Plr:GetMouse()
 
function To(position)
local Chr = Plr.Character
if Chr ~= nil then
local ts = game:GetService("TweenService")
local char = game.Players.LocalPlayer.Character
local hm = char.HumanoidRootPart
local dist = (hm.Position - Mouse.Hit.p).magnitude
local tweenspeed = dist/tonumber(speed)
local ti = TweenInfo.new(tonumber(tweenspeed), Enum.EasingStyle.Linear)
local tp = {CFrame = CFrame.new(position)}
ts:Create(hm, ti, tp):Play()
if bodyvelocityenabled == true then
local bv = Instance.new("BodyVelocity")
bv.Parent = hm
bv.MaxForce = Vector3.new(100000,100000,100000)
bv.Velocity = Vector3.new(0,0,0)
wait(tonumber(tweenspeed))
bv:Destroy()
end
end
end
 
Imput.InputBegan:Connect(function(input)
   if input.UserInputType == Enum.UserInputType.MouseButton1 and Imput:IsKeyDown(Enum.KeyCode.LeftControl) then
       To(Mouse.Hit.p)
   end
end)
  	end    
})

Tab:AddButton({
	Name = "NoClip",
	Callback = function()
      		local Noclip = nil
local Clip = nil

function noclip()
	Clip = false
	local function Nocl()
		if Clip == false and game.Players.LocalPlayer.Character ~= nil then
			for _,v in pairs(game.Players.LocalPlayer.Character:GetDescendants()) do
				if v:IsA('BasePart') and v.CanCollide and v.Name ~= floatName then
					v.CanCollide = false
				end
			end
		end
		wait(0.21) -- basic optimization
	end
	Noclip = game:GetService('RunService').Stepped:Connect(Nocl)
end

function clip()
	if Noclip then Noclip:Disconnect() end
	Clip = true
end

noclip() -- to toggle noclip() and clip()
  	end    
})

local Tab = Window:MakeTab({
	Name = "Fun Functions",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

local Section = Tab:AddSection({
	Name = "Functions"
})

Tab:AddButton({
	Name = "Stunned",
	Callback = function()
      		-- Create a function to enable flying
local function enableFly(player)
    local humanoid = player.Character and player.Character:FindFirstChild("Humanoid")
    
    if humanoid then
        humanoid.PlatformStand = true
        humanoid.Sit = true
        humanoid.Swim = true
        humanoid.Jump = true
        humanoid.WalkSpeed = 0
        humanoid.Name = "Humanoid_Flying"
    end
end

-- Create a function to disable flying
local function disableFly(player)
    local humanoidFlying = player.Character and player.Character:FindFirstChild("Humanoid_Flying")
    
    if humanoidFlying then
        humanoidFlying.PlatformStand = false
        humanoidFlying.Sit = false
        humanoidFlying.Swim = false
        humanoidFlying.Jump = false
        humanoidFlying.WalkSpeed = 16
        humanoidFlying.Name = "Humanoid"
    end
end

-- Enable flying when 'e' key is pressed
game:GetService("UserInputService").InputBegan:Connect(function(input)
    if input.KeyCode == Enum.KeyCode.E then
        enableFly(game.Players.LocalPlayer)
    end
end)

-- Disable flying when 'f' key is pressed
game:GetService("UserInputService").InputBegan:Connect(function(input)
    if input.KeyCode == Enum.KeyCode.F then
        disableFly(game.Players.LocalPlayer)
    end
end)
  	end    
})

Tab:AddParagraph("Warning","Don't include this with the noclip unless you want to pay with your life.")
Tab:AddParagraph("I clicked, but nothing happened..","Press [E]")

local Tab = Window:MakeTab({
	Name = "Client Functions",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

local Section = Tab:AddSection({
	Name = "Functions"
})
Tab:AddButton({
	Name = "Crash Client",
	Callback = function()
      		local Players = game:GetService("Players")

local LocalPlayer = Players.LocalPlayer
local Character = LocalPlayer.Character
local Humanoid = Character:WaitForChild("Humanoid")

local Animation = Instance.new("Animation", Character)
Animation.AnimationId = "rbxassetid://84315373"

local Track = Humanoid:LoadAnimation(Animation)
Track:Play()
  	end    
})

Tab:AddParagraph("What's it?","The roblox client is just crashing. EVERYONE HAS.")

OrionLib:Init()
