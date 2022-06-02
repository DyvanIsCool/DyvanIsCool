
local Library = loadstring(game:HttpGet("https://pastebin.com/raw/vff1bQ9F"))()
local Window = Library.CreateLib("Dyvan", "DarkTheme")



local Tab = Window:NewTab("Script")
local Tab1Section = Tab1:NewSection("Scripts")





Section:NewButton("Inf Jumps", "Enables Inf Jumps", function()
    local InfiniteJumpEnabled = true
game:GetService("UserInputService").JumpRequest:connect(function()
	if InfiniteJumpEnabled then
		game:GetService"Players".LocalPlayer.Character:FindFirstChildOfClass'Humanoid':ChangeState("Jumping")
	end
end)
end)

Section:NewToggle("Fov", "Changes Fov", function(state)
    if state then
        game.Workspace.CurrentCamera.FieldOfView = 120
    else
        game.Workspace.CurrentCamera.FieldOfView = 80
    end
end)

Section:NewSlider("Speed", "Sussy Speed", 250, 120, function(v)
    game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = v
end)

Section:NewButton("Fly", "can control speed and fly", function()
    loadstring("\108\111\97\100\115\116\114\105\110\103\40\103\97\109\101\58\72\116\116\112\71\101\116\40\40\39\104\116\116\112\115\58\47\47\103\105\115\116\46\103\105\116\104\117\98\117\115\101\114\99\111\110\116\101\110\116\46\99\111\109\47\109\101\111\122\111\110\101\89\84\47\98\102\48\51\55\100\102\102\57\102\48\97\55\48\48\49\55\51\48\52\100\100\100\54\55\102\100\99\100\51\55\48\47\114\97\119\47\101\49\52\101\55\52\102\52\50\53\98\48\54\48\100\102\53\50\51\51\52\51\99\102\51\48\98\55\56\55\48\55\52\101\98\51\99\53\100\50\47\97\114\99\101\117\115\37\50\53\50\48\120\37\50\53\50\48\102\108\121\37\50\53\50\48\50\37\50\53\50\48\111\98\102\108\117\99\97\116\111\114\39\41\44\116\114\117\101\41\41\40\41\10\10")()
end)


Section:NewButton("Keyboard", "Working legit", function()
    loadstring(game:HttpGet(('https://raw.githubusercontent.com/manimcool21/Keyboard-FE/main/Protected%20(3).lua'),true))()
end)

Section:NewButton("Ho Ho Hub", "Blox fruit script", function()
    loadstring(game:HttpGet('https://raw.githubusercontent.com/acsu123/HOHO_H/main/Loading_UI'))()
end)

