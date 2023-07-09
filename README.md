local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()

local Window = OrionLib:MakeWindow({Name = "R.H.R HUB", HidePremium = false, SaveConfig = true, ConfigFolder = "OrionTest"})

local Tab = Window:MakeTab({
	Name = "Main🚹",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

local Section = Tab:AddSection({
	Name = "Defolt"
})

OrionLib:MakeNotification({
	Name = "DETECT",
	Content = "R.H.R SCRIPT is enabled",
	Image = "rbxassetid://4483345998",
	Time = 60
})

Tab:AddSlider({
	Name = "WalkSpeed",
	Min = 12,
	Max = 200,
	Default = 12,
	Color = Color3.fromRGB(255,255,255),
	Increment = 1,
	ValueName = "WS",
	Callback = function(Value)
		game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = Value
	end    
})

Tab:AddSlider({
	Name = "JumpPower",
	Min = 60,
	Max = 500,
	Default = 60,
	Color = Color3.fromRGB(255,255,255),
	Increment = 67,
	ValueName = "WS",
	Callback = function(Value)
		game.Players.LocalPlayer.Character.Humanoid.JumpPower = Value
	end    
})

local Section = Tab:AddSection({
	Name = "Player"
})

Tab:AddButton({
	Name = "ESP",
	Callback = function()
      		while wait(0.5) do
    for i, childrik in ipairs(workspace:GetDescendants()) do
        if childrik:FindFirstChild("Humanoid") then
            if not childrik:FindFirstChild("EspBox") then
                if childrik ~= game.Players.LocalPlayer.Character then
                    local esp = Instance.new("BoxHandleAdornment",childrik)
                    esp.Adornee = childrik
                    esp.ZIndex = 0
                    esp.Size = Vector3.new(4, 5, 1)
                    esp.Transparency = 0.65
                    esp.Color3 = Color3.fromRGB(255,48,48)
                    esp.AlwaysOnTop = true
                    esp.Name = "EspBox"
                end
            end
        end
    end
end
  	end    
})

Tab:AddButton({
	Name = "(FE) Tp part",
	Callback = function()
      		for i,v in pairs(game:GetDescendants()) do
if v.Name == 'Part' then
v.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
end
end

  	end    
})

local Tab = Window:MakeTab({
	Name = "Build a Boat⛵",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

local Section = Tab:AddSection({
	Name = "Farm"
})

Tab:AddButton({
	Name = "Auto farm",
	Callback = function()
      		loadstring(game:HttpGet("https://raw.githubusercontent.com/suno-development/BABFT-Auto-Gold/main/farm.lua", true))()
  	end    
})

local Section = Tab:AddSection({
	Name = "Settings"
})

Tab:AddSlider({
	Name = "Graviti",
	Min = 0,
	Max = 196.2,
	Default = 196.2,
	Color = Color3.fromRGB(255,255,255),
	Increment = 67,
	ValueName = "GR",
	Callback = function(Value)
		game.workspace.Gravity = Value
	end    
})

local Section = Tab:AddSection({
	Name = "Graphics settings"
})

Tab:AddButton({
	Name = "Fix lag",
	Callback = function()
      		      		local ToDisable = {
	Textures = true,
	VisualEffects = true,
	Parts = true,
	Particles = true,
	Sky = true
}

local ToEnable = {
	FullBright = false
}

local Stuff = {}

for _, v in next, game:GetDescendants() do
	if ToDisable.Parts then
		if v:IsA("Part") or v:IsA("Union") or v:IsA("BasePart") then
			v.Material = Enum.Material.SmoothPlastic
			table.insert(Stuff, 1, v)
		end
	end
	
	if ToDisable.Particles then
		if v:IsA("ParticleEmitter") or v:IsA("Smoke") or v:IsA("Explosion") or v:IsA("Sparkles") or v:IsA("Fire") then
			v.Enabled = false
			table.insert(Stuff, 1, v)
		end
	end
	
	if ToDisable.VisualEffects then
		if v:IsA("BloomEffect") or v:IsA("BlurEffect") or v:IsA("DepthOfFieldEffect") or v:IsA("SunRaysEffect") then
			v.Enabled = false
			table.insert(Stuff, 1, v)
		end
	end
	
	if ToDisable.Textures then
		if v:IsA("Decal") or v:IsA("Texture") then
			v.Texture = ""
			table.insert(Stuff, 1, v)
		end
	end
	
	if ToDisable.Sky then
		if v:IsA("Sky") then
			v.Parent = nil
			table.insert(Stuff, 1, v)
		end
	end
end

game:GetService("TestService"):Message("Effects Disabler Script : Successfully disabled "..#Stuff.." assets / effects. Settings :")

for i, v in next, ToDisable do
	print(tostring(i)..": "..tostring(v))
end

if ToEnable.FullBright then
    local Lighting = game:GetService("Lighting")
    
    Lighting.FogColor = Color3.fromRGB(255, 255, 255)
    Lighting.FogEnd = math.huge
    Lighting.FogStart = math.huge
    Lighting.Ambient = Color3.fromRGB(255, 255, 255)
    Lighting.Brightness = 5
    Lighting.ColorShift_Bottom = Color3.fromRGB(255, 255, 255)
    Lighting.ColorShift_Top = Color3.fromRGB(255, 255, 255)
    Lighting.OutdoorAmbient = Color3.fromRGB(255, 255, 255)
    Lighting.Outlines = true
end
  	end    
})

local Section = Tab:AddSection({
	Name = "Rock"
})

Tab:AddButton({
	Name = "Rock Tp (1loca)",
	Callback = function()
      		for i,v in pairs(game:GetDescendants()) do
if v.Name == 'Rock1' then
v.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
end
end
      		for i,v in pairs(game:GetDescendants()) do
if v.Name == 'Rock2' then
v.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
end
end
      		for i,v in pairs(game:GetDescendants()) do
if v.Name == 'Rock3' then
v.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
end
end
  	end    
})

Tab:AddButton({
	Name = "Rock Tp (2loca)",
	Callback = function()
      		for i,v in pairs(game:GetDescendants()) do
if v.Name == 'Gear' then
v.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
end
end
      		for i,v in pairs(game:GetDescendants()) do
if v.Name == 'Rock' then
v.CFrame = game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame
end
end
  	end    
})

local Tab = Window:MakeTab({
	Name = "Ragdoll engine🧞",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

Tab:AddButton({
	Name = "Anti ragdoll",
	Callback = function()
      		local ragdoll = game:GetService("Players").LocalPlayer.Character:FindFirstChild("RagdollMe")
ragdoll:Remove()
local ragdoll = game:GetService("Players").LocalPlayer.Character:FindFirstChild("Pushed")
ragdoll:Remove()

  	end    
})

Tab:AddButton({
	Name = "Push all",
	Callback = function()
      		for i, v in pairs(game.Workspace:GetDescendants()) do
   if string.find(v.Name, "Ragdoll") then
       v:Destroy()
   end
end
game.Workspace.Gravity = math.huge
while task.wait(.2) do
   pcall(
       function()
           for i, v in pairs(game.Players:GetPlayers()) do
               if v.Name == game.Players.LocalPlayer.Name then
               else
                   game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame =
                       game.Players[v.Name].Character.HumanoidRootPart.CFrame * CFrame.new(0, 3, 0)
                   wait(.1)
                   local args = {
                       [1] = game:GetService("Players")[v.Name].Character
                   }
 
                   game:GetService("Players").LocalPlayer.Character.Push.PushTool:FireServer(unpack(args))
               end
           end
       end
   )
end

  	end    
})

Tab:AddButton({
	Name = "Anti fling",
	Callback = function()
      		-- // Constants \\ --
-- [ Services ] --
local Services = setmetatable({}, {__index = function(Self, Index)
local NewService = game.GetService(game, Index)
if NewService then
Self[Index] = NewService
end
return NewService
end})

-- [ LocalPlayer ] --
local LocalPlayer = Services.Players.LocalPlayer

-- // Functions \\ --
local function PlayerAdded(Player)
   local Detected = false
   local Character;
   local PrimaryPart;

   local function CharacterAdded(NewCharacter)
       Character = NewCharacter
       repeat
           wait()
           PrimaryPart = NewCharacter:FindFirstChild("HumanoidRootPart")
       until PrimaryPart
       Detected = false
   end

   CharacterAdded(Player.Character or Player.CharacterAdded:Wait())
   Player.CharacterAdded:Connect(CharacterAdded)
   Services.RunService.Heartbeat:Connect(function()
       if (Character and Character:IsDescendantOf(workspace)) and (PrimaryPart and PrimaryPart:IsDescendantOf(Character)) then
           if PrimaryPart.AssemblyAngularVelocity.Magnitude > 50 or PrimaryPart.AssemblyLinearVelocity.Magnitude > 100 then
               if Detected == false then
                   game.StarterGui:SetCore("ChatMakeSystemMessage", {
                       Text = "Fling Exploit detected, Player: " .. tostring(Player);
                       Color = Color3.fromRGB(255, 200, 0);
                   })
               end
               Detected = true
               for i,v in ipairs(Character:GetDescendants()) do
                   if v:IsA("BasePart") then
                       v.CanCollide = false
                       v.AssemblyAngularVelocity = Vector3.new(0, 0, 0)
                       v.AssemblyLinearVelocity = Vector3.new(0, 0, 0)
                       v.CustomPhysicalProperties = PhysicalProperties.new(0, 0, 0)
                   end
               end
               PrimaryPart.CanCollide = false
               PrimaryPart.AssemblyAngularVelocity = Vector3.new(0, 0, 0)
               PrimaryPart.AssemblyLinearVelocity = Vector3.new(0, 0, 0)
               PrimaryPart.CustomPhysicalProperties = PhysicalProperties.new(0, 0, 0)
           end
       end
   end)
end

-- // Event Listeners \\ --
for i,v in ipairs(Services.Players:GetPlayers()) do
   if v ~= LocalPlayer then
       PlayerAdded(v)
   end
end
Services.Players.PlayerAdded:Connect(PlayerAdded)

local LastPosition = nil
Services.RunService.Heartbeat:Connect(function()
   pcall(function()
       local PrimaryPart = LocalPlayer.Character.PrimaryPart
       if PrimaryPart.AssemblyLinearVelocity.Magnitude > 250 or PrimaryPart.AssemblyAngularVelocity.Magnitude > 250 then
           PrimaryPart.AssemblyAngularVelocity = Vector3.new(0, 0, 0)
           PrimaryPart.AssemblyLinearVelocity = Vector3.new(0, 0, 0)
           PrimaryPart.CFrame = LastPosition

           game.StarterGui:SetCore("ChatMakeSystemMessage", {
               Text = "You were flung. Neutralizing velocity.";
               Color = Color3.fromRGB(255, 0, 0);
           })
       elseif PrimaryPart.AssemblyLinearVelocity.Magnitude < 50 or PrimaryPart.AssemblyAngularVelocity.Magnitude > 50 then
           LastPosition = PrimaryPart.CFrame
       end
   end)
end)
  	end    
})