Section:NewButton("Cart rdite", "Script rdite gui", function()
    --Not obfuscated because I don't care
--Works best with the rdite one Idk about the others
 
print("ok cart game troll GUI loaded lmao") --remove if you want
 
local Library = loadstring(game:HttpGet("https://raw.githubusercontent.com/xHeptc/Kavo-UI-Library/main/source.lua"))()
local Window = Library.CreateLib("Cart Ride Into Rdite", "Ocean")
 
--TABS
local Cart = Window:NewTab("Carts")
local Plr = Window:NewTab("Player")
local Setting = Window:NewTab("Info/Setting")
 
--SECTIONS INSIDE TABS
local CartMain = Cart:NewSection("Carts")
local AutoCart = Cart:NewSection("Auto Cart")
 
local PlrMod = Plr:NewSection("Modification")
local PlrTP = Plr:NewSection("Teleports")
 
local SettingGUI = Setting:NewSection("GUI")
 
--CART TAB BEGINS
CartMain:NewButton("Toggle All Carts", "Toggles activation on every cart that is spawned", function()
for i,v in pairs(game.workspace:GetDescendants()) do
if v.Name == "On" then
fireclickdetector(v.Click)
end
end
end)
 
CartMain:NewButton("Speed Up All Carts", "Speeds up every cart", function()
for i,v in pairs(game.workspace:GetDescendants()) do
if v.Name == "Up" then
fireclickdetector(v.Click)
end
end
end)
 
CartMain:NewButton("Slow Down All Carts", "Slows down every cart", function()
for i,v in pairs(game.workspace:GetDescendants()) do
if v.Name == "Down" then
fireclickdetector(v.Click)
end
end
end)
 
CartMain:NewButton("Spawn All Cart", "Spawns Every Cart", function()
for i,v in pairs(game.workspace:GetDescendants()) do
if v.Name == "1Regen" or v.Name == "2Regen" or v.Name == "3Regen" or v.Name == "4Regen" then
fireclickdetector(v.Click)
end
end
end)
 
--AUTO TAB BEGINS
AutoCart:NewToggle("Auto Toggle", "Really Annoying!", function(tog)
if tog == true then
    --yes ik i can just use _G, break or some other shit but nahhh
local TogAutoToggle = Instance.new("Part")
TogAutoToggle.Parent = workspace
TogAutoToggle.Name = "AutoTogSupport"
workspace.AutoTogSupport.Anchored = true
 
while workspace:FindFirstChild("AutoTogSupport") do
wait(.5)
for i,v in pairs(game.workspace:GetDescendants()) do
if v.Name == "On" then
fireclickdetector(v.Click)
end
end
end
     else
workspace.AutoTogSupport:Destroy() --destroys the part to stop the loopðŸ˜±ðŸ˜±ðŸ˜±, real shit ikr
    end
end)
 
AutoCart:NewToggle("Auto Speed Up", "Speeds every cart up super fast", function(tog)
if tog == true then
local TogAutoSpeed = Instance.new("Part")
TogAutoSpeed.Parent = workspace
TogAutoSpeed.Name = "AutoSpeedSupport"
workspace.AutoSpeedSupport.Anchored = true
 
while workspace:FindFirstChild("AutoSpeedSupport") do
wait(.1)
for i,v in pairs(game.workspace:GetDescendants()) do
if v.Name == "Up" then
fireclickdetector(v.Click)
end
end
end
     else
workspace.AutoSpeedSupport:Destroy()
    end
end)
 
AutoCart:NewToggle("Auto Slow Down", "Slows down every cart up super fast", function(tog)
if tog == true then
local TogAutoSlow = Instance.new("Part")
TogAutoSlow.Parent = workspace
TogAutoSlow.Name = "AutoSlowSupport"
workspace.AutoSlowSupport.Anchored = true
 
while workspace:FindFirstChild("AutoSlowSupport") do
wait(.1)
for i,v in pairs(game.workspace:GetDescendants()) do
if v.Name == "Down" then
fireclickdetector(v.Click)
end
end
end
     else
workspace.AutoSlowSupport:Destroy()
    end
end)
 
AutoCart:NewToggle("Auto Spawn Cart", "Spawns every cart in automatically", function(tog)
if tog == true then
local TogSpawnCart = Instance.new("Part")
TogSpawnCart.Parent = workspace
TogSpawnCart.Name = "AutoSpawnCart"
workspace.AutoSpawnCart.Anchored = true
 
while workspace:FindFirstChild("AutoSpawnCart") do
wait(.1)
for i,v in pairs(game.workspace:GetDescendants()) do
if v.Name == "1Regen" or v.Name == "2Regen" or v.Name == "3Regen" or v.Name == "4Regen" then
fireclickdetector(v.Click)
end
end
end
     else
workspace.AutoSpawnCart:Destroy()
    end
end)
 
--PLAYER TAB BEGINS
PlrMod:NewButton("Teleport Tool", "Equip and aim your mouse then click to TP to that position", function()
   mouse = game.Players.LocalPlayer:GetMouse()
tool = Instance.new("Tool")
tool.RequiresHandle = false
tool.Name = "TP Tool"
tool.Activated:connect(function()
local pos = mouse.Hit+Vector3.new(0,2.5,0)
pos = CFrame.new(pos.X,pos.Y,pos.Z)
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = pos
end)
tool.Parent = game.Players.LocalPlayer.Backpack
end)
 
PlrMod:NewButton("Infinite Zoom", "Gives infinite zoom", function()
game.Players.LocalPlayer.CameraMaxZoomDistance = math.huge
end)
 
PlrMod:NewToggle("Infinite Jump", "Lets you jump without cooldown", function(tog)
    if tog then
_G.infinjump = true
local Player = game:GetService("Players").LocalPlayer
local Mouse = Player:GetMouse()
Mouse.KeyDown:connect(function(k)
if _G.infinjump then
if k:byte() == 32 then
Humanoid = game:GetService("Players").LocalPlayer.Character:FindFirstChildOfClass("Humanoid")
Humanoid:ChangeState("Jumping")
wait(0.1)
Humanoid:ChangeState("Seated")
end
end
end)
local Player = game:GetService("Players").LocalPlayer
local Mouse = Player:GetMouse()
    else
if _G.infinjump == true then
_G.infinjump = false
else
_G.infinjump = true
end
end
end)
 
PlrMod:NewButton("Get All Paths", "Gets all the paths", function()
local Hitter = game.Players.LocalPlayer.Character.HumanoidRootPart
for i, v in pairs(workspace:GetDescendants()) do
    if v.Name == "Giver" then
firetouchinterest(Hitter, v, 0)
wait(.1)
firetouchinterest(Hitter, v, 1)
end
end
end)
 
PlrMod:NewTextBox("WalkSpeed", "Type 're' to reset do default", function(txt)
 if txt == "re" then
        game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = 16
        else
game.Players.LocalPlayer.Character.Humanoid.WalkSpeed = txt
end
end)
 
PlrMod:NewTextBox("JumpPower", "Type 're' to reset do default", function(txt)
if txt == "re" then
    game.Players.LocalPlayer.Character.Humanoid.JumpPower = 50
        else
    game.Players.LocalPlayer.Character.Humanoid.JumpPower = txt
end
end)
 
PlrTP:NewButton("TP Spawn", "Teleports your character here", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(44, 13, -76)
end)
 
PlrTP:NewButton("TP Winners", "Teleports your character here", function()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(310, 863, 322)
end)
 
PlrTP:NewButton("TP Cart", "Teleports your character here", function()
for i,v in pairs(game.workspace:GetDescendants()) do
if v.Name == "Seat" then
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(v.Position)
end
end
end)
 
PlrTP:NewTextBox("Goto Player", "Can be shortened", function(txt)
local player = game.Players.LocalPlayer
for i,v in pairs(game.Players:GetChildren()) do
if (string.sub(string.lower(v.Name),1,string.len(txt))) == string.lower(txt) then
txt = v.Name
end
end
 
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = CFrame.new(game.Players[txt].Character.Head.Position)
 
end)
 
SettingGUI:NewKeybind("Toggle", "Shows/Hides GUI when button has been pressed", Enum.KeyCode.E, function()
	Library:ToggleUI()
end)
 
SettingGUI:NewLabel("Get more here: https://discord.gg/2dvx2CQP36")
end)

Section:NewButton("Night Mare Hub", "Fe hats", function()
 loadstring(game:HttpGet(('https://pastefy.ga/lrjtanrp/raw'),true))()
end)


Section:NewButton("Pop It Trading ", "Can Dupe", function()
    loadstring(game:HttpGet(("https://thekillerhood.xyz/cracked/CRACKEDBYKILLERHOOD"),true))()
end)


Section:NewButton("Pop it trading", "Can Buy ben", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/RTHRTHTH3R34/ygygygloloibrahi/main/README.md"))()
end)

Section:NewButton("Titanic Gui", "Can give infinity coins", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/pattingbabies/blora/main/titanicgui"))()
end)

Section:NewButton("Aimbot Gui", "Credits To kiko", function()
    -- Gui to Lua
-- Version: 3.2

-- Instances:

local ScreenGui = Instance.new("ScreenGui")
local Frame = Instance.new("Frame")
local Frame_2 = Instance.new("Frame")
local TextLabel = Instance.new("TextLabel")
local TextButton = Instance.new("TextButton")
local TextButton_2 = Instance.new("TextButton")
local TextLabel_2 = Instance.new("TextLabel")

--Properties:

ScreenGui.Parent = game.Players.LocalPlayer:WaitForChild("PlayerGui")
ScreenGui.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

Frame.Parent = ScreenGui
Frame.BackgroundColor3 = Color3.fromRGB(31, 31, 31)
Frame.BorderColor3 = Color3.fromRGB(16, 16, 16)
Frame.Position = UDim2.new(0.326547235, 0, 0.442340851, 0)
Frame.Size = UDim2.new(0.346905529, 0, 0.194492236, 0)

Frame_2.Parent = Frame
Frame_2.BackgroundColor3 = Color3.fromRGB(24, 24, 24)
Frame_2.BorderColor3 = Color3.fromRGB(16, 16, 16)
Frame_2.Size = UDim2.new(1, 0, 0.26777932, 0)

TextLabel.Parent = Frame_2
TextLabel.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.BackgroundTransparency = 1.000
TextLabel.Size = UDim2.new(1.00234735, 0, 1.08253634, 0)
TextLabel.Font = Enum.Font.SourceSansSemibold
TextLabel.Text = "Arceus | Aimbot"
TextLabel.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel.TextSize = 16.000

TextButton.Parent = Frame_2
TextButton.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextButton.BackgroundTransparency = 1.000
TextButton.Position = UDim2.new(0.92957741, 0, 0, 0)
TextButton.Size = UDim2.new(0.0697798356, 0, 0.991438508, 0)
TextButton.Font = Enum.Font.SourceSansSemibold
TextButton.Text = "_"
TextButton.TextColor3 = Color3.fromRGB(255, 255, 255)
TextButton.TextSize = 14.000

TextButton_2.Parent = Frame
TextButton_2.BackgroundColor3 = Color3.fromRGB(25, 25, 25)
TextButton_2.BorderColor3 = Color3.fromRGB(20, 20, 20)
TextButton_2.Position = UDim2.new(0.0492957756, 0, 0.495575249, 0)
TextButton_2.Size = UDim2.new(0.0469483584, 0, 0.176991165, 0)
TextButton_2.Font = Enum.Font.SourceSansSemibold
TextButton_2.Text = ""
TextButton_2.TextColor3 = Color3.fromRGB(255, 255, 255)
TextButton_2.TextScaled = true
TextButton_2.TextSize = 20.000
TextButton_2.TextWrapped = true

TextLabel_2.Parent = TextButton_2
TextLabel_2.BackgroundColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_2.BackgroundTransparency = 1.000
TextLabel_2.Position = UDim2.new(1.54999995, 0, 0, 0)
TextLabel_2.Size = UDim2.new(17.7999992, 0, 1, 0)
TextLabel_2.Font = Enum.Font.SourceSansSemibold
TextLabel_2.Text = "Aimbot"
TextLabel_2.TextColor3 = Color3.fromRGB(255, 255, 255)
TextLabel_2.TextSize = 16.000
TextLabel_2.TextWrapped = true
TextLabel_2.TextXAlignment = Enum.TextXAlignment.Left

-- Scripts:

local function RPTXOJ_fake_script() -- TextButton.LocalScript 
	local script = Instance.new('LocalScript', TextButton)

	local state = true
	script.Parent.MouseButton1Down:Connect(function()
		print"t"
		state = not state
		local LB_Size = script.Parent.Parent.AbsoluteSize
		local NW_Size = UDim2.new(0, LB_Size.X, 0, LB_Size.Y)
		if not state then
			script.Parent.Text = "+"
			game:GetService("TweenService"):Create(script.Parent.Parent.Parent, TweenInfo.new(0.5, Enum.EasingStyle.Linear), {
				BackgroundTransparency = 1
			}):Play()
			for i, v in pairs(script.Parent.Parent.Parent:GetChildren()) do
				if v:IsA("TextButton") then 
					v.Visible = false
					v.TextLabel.Visible = false
				end
			end
		else
			script.Parent.Text = "_"
			game:GetService("TweenService"):Create(script.Parent.Parent.Parent, TweenInfo.new(0.5, Enum.EasingStyle.Linear), {
				BackgroundTransparency = 0
			}):Play()
			for i, v in pairs(script.Parent.Parent.Parent:GetChildren()) do
				if v:IsA("TextButton") then 
					v.Visible = true
					v.TextLabel.Visible = true
				end
			end
		end
	end)
end
coroutine.wrap(RPTXOJ_fake_script)()
local function CIXXD_fake_script() -- TextButton_2.LocalScript 
	local script = Instance.new('LocalScript', TextButton_2)

	local state = false
	script.Parent.MouseButton1Down:Connect(function()
		state = not state
		if state then 
			script.Parent.Text = "x"
		else
			script.Parent.Text = ""
		end
	end)
	
	local Cam = workspace.CurrentCamera
	
	local hotkey = true
	function lookAt(target, eye)
		Cam.CFrame = CFrame.new(target, eye)
	end
	
	function getClosestPlayerToCursor(trg_part)
		local nearest = nil
		local last = math.huge
		for i,v in pairs(game.Players:GetPlayers()) do
			if v ~= game.Players.LocalPlayer and game.Players.LocalPlayer.Character and v.Character and v.Character:FindFirstChild(trg_part) then
				if game.Players.LocalPlayer.Character:FindFirstChild(trg_part) then
					local ePos, vissss = workspace.CurrentCamera:WorldToViewportPoint(v.Character[trg_part].Position)
					local AccPos = Vector2.new(ePos.x, ePos.y)
					local mousePos = Vector2.new(workspace.CurrentCamera.ViewportSize.x / 2, workspace.CurrentCamera.ViewportSize.y / 2)
					local distance = (AccPos - mousePos).magnitude
					if distance < last and vissss and hotkey and distance < 400 then
						last = distance
						nearest = v
					end
				end
			end
		end
		return nearest
	end
	
	game:GetService("RunService").RenderStepped:Connect(function()
		local closest = getClosestPlayerToCursor("Head")
		if state and closest and closest.Character:FindFirstChild("Head") then
			lookAt(Cam.CFrame.p, closest.Character:FindFirstChild("Head").Position)
		end
	end)
end
coroutine.wrap(CIXXD_fake_script)()
local function QNWNII_fake_script() -- Frame.LocalScript 
	local script = Instance.new('LocalScript', Frame)

	script.Parent.Active = true
	script.Parent.Selectable = true
	script.Parent.Draggable = true
end
coroutine.wrap(QNWNII_fake_script)()
end)


Section:NewButton("Untitled hood Fe admin", "Fe ss made script", function()
    loadstring(game:HttpGet('https://raw.githubusercontent.com/ver-creator/Untitled-Hood-Commands/main/.Lua'))()
end)


Section:NewButton("Fe hat V2", "New .angular function", function()
    --[[Works with any hats!
Commands:
.speed (number)
.mode (number)
.offset (number)
.angular (number)
]]--
local plr = game.Players.LocalPlayer;
local chr = plr.Character;
local hum = chr.Humanoid;
local mov = {};
local mov2 = {};

--[[Network]]
coroutine.resume(coroutine.create(function()
	settings().Physics.AllowSleep = false;
	game.RunService.RenderStepped:Connect(function()
		for i, v in pairs(game.Players:GetPlayers()) do
			if v ~= plr then
				v.MaximumSimulationRadius = 0.1;
				v.SimulationRadius = 0;
			else
				v.MaximumSimulationRadius = math.pow(math.huge, math.huge);
				v.SimulationRadius = math.pow(math.huge, 2);
			end
		end
	end)
end))

function ftp(str)
    local pt = {};
    if str ~= 'me' and str ~= 'random' then
        for i, v in pairs(game.Players:GetPlayers()) do
            if v.Name:lower():find(str:lower()) then
                table.insert(pt, v);
            end
        end
    elseif str == 'me' then
        table.insert(pt, plr);
	elseif str == 'random' then
		table.insert(pt, game.Players:GetPlayers()[math.random(1, #game.Players:GetPlayers())]);
    end
    return pt;
end

local netlessvel = Vector3.new(0, 25.1, 0)
local rs = game:GetService("RunService")
local renderstepped = rs.RenderStepped
local heartbeat = rs.Heartbeat
local function MW_netless(part) --MyWorld#4430 was here (discord.gg/pYVHtSJmEY)
	local vel = part.Velocity
	local con0, con1
	part:GetPropertyChangedSignal("Parent"):Connect(function()
		if part and part.Parent then
			return
		end
		con0:Disconnect()
		con1:Disconnect()
	end)
	con0 = renderstepped:Connect(function()
		part.Velocity = vel
	end)
	con1 = heartbeat:Connect(function()
		vel = part.Velocity
		part.Velocity = netlessvel
	end)
end

for _, v in pairs(hum:GetAccessories()) do
	local b = v.Handle;
	b.CustomPhysicalProperties = PhysicalProperties.new(0, 0, 0, 0, 0);
	b.CanCollide = false;
	b:BreakJoints();
	for _, k in pairs(v:GetChildren()) do
		if not k:IsA'SpecialMesh' and not k:IsA'Part' then
			k:Destroy();
		end
	end
	local still = Instance.new('BodyAngularVelocity', b);
	still.MaxTorque = Vector3.new(math.huge, math.huge, math.huge);
	still.AngularVelocity = Vector3.new(0, 0, 0);
	local align = Instance.new('AlignPosition', b);
	align.MaxForce = 1000000;
	align.MaxVelocity = math.huge;
	align.RigidityEnabled = false;
	align.ApplyAtCenterOfMass = true;
	align.Responsiveness = 200;
	local a0 = Instance.new('Attachment', b);
	local a1 = Instance.new('Attachment', chr.Head);
	align.Attachment0 = a0;
	align.Attachment1 = a1;
	table.insert(mov, a1);
	table.insert(mov2, still);
	MW_netless(b)
end

local par = {};
for _, v in pairs(mov) do
	local parr = Instance.new('Part', workspace);
	parr.Anchored = true;
	parr.Size = Vector3.new(1, 1, 1);
	parr.Transparency = 1;
	parr.CanCollide = false;
	table.insert(par, parr);
end

local rotx = 0;
local rotz = math.pi / 2;
local height = 0;
local heighti = 1;
local offset = 10;
local speed = 0.5;
local mode = 4;
local angular = Vector3.new(0, 0, 0);
local l = 1;
game['Run Service'].RenderStepped:Connect(function()
	rotx = rotx + speed / 100;
	rotz = rotz + speed / 100;
	l = (l >= 360 and 1 or l + speed);
	
	for i, v in pairs(par) do
		v.CFrame = CFrame.new(chr.HumanoidRootPart.Position) * CFrame.fromEulerAnglesXYZ(0, math.rad(l + (360 / #par) * i + speed), 0) * CFrame.new(offset, 0, 0);
	end
	
	if heighti == 1 then
		height = height + speed / 100;
	elseif heighti == 2 then
		height = height - speed / 100;
	end
	if height > 2 then
		heighti = 2;
	end
	if height < -1 then
		heighti = 1;
	end
	
	if mode == 1 then
		for _, v in pairs(mov) do
			v.Position = Vector3.new(math.sin(rotx) * offset, 0, math.sin(rotz) * offset);
		end
	elseif mode == 2 then
		for _, v in pairs(mov) do
			v.Position = Vector3.new(offset, height, offset);
		end
	elseif mode == 3 then
		for _, v in pairs(mov) do
			v.Position = Vector3.new(math.sin(rotx) * offset, height, math.sin(rotz) * offset);
		end
	elseif mode == 4 then
		for i, v in pairs(mov) do
			v.Position = Vector3.new(chr.HumanoidRootPart.CFrame:ToObjectSpace(CFrame.new(par[i].Position)).X, chr.HumanoidRootPart.CFrame:ToObjectSpace(CFrame.new(par[i].Position)).Y, chr.HumanoidRootPart.CFrame:ToObjectSpace(CFrame.new(par[i].Position)).Z);
		end
	elseif mode == 5 then
		for i, v in pairs(mov) do
			v.Position = Vector3.new((math.sin(rotx)) * offset, height, (math.cos(rotz) - i) * offset);
		end
	elseif mode == 6 then
		for i, v in pairs(mov) do
			v.Position = Vector3.new((math.sin(rotx)) * offset, height, (math.tan(rotz) - i) * offset);
		end
	elseif mode == 7 then
		for i, v in pairs(mov) do
			v.Position = Vector3.new(math.cos(rotx * i) * offset, 0, math.cos(rotz * i) * offset);
		end
	elseif mode == 8 then
	    for i, v in pairs(mov) do
			v.Position = Vector3.new(math.sin(rotx) * i * offset, 0, math.sin(rotz) * i * offset);
		end
	elseif mode == 9 then
		pcall(function()
			local so = nil;
			for k, b in pairs(chr:GetChildren()) do
				if b:IsA'Tool' then
					for h, j in pairs(b:GetDescendants()) do
						if j:IsA'Sound' then
							so = j;
						end
					end
				end
			end
			if so ~= nil then
				offset = so.PlaybackLoudness / 35;
				speed = so.PlaybackLoudness / 500;
				angular = Vector3.new(0, so.PlaybackLoudness / 75, 0);
			end
		end)
		for i, v in pairs(mov) do
			v.Position = Vector3.new(chr.HumanoidRootPart.CFrame:ToObjectSpace(CFrame.new(par[i].Position)).X, chr.HumanoidRootPart.CFrame:ToObjectSpace(CFrame.new(par[i].Position)).Y, chr.HumanoidRootPart.CFrame:ToObjectSpace(CFrame.new(par[i].Position)).Z);
		end
	elseif mode == 10 then
		offset = height * 15;
		for i, v in pairs(mov) do
			v.Position = Vector3.new(chr.HumanoidRootPart.CFrame:ToObjectSpace(CFrame.new(par[i].Position)).X, chr.HumanoidRootPart.CFrame:ToObjectSpace(CFrame.new(par[i].Position)).Y, chr.HumanoidRootPart.CFrame:ToObjectSpace(CFrame.new(par[i].Position)).Z);
		end
	elseif mode == 11 then
		for i, v in pairs(mov) do
			v.Position = Vector3.new(chr.HumanoidRootPart.CFrame:ToObjectSpace(CFrame.new(plr:GetMouse().Hit.p)).X, chr.HumanoidRootPart.CFrame:ToObjectSpace(CFrame.new(plr:GetMouse().Hit.p)).Y, chr.HumanoidRootPart.CFrame:ToObjectSpace(CFrame.new(plr:GetMouse().Hit.p)).Z) + Vector3.new(chr.HumanoidRootPart.CFrame:ToObjectSpace(CFrame.new(par[i].Position)).X, chr.HumanoidRootPart.CFrame:ToObjectSpace(CFrame.new(par[i].Position)).Y, chr.HumanoidRootPart.CFrame:ToObjectSpace(CFrame.new(par[i].Position)).Z);
		end
	end
	for _, v in pairs(mov2) do
		v.AngularVelocity = angular;
	end
end)
game.Players.LocalPlayer.Chatted:Connect(function(c)
	if c:split(' ')[1] == '.orbit' then
		for _, v in pairs(mov) do
			chr = ftp(c:split(' ')[2])[1].Character;
			v.Parent = ftp(c:split(' ')[2])[1].Character.HumanoidRootPart;
		end
	end
	if c:split(' ')[1] == '.speed' then
		speed = tonumber(c:split(' ')[2]);
	end
	if c:split(' ')[1] == '.mode' then
		mode = tonumber(c:split(' ')[2]);
	end
	if c:split(' ')[1] == '.offset' then
		offset = tonumber(c:split(' ')[2]);
	end
	if c:split(' ')[1] == '.angular' then
		angular = Vector3.new(tonumber(c:split(' ')[2]), tonumber(c:split(' ')[3]), tonumber(c:split(' ')[4]));
	end
end)
end)






Section:NewButton("Hitbox Gui", "Ok", function()
    loadstring("\108\111\97\100\115\116\114\105\110\103\40\103\97\109\101\58\72\116\116\112\71\101\116\40\39\104\116\116\112\115\58\47\47\112\97\115\116\101\98\105\110\46\99\111\109\47\114\97\119\47\84\117\76\56\53\57\57\77\39\41\41\40\41\10")()
end)















Section:NewButton("Bulked up", "Bulked up script", function()
    loadstring(game:HttpGet(("https://dosage.wtf/files/bulkedup.lua"), true))()
end)


Section:NewButton("Pop it trading 3", "pop it trading gui", function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/Secrethumanbepro/Secrethumanbepro/main/Pop%20it%20trading%20tester",true))()
end)

Section:NewButton("Genesis op", "Genesis for all games", function()
   loadstring(game:HttpGet('https://raw.githubusercontent.com/raw-scriptpastebin/raw/main/B_Genesis'))()
end)

Section:NewButton("Invisible Tool Fe", "Invisible fe", function()
    loadstring(game:HttpGet("https://gist.githubusercontent.com/skid123skidlol/cd0d2dce51b3f20ad1aac941da06a1a1/raw/f58b98cce7d51e53ade94e7bb460e4f24fb7e0ff/%257BFE%257D%2520Invisible%2520Tool%2520(can%2520hold%2520tools)",true))()
end)

Section:NewButton("Project fe", "Project Gelatek", function()
    _G.Velocity = Vector3.new(30,0,0)
loadstring(game:HttpGet("https://raw.githubusercontent.com/Gelatek/ProjectTerm/main/main.lua"))()
end







Section:NewKeybind("Close Q", "Close Q", Enum.KeyCode.Q, function()
    Library:ToggleUI()
end)
