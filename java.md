if game.PlaceId == 2753915549 then

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------print("108/111/97/100/115/116/114/105/110/103/40/34/68/101/99/111/100/101/83/99/114/105/112/116/65/108/116/34/41/44/40/116/114/117/101/41/5if game.PlaceId == 2753915549 then

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local shift = Instance.new("TextButton")
local f9 = Instance.new("TextButton")
local delete = Instance.new("TextButton")
local shift4 = Instance.new("TextButton")
local main = Instance.new("ScreenGui")
local pon = Instance.new("ScreenGui")
local vis = Instance.new("TextButton")
local rj = Instance.new("TextButton")

pon.Parent = game.CoreGui
pon.Name = "Pons"
pon.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

main.Name = "Main"
main.Parent = game.CoreGui
main.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

shift.Name = "shift"
shift.Parent = main
shift.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
shift.BorderSizePixel = 1
shift.BorderColor3 = Color3.fromRGB(255, 160, 30)
shift.Position = UDim2.new(0.200683122, 0, 0, 0)
shift.Size = UDim2.new(0, 50, 0, 50)
shift.Font = Enum.Font.PermanentMarker
shift.Text = "Shift"
shift.TextColor3 = Color3.fromRGB(255, 160, 30)
shift.TextSize = 20.000
shift.TextWrapped = true
shift.MouseButton1Click:Connect(function()
	game:GetService("VirtualInputManager"):SendKeyEvent(true, "RightShift" ,false ,game)
end)

f9.Name = "f9"
f9.Parent = main
f9.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
f9.BorderSizePixel = 1
f9.BorderColor3 = Color3.fromRGB(255, 160, 30)
f9.Position = UDim2.new(0.240683122, 0, 0, 0)
f9.Size = UDim2.new(0, 50, 0, 50)
f9.Font = Enum.Font.PermanentMarker
f9.Text = "f9"
f9.TextColor3 = Color3.fromRGB(255, 160, 30)
f9.TextSize = 35.000
f9.TextWrapped = true
f9.MouseButton1Click:Connect(function()
	game:GetService("VirtualInputManager"):SendKeyEvent(true, "F9" ,false ,game)
end)

delete.Name = "delete"
delete.Parent = main
delete.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
delete.BorderSizePixel = 1
delete.BorderColor3 = Color3.fromRGB(255, 160, 30)
delete.Position = UDim2.new(0.280683122, 0, 0, 0)
delete.Size = UDim2.new(0, 50, 0, 50)
delete.Font = Enum.Font.PermanentMarker
delete.Text = "DEL"
delete.TextColor3 = Color3.fromRGB(255, 160, 30)
delete.TextSize = 35.000
delete.TextWrapped = true
delete.MouseButton1Click:Connect(function()
	main:Destroy()
	pon:Destroy()
end)

vis.Name = "Hide"
vis.Parent = pon
vis.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
vis.BorderSizePixel = 1
vis.BorderColor3 = Color3.fromRGB(255, 160, 30)
vis.Position = UDim2.new(0.320683122, 0, 0, 0)
vis.Size = UDim2.new(0, 50, 0, 50)
vis.Font = Enum.Font.PermanentMarker
vis.Text = "HIDE"
vis.TextColor3 = Color3.fromRGB(255, 160, 30)
vis.TextSize = 20.000
vis.TextWrapped = true
vis.MouseButton1Click:Connect(function()
local maine = game.CoreGui.Main.shift
local del = game.CoreGui.Main.delete
local f9 = game.CoreGui.Main.f9
local rj = game.CoreGui.Main.rj
if maine.Visible == false then
maine.Visible = true
f9.Visible = true
del.Visible = true
rj.Visible = true
		else
			maine.Visible = false
            f9.Visible = false
            del.Visible = false
            rj.Visible = false
		end
end)

rj.Name = "rj"
rj.Parent = main
rj.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
rj.BorderSizePixel = 1
rj.BorderColor3 = Color3.fromRGB(255, 160, 30)
rj.Position = UDim2.new(0.240683122, 0, 0, 0)
rj.Size = UDim2.new(0, 50, 0, 50)
rj.Font = Enum.Font.PermanentMarker
rj.Text = "RJ"
rj.TextColor3 = Color3.fromRGB(255, 160, 30)
rj.TextSize = 35.000
rj.TextWrapped = true
rj.MouseButton1Click:Connect(function()
	if #game.Players:GetPlayers() == 1 then
		game.Players.LocalPlayer:Kick("\nRejoin...")
		wait()
		game:GetService("TeleportService"):Teleport(game.PlaceId, game.Players.LocalPlayer)
	else
		game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId, game.JobId, game.Players.LocalPlayer)
	end
end)

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local OrionLib = loadstring(game:HttpGet(('https://pastebin.com/raw/NDL9HYmx')))()
local Window = OrionLib:MakeWindow({Name = "PoistHub • Sea1", HidePremium = false, SaveConfig = true, ConfigFolder = "PoistHub"})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

--Значения
_G.killaura = true
_G.autochest1 = true
_G.autochest2 = true
_G.autochest3 = true
_G.hitbox = true
_G.automelee = true
_G.autodefense = true
_G.autosword = true
_G.autogun = true
_G.autodevil = true
_G.autorace = true
_G.autobuso = true

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

--Функции

if game.PlaceId == 2753915549 then
World1 = true
elseif game.PlaceId == 4442272183 then
World2 = true
elseif game.PlaceId == 7449423635 then
World3 = true
end

function isnil(thing)
return (thing == nil)
end

local function round(n)
return math.floor(tonumber(n) + 0.5)
end


function UpdateEspPlayer()
if ESPPlayer then
for i,v in pairs(game:GetService("Players"):GetPlayers()) do
if not isnil(v.Character) then
if not v.Character.Head:FindFirstChild('NameEsp'..v.Name) then
local BillboardGui = Instance.new("BillboardGui")
local ESP = Instance.new("TextLabel")
local HealthESP = Instance.new("TextLabel")
BillboardGui.Parent = v.Character.Head
BillboardGui.Name = 'NameEsp'..v.Name
BillboardGui.ExtentsOffset = Vector3.new(0, 1, 0)
BillboardGui.Size = UDim2.new(1,200,1,30)
BillboardGui.Adornee = v.Character.Head
BillboardGui.AlwaysOnTop = true
ESP.Name = "ESP"
ESP.Parent = BillboardGui
ESP.TextTransparency = 0
ESP.BackgroundTransparency = 1
ESP.Size = UDim2.new(0, 200, 0, 30)
ESP.Position = UDim2.new(0,25,0,0)
ESP.Font = Enum.Font.Gotham
ESP.Text = (v.Name ..' '.."[ "..round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Character.Head.Position).Magnitude/3) ..' M'.." ]")
if v.Team == game:GetService("Players").LocalPlayer.Team then
ESP.TextColor3 = Color3.new(255, 160, 30)
else
ESP.TextColor3 = Color3.new(255, 120,30)
end
ESP.TextSize = 14
ESP.TextStrokeTransparency = 0.500
ESP.TextWrapped = true
HealthESP.Name = "HealthESP"
HealthESP.Parent = ESP
HealthESP.TextTransparency = 0
HealthESP.BackgroundTransparency = 1
HealthESP.Position = ESP.Position + UDim2.new(0, -25, 0, 15)
HealthESP.Size = UDim2.new(0, 200, 0, 30)
HealthESP.Font = Enum.Font.Gotham
HealthESP.TextColor3 = Color3.fromRGB(255, 0, 0)
HealthESP.TextSize = 14
HealthESP.TextStrokeTransparency = 0.500
HealthESP.TextWrapped = true
HealthESP.Text = "Level"..v.Data.Level.Value.."Health "..math.floor(v.Character.Humanoid.Health).."/"..math.floor(v.Character.Humanoid.MaxHealth)
else
v.Character.Head['NameEsp'..v.Name].ESP.Text = (v.Name ..' '..round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Character.Head.Position).Magnitude/3) ..' M')
v.Character.Head['NameEsp'..v.Name].ESP.HealthESP.Text = "Level"..v.Data.Level.Value.."Health "..math.floor(v.Character.Humanoid.Health).."/"..math.floor(v.Character.Humanoid.MaxHealth)
v.Character.Head:FindFirstChild('NameEsp'..v.Name).ESP.TextTransparency = 0
v.Character.Head:FindFirstChild('NameEsp'..v.Name).ESP.HealthESP.TextTransparency = 0
end
end
end
else
for i,v in pairs(game:GetService("Players"):GetPlayers()) do
if v.Character.Head:FindFirstChild('NameEsp'..v.Name) then
v.Character.Head:FindFirstChild('NameEsp'..v.Name).ESP.TextTransparency = 1
v.Character.Head:FindFirstChild('NameEsp'..v.Name).ESP.TextStrokeTransparency = 1
v.Character.Head:FindFirstChild('NameEsp'..v.Name).ESP.HealthESP.TextTransparency = 1
v.Character.Head:FindFirstChild('NameEsp'..v.Name).ESP.HealthESP.TextStrokeTransparency = 1
end
end
end
end

function UpdateIslandESP()
for i,v in pairs(game:GetService("Workspace")["_WorldOrigin"].Locations:GetChildren()) do
pcall(function()
if IslandESP then
if v.Name ~= "Sea" then
if not v:FindFirstChild('NameEsp') then
local bill = Instance.new('BillboardGui',v)
bill.Name = 'NameEsp'
bill.ExtentsOffset = Vector3.new(0, 1, 0)
bill.Size = UDim2.new(1,200,1,30)
bill.Adornee = v
bill.AlwaysOnTop = true
local name = Instance.new('TextLabel',bill)
name.Font = "GothamBold"
name.FontSize = "Size14"
name.TextWrapped = true
name.Size = UDim2.new(1,0,1,0)
name.TextYAlignment = 'Top'
name.BackgroundTransparency = 1
name.TextStrokeTransparency = 0.5
name.TextColor3 = Color3.fromRGB(80, 245, 245)
else
v['NameEsp'].TextLabel.Text = (v.Name ..'   \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')
end
end
else
if v:FindFirstChild('NameEsp') then
v:FindFirstChild('NameEsp'):Destroy()
end
end
end)
end
end

function UpdateChestEsp()
for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
pcall(function()
if string.find(v.Name,"Chest") then
if ChestESP then
if string.find(v.Name,"Chest") then
if not v:FindFirstChild('NameEsp'..Number) then
local bill = Instance.new('BillboardGui',v)
bill.Name = 'NameEsp'..Number
bill.ExtentsOffset = Vector3.new(0, 1, 0)
bill.Size = UDim2.new(1,200,1,30)
bill.Adornee = v
bill.AlwaysOnTop = true
local name = Instance.new('TextLabel',bill)
name.Font = "GothamBold"
name.FontSize = "Size14"
name.TextWrapped = true
name.Size = UDim2.new(1,0,1,0)
name.TextYAlignment = 'Top'
name.BackgroundTransparency = 1
name.TextStrokeTransparency = 0.5
name.TextColor3 = Color3.fromRGB(255, 160, 30)
if v.Name == "Chest1" then
name.Text = ("Silver Chest" ..' \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')
end
if v.Name == "Chest2" then
name.Text = ("Gold Chest" ..' \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')
end
if v.Name == "Chest3" then
name.Text = ("Diamond Chest" ..' \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')
end
else
v['NameEsp'..Number].TextLabel.Text = (v.Name ..'   \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')
end
end
else
if v:FindFirstChild('NameEsp'..Number) then
v:FindFirstChild('NameEsp'..Number):Destroy()
end
end
end
end)
end
end

function UpdateBfEsp()
for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
pcall(function()
if DevilFruitESP then
if string.find(v.Name, "Fruit") then
if not v.Handle:FindFirstChild('NameEsp'..Number) then
local bill = Instance.new('BillboardGui',v.Handle)
bill.Name = 'NameEsp'..Number
bill.ExtentsOffset = Vector3.new(0, 1, 0)
bill.Size = UDim2.new(1,200,1,30)
bill.Adornee = v.Handle
bill.AlwaysOnTop = true
local name = Instance.new('TextLabel',bill)
name.Font = "GothamBold"
name.FontSize = "Size14"
name.TextWrapped = true
name.Size = UDim2.new(1,0,1,0)
name.TextYAlignment = 'Top'
name.BackgroundTransparency = 1
name.TextStrokeTransparency = 0.5
name.TextColor3 = Color3.fromRGB(255, 160, 30)
name.Text = (v.Name ..' \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Handle.Position).Magnitude/3) ..' M')
else
v.Handle['NameEsp'..Number].TextLabel.Text = (v.Name ..'   \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Handle.Position).Magnitude/3) ..' M')
end
end
else
if v.Handle:FindFirstChild('NameEsp'..Number) then
v.Handle:FindFirstChild('NameEsp'..Number):Destroy()
end
end
end)
end
end

function topos(Pos)
Distance = (Pos.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
if game.Players.LocalPlayer.Character.Humanoid.Sit == true then game.Players.LocalPlayer.Character.Humanoid.Sit = false end
pcall(function() tween = game:GetService("TweenService"):Create(game.Players.LocalPlayer.Character.HumanoidRootPart,TweenInfo.new(Distance/210, Enum.EasingStyle.Linear),{CFrame = Pos}) end)
tween:Play()
if Distance <= 250 then
tween:Cancel()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Pos
end
if _G.StopTween == true then
tween:Cancel()
_G.Clip = false
end
end

function toClipboard(String)
	local clipBoard = setclipboard or toclipboard or set_clipboard or (Clipboard and Clipboard.set)
	if clipBoard then
		clipBoard(String)
	end
end

local jobId = ''..game.JobId..''
toClipboard(jobId..' если вылетит, вставьте в Join Server этот айди')
	


function getPlayerByNick(nick:string)
    local firstTry;
    local secondTry;
    local thirdTry;
    local fourthTry;
    nick = string.lower(nick)
    local playerList = game.Players:GetPlayers()
    for _,plr in pairs(playerList) do
        if string.lower(plr.Name) == nick then
            firstTry = plr
            break
        end
    end
    for _,plr in pairs(playerList) do
        if string.lower(plr.DisplayName) == nick then
            secondTry = plr
            break
        end
    end
    for _,plr in pairs(playerList) do
        if string.sub(string.lower(plr.Name), 1, #nick) == nick then
            thirdTry = plr
            break
        end
    end
    for _,plr in pairs(playerList) do
        if string.sub(string.lower(plr.DisplayName), 1, #nick) == nick then
            fourthTry = plr
            break
        end
    end
    return firstTry or nick == 'me' and game.Players.LocalPlayer or secondTry or thirdTry or fourthTry
end

function autobuso()
while _G.autobuso == true do
if not game.Players.LocalPlayer.Character:FindFirstChild('HasBuso') then
       game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
       elseif game.Players.LocalPlayer.Character:FindFirstChild('HasBuso') then
print("Buso Activates")
wait(0.5)
end
end
end

function autorace()
while _G.autorace == true do
game:GetService("ReplicatedStorage").Remotes.CommE:FireServer("ActivateAbility")
wait(0.01)
end
end

function automelee()
while _G.automelee == true do
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Melee", 1)
wait(0.01)
end
end

function autodefense()
while _G.autodefense == true do
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Defense", 1)
wait(0.01)
end
end

function autosword()
while _G.autosword == true do
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Sword", 1)
wait(0.01)
end
end

function autogun()
while _G.autogun == true do
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Gun", 1)
wait(0.01)
end
end

function autodevil()
while _G.autodevil == true do
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Demon Fruit", 1)
wait(0.01)
end
end

function autochest1()
while _G.autochest1 == true do
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Workspace.Chest1.CFrame
wait(0.01)
end
end

function autochest2()
while _G.autochest2 == true do
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Workspace.Chest2.CFrame
wait(0.01)
end
end

function autochest3()
while _G.autochest3 == true do
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Workspace.Chest3.CFrame
wait(0.01)
end
end

function killaura()
while _G.killaura == true do
for _,enemy in ipairs(workspace.Enemies:GetDescendants()) do
    if enemy:FindFirstChild('HumanoidRootPart') then
z = enemy.UpperTorso
x = enemy.Head
x:Destroy()
z:Destroy()
wait(.0000001)
end
end
end
end

function hitbox()
while _G.hitbox == true do
for _,enemy in ipairs(workspace.Enemies:GetDescendants()) do
    if enemy:FindFirstChild('HumanoidRootPart') then
local z = enemy.HumanoidRootPart
local x = enemy.Humanoid
        z.Size = Vector3.new(50,50,50)
        z.Shape = "Block"
        z.Transparency = 0.2
        z.Color = Color3.fromRGB(255,160,30)
        z.Material = "ForceField"
        z.CanCollide = false
        z.Anchored = true
        x.Sit = true
       wait(.000000000000001)
    end
end
end
end

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({
	Name = "",
	Icon = "",
	PremiumOnly = false
})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({
	Name = "Tools",
	Icon = "rbxassetid://12496252828",
	PremiumOnly = false
})

local a = game.Lighting
local c = Instance.new("ColorCorrectionEffect", a)
local e = Instance.new("ColorCorrectionEffect", a)
OldAmbient = a.Ambient
OldBrightness = a.Brightness
OldColorShift_Top = a.ColorShift_Top
OldBrightnessc = c.Brightness
OldContrastc = c.Contrast
OldTintColorc = c.TintColor
OldTintColore = e.TintColor
Tab:AddToggle({
	Name = "RTX",
	Default = false,
	Callback = function(Suka)
_G.RTXMode = Suka
if not _G.RTXMode then return end
while _G.RTXMode do wait()
a.Ambient = Color3.fromRGB(33, 33, 33)
a.Brightness = 0.3
c.Brightness = 0.176
c.Contrast = 0.39
c.TintColor = Color3.fromRGB(217, 145, 57)
game.Lighting.FogEnd = 999
if not game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("PointLight") then
local a2 = Instance.new("PointLight")
a2.Parent = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart
a2.Range = 15
a2.Color = Color3.fromRGB(217, 145, 57)
end
if not _G.RTXMode then
a.Ambient = OldAmbient
a.Brightness = OldBrightness
a.ColorShift_Top = OldColorShift_Top
c.Contrast = OldContrastc
c.Brightness = OldBrightnessc
c.TintColor = OldTintColorc
e.TintColor = OldTintColore
game.Lighting.FogEnd = 2500
game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("PointLight"):Destroy()
end
end
end
})

Tab:AddButton({
	Name = "Tp Tool" ,
	Callback = function()
local TpTool = Instance.new("Tool")
	TpTool.Name = "Teleport Tool"
	TpTool.RequiresHandle = false
	TpTool.Parent = game.Players.LocalPlayer.Backpack
	TpTool.Activated:Connect(function()
		local Char = game.Players.LocalPlayer.Character or workspace:FindFirstChild(game.Players.LocalPlayer.Name)
		local HRP = Char and Char:FindFirstChild("HumanoidRootPart")
		if not Char or not HRP then
			return warn("Failed to find HumanoidRootPart")
		end
		HRP.CFrame = CFrame.new(game.Players.LocalPlayer:GetMouse().Hit.X, game.Players.LocalPlayer:GetMouse().Hit.Y + 3, game.Players.LocalPlayer:GetMouse().Hit.Z, select(4, HRP.CFrame:components()))
	end)
end
})

Tab:AddButton({
	Name = "Tween Tp Tool" ,
	Callback = function()
local a = game:GetService("Players").LocalPlayer
            local b = Instance.new('Tool',a.Backpack)
            local g = game:GetService("TweenService")
            b.RequiresHandle = false
            b.Name = "TweenTp"
            b.Activated:connect(function()
            g:Create(
            a.Character:FindFirstChildOfClass("Humanoid").RootPart,
            TweenInfo.new(tonumber(2),Enum.EasingStyle.Linear),
            {CFrame = CFrame.new(a:GetMouse().Hit.Position+Vector3.new(0,5,0))}
            ):Play()
            end)
         end
})

Tab:AddButton({
	Name = "Remote Spy" ,
	Callback = function()
loadstring(game:HttpGet("https://github.com/exxtremestuffs/SimpleSpySource/raw/master/SimpleSpy.lua"))()
  	end    
})

Tab:AddButton({
	Name = "Dex V3" ,
	Callback = function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/Babyhamsta/RBLX_Scripts/main/Universal/BypassedDarkDexV3.lua", true))()
  	end
})

Tab:AddButton({
	Name = "Dex V4" ,
	Callback = function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/peyton2465/Dex/master/out.lua"))()
  	end
})

Tab:AddButton({
	Name = "Big Jump" ,
	Callback = function()
    game.Players.LocalPlayer.PlayerGui.TouchGui.TouchControlFrame.JumpButton.Size = UDim2.new(0,200,0,200)
  	end    
})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({
	Name = "BuyItem",
	Icon = "http://www.roblox.com/asset/?id=12496227758",
	PremiumOnly = false
})

local Section = Tab:AddSection({
	Name = "Abilities"
})

Tab:AddButton({
	Name = "Geppo 10.000$",
	Callback = function()
              game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyHaki", "Geppo")
  	end    
})

Tab:AddButton({
	Name = "Buso 25.000$",
	Callback = function()
      		 game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyHaki", "Buso")
  	end    
})

Tab:AddButton({
	Name = "Soru 100.000$",
	Callback = function()
      		 game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyHaki", "Soru")
  	end
})

Tab:AddButton({
	Name = "Ken 750.000$(need kill shanks)",
	Callback = function()
      		game:GetService("ReplicatedStorage").Remotes.CommE:FireServer("Ken",true)
  	end    
})

local Section = Tab:AddSection({
	Name = "Fighting Styles"
})

Tab:AddButton({
	Name = "Dark Step 250.000$",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBlackLeg" )
  	end    
})

Tab:AddButton({
	Name = "Electro 500.000$",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyElectro" )
  	end    
})

Tab:AddButton({
	Name = "Water Kung-Fu 750.000$",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyFishmanKarate" )
  	end    
})

Tab:AddButton({
	Name = "Dragon Breath",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","DragonClaw","2")
  	end    
})

Tab:AddButton({
	Name = "Superhuman 3.000.000$",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySuperhuman" )
  	end    
})

Tab:AddButton({
	Name = "Death Step 2.500.000$ 2.500F",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyDeathStep" )
  	end    
})

Tab:AddButton({
	Name = "Electric Claw 2.500.000$ 2.500F",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyElectricClaw" )
  	end    
})

Tab:AddButton({
	Name = "Sharkman Karate 2.500.000$ 2.500F",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySharkmanKarate" )
  	end    
})

Tab:AddButton({
	Name = "Dragon Talon 2.500.000$ 2.500F",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyDragonTalon" )
  	end    
})

Tab:AddButton({
	Name = "Godhuman 5.000.000$ 5.000F",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyGodhuman" )
  	end    
})

local Section = Tab:AddSection({
	Name = "Fragments"
})

Tab:AddButton({
	Name = "Check Color Haki Dealer",
	Callback = function()
	OrionLib:MakeNotification({
	Name = "Haki Colors Dealer",
    Content = "".. game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ColorsDealer", "1") .."",
	Image = "rbxassetid://4483345998",
	Time = 5
})
	end
})

Tab:AddButton({
	Name = "Buy Color Buso Haki",
	Callback = function()
	game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ColorsDealer", "2")
	end
})

Tab:AddButton({
	Name = "Ghoul 0F",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Ectoplasm","Change",4)
  	end    
})

Tab:AddButton({
	Name = "Cyborg 2.500F",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("CyborgTrainer","Buy")
  	end    
})

Tab:AddButton({
	Name = "Reset Stats 2.500F",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","Refund","2")
  	end    
})

Tab:AddButton({
	Name = "Race Reroll 3.000F",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","Reroll","2")
  	end    
})

local Section = Tab:AddSection({
	Name = "Bones"
})

Tab:AddButton({
	Name = "Surprise 50bones",
	Callback = function()
      		for i = 1, 10 do
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Bones", "Buy", 1, 1)
            end
  	end    
})

local Section = Tab:AddSection({
	Name = "Swords soon.."
})

local Section = Tab:AddSection({
	Name = "Guns soon.."
})

local Section = Tab:AddSection({
	Name = "Accessories soon.."
})

Tab:AddButton({
	Name = "Tomoe Ring 500.000$",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Tomoe Ring")
end
})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({
	Name = "Farming",
	Icon = "rbxassetid://12505503302",
	PremiumOnly = false
})

Tab:AddToggle({
	Name = "HitBox",
	Default = false,
	Callback = function(lolek)
	_G.hitbox = lolek
hitbox()
		end
})

local Section = Tab:AddSection({
    Name = "START"
})

Tab:AddButton({
	Name = "5Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", "BanditQuest1", 1)
end
})

local Section = Tab:AddSection({
    Name = "JUNGLE"
})

Tab:AddButton({
	Name = "10Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","JungleQuest",1)
end
})

Tab:AddButton({
	Name = "15Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","JungleQuest",2)
end
})

Tab:AddButton({
	Name = "20Lvl [BOSS]",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","JungleQuest",3)    
end
})

local Section = Tab:AddSection({
    Name = "PIRATE VILLAGE"
})

Tab:AddButton({
	Name = "30Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","BuggyQuest1",1)
end
})

Tab:AddButton({
	Name = "50Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","BuggyQuest1",2)
end
})

Tab:AddButton({
	Name = "55Lvl [BOSS]",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","BuggyQuest1",3)
end
})

local Section = Tab:AddSection({
    Name = "DESERT"
})

Tab:AddButton({
	Name = "60Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","DesertQuest",1)
end
})

Tab:AddButton({
	Name = "75Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","DesertQuest",2)
end
})

local Section = Tab:AddSection({
    Name = "SNOW VILLAGE"
})

Tab:AddButton({
	Name = "90Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", "SnowQuest", 1)
end
})

Tab:AddButton({
	Name = "100Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", "SnowQuest", 2)
end
})

Tab:AddButton({
	Name = "105Lvl [BOSS]",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", "SnowQuest", 3)
end
})

local Section = Tab:AddSection({
    Name = "MARINE FORTRESS"
})

Tab:AddButton({
	Name = "120Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", "BanditQuest1", 1)
end
})

Tab:AddButton({
	Name = "130Lvl [BOSS]",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", "BanditQuest1", 1)
end
})

local Section = Tab:AddSection({
    Name = "SKY1"
})

Tab:AddButton({
	Name = "150Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","SkyQuest",1)
end
})

Tab:AddButton({
	Name = "170Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","SkyQuest",2)
end
})

local Section = Tab:AddSection({
    Name = "PRISON"
})

Tab:AddButton({
	Name = "190Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","PrisonerQuest",1)
end
})

Tab:AddButton({
	Name = "210Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","PrisonerQuest",2)
end
})

Tab:AddButton({
	Name = "220Lvl [BOSS]",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","ImpelQuest",1)
end
})

Tab:AddButton({
	Name = "230Lvl [BOS]",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","ImpelQuest",2)
end
})

Tab:AddButton({
	Name = "240Lvl [BOSS]",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","ImpelQuest",3)
end
})

local Section = Tab:AddSection({
    Name = "COLOSSEUM"
})

Tab:AddButton({
	Name = "250Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","ColosseumQuest",1)
end
})

Tab:AddButton({
	Name = "275Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","ColosseumQuest",2)
end
})

local Section = Tab:AddSection({
    Name = "MAGMA VILLAGE"
})

Tab:AddButton({
	Name = "300Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","MagmaQuest",1)
end
})

Tab:AddButton({
	Name = "325Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","MagmaQuest",2)
end
})

Tab:AddButton({
	Name = "350Lvl [BOSS]",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","MagmaQuest",3)
end
})

local Section = Tab:AddSection({
    Name = "UNDERWATER"
})

Tab:AddButton({
	Name = "375Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","FishmanQuest",1)
end
})

Tab:AddButton({
	Name = "400Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","FishmanQuest",2)
end
})

Tab:AddButton({
	Name = "425Lvl [BOSS]",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","FishmanQuest",3)
end
})

local Section = Tab:AddSection({
    Name = "SKY2-3"
})

Tab:AddButton({
	Name = "450Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","SkyExp1Quest",1)
end
})

Tab:AddButton({
	Name = "475Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","SkyExp1Quest",2)
end
})

Tab:AddButton({
	Name = "500Lvl [BOSS]",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","SkyExp1Quest",3)
end
})

Tab:AddButton({
	Name = "525Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", "SkyExp2Quest", 1)
end
})

Tab:AddButton({
	Name = "550Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", "SkyExp2Quest", 2)
end
})

Tab:AddButton({
	Name = "575Lvl [BOSS]",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", "SkyExp2Quest", 3)
end
})

local Section = Tab:AddSection({
    Name = "FOUNTAIN CITY"
})

Tab:AddButton({
	Name = "625Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","FountainQuest",1)
end
})

Tab:AddButton({
	Name = "650Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","FountainQuest",2)
end
})

Tab:AddButton({
	Name = "675Lvl [BOSS]",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","FountainQuest",3)
end
})

--мб дропдауны под секции

Tab:AddButton({
	Name = "Player Quest",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer( "PlayerHunter")
end
})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({
	Name = "Esp",
	Icon = "rbxassetid://12496239839",
	PremiumOnly = false
})

esps = {}

Tab:AddToggle({

    Name = "Fruit ESP",

    Default = false,

    Callback = function(Value) 

        if Value == true then

            fruitNames = {'Fruit ','Kilo Fruit', 'Spin Fruit', 'Chop Fruit', 'Spring Fruit', 'Bomb Fruit', 'Smoke Fruit', 'Spike Fruit', 'Flame Fruit', 'Bird: Falcon Fruit', 'Ice Fruit', 'Sand Fruit', 'Dark Fruit', 'Revive Fruit', 'Diamond Fruit', 'Light Fruit', 'Love Fruit', 'Rubber Fruit', 'Barrier Fruit', 'Magma Fruit', 'Quake Fruit', 'Human: Buddha Fruit', 'String Fruit', 'Bird: Phoenix Fruit', 'Portal Fruit', 'Rumble Fruit', 'Paw Fruit', 'Blizzard Fruit', 'Gravity Fruit', 'Dough Fruit', 'Shadow Fruit', 'Venom Fruit', 'Control Fruit', 'Spirit Fruit', 'Dragon Fruit', 'Leopard Fruit'}

            for key, value in pairs(fruitNames) do

                fruitNames[value] = key

            end



            for _, obj in pairs(workspace:GetChildren()) do

                if fruitNames[obj.Name] then

                    local billBoard = Instance.new("BillboardGui", obj.Handle)

                    local espText = Instance.new("TextLabel", billBoard)

                    

                    billBoard.Adornee = obj.Handle

                    billBoard.AlwaysOnTop = true

                    billBoard.Size = UDim2.new(1,200,1,30)

                    billBoard.Name = "Board"

                    

                    espText.Size = UDim2.new(1,0,1,0)

                    espText.Text = obj.Name

                    espText.TextColor3 = Color3.fromRGB(255,160,30)

                    espText.TextStrokeTransparency = 0

                    espText.BackgroundTransparency = 1

                    espText.TextSize = 10

                    espText.Name = "Text"

                    esps[billBoard] = obj

OrionLib:MakeNotification({

	Name = obj.Name,

	Content = "This fruit was found",

	Image = "rbxassetid://12496254877",

	Time = 10

})

                end

            end

        elseif Value == false then

            for esp, obj in pairs(esps) do

                esp:Destroy()

            end

            esps = {}

        end

    end

})

Tab:AddButton({
	Name = "Tracers",
	Callback = function()
local camera = workspace.CurrentCamera
for _,v in pairs(game.Players:GetPlayers()) do
if v ~= game.Players.LocalPlayer and v.Character ~= nil and v.Character:FindFirstChild("HumanoidRootPart") ~= nil then
local vector,onScreen = camera:WorldToScreenPoint(v.Character.HumanoidRootPart.Position)
local Line = Drawing.new("Line")
Line.Visible = true
Line.From = Vector2.new(camera.ViewportSize.X / 2, camera.ViewportSize.Y / 1)
Line.To = Vector2.new(vector.X, vector.Y)
Line.Color = Color3.fromRGB(255,160,30)
Line.Thickness = 2
Line.Transparency = 1
function script()
game:GetService("RunService").RenderStepped:Connect(function(step)
if v.Character ~= nil and v.Character:FindFirstChild("HumanoidRootPart") ~= nil then
local vector,onScreen = camera:WorldToScreenPoint(v.Character.HumanoidRootPart.Position)
if onScreen == true then
Line.To = Vector2.new(vector.X, vector.Y)
Line.Visible = true
else
Line.Visible = false
end
end
end)
end
coroutine.wrap(script)()
end
v.CharacterAdded:Connect(function()
repeat wait()  until v.Character ~= nil
repeat wait()  until v.Character:FindFirstChild("HumanoidRootPart") ~= nil
local vector,onScreen = camera:WorldToScreenPoint(v.Character.HumanoidRootPart.Position)
local Line = Drawing.new("Line")
Line.Visible = true
Line.From = Vector2.new(camera.ViewportSize.X / 2, camera.ViewportSize.Y / 1)
Line.To = Vector2.new(vector.X, vector.Y)
Line.Color = Color3.fromRGB(255,160,30)
Line.Thickness = 2
Line.Transparency = 1
function script()
game:GetService("RunService").RenderStepped:Connect(function(step)
if v.Character ~= nil and v.Character:FindFirstChild("HumanoidRootPart") ~= nil then
local vector,onScreen = camera:WorldToScreenPoint(v.Character.HumanoidRootPart.Position)
if onScreen == true then
Line.To = Vector2.new(vector.X, vector.Y)
Line.Visible = true
else
Line.Visible = false
end
end
end)
end
coroutine.wrap(script)()
end)
end
end
})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({
	Name = "Fruit",
	Icon = "http://www.roblox.com/asset/?id=12496254877",
	PremiumOnly = false
})

Tab:AddToggle({
	Name = "Tp Fruit",
	Default = false,
	Callback = function(Grab)
_G.BringFruit = Grab
pcall(function()
while _G.BringFruit do wait(.1)
for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
if v:IsA("Tool") then
local OldCFrame = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame
game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = v.Handle.CFrame * CFrame.new(0,0,0)
v.Handle.CFrame = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame
wait(.1)
game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = OldCFrame
end
end
end
end)
end
})

Tab:AddButton({
	Name = "Random Fruit",
	Callback = function()
      		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Cousin", "Buy")
  	end    
})

Tab:AddButton({
	Name = "Fruit Shop",
	Callback = function()
game.Players.LocalPlayer.PlayerGui.Main.FruitShop.Visible = true
  	end
})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({
	Name = "Points",
	Icon = "rbxassetid://12530069729",
	PremiumOnly = false
})

Tab:AddToggle({
	NameA = "uto Melee",
	Default = false,
	Callback = function(Melee1)
	_G.automelee = Melee1
automelee()
		end
})

Tab:AddToggle({
	Name = "Auto Defense",
	Default = false, 
	Callback = function(Defense1)
	_G.autodefense = Defense1
autodefense()
		end
})

Tab:AddToggle({
	Name = "Auto Sword",
	Default = false,
	Callback = function(Sword1)
	_G.autosword = Sword1
autosword()
		end
})

Tab:AddToggle({
	Name = "Auto Gun",
	Default = false,
	Callback = function(Gun1)
	_G.autogun = Gun1
autogun()
		end
})

Tab:AddToggle({
	Name = "Auto Devil Fruit",
	Default = false,
	Callback = function(Devil1)
	_G.autodevil = Devil1
autodevil()
		end
})

Tab:AddTextbox({
	Name = "Melee",
	Default = nil,
	TextDisappear = true,
	Callback = function(Melee)
		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Melee", Melee) 
	end	  
})

Tab:AddTextbox({
	Name = "Defense",
	Default = nil,
	TextDisappear = true,
	Callback = function(Defense)
		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Defense", Defense)
	end
})

Tab:AddTextbox({
	Name = "Sword",
	Default = nil,
	TextDisappear = true,
	Callback = function(Sword)
		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Sword", Sword)
	end
})

Tab:AddTextbox({
	Name = "Gun",
	Default = nil,
	TextDisappear = true,
	Callback = function(Gun)
		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Gun", Gun)
	end
})

Tab:AddTextbox({
	Name = "Devil Fruit",
	Default = nil,
	TextDisappear = true,
	Callback = function(Devil)
		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Demon Fruit", Devil)
	end
})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({
	Name =  "GUIs soon...",
	Icon = "rbxassetid://12505501154",
	PremiumOnly = false
})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({
	Name =  "Any Auto",
	Icon = "rbxassetid://12505499132",
	PremiumOnly = false
})

Tab:AddButton({
	Name = "Auto Sea2 testing..",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("DressrosaQuestProgress","Detective")
wait(.00001)
topos(CFrame.new(1349.4, 37.5, -1326.2))
wait(.1)
local z = game.Players.LocalPlayer.Backpack.Key
z.Parent = game.Players.LocalPlayer.Character
end
})

Tab:AddToggle({
	Name = "Auto Silver Chest",
	Default = false,
	Callback = function(Chest1)
	_G.autochest1 = Chest1
autochest1()
		end
})

Tab:AddToggle({
	Name = "Auto Gold Chest",
	Default = false,
	Callback = function(Chest2)
	_G.autochest2 = Chest2
autochest2()
		end
})

Tab:AddToggle({
	Name = "Auto Diamond Chest",
    Default = false,
	Callback = function(Chest3)
	_G.autochest3 = Chest3
autochest3()
		end
})

Tab:AddToggle({
	Name = "Auto Buso",
	Default = false,
	Callback = function(Toggle1)
	_G.autobuso = Toggle1
autobuso()
		end
})

Tab:AddToggle({
	Name = "Auto Race",
	Default = false,
	Callback = function(Toggle5)
	_G.autorace = Toggle5
autorace()
		end
})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({
	Name = "Teleport",
	Icon = "rbxassetid://12496230420",
	PremiumOnly = false
})

local Section = Tab:AddSection({
	Name = "Servers"
})

Tab:AddButton({
	Name = "Server Id",
	Callback = function()
    jobId = ''..game.JobId..''
	toClipboard(jobId)
	OrionLib:MakeNotification({
	Name = "Server ID copied to clipboard!",
	Content = "Paste this in Server Join Id",
	Image = "rbxassetid://4483345998",
	Time = 5
})
end
})

Tab:AddTextbox({
	Name = "Join Id Server",
	Default = ""..game.JobId.."",
	TextDisappear = true,
	Callback = function(Ponon)
		game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId,Ponon,game.Players.LocalPlayer)
	end
})

Tab:AddButton({
	Name = "Rejoin",
	Callback = function()
if #game.Players:GetPlayers() == 1 then
		game.Players.LocalPlayer:Kick("\nRejoin...")
		wait()
		game:GetService("TeleportService"):Teleport(game.PlaceId, game.Players.LocalPlayer)
	else
		game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId, game.JobId, game.Players.LocalPlayer)
	end
  	end
})

Tab:AddButton({
	Name = "Server Hop",
	Callback = function()
loadstring(game:HttpGet"https://raw.githubusercontent.com/LeoKholYt/roblox/main/lk_serverhop.lua")():Teleport(game.PlaceId)
  	end    
})

local Section = Tab:AddSection({
	Name = "Worlds"
})

Tab:AddButton({
	Name = "Sea1",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TravelMain")
  	end
})

Tab:AddButton({
	Name = "Sea2",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TravelDressrosa")
  	end
})

Tab:AddButton({
	Name = "Sea3",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TravelZou")
  	end    
})

local Section = Tab:AddSection({
	Name = "Settings"
})

Tab:AddButton({
	Name = "Stop Tween",
	Callback = function()
topos(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame)
end
})

local Section = Tab:AddSection({
	Name = "Islands"
})

Tab:AddButton({
	Name = "Marine Start",
	Callback = function()
topos(CFrame.new(-2566.4296875, 6.8556680679321, 2045.2561035156))
end
})

Tab:AddButton({
	Name = "Pirate Start",
	Callback = function()
topos(CFrame.new(979.79895019531, 16.516613006592, 1429.0466308594))
end
})

Tab:AddButton({
	Name = "Jungle",
	Callback = function()
topos(CFrame.new(-1612.7957763672, 36.852081298828, 149.12843322754))
end
})

Tab:AddButton({
	Name = "Pirate Village",
	Callback = function()
topos(CFrame.new(-1181.3093261719, 4.7514905929565, 3803.5456542969))
end
})

Tab:AddButton({
	Name = "Desert",
	Callback = function()
topos(CFrame.new(944.15789794922, 20.919729232788, 4373.3002929688))
end
})

Tab:AddButton({
	Name = "Snow Village",
	Callback = function()
topos(CFrame.new(1347.8067626953, 104.66806030273, -1319.7370605469))
end
})

Tab:AddButton({
	Name = "Marine Fortress",
	Callback = function()
topos(CFrame.new(-4914.8212890625, 50.963626861572, 4281.0278320313))
end
})

Tab:AddButton({
	Name = "Sky1",
	Callback = function()
topos(CFrame.new(-4869.1025390625, 733.46051025391, -2667.0180664063))
end
})

Tab:AddButton({
	Name = "Sky2",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-4607.82275, 872.54248, -1667.55688))
  	end    
})

Tab:AddButton({
	Name = "Sky3",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-7894.6176757813, 5547.1416015625, -380.29119873047))
  	end    
})

Tab:AddButton({

	Name = "Prison",
	Callback = function()
topos( CFrame.new(4875.330078125, 5.6519818305969, 734.85021972656))
end
})

Tab:AddButton({
	Name = "Colloseum",
	Callback = function()
topos( CFrame.new(-1427.6203613281, 7.2881078720093, -2792.7722167969))
end
})

Tab:AddButton({
	Name = "Magma Village",
	Callback = function()
topos(CFrame.new(-5247.7163085938, 12.883934020996, 8504.96875))
end
})

Tab:AddButton({
	Name = "Under Water City",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(61163.8515625, 11.6796875, 1819.7841796875))
end
})

Tab:AddButton({
	Name = "Fountain City",
	Callback = function()
topos(CFrame.new(5411.8, 188.9, 4281.4))
end
})

Tab:AddButton({
	Name = "Mob Island",
	Callback = function()
topos( CFrame.new(-1503.6224365234, 219.7956237793, 1369.3101806641))
end
})

Tab:AddButton({
	Name = "Shank Room",
	Callback = function()
topos(CFrame.new(-1442.16553, 29.8788261, -28.3547478))
end
})

Tab:AddButton({
	Name = "Middle Town",
	Callback = function()
topos(CFrame.new(-2850.20068, 7.39224768, 5354.99268))
end
})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({
	Name = "Boats",
	Icon = "rbxassetid://12496247656",
	PremiumOnly = false
})

local Section = Tab:AddSection({
	Name = "Pirate"
})

Tab:AddButton({
	Name = "Pirate Sloop 600$",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "PirateSloop")
  	end
})

Tab:AddButton({
	Name = "Pirate Basic 1.000$",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "PirateBasic")
   	end    
})

Tab:AddButton({
	Name = "Pirate Brigade 4.000$",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "PirateBrigade")
  	end    
})

local Section = Tab:AddSection({
	Name = "Marine"
})

Tab:AddButton({
	Name = "Marine Sloop 150$",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "MarineSloop")
  	end
})

Tab:AddButton({
	Name = "Marine Basic 600$",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "MarineBasic")
  	end
})

Tab:AddButton({
	Name = "MarineBrigade 2.000$",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "MarineBrigade")
  	end
})

local Section = Tab:AddSection({
	Name = "Luxury"
})

Tab:AddButton({
	Name = "RocketBoost 0$",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "RocketBoost")
  	end
})

Tab:AddButton({
	Name = "Enforcer 1.000$",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "Enforcer")
  	end
})

Tab:AddButton({
	Name = "Swan 5.000$",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "Swan")
  	end
})

Tab:AddButton({
	Name = "Flower 5.000$",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "Flower")
  	end    
})

Tab:AddButton({
	Name = "Sleigh 5.000$",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "Sleigh")
  	end
})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({
	Name = "Fast Cmd soon...",
	Icon = "rbxassetid://12496242729",
	PremiumOnly = false
})    

Tab:AddTextbox({
	Name = "Textbox",
	Default = "soon...",
	TextDisappear = true,
	Callback = function(Cmd)
		if Cmd == pon then
print("pon")
elseif Cmd == pon1 then
print("pon1")
end
	end
})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({
	Name = "Combat soon..",
	Icon = "rbxassetid://12496236549",
	PremiumOnly = false
})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({
	Name = "Raids soon..",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({
	Name = "Troll",
	Icon = "rbxassetid://12505494337",
	PremiumOnly = false
})

Tab:AddToggle({
	Name = "Freeze",
	Default = nil,
	Callback = function(Value1)
	if Value1 == true then   game.Players.LocalPlayer.Character.HumanoidRootPart.Anchored = true
elseif Value1 == false then
game.Players.LocalPlayer.Character.HumanoidRootPart.Anchored = false
	end 
end   
})

Tab:AddButton({
	Name = "Sit",
	Callback = function()
game.Players.LocalPlayer.Character.Humanoid.Sit = true
  	end
})

Tab:AddButton({
	Name = "Lay Down",
	Callback = function()
local Human = game.Players.LocalPlayer.Character and game.Players.LocalPlayer.Character:FindFirstChildOfClass('Humanoid')
	if not Human then
		return
	end
	Human.Sit = true
	task.wait(.1)
	Human.RootPart.CFrame = Human.RootPart.CFrame * CFrame.Angles(math.pi * .5, 0, 0)
	for _, v in ipairs(Human:GetPlayingAnimationTracks()) do
		v:Stop()
	end
  	end  
})

Tab:AddTextbox({
	Name = "Spin",
	Default = nil,
	TextDisappear = true,
	Callback = function(SPINN)
		function getRoot(char)
	local rootPart = char:FindFirstChild('HumanoidRootPart') or char:FindFirstChild('Torso') or char:FindFirstChild('UpperTorso')
	return rootPart
end
local Spin = Instance.new("BodyAngularVelocity")
	Spin.Name = "Spinning"
	Spin.Parent = getRoot(game.Players.LocalPlayer.Character)
	Spin.MaxTorque = Vector3.new(0, math.huge, 0)
	Spin.AngularVelocity = Vector3.new(0, SPINN, 0)
	end
})

Tab:AddButton({
	Name = "Stop Spin",
	Callback = function()
function getRoot(char)
	local rootPart = char:FindFirstChild('HumanoidRootPart') or char:FindFirstChild('Torso') or char:FindFirstChild('UpperTorso')
	return rootPart
end
for i,v in pairs(getRoot(game.Players.LocalPlayer.Character):GetChildren()) do
		if v.Name == "Spinning" then
			v:Destroy()
		end
	end
  	end
})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({
	Name = "Codes soon...",
	Icon = "rbxassetid://12496297350",
	PremiumOnly = false
})  

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({
	Name = "Player Settings",
	Icon = "rbxassetid://12496250171",
	PremiumOnly = false
})

Tab:AddTextbox({
	Name = "Chat",
	Default = "Chat",
	TextDisappear = true,
	Callback = function(Say)
		game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(Say,"All")
	end	 
})

Tab:AddDropdown({
	Name = "Buso State",
	Default = nil,
	Options = {"0", "1", "2", "3", "4", "5"},
	Callback = function(statebuso)
		if statebuso == "0" then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ChangeBusoStage",0)
elseif statebuso == "1" then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ChangeBusoStage",1)
elseif statebuso == "2" then 
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ChangeBusoStage",2)
elseif statebuso == "3" then 
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ChangeBusoStage",3)
elseif statebuso == "4" then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ChangeBusoStage",4)
elseif statebuso == "5" then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ChangeBusoStage",5)
	end
	end
})

Tab:AddTextbox({
	Name = "Ken Range",
	Default = "Ken Range(30k+ lag)",
	TextDisappear = true,
	Callback = function(KenRange)
		game.Players.LocalPlayer.VisionRadius.Value = KenRange
	end	 
})

Tab:AddButton({
	Name = "Reset",
	Callback = function()
game.Players.LocalPlayer.Character:BreakJoints()
  	end
})

Tab:AddTextbox({
	Name = "Title",
	Default = "Title",
	TextDisappear = true,
	Callback = function(title)
		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateTitle", title)
	end
})

Tab:AddButton({
	Name = "Pirates",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetTeam", "Pirates")
  	end
})

Tab:AddButton({
	Name = "Marines",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetTeam", "Marines")
  	end
})

Tab:AddDropdown({
	Name = "Buso Color",
	Default = nil,
	Options = {"Rainbow Saviour","Winter Sky", "Pure Red", "Snow White","Absolute Zero","Fiery Rose","Heat Wave","Plump Purple","Blue Jeans","Green Lizard","Slimy Green","Yellow Sunshine","Bright Yellow","Orange Soda"},
	Callback = function(busoColor)
if busoColor == "Rainbow Saviour" then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Rainbow Saviour")
   elseif busoColor == "Winter Sky" then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Winter Sky")
   elseif busoColor == "Pure Red" then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Pure Red")
   elseif busoColor == "Snow White" then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Snow White")
   elseif busoColor == "Absolute Zero" then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Absolute Zero")
   elseif busoColor == "Heat Wave" then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Heat Wave")
   elseif busoColor == "Fiery Rose" then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Fiery Rose")
   elseif busoColor == "Plump Purple" then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Plump Purple")
   elseif busoColor == "Blue Jeans" then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Blue Jeans")
   elseif busoColor == "Green Lizard" then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Green Lizard")
   elseif busoColor == "Slimy Green" then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Slimy Green")
   elseif busoColor == "Yellow Sunshine" then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Yellow Sunshine")
   elseif busoColor == "Bright Yellow" then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Bright Yellow")
   elseif busoColor == "Orange Soda" then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Orange Soda")
end
end
})

Tab:AddTextbox({
	Name = "Mastery info",
	Default = nil,
	TextDisappear = true,
	Callback = function(plrName1)
     for _,obj in pairs(getPlayerByNick(plrName1).Backpack:GetChildren()) do
    if obj.ClassName == 'Tool' then
        OrionLib:MakeNotification({
	Name = "Stats",
	Content = 'Name:'.. obj.Name ..'| Mastery:'.. obj.Level.Value ..'.',
	Image = "rbxassetid://4483345998",
	Time = 15
})
end	  
end
end
})

Tab:AddTextbox({
    Name = "Check Stats",
    Default = nil,
    TextDisappear = true,
    Callback = function(plrName)
        OrionLib:MakeNotification({
            Name = "Beli:"..getPlayerByNick(plrName).Data.Beli.Value.."Frags:"..getPlayerByNick(plrName).Data.Fragments.Value..'.',
            Content = "Player's stats",
            Image = "rbxassetid://12496227758",
            Time = 10
        })
    end
})

Tab:AddButton({
	Name = "Check Accessories Info",
	Callback = function()
OrionLib:MakeNotification({
	Name = ''.. game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Nerd") ..'',
	Content = "Nerd",
	Image = "rbxassetid://4483345998",
	Time = 5
})
end
})

Tab:AddButton({
	Name = "X-ray",
	Callback = function()
local sc = (debug and debug.setconstant) or setconstant
	local gc = (debug and debug.getconstants) or getconstants
local pop = game.Players.LocalPlayer.PlayerScripts.PlayerModule.CameraModule.ZoomController.Popper
	for _, v in pairs(getgc()) do
		if type(v) == 'function' and getfenv(v).script == pop then
			for i, v1 in pairs(gc(v)) do
				if tonumber(v1) == .25 then
					sc(v, i, 0)
				elseif tonumber(v1) == 0 then
					sc(v, i, .25)
				end
			end
		end
	end
end
})

Tab:AddButton({
	Name = "No Fog",
	Callback = function()
game.Lighting.FogEnd = 100000
	for i,v in pairs(Lighting:GetDescendants()) do
		if v:IsA("Atmosphere") then
			v:Destroy()
		end
	end
end
})

Tab:AddButton({
	Name = "MaxZoom inf",
	Callback = function()
game.Players.LocalPlayer.CameraMaxZoomDistance = 999999
end
})

Tab:AddButton({
	Name = "MaxZoom normal",
	Callback = function()
game.Players.LocalPlayer.CameraMaxZoomDistance = 100
end
})

конец

local shift = Instance.new("TextButton")
local f9 = Instance.new("TextButton")
local delete = Instance.new("TextButton")
local shift4 = Instance.new("TextButton")
local main = Instance.new("ScreenGui")
local pon = Instance.new("ScreenGui")
local vis = Instance.new("TextButton")
local rj = Instance.new("TextButton")

pon.Name = "Pons"
pon.Parent = game.CoreGui
pon.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

main.Name = "Keyboard gui"
main.Parent = game.CoreGui
main.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

shift.Name = "shift"
shift.Parent = main
shift.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
shift.BorderSizePixel = 1
shift.BorderColor3 = Color3.fromRGB(255, 160, 30)
shift.Position = UDim2.new(0.200683122, 0, 0, 0)
shift.Size = UDim2.new(0, 50, 0, 50)
shift.Font = Enum.Font.PermanentMarker
shift.Text = "Shift"
shift.TextColor3 = Color3.fromRGB(255, 160, 30)
shift.TextSize = 20.000
shift.TextWrapped = true
shift.MouseButton1Click:Connect(function()
	game:GetService("VirtualInputManager"):SendKeyEvent(true, "RightShift" ,false ,game)
end)

f9.Name = "f9"
f9.Parent = main
f9.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
f9.BorderSizePixel = 1
f9.BorderColor3 = Color3.fromRGB(255, 160, 30)
f9.Position = UDim2.new(0.240683122, 0, 0, 0)
f9.Size = UDim2.new(0, 50, 0, 50)
f9.Font = Enum.Font.PermanentMarker
f9.Text = "f9"
f9.TextColor3 = Color3.fromRGB(255, 160, 30)
f9.TextSize = 35.000
f9.TextWrapped = true
f9.MouseButton1Click:Connect(function()
	game:GetService("VirtualInputManager"):SendKeyEvent(true, "F9" ,false ,game)
end)

delete.Name = "delete"
delete.Parent = main
delete.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
delete.BorderSizePixel = 1
delete.BorderColor3 = Color3.fromRGB(255, 160, 30)
delete.Position = UDim2.new(0.280683122, 0, 0, 0)
delete.Size = UDim2.new(0, 50, 0, 50)
delete.Font = Enum.Font.PermanentMarker
delete.Text = "DEL"
delete.TextColor3 = Color3.fromRGB(255, 160, 30)
delete.TextSize = 35.000
delete.TextWrapped = true
delete.MouseButton1Click:Connect(function()
	main:Destroy()
	pon:Destroy()
end)

vis.Name = "Hide"
vis.Parent = pon
vis.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
vis.BorderSizePixel = 1
vis.BorderColor3 = Color3.fromRGB(255, 160, 30)
vis.Position = UDim2.new(0.320683122, 0, 0, 0)
vis.Size = UDim2.new(0, 50, 0, 50)
vis.Font = Enum.Font.PermanentMarker
vis.Text = "HIDE"
vis.TextColor3 = Color3.fromRGB(255, 160, 30)
vis.TextSize = 20.000
vis.TextWrapped = true
vis.MouseButton1Click:Connect(function()
local maine = game.CoreGui.Main.shift
local del = game.CoreGui.Main.delete
local f9 = game.CoreGui.Main.f9
local rj = game.CoreGui.Main.rj
if maine.Visible == false then
maine.Visible = true
f9.Visible = true
del.Visible = true
rj.Visible = true
		else
			maine.Visible = false
            f9.Visible = false
            del.Visible = false
            rj.Visible = false
		end
end)

rj.Name = "rj"
rj.Parent = main
rj.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
rj.BorderSizePixel = 1
rj.BorderColor3 = Color3.fromRGB(255, 160, 30)
rj.Position = UDim2.new(0.240683122, 0, 0, 0)
rj.Size = UDim2.new(0, 50, 0, 50)
rj.Font = Enum.Font.PermanentMarker
rj.Text = "RJ"
rj.TextColor3 = Color3.fromRGB(255, 160, 30)
rj.TextSize = 35.000
rj.TextWrapped = true
rj.MouseButton1Click:Connect(function()
	if #game.Players:GetPlayers() == 1 then
		game.Players.LocalPlayer:Kick("\nRejoin...")
		wait()
		game:GetService("TeleportService"):Teleport(game.PlaceId, game.Players.LocalPlayer)
	else
		game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId, game.JobId, game.Players.LocalPlayer)
	end
end)

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local OrionLib = loadstring(game:HttpGet(('https://pastebin.com/raw/NDL9HYmx')))()
local Window = OrionLib:MakeWindow({Name = "PoistHub • Sea1", HidePremium = false, SaveConfig = true, ConfigFolder = "PoistHub"})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

--Значения
_G.killaura = true
_G.autochest1 = true
_G.autochest2 = true
_G.autochest3 = true
_G.hitbox = true
_G.automelee = true
_G.autodefense = true
_G.autosword = true
_G.autogun = true
_G.autodevil = true
_G.autorace = true
_G.autobuso = true

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

--Функции
if game.PlaceId == 2753915549 then
World1 = true
elseif game.PlaceId == 4442272183 then
World2 = true
elseif game.PlaceId == 7449423635 then
World3 = true
end

function CheckQuest()
MyLevel = game:GetService("Players").LocalPlayer.Data.Level.Value
if World1 then
if MyLevel == 1 or MyLevel <= 9 then
Mon = "Bandit [Lv. 5]"
LevelQuest = 1
NameQuest = "BanditQuest1"
NameMon = "Bandit"
CFrameQuest = CFrame.new(1059.37195, 15.4495068, 1550.4231, 0.939700544, -0, -0.341998369, 0, 1, -0, 0.341998369, 0, 0.939700544)
elseif MyLevel == 10 or MyLevel <= 14 then
Mon = "Monkey [Lv. 14]"
LevelQuest = 1
NameQuest = "JungleQuest"
NameMon = "Monkey"
CFrameQuest = CFrame.new(-1598.08911, 35.5501175, 153.377838, 0, 0, 1, 0, 1, -0, -1, 0, 0)
elseif MyLevel == 15 or MyLevel <= 29 then
Mon = "Gorilla [Lv. 20]"
LevelQuest = 2
NameQuest = "JungleQuest"
NameMon = "Gorilla"
CFrameQuest = CFrame.new(-1598.08911, 35.5501175, 153.377838, 0, 0, 1, 0, 1, -0, -1, 0, 0)
elseif MyLevel == 30 or MyLevel <= 39 then
Mon = "Pirate [Lv. 35]"
LevelQuest = 1
NameQuest = "BuggyQuest1"
NameMon = "Pirate"
CFrameQuest = CFrame.new(-1141.07483, 4.10001802, 3831.5498, 0.965929627, -0, -0.258804798, 0, 1, -0, 0.258804798, 0, 0.965929627)
elseif MyLevel == 40 or MyLevel <= 59 then
Mon = "Brute [Lv. 45]"
LevelQuest = 2
NameQuest = "BuggyQuest1"
NameMon = "Brute"
CFrameQuest = CFrame.new(-1141.07483, 4.10001802, 3831.5498, 0.965929627, -0, -0.258804798, 0, 1, -0, 0.258804798, 0, 0.965929627)
elseif MyLevel == 60 or MyLevel <= 74 then
Mon = "Desert Bandit [Lv. 60]"
LevelQuest = 1
NameQuest = "DesertQuest"
NameMon = "Desert Bandit"
CFrameQuest = CFrame.new(894.488647, 5.14000702, 4392.43359, 0.819155693, -0, -0.573571265, 0, 1, -0, 0.573571265, 0, 0.819155693)
elseif MyLevel == 75 or MyLevel <= 89 then
Mon = "Desert Officer [Lv. 70]"
LevelQuest = 2
NameQuest = "DesertQuest"
NameMon = "Desert Officer"
CFrameQuest = CFrame.new(894.488647, 5.14000702, 4392.43359, 0.819155693, -0, -0.573571265, 0, 1, -0, 0.573571265, 0, 0.819155693)
elseif MyLevel == 90 or MyLevel <= 99 then
Mon = "Snow Bandit [Lv. 90]"
LevelQuest = 1
NameQuest = "SnowQuest"
NameMon = "Snow Bandit"
CFrameQuest = CFrame.new(1389.74451, 88.1519318, -1298.90796, -0.342042685, 0, 0.939684391, 0, 1, 0, -0.939684391, 0, -0.342042685)
elseif MyLevel == 100 or MyLevel <= 119 then
Mon = "Snowman [Lv. 100]"
LevelQuest = 2
NameQuest = "SnowQuest"
NameMon = "Snowman"
CFrameQuest = CFrame.new(1389.74451, 88.1519318, -1298.90796, -0.342042685, 0, 0.939684391, 0, 1, 0, -0.939684391, 0, -0.342042685)
elseif MyLevel == 120 or MyLevel <= 149 then
Mon = "Chief Petty Officer [Lv. 120]"
LevelQuest = 1
NameQuest = "MarineQuest2"
NameMon = "Chief Petty Officer"
CFrameQuest = CFrame.new(-5039.58643, 27.3500385, 4324.68018, 0, 0, -1, 0, 1, 0, 1, 0, 0)
elseif MyLevel == 150 or MyLevel <= 174 then
Mon = "Sky Bandit [Lv. 150]"
LevelQuest = 1
NameQuest = "SkyQuest"
NameMon = "Sky Bandit"
CFrameQuest = CFrame.new(-4839.53027, 716.368591, -2619.44165, 0.866007268, 0, 0.500031412, 0, 1, 0, -0.500031412, 0, 0.866007268)
elseif MyLevel == 175 or MyLevel <= 189 then
Mon = "Dark Master [Lv. 175]"
LevelQuest = 2
NameQuest = "SkyQuest"
NameMon = "Dark Master"
CFrameQuest = CFrame.new(-4839.53027, 716.368591, -2619.44165, 0.866007268, 0, 0.500031412, 0, 1, 0, -0.500031412, 0, 0.866007268)
elseif MyLevel == 190 or MyLevel <= 209 then
Mon = "Prisoner [Lv. 190]"
LevelQuest = 1
NameQuest = "PrisonerQuest"
NameMon = "Prisoner"
CFrameQuest = CFrame.new(5308.93115, 1.65517521, 475.120514, -0.0894274712, -5.00292918e-09, -0.995993316, 1.60817859e-09, 1, -5.16744869e-09, 0.995993316, -2.06384709e-09, -0.0894274712)
elseif MyLevel == 210 or MyLevel <= 249 then
Mon = "Dangerous Prisoner [Lv. 210]"
LevelQuest = 2
NameQuest = "PrisonerQuest"
NameMon = "Dangerous Prisoner"
CFrameQuest = CFrame.new(5308.93115, 1.65517521, 475.120514, -0.0894274712, -5.00292918e-09, -0.995993316, 1.60817859e-09, 1, -5.16744869e-09, 0.995993316, -2.06384709e-09, -0.0894274712)
elseif MyLevel == 250 or MyLevel <= 274 then
Mon = "Toga Warrior [Lv. 250]"
LevelQuest = 1
NameQuest = "ColosseumQuest"
NameMon = "Toga Warrior"
CFrameQuest = CFrame.new(-1580.04663, 6.35000277, -2986.47534, -0.515037298, 0, -0.857167721, 0, 1, 0, 0.857167721, 0, -0.515037298)
elseif MyLevel == 275 or MyLevel <= 299 then
Mon = "Gladiator [Lv. 275]"
LevelQuest = 2
NameQuest = "ColosseumQuest"
NameMon = "Gladiator"
CFrameQuest = CFrame.new(-1580.04663, 6.35000277, -2986.47534, -0.515037298, 0, -0.857167721, 0, 1, 0, 0.857167721, 0, -0.515037298)
elseif MyLevel == 300 or MyLevel <= 324 then
Mon = "Military Soldier [Lv. 300]"
LevelQuest = 1
NameQuest = "MagmaQuest"
NameMon = "Military Soldier"
CFrameQuest = CFrame.new(-5313.37012, 10.9500084, 8515.29395, -0.499959469, 0, 0.866048813, 0, 1, 0, -0.866048813, 0, -0.499959469)
elseif MyLevel == 325 or MyLevel <= 374 then
Mon = "Military Spy [Lv. 325]"
LevelQuest = 2
NameQuest = "MagmaQuest"
NameMon = "Military Spy"
CFrameQuest = CFrame.new(-5313.37012, 10.9500084, 8515.29395, -0.499959469, 0, 0.866048813, 0, 1, 0, -0.866048813, 0, -0.499959469)
elseif MyLevel == 375 or MyLevel <= 399 then
Mon = "Fishman Warrior [Lv. 375]"
LevelQuest = 1
NameQuest = "FishmanQuest"
NameMon = "Fishman Warrior"
CFrameQuest = CFrame.new(61122.65234375, 18.497442245483, 1569.3997802734)
if _G.AutoFarm and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 10000 then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(61163.8515625, 11.6796875, 1819.7841796875))
end
elseif MyLevel == 400 or MyLevel <= 449 then
Mon = "Fishman Commando [Lv. 400]"
LevelQuest = 2
NameQuest = "FishmanQuest"
NameMon = "Fishman Commando"
CFrameQuest = CFrame.new(61122.65234375, 18.497442245483, 1569.3997802734)
if _G.AutoFarm and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 10000 then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(61163.8515625, 11.6796875, 1819.7841796875))
end
elseif MyLevel == 450 or MyLevel <= 474 then
Mon = "God's Guard [Lv. 450]"
LevelQuest = 1
NameQuest = "SkyExp1Quest"
NameMon = "God's Guard"
CFrameQuest = CFrame.new(-4721.88867, 843.874695, -1949.96643, 0.996191859, -0, -0.0871884301, 0, 1, -0, 0.0871884301, 0, 0.996191859)
if _G.AutoFarm and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 10000 then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-4607.82275, 872.54248, -1667.55688))
end
elseif MyLevel == 475 or MyLevel <= 524 then
Mon = "Shanda [Lv. 475]"
LevelQuest = 2
NameQuest = "SkyExp1Quest"
NameMon = "Shanda"
CFrameQuest = CFrame.new(-7859.09814, 5544.19043, -381.476196, -0.422592998, 0, 0.906319618, 0, 1, 0, -0.906319618, 0, -0.422592998)
if _G.AutoFarm and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 10000 then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-7894.6176757813, 5547.1416015625, -380.29119873047))
end
elseif MyLevel == 525 or MyLevel <= 549 then
Mon = "Royal Squad [Lv. 525]"
LevelQuest = 1
NameQuest = "SkyExp2Quest"
NameMon = "Royal Squad"
CFrameQuest = CFrame.new(-7906.81592, 5634.6626, -1411.99194, 0, 0, -1, 0, 1, 0, 1, 0, 0)
elseif MyLevel == 550 or MyLevel <= 624 then
Mon = "Royal Soldier [Lv. 550]"
LevelQuest = 2
NameQuest = "SkyExp2Quest"
NameMon = "Royal Soldier"
CFrameQuest = CFrame.new(-7906.81592, 5634.6626, -1411.99194, 0, 0, -1, 0, 1, 0, 1, 0, 0)
elseif MyLevel == 625 or MyLevel <= 649 then
Mon = "Galley Pirate [Lv. 625]"
LevelQuest = 1
NameQuest = "FountainQuest"
NameMon = "Galley Pirate"
CFrameQuest = CFrame.new(5259.81982, 37.3500175, 4050.0293, 0.087131381, 0, 0.996196866, 0, 1, 0, -0.996196866, 0, 0.087131381)
elseif MyLevel >= 650 then
Mon = "Galley Captain [Lv. 650]"
LevelQuest = 2
NameQuest = "FountainQuest"
NameMon = "Galley Captain"
CFrameQuest = CFrame.new(5259.81982, 37.3500175, 4050.0293, 0.087131381, 0, 0.996196866, 0, 1, 0, -0.996196866, 0, 0.087131381)
end
elseif World2 then
if MyLevel == 700 or MyLevel <= 724 then
Mon = "Raider [Lv. 700]"
LevelQuest = 1
NameQuest = "Area1Quest"
NameMon = "Raider"
CFrameQuest = CFrame.new(-429.543518, 71.7699966, 1836.18188, -0.22495985, 0, -0.974368095, 0, 1, 0, 0.974368095, 0, -0.22495985)
elseif MyLevel == 725 or MyLevel <= 774 then
Mon = "Mercenary [Lv. 725]"
LevelQuest = 2
NameQuest = "Area1Quest"
NameMon = "Mercenary"
CFrameQuest = CFrame.new(-429.543518, 71.7699966, 1836.18188, -0.22495985, 0, -0.974368095, 0, 1, 0, 0.974368095, 0, -0.22495985)
elseif MyLevel == 775 or MyLevel <= 799 then
Mon = "Swan Pirate [Lv. 775]"
LevelQuest = 1
NameQuest = "Area2Quest"
NameMon = "Swan Pirate"
CFrameQuest = CFrame.new(638.43811, 71.769989, 918.282898, 0.139203906, 0, 0.99026376, 0, 1, 0, -0.99026376, 0, 0.139203906)
elseif MyLevel == 800 or MyLevel <= 874 then
Mon = "Factory Staff [Lv. 800]"
NameQuest = "Area2Quest"
LevelQuest = 2
NameMon = "Factory Staff"
CFrameQuest = CFrame.new(632.698608, 73.1055908, 918.666321, -0.0319722369, 8.96074881e-10, -0.999488771, 1.36326533e-10, 1, 8.92172336e-10, 0.999488771, -1.07732087e-10, -0.0319722369)
elseif MyLevel == 875 or MyLevel <= 899 then
Mon = "Marine Lieutenant [Lv. 875]"
LevelQuest = 1
NameQuest = "MarineQuest3"
NameMon = "Marine Lieutenant"
CFrameQuest = CFrame.new(-2440.79639, 71.7140732, -3216.06812, 0.866007268, 0, 0.500031412, 0, 1, 0, -0.500031412, 0, 0.866007268)
elseif MyLevel == 900 or MyLevel <= 949 then
Mon = "Marine Captain [Lv. 900]"
LevelQuest = 2
NameQuest = "MarineQuest3"
NameMon = "Marine Captain"
CFrameQuest = CFrame.new(-2440.79639, 71.7140732, -3216.06812, 0.866007268, 0, 0.500031412, 0, 1, 0, -0.500031412, 0, 0.866007268)
elseif MyLevel == 950 or MyLevel <= 974 then
Mon = "Zombie [Lv. 950]"
LevelQuest = 1
NameQuest = "ZombieQuest"
NameMon = "Zombie"
CFrameQuest = CFrame.new(-5497.06152, 47.5923004, -795.237061, -0.29242146, 0, -0.95628953, 0, 1, 0, 0.95628953, 0, -0.29242146)
elseif MyLevel == 975 or MyLevel <= 999 then
Mon = "Vampire [Lv. 975]"
LevelQuest = 2
NameQuest = "ZombieQuest"
NameMon = "Vampire"
CFrameQuest = CFrame.new(-5497.06152, 47.5923004, -795.237061, -0.29242146, 0, -0.95628953, 0, 1, 0, 0.95628953, 0, -0.29242146)
elseif MyLevel == 1000 or MyLevel <= 1049 then
Mon = "Snow Trooper [Lv. 1000]"
LevelQuest = 1
NameQuest = "SnowMountainQuest"
NameMon = "Snow Trooper"
CFrameQuest = CFrame.new(609.858826, 400.119904, -5372.25928, -0.374604106, 0, 0.92718488, 0, 1, 0, -0.92718488, 0, -0.374604106)
elseif MyLevel == 1050 or MyLevel <= 1099 then
Mon = "Winter Warrior [Lv. 1050]"
LevelQuest = 2
NameQuest = "SnowMountainQuest"
NameMon = "Winter Warrior"
CFrameQuest = CFrame.new(609.858826, 400.119904, -5372.25928, -0.374604106, 0, 0.92718488, 0, 1, 0, -0.92718488, 0, -0.374604106)
elseif MyLevel == 1100 or MyLevel <= 1124 then
Mon = "Lab Subordinate [Lv. 1100]"
LevelQuest = 1
NameQuest = "IceSideQuest"
NameMon = "Lab Subordinate"
CFrameQuest = CFrame.new(-6064.06885, 15.2422857, -4902.97852, 0.453972578, -0, -0.891015649, 0, 1, -0, 0.891015649, 0, 0.453972578)
elseif MyLevel == 1125 or MyLevel <= 1174 then
Mon = "Horned Warrior [Lv. 1125]"
LevelQuest = 2
NameQuest = "IceSideQuest"
NameMon = "Horned Warrior"
CFrameQuest = CFrame.new(-6064.06885, 15.2422857, -4902.97852, 0.453972578, -0, -0.891015649, 0, 1, -0, 0.891015649, 0, 0.453972578)
elseif MyLevel == 1175 or MyLevel <= 1199 then
Mon = "Magma Ninja [Lv. 1175]"
LevelQuest = 1
NameQuest = "FireSideQuest"
NameMon = "Magma Ninja"
CFrameQuest = CFrame.new(-5428.03174, 15.0622921, -5299.43457, -0.882952213, 0, 0.469463557, 0, 1, 0, -0.469463557, 0, -0.882952213)
elseif MyLevel == 1200 or MyLevel <= 1249 then
Mon = "Lava Pirate [Lv. 1200]"
LevelQuest = 2
NameQuest = "FireSideQuest"
NameMon = "Lava Pirate"
CFrameQuest = CFrame.new(-5428.03174, 15.0622921, -5299.43457, -0.882952213, 0, 0.469463557, 0, 1, 0, -0.469463557, 0, -0.882952213)
elseif MyLevel == 1250 or MyLevel <= 1274 then
Mon = "Ship Deckhand [Lv. 1250]"
LevelQuest = 1
NameQuest = "ShipQuest1"
NameMon = "Ship Deckhand"
CFrameQuest = CFrame.new(1037.80127, 125.092171, 32911.6016)
if _G.AutoFarm and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 10000 then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(923.21252441406, 126.9760055542, 32852.83203125))
end
elseif MyLevel == 1275 or MyLevel <= 1299 then
Mon = "Ship Engineer [Lv. 1275]"
LevelQuest = 2
NameQuest = "ShipQuest1"
NameMon = "Ship Engineer"
CFrameQuest = CFrame.new(1037.80127, 125.092171, 32911.6016)
if _G.AutoFarm and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 10000 then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(923.21252441406, 126.9760055542, 32852.83203125))
end
elseif MyLevel == 1300 or MyLevel <= 1324 then
Mon = "Ship Steward [Lv. 1300]"
LevelQuest = 1
NameQuest = "ShipQuest2"
NameMon = "Ship Steward"
CFrameQuest = CFrame.new(968.80957, 125.092171, 33244.125)
if _G.AutoFarm and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 10000 then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(923.21252441406, 126.9760055542, 32852.83203125))
end
elseif MyLevel == 1325 or MyLevel <= 1349 then
Mon = "Ship Officer [Lv. 1325]"
LevelQuest = 2
NameQuest = "ShipQuest2"
NameMon = "Ship Officer"
CFrameQuest = CFrame.new(968.80957, 125.092171, 33244.125)
if _G.AutoFarm and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 10000 then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(923.21252441406, 126.9760055542, 32852.83203125))
end
elseif MyLevel == 1350 or MyLevel <= 1374 then
Mon = "Arctic Warrior [Lv. 1350]"
LevelQuest = 1
NameQuest = "FrostQuest"
NameMon = "Arctic Warrior"
CFrameQuest = CFrame.new(5667.6582, 26.7997818, -6486.08984, -0.933587909, 0, -0.358349502, 0, 1, 0, 0.358349502, 0, -0.933587909)
if _G.AutoFarm and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 10000 then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-6508.5581054688, 5000.034996032715, -132.83953857422))
end
elseif MyLevel == 1375 or MyLevel <= 1424 then
Mon = "Snow Lurker [Lv. 1375]"
LevelQuest = 2
NameQuest = "FrostQuest"
NameMon = "Snow Lurker"
CFrameQuest = CFrame.new(5667.6582, 26.7997818, -6486.08984, -0.933587909, 0, -0.358349502, 0, 1, 0, 0.358349502, 0, -0.933587909)
elseif MyLevel == 1425 or MyLevel <= 1449 then
Mon = "Sea Soldier [Lv. 1425]"
LevelQuest = 1
NameQuest = "ForgottenQuest"
NameMon = "Sea Soldier"
CFrameQuest = CFrame.new(-3054.44458, 235.544281, -10142.8193, 0.990270376, -0, -0.13915664, 0, 1, -0, 0.13915664, 0, 0.990270376)
elseif MyLevel >= 1450 then
Mon = "Water Fighter [Lv. 1450]"
LevelQuest = 2
NameQuest = "ForgottenQuest"
NameMon = "Water Fighter"
CFrameQuest = CFrame.new(-3054.44458, 235.544281, -10142.8193, 0.990270376, -0, -0.13915664, 0, 1, -0, 0.13915664, 0, 0.990270376)
end
elseif World3 then
if MyLevel == 1500 or MyLevel <= 1524 then
Mon = "Pirate Millionaire [Lv. 1500]"
LevelQuest = 1
NameQuest = "PiratePortQuest"
NameMon = "Pirate Millionaire"
CFrameQuest = CFrame.new(-290.074677, 42.9034653, 5581.58984, 0.965929627, -0, -0.258804798, 0, 1, -0, 0.258804798, 0, 0.965929627)
elseif MyLevel == 1525 or MyLevel <= 1574 then
Mon = "Pistol Billionaire [Lv. 1525]"
LevelQuest = 2
NameQuest = "PiratePortQuest"
NameMon = "Pistol Billionaire"
CFrameQuest = CFrame.new(-290.074677, 42.9034653, 5581.58984, 0.965929627, -0, -0.258804798, 0, 1, -0, 0.258804798, 0, 0.965929627)
elseif MyLevel == 1575 or MyLevel <= 1599 then
Mon = "Dragon Crew Warrior [Lv. 1575]"
LevelQuest = 1
NameQuest = "AmazonQuest"
NameMon = "Dragon Crew Warrior"
CFrameQuest = CFrame.new(5832.83594, 51.6806107, -1101.51563, 0.898790359, -0, -0.438378751, 0, 1, -0, 0.438378751, 0, 0.898790359)
elseif MyLevel == 1600 or MyLevel <= 1624 then
Mon = "Dragon Crew Archer [Lv. 1600]"
NameQuest = "AmazonQuest"
LevelQuest = 2
NameMon = "Dragon Crew Archer"
CFrameQuest = CFrame.new(5833.1147460938, 51.60498046875, -1103.0693359375)
elseif MyLevel == 1625 or MyLevel <= 1649 then
Mon = "Female Islander [Lv. 1625]"
NameQuest = "AmazonQuest2"
LevelQuest = 1
NameMon = "Female Islander"
CFrameQuest = CFrame.new(5446.8793945313, 601.62945556641, 749.45672607422)
elseif MyLevel == 1650 or MyLevel <= 1699 then
Mon = "Giant Islander [Lv. 1650]"
NameQuest = "AmazonQuest2"
LevelQuest = 2
NameMon = "Giant Islander"
CFrameQuest = CFrame.new(5446.8793945313, 601.62945556641, 749.45672607422)
elseif MyLevel == 1700 or MyLevel <= 1724 then
Mon = "Marine Commodore [Lv. 1700]"
LevelQuest = 1
NameQuest = "MarineTreeIsland"
NameMon = "Marine Commodore"
CFrameQuest = CFrame.new(2180.54126, 27.8156815, -6741.5498, -0.965929747, 0, 0.258804798, 0, 1, 0, -0.258804798, 0, -0.965929747)
elseif MyLevel == 1725 or MyLevel <= 1774 then
Mon = "Marine Rear Admiral [Lv. 1725]"
NameMon = "Marine Rear Admiral"
NameQuest = "MarineTreeIsland"
LevelQuest = 2
CFrameQuest = CFrame.new(2179.98828125, 28.731239318848, -6740.0551757813)
elseif MyLevel == 1775 or MyLevel <= 1799 then
Mon = "Fishman Raider [Lv. 1775]"
LevelQuest = 1
NameQuest = "DeepForestIsland3"
NameMon = "Fishman Raider"
CFrameQuest = CFrame.new(-10581.6563, 330.872955, -8761.18652, -0.882952213, 0, 0.469463557, 0, 1, 0, -0.469463557, 0, -0.882952213)
elseif MyLevel == 1800 or MyLevel <= 1824 then
Mon = "Fishman Captain [Lv. 1800]"
LevelQuest = 2
NameQuest = "DeepForestIsland3"
NameMon = "Fishman Captain"
CFrameQuest = CFrame.new(-10581.6563, 330.872955, -8761.18652, -0.882952213, 0, 0.469463557, 0, 1, 0, -0.469463557, 0, -0.882952213)
elseif MyLevel == 1825 or MyLevel <= 1849 then
Mon = "Forest Pirate [Lv. 1825]"
LevelQuest = 1
NameQuest = "DeepForestIsland"
NameMon = "Forest Pirate"
CFrameQuest = CFrame.new(-13234.04, 331.488495, -7625.40137, 0.707134247, -0, -0.707079291, 0, 1, -0, 0.707079291, 0, 0.707134247)
elseif MyLevel == 1850 or MyLevel <= 1899 then
Mon = "Mythological Pirate [Lv. 1850]"
LevelQuest = 2
NameQuest = "DeepForestIsland"
NameMon = "Mythological Pirate"
CFrameQuest = CFrame.new(-13234.04, 331.488495, -7625.40137, 0.707134247, -0, -0.707079291, 0, 1, -0, 0.707079291, 0, 0.707134247)
elseif MyLevel == 1900 or MyLevel <= 1924 then
Mon = "Jungle Pirate [Lv. 1900]"
LevelQuest = 1
NameQuest = "DeepForestIsland2"
NameMon = "Jungle Pirate"
CFrameQuest = CFrame.new(-12680.3818, 389.971039, -9902.01953, -0.0871315002, 0, 0.996196866, 0, 1, 0, -0.996196866, 0, -0.0871315002)
elseif MyLevel == 1925 or MyLevel <= 1974 then
Mon = "Musketeer Pirate [Lv. 1925]"
LevelQuest = 2
NameQuest = "DeepForestIsland2"
NameMon = "Musketeer Pirate"
CFrameQuest = CFrame.new(-12680.3818, 389.971039, -9902.01953, -0.0871315002, 0, 0.996196866, 0, 1, 0, -0.996196866, 0, -0.0871315002)
elseif MyLevel == 1975 or MyLevel <= 1999 then
Mon = "Reborn Skeleton [Lv. 1975]"
LevelQuest = 1
NameQuest = "HauntedQuest1"
NameMon = "Reborn Skeleton"
CFrameQuest = CFrame.new(-9479.2168, 141.215088, 5566.09277, 0, 0, 1, 0, 1, -0, -1, 0, 0)
elseif MyLevel == 2000 or MyLevel <= 2024 then
Mon = "Living Zombie [Lv. 2000]"
LevelQuest = 2
NameQuest = "HauntedQuest1"
NameMon = "Living Zombie"
CFrameQuest = CFrame.new(-9479.2168, 141.215088, 5566.09277, 0, 0, 1, 0, 1, -0, -1, 0, 0)
elseif MyLevel == 2025 or MyLevel <= 2049 then
Mon = "Demonic Soul [Lv. 2025]"
LevelQuest = 1
NameQuest = "HauntedQuest2"
NameMon = "Demonic Soul"
CFrameQuest = CFrame.new(-9516.99316, 172.017181, 6078.46533, 0, 0, -1, 0, 1, 0, 1, 0, 0)
elseif MyLevel == 2050 or MyLevel <= 2074 then
Mon = "Posessed Mummy [Lv. 2050]"
LevelQuest = 2
NameQuest = "HauntedQuest2"
NameMon = "Posessed Mummy"
CFrameQuest = CFrame.new(-9516.99316, 172.017181, 6078.46533, 0, 0, -1, 0, 1, 0, 1, 0, 0)
elseif MyLevel == 2075 or MyLevel <= 2099 then
Mon = "Peanut Scout [Lv. 2075]"
LevelQuest = 1
NameQuest = "NutsIslandQuest"
NameMon = "Peanut Scout"
CFrameQuest = CFrame.new(-2104.3908691406, 38.104167938232, -10194.21875, 0, 0, -1, 0, 1, 0, 1, 0, 0)
elseif MyLevel == 2100 or MyLevel <= 2124 then
Mon = "Peanut President [Lv. 2100]"
LevelQuest = 2
NameQuest = "NutsIslandQuest"
NameMon = "Peanut President"
CFrameQuest = CFrame.new(-2104.3908691406, 38.104167938232, -10194.21875, 0, 0, -1, 0, 1, 0, 1, 0, 0)
elseif MyLevel == 2125 or MyLevel <= 2149 then
Mon = "Ice Cream Chef [Lv. 2125]"
LevelQuest = 1
NameQuest = "IceCreamIslandQuest"
NameMon = "Ice Cream Chef"
CFrameQuest = CFrame.new(-820.64825439453, 65.819526672363, -10965.795898438, 0, 0, -1, 0, 1, 0, 1, 0, 0)
elseif MyLevel == 2150 or MyLevel <= 2199 then
Mon = "Ice Cream Commander [Lv. 2150]"
LevelQuest = 2
NameQuest = "IceCreamIslandQuest"
NameMon = "Ice Cream Commander"
CFrameQuest = CFrame.new(-820.64825439453, 65.819526672363, -10965.795898438, 0, 0, -1, 0, 1, 0, 1, 0, 0)
elseif MyLevel == 2200 or MyLevel <= 2224 then
Mon = "Cookie Crafter [Lv. 2200]"
LevelQuest = 1
NameQuest = "CakeQuest1"
NameMon = "Cookie Crafter"
CFrameQuest = CFrame.new(-2021.32007, 37.7982254, -12028.7295, 0.957576931, -8.80302053e-08, 0.288177818, 6.9301187e-08, 1, 7.51931211e-08, -0.288177818, -5.2032135e-08, 0.957576931)
elseif MyLevel == 2225 or MyLevel <= 2249 then
Mon = "Cake Guard [Lv. 2225]"
LevelQuest = 2
NameQuest = "CakeQuest1"
NameMon = "Cake Guard"
CFrameQuest = CFrame.new(-2021.32007, 37.7982254, -12028.7295, 0.957576931, -8.80302053e-08, 0.288177818, 6.9301187e-08, 1, 7.51931211e-08, -0.288177818, -5.2032135e-08, 0.957576931)
elseif MyLevel == 2250 or MyLevel <= 2274 then
Mon = "Baking Staff [Lv. 2250]"
LevelQuest = 1
NameQuest = "CakeQuest2"
NameMon = "Baking Staff"
CFrameQuest = CFrame.new(-1927.91602, 37.7981339, -12842.5391, -0.96804446, 4.22142143e-08, 0.250778586, 4.74911062e-08, 1, 1.49904711e-08, -0.250778586, 2.64211941e-08, -0.96804446)
elseif MyLevel >= 2275 then
Mon = "Head Baker [Lv. 2275]"
LevelQuest = 2
NameQuest = "CakeQuest2"
NameMon = "Head Baker"
CFrameQuest = CFrame.new(-1927.91602, 37.7981339, -12842.5391, -0.96804446, 4.22142143e-08, 0.250778586, 4.74911062e-08, 1, 1.49904711e-08, -0.250778586, 2.64211941e-08, -0.96804446)
end
end
end

function isnil(thing)
return (thing == nil)
end

local function round(n)
return math.floor(tonumber(n) + 0.5)
end


function UpdateEspPlayer()
if ESPPlayer then
for i,v in pairs(game:GetService("Players"):GetPlayers()) do
if not isnil(v.Character) then
if not v.Character.Head:FindFirstChild('NameEsp'..v.Name) then
local BillboardGui = Instance.new("BillboardGui")
local ESP = Instance.new("TextLabel")
local HealthESP = Instance.new("TextLabel")
BillboardGui.Parent = v.Character.Head
BillboardGui.Name = 'NameEsp'..v.Name
BillboardGui.ExtentsOffset = Vector3.new(0, 1, 0)
BillboardGui.Size = UDim2.new(1,200,1,30)
BillboardGui.Adornee = v.Character.Head
BillboardGui.AlwaysOnTop = true
ESP.Name = "ESP"
ESP.Parent = BillboardGui
ESP.TextTransparency = 0
ESP.BackgroundTransparency = 1
ESP.Size = UDim2.new(0, 200, 0, 30)
ESP.Position = UDim2.new(0,25,0,0)
ESP.Font = Enum.Font.Gotham
ESP.Text = (v.Name ..' '.."[ "..round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Character.Head.Position).Magnitude/3) ..' M'.." ]")
if v.Team == game:GetService("Players").LocalPlayer.Team then
ESP.TextColor3 = Color3.new(0, 255, 255)
else
ESP.TextColor3 = Color3.new(255, 0, 0)
end
ESP.TextSize = 14
ESP.TextStrokeTransparency = 0.500
ESP.TextWrapped = true
HealthESP.Name = "HealthESP"
HealthESP.Parent = ESP
HealthESP.TextTransparency = 0
HealthESP.BackgroundTransparency = 1
HealthESP.Position = ESP.Position + UDim2.new(0, -25, 0, 15)
HealthESP.Size = UDim2.new(0, 200, 0, 30)
HealthESP.Font = Enum.Font.Gotham
HealthESP.TextColor3 = Color3.fromRGB(255, 0, 0)
HealthESP.TextSize = 14
HealthESP.TextStrokeTransparency = 0.500
HealthESP.TextWrapped = true
HealthESP.Text = "Health "..math.floor(v.Character.Humanoid.Health).."/"..math.floor(v.Character.Humanoid.MaxHealth)
else
v.Character.Head['NameEsp'..v.Name].ESP.Text = (v.Name ..' '..round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Character.Head.Position).Magnitude/3) ..' M')
v.Character.Head['NameEsp'..v.Name].ESP.HealthESP.Text = "Health "..math.floor(v.Character.Humanoid.Health).."/"..math.floor(v.Character.Humanoid.MaxHealth)
v.Character.Head:FindFirstChild('NameEsp'..v.Name).ESP.TextTransparency = 0
v.Character.Head:FindFirstChild('NameEsp'..v.Name).ESP.HealthESP.TextTransparency = 0
end
end
end
else
for i,v in pairs(game:GetService("Players"):GetPlayers()) do
if v.Character.Head:FindFirstChild('NameEsp'..v.Name) then
v.Character.Head:FindFirstChild('NameEsp'..v.Name).ESP.TextTransparency = 1
v.Character.Head:FindFirstChild('NameEsp'..v.Name).ESP.HealthESP.TextTransparency = 1
end
end
end
end

function UpdateIslandESP()
for i,v in pairs(game:GetService("Workspace")["_WorldOrigin"].Locations:GetChildren()) do
pcall(function()
if IslandESP then
if v.Name ~= "Sea" then
if not v:FindFirstChild('NameEsp') then
local bill = Instance.new('BillboardGui',v)
bill.Name = 'NameEsp'
bill.ExtentsOffset = Vector3.new(0, 1, 0)
bill.Size = UDim2.new(1,200,1,30)
bill.Adornee = v
bill.AlwaysOnTop = true
local name = Instance.new('TextLabel',bill)
name.Font = "GothamBold"
name.FontSize = "Size14"
name.TextWrapped = true
name.Size = UDim2.new(1,0,1,0)
name.TextYAlignment = 'Top'
name.BackgroundTransparency = 1
name.TextStrokeTransparency = 0.5
name.TextColor3 = Color3.fromRGB(80, 245, 245)
else
v['NameEsp'].TextLabel.Text = (v.Name ..'   \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')
end
end
else
if v:FindFirstChild('NameEsp') then
v:FindFirstChild('NameEsp'):Destroy()
end
end
end)
end
end

function UpdateChestEsp()
for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
pcall(function()
if string.find(v.Name,"Chest") then
if ChestESP then
if string.find(v.Name,"Chest") then
if not v:FindFirstChild('NameEsp'..Number) then
local bill = Instance.new('BillboardGui',v)
bill.Name = 'NameEsp'..Number
bill.ExtentsOffset = Vector3.new(0, 1, 0)
bill.Size = UDim2.new(1,200,1,30)
bill.Adornee = v
bill.AlwaysOnTop = true
local name = Instance.new('TextLabel',bill)
name.Font = "GothamBold"
name.FontSize = "Size14"
name.TextWrapped = true
name.Size = UDim2.new(1,0,1,0)
name.TextYAlignment = 'Top'
name.BackgroundTransparency = 1
name.TextStrokeTransparency = 0.5
name.TextColor3 = Color3.fromRGB(0, 255, 250)
if v.Name == "Chest1" then
name.Text = ("Chest 1" ..' \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')
end
if v.Name == "Chest2" then
name.Text = ("Chest 2" ..' \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')
end
if v.Name == "Chest3" then
name.Text = ("Chest 3" ..' \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')
end
else
v['NameEsp'..Number].TextLabel.Text = (v.Name ..'   \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')
end
end
else
if v:FindFirstChild('NameEsp'..Number) then
v:FindFirstChild('NameEsp'..Number):Destroy()
end
end
end
end)
end
end

function UpdateBfEsp()
for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
pcall(function()
if DevilFruitESP then
if string.find(v.Name, "Fruit") then
if not v.Handle:FindFirstChild('NameEsp'..Number) then
local bill = Instance.new('BillboardGui',v.Handle)
bill.Name = 'NameEsp'..Number
bill.ExtentsOffset = Vector3.new(0, 1, 0)
bill.Size = UDim2.new(1,200,1,30)
bill.Adornee = v.Handle
bill.AlwaysOnTop = true
local name = Instance.new('TextLabel',bill)
name.Font = "GothamBold"
name.FontSize = "Size14"
name.TextWrapped = true
name.Size = UDim2.new(1,0,1,0)
name.TextYAlignment = 'Top'
name.BackgroundTransparency = 1
name.TextStrokeTransparency = 0.5
name.TextColor3 = Color3.fromRGB(255, 0, 0)
name.Text = (v.Name ..' \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Handle.Position).Magnitude/3) ..' M')
else
v.Handle['NameEsp'..Number].TextLabel.Text = (v.Name ..'   \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Handle.Position).Magnitude/3) ..' M')
end
end
else
if v.Handle:FindFirstChild('NameEsp'..Number) then
v.Handle:FindFirstChild('NameEsp'..Number):Destroy()
end
end
end)
end
end

function UpdateFlowerEsp()
for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
pcall(function()
if v.Name == "Flower2" or v.Name == "Flower1" then
if FlowerESP then
if not v:FindFirstChild('NameEsp'..Number) then
local bill = Instance.new('BillboardGui',v)
bill.Name = 'NameEsp'..Number
bill.ExtentsOffset = Vector3.new(0, 1, 0)
bill.Size = UDim2.new(1,200,1,30)
bill.Adornee = v
bill.AlwaysOnTop = true
local name = Instance.new('TextLabel',bill)
name.Font = "GothamBold"
name.FontSize = "Size14"
name.TextWrapped = true
name.Size = UDim2.new(1,0,1,0)
name.TextYAlignment = 'Top'
name.BackgroundTransparency = 1
name.TextStrokeTransparency = 0.5
name.TextColor3 = Color3.fromRGB(255, 0, 0)
if v.Name == "Flower1" then
name.Text = ("Blue Flower" ..' \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')
name.TextColor3 = Color3.fromRGB(0, 0, 255)
end
if v.Name == "Flower2" then
name.Text = ("Red Flower" ..' \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')
name.TextColor3 = Color3.fromRGB(255, 0, 0)
end
else
v['NameEsp'..Number].TextLabel.Text = (v.Name ..'   \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')
end
else
if v:FindFirstChild('NameEsp'..Number) then
v:FindFirstChild('NameEsp'..Number):Destroy()
end
end
end
end)
end
end

function topos(Pos)
Distance = (Pos.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
if game.Players.LocalPlayer.Character.Humanoid.Sit == true then game.Players.LocalPlayer.Character.Humanoid.Sit = false end
pcall(function() tween = game:GetService("TweenService"):Create(game.Players.LocalPlayer.Character.HumanoidRootPart,TweenInfo.new(Distance/210, Enum.EasingStyle.Linear),{CFrame = Pos}) end)
tween:Play()
if Distance <= 250 then
tween:Cancel()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Pos
end
if _G.StopTween == true then
tween:Cancel()
_G.Clip = false
end
end

function toClipboard(String)
	local clipBoard = setclipboard or toclipboard or set_clipboard or (Clipboard and Clipboard.set)
	if clipBoard then
		clipBoard(String)
	end
end



function getPlayerByNick(nick:string)
    local firstTry;
    local secondTry;
    local thirdTry;
    local fourthTry;
    nick = string.lower(nick)
    local playerList = game.Players:GetPlayers()
    for _,plr in pairs(playerList) do
        if string.lower(plr.Name) == nick then
            firstTry = plr
            break
        end
    end
    for _,plr in pairs(playerList) do
        if string.lower(plr.DisplayName) == nick then
            secondTry = plr
            break
        end
    end
    for _,plr in pairs(playerList) do
        if string.sub(string.lower(plr.Name), 1, #nick) == nick then
            thirdTry = plr
            break
        end
    end
    for _,plr in pairs(playerList) do
        if string.sub(string.lower(plr.DisplayName), 1, #nick) == nick then
            fourthTry = plr
            break
        end
    end
    return firstTry or nick == 'me' and game.Players.LocalPlayer or secondTry or thirdTry or fourthTry
end

function autobuso()
while _G.autobuso == true do
if not game.Players.LocalPlayer.Character:FindFirstChild('HasBuso') then
       game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
       elseif game.Players.LocalPlayer.Character:FindFirstChild('HasBuso') then
print("Buso Activates")
wait(0.5)
end
end
end

function autorace()
while _G.autorace == true do
game:GetService("ReplicatedStorage").Remotes.CommE:FireServer("ActivateAbility")
wait(0.01)
end
end

function automelee()
while _G.automelee == true do
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Melee", 1)
wait(0.01)
end
end

function autodefense()
while _G.autodefense == true do
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Defense", 1)
wait(0.01)
end
end

function autosword()
while _G.autosword == true do
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Sword", 1)
wait(0.01)
end
end

function autogun()
while _G.autogun == true do
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Gun", 1)
wait(0.01)
end
end

function autodevil()
while _G.autodevil == true do
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Demon Fruit", 1)
wait(0.01)
end
end

function autochest1()
while _G.autochest1 == true do
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Workspace.Chest1.CFrame
wait(0.01)
end
end

function autochest2()
while _G.autochest2 == true do
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Workspace.Chest2.CFrame
wait(0.01)
end
end

function autochest3()
while _G.autochest3 == true do
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Workspace.Chest3.CFrame
wait(0.01)
end
end

function killaura()
while _G.killaura == true do
for _,enemy in ipairs(workspace.Enemies:GetDescendants()) do
    if enemy:FindFirstChild('HumanoidRootPart') then
z = enemy.UpperTorso
x = enemy.Head
x:Destroy()
z:Destroy()
wait(.0000001)
end
end
end
end

function hitbox()
while _G.hitbox == true do
for _,enemy in ipairs(workspace.Enemies:GetDescendants()) do
    if enemy:FindFirstChild('HumanoidRootPart') then
local z = enemy.HumanoidRootPart
local x = enemy.Humanoid
        z.Size = Vector3.new(50,50,50)
        z.Shape = "Block"
        z.Transparency = 0.2
        z.Color = Color3.fromRGB(255,160,30)
        z.Material = "ForceField"
        z.CanCollide = false
        z.Anchored = true
        x.Sit = true
       wait(.000000000000001)
    end
end
end
end

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({
	Name = "",
	Icon = "",
	PremiumOnly = false
})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({
	Name = "Tools",
	Icon = "rbxassetid://12496252828",
	PremiumOnly = false
})

local a = game.Lighting
local c = Instance.new("ColorCorrectionEffect", a)
local e = Instance.new("ColorCorrectionEffect", a)
OldAmbient = a.Ambient
OldBrightness = a.Brightness
OldColorShift_Top = a.ColorShift_Top
OldBrightnessc = c.Brightness
OldContrastc = c.Contrast
OldTintColorc = c.TintColor
OldTintColore = e.TintColor
Tab:AddToggle({
	Name = "RTX",
	Default = false,
	Callback = function(Suka)
_G.RTXMode = Suka
if not _G.RTXMode then return end
while _G.RTXMode do wait()
a.Ambient = Color3.fromRGB(33, 33, 33)
a.Brightness = 0.3
c.Brightness = 0.176
c.Contrast = 0.39
c.TintColor = Color3.fromRGB(217, 145, 57)
game.Lighting.FogEnd = 999
if not game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("PointLight") then
local a2 = Instance.new("PointLight")
a2.Parent = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart
a2.Range = 15
a2.Color = Color3.fromRGB(217, 145, 57)
end
if not _G.RTXMode then
a.Ambient = OldAmbient
a.Brightness = OldBrightness
a.ColorShift_Top = OldColorShift_Top
c.Contrast = OldContrastc
c.Brightness = OldBrightnessc
c.TintColor = OldTintColorc
e.TintColor = OldTintColore
game.Lighting.FogEnd = 2500
game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("PointLight"):Destroy()
end
end
end
})

Tab:AddButton({
	Name = "Tp Tool" ,
	Callback = function()
local TpTool = Instance.new("Tool")
	TpTool.Name = "Teleport Tool"
	TpTool.RequiresHandle = false
	TpTool.Parent = game.Players.LocalPlayer.Backpack
	TpTool.Activated:Connect(function()
		local Char = game.Players.LocalPlayer.Character or workspace:FindFirstChild(game.Players.LocalPlayer.Name)
		local HRP = Char and Char:FindFirstChild("HumanoidRootPart")
		if not Char or not HRP then
			return warn("Failed to find HumanoidRootPart")
		end
		HRP.CFrame = CFrame.new(game.Players.LocalPlayer:GetMouse().Hit.X, game.Players.LocalPlayer:GetMouse().Hit.Y + 3, game.Players.LocalPlayer:GetMouse().Hit.Z, select(4, HRP.CFrame:components()))
	end)
end
})

Tab:AddButton({
	Name = "Tween Tp Tool" ,
	Callback = function()
local a = game:GetService("Players").LocalPlayer
            local b = Instance.new('Tool',a.Backpack)
            local g = game:GetService("TweenService")
            b.RequiresHandle = false
            b.Name = "TweenTp"
            b.Activated:connect(function()
            g:Create(
            a.Character:FindFirstChildOfClass("Humanoid").RootPart,
            TweenInfo.new(tonumber(2),Enum.EasingStyle.Linear),
            {CFrame = CFrame.new(a:GetMouse().Hit.Position+Vector3.new(0,5,0))}
            ):Play()
            end)
         end
})

Tab:AddButton({
	Name = "Remote Spy" ,
	Callback = function()
loadstring(game:HttpGet("https://github.com/exxtremestuffs/SimpleSpySource/raw/master/SimpleSpy.lua"))()
  	end    
})

Tab:AddButton({
	Name = "CHANGE GUIs" ,
	Callback = function()
game:GetService("CoreGui").FluxusAndroidUI.Container.ToggleBtn.Icon.BorderColor3 = Color3.fromRGB(255, 160, 30)
wait(0.1)
game:GetService("CoreGui").FluxusAndroidUI.Container.ToggleBtn.Icon.BackgroundTransparency = 0
wait(0.1)
game:GetService("CoreGui").FluxusAndroidUI.Container.ToggleBtn.Border:Destroy()
wait(0.1)
game:GetService("CoreGui").FluxusAndroidUI.Container.ToggleBtn.Icon.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
wait(0.1)
game:GetService("CoreGui").FluxusAndroidUI.Container.ToggleBtn.Icon.BorderSizePixel = 5
wait(0.1)
game:GetService("CoreGui").FluxusAndroidUI.Container.ToggleBtn.ClickHandler.Text = "POISTER               CUSTOM."
wait(0.1)
game:GetService("CoreGui").FluxusAndroidUI.Container.ToggleBtn.ClickHandler.TextSize = 20
wait(0.1)
game:GetService("CoreGui").FluxusAndroidUI.Container.ToggleBtn.Icon.Rotation = 30
wait(0.1)
game.Players.LocalPlayer.PlayerGui.Main.SafeZone.Position = UDim2.new(0,680,1,-150)
wait(0.1)
game.Players.LocalPlayer.PlayerGui.Main.SafeZone.Text = "PVP - DISABLED.SAFEZONE😈👿😈"
wait(0.1)
game.Players.LocalPlayer.PlayerGui.Main.SafeZone.TextColor3 = Color3.fromRGB(255, 160, 30)
wait(0.1)
game.Players.LocalPlayer.PlayerGui.Main.Quest.Title.TextColor3 = Color3.fromRGB(255, 160, 30)
wait(0.1)
game.Players.LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.BackgroundColor3 = Color3.fromRGB(255, 160, 30)
wait(0.1)
game.Players.LocalPlayer.PlayerGui.Main.Quest.Container.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
wait(0.1)
game.Players.LocalPlayer.PlayerGui.Main.Quest.BackgroundTransparency = 0
wait(0.1)
game.Players.LocalPlayer.PlayerGui.Main.Quest.Container.BackgroundTransparency = 0
wait(0.1)
game.Players.LocalPlayer.PlayerGui.Main.Skills.Title.BackgroundTransparency = 0
wait(0.1)
game.Players.LocalPlayer.PlayerGui.Main.Skills.Title.TextColor3 = Color3.fromRGB(255,160,30)
wait(0.1)
game.Players.LocalPlayer.PlayerGui.Main.Skills.Level.TextColor3 = Color3.fromRGB(255,160,30)
wait(0.1)
game.Players.LocalPlayer.PlayerGui.Main.Skills.Rage.TextColor3 = Color3.fromRGB(255, 160, 30)
wait(0.1)
game.Players.LocalPlayer.PlayerGui.Main.Skills.Level.Bar.BackgroundColor3 = Color3.fromRGB(255, 160, 30)
wait(0.1)
game.Players.LocalPlayer.PlayerGui.Main.Skills.Level.Bar2.BackgroundColor3 = Color3.fromRGB(255, 160, 30)
wait(0.1)
game.Players.LocalPlayer.PlayerGui.Main.Trade.BackgroundTransparency = 1
wait(0.1)
game.Players.LocalPlayer.PlayerGui.Main.Trade.Title.TextColor3 = Color3.fromRGB(255,160,30)
wait(0.1)
game.Players.LocalPlayer.PlayerGui.Main.Trade.Title.BackgroundTransparency = 1
wait(0.1)
game.Players.LocalPlayer.PlayerGui.Main.Trade.Title.Text = "TRADING"
wait(0.1)
game.Players.LocalPlayer.PlayerGui.Main.Trade.Container["1"].BackgroundColor3 = Color3.fromRGB(255,160,30)
wait(0.1)
game.Players.LocalPlayer.PlayerGui.Main.Trade.Container["2"].BackgroundColor3 = Color3.fromRGB(0,0,0)
wait(0.1)
game.Players.LocalPlayer.PlayerGui.Main.Trade.Container["1"].BorderColor3 = Color3.fromRGB(255,255,255)
wait(0.1)
game.Players.LocalPlayer.PlayerGui.Main.Trade.Container["2"].BorderColor3 = Color3.fromRGB(255,255,255)
wait(0.1)
game.Players.LocalPlayer.PlayerGui.Main.Trade.Info.BorderColor3 = Color3.fromRGB(255,255,255)
wait(0.1)
game.Players.LocalPlayer.PlayerGui.Main.Trade.Info.Accept.BorderColor3 = Color3.fromRGB(255,160,30)
wait(0.1)
game.Players.LocalPlayer.PlayerGui.Main.Trade.Info.Cancel.BorderColor3 = Color3.fromRGB(255,160,30)
wait(0.1)
game.Players.LocalPlayer.PlayerGui.Main.Trade.Info.Accept.BorderColor3 = Color3.fromRGB(255,160,30)
wait(0.1)
game.Players.LocalPlayer.PlayerGui.Main.Trade.Info.Accept.BackgroundColor3 = Color3.fromRGB(0,0,0)
wait(0.1)
game.Players.LocalPlayer.PlayerGui.Main.Trade.Info.Accept.BorderColor3 = Color3.fromRGB(255,160,30)
wait(0.1)
game.Players.LocalPlayer.PlayerGui.Main.Trade.Info.Accept.Trans.BackgroundColor3 = Color3.fromRGB(0,0,0)
wait(0.1)
game.Players.LocalPlayer.PlayerGui.Main.Trade.Info.Cancel.Trans.BackgroundColor3 = Color3.fromRGB(0,0,0)
wait(0.1)
game.Players.LocalPlayer.PlayerGui.Main.Trade.Info.Cancel.BackgroundColor3 = Color3.fromRGB(0,0,0)
wait(0.1)
game.Players.LocalPlayer.PlayerGui.Main.Trade.Info.Accept.Trans.BorderColor3 = Color3.fromRGB(255,160,30)
wait(0.1)
game.Players.LocalPlayer.PlayerGui.Main.Trade.Info.Accept.TextLabel.TextColor3 = Color3.fromRGB(255,160,30)
  	end
})

Tab:AddButton({
	Name = "Dex V3" ,
	Callback = function()
loadstring(game:HttpGet("https://raw.githubusercontent.com/Babyhamsta/RBLX_Scripts/main/Universal/BypassedDarkDexV3.lua", true))()
  	end
})

Tab:AddButton({
	Name = "Dex V4" ,
	Callback = function()
    loadstring(game:HttpGet("https://raw.githubusercontent.com/peyton2465/Dex/master/out.lua"))()
  	end
})

Tab:AddButton({
	Name = "Big Jump" ,
	Callback = function()
    game.Players.LocalPlayer.PlayerGui.TouchGui.TouchControlFrame.JumpButton.Size = UDim2.new(0,200,0,200)
  	end    
})

Tab:AddButton({
	Name = "Remove Button" ,
	Callback = function()
    f9.Visible = false
  	end    
})

Tab:AddButton({
	Name = "" ,
	Callback = function()
game.Players.LocalPlayer.PlayerGui.TouchGui.TouchControlFrame.JumpButton.Size = UDim2.new(0,200,0,200)
  	end    
})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({
	Name = "BuyItem",
	Icon = "http://www.roblox.com/asset/?id=12496227758",
	PremiumOnly = false
})

local Section = Tab:AddSection({
	Name = "Abilities"
})

Tab:AddButton({
	Name = "Buso",
	Callback = function()
      		print("button pressed")
  	end    
})

Tab:AddButton({
	Name = "Geppo",
	Callback = function()
      		print("button pressed")
  	end    
})

Tab:AddButton({
	Name = "Soru",
	Callback = function()
      		print("button pressed")
  	end    
})

Tab:AddButton({
	Name = "Ken",
	Callback = function()
      		print("button pressed")
  	end    
})

local Section = Tab:AddSection({
	Name = "Fighting Styles"
})

Tab:AddButton({
	Name = "Dark Step 250.000$",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBlackLeg" )
  	end    
})

Tab:AddButton({
	Name = "Electro 500.000$",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyElectro" )
  	end    
})

Tab:AddButton({
	Name = "Water Kung-Fu 750.000$",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyFishmanKarate" )
  	end    
})

Tab:AddButton({
	Name = "Dragon Breath",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","DragonClaw","2")
  	end    
})

Tab:AddButton({
	Name = "Superhuman 3.000.000$",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySuperhuman" )
  	end    
})

Tab:AddButton({
	Name = "Death Step 2.500.000$ 2.500F",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyDeathStep" )
  	end    
})

Tab:AddButton({
	Name = "Electric Claw 2.500.000$ 2.500F",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyElectricClaw" )
  	end    
})

Tab:AddButton({
	Name = "Sharkman Karate 2.500.000$ 2.500F",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySharkmanKarate" )
  	end    
})

Tab:AddButton({
	Name = "Dragon Talon 2.500.000$ 2.500F",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyDragonTalon" )
  	end    
})

Tab:AddButton({
	Name = "Godhuman 5.000.000$ 5.000F",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyGodhuman" )
  	end    
})

local Section = Tab:AddSection({
	Name = "Fragments"
})

Tab:AddButton({
	Name = "Check Color Haki Dealer",
	Callback = function()
	OrionLib:MakeNotification({
	Name = "Haki Colors Dealer",
    Content = "".. game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ColorsDealer", "1") .."",
	Image = "rbxassetid://4483345998",
	Time = 5
})
	end
})

Tab:AddButton({
	Name = "Buy Color Buso Haki",
	Callback = function()
	game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ColorsDealer", "2")
	end
})

Tab:AddButton({
	Name = "Ghoul 0F",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Ectoplasm","Change",4)
  	end    
})

Tab:AddButton({
	Name = "Cyborg 2.500F",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("CyborgTrainer","Buy")
  	end    
})

Tab:AddButton({
	Name = "Reset Stats 2.500F",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","Refund","2")
  	end    
})

Tab:AddButton({
	Name = "Race Reroll 3.000F",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","Reroll","2")
  	end    
})

local Section = Tab:AddSection({
	Name = "Bones"
})

Tab:AddButton({
	Name = "Surprise 50bones",
	Callback = function()
      		for i = 1, 10 do
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Bones", "Buy", 1, 1)
            end
  	end    
})

local Section = Tab:AddSection({
	Name = "Swords"
})

local Section = Tab:AddSection({
	Name = "Guns"
})

local Section = Tab:AddSection({
	Name = "Accessories"
})

Tab:AddButton({
	Name = "Tomoe Ring 500.000$",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyItem","Tomoe Ring")
end
})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({
	Name = "Farming",
	Icon = "rbxassetid://12505503302",
	PremiumOnly = false
})

Tab:AddToggle({
	Name = "HitBox",
	Default = false,
	Callback = function(lolek)
	_G.hitbox = lolek
hitbox()
		end
})

Tab:AddToggle({
	Name = "Test",
	Default = false,
	Callback = function()
	print("108\111\97\100\115\116\114\105\110\103\40\34\68\101\99\111\100\101\83\99\114\105\112\116\65\108\116\34\41\44\40\116\114\117\101\41\59")

		end
})

local Section = Tab:AddSection({
    Name = "START"
})

Tab:AddButton({
	Name = "5Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", "BanditQuest1", 1)
end
})

local Section = Tab:AddSection({
    Name = "JUNGLE"
})

Tab:AddButton({
	Name = "10Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","JungleQuest",1)
end
})

Tab:AddButton({
	Name = "15Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","JungleQuest",2)
end
})

Tab:AddButton({
	Name = "20Lvl [BOSS]",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","JungleQuest",3)    
end
})

local Section = Tab:AddSection({
    Name = "PIRATE VILLAGE"
})

Tab:AddButton({
	Name = "30Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","BuggyQuest1",1)
end
})

Tab:AddButton({
	Name = "50Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","BuggyQuest1",2)
end
})

Tab:AddButton({
	Name = "55Lvl [BOSS]",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","BuggyQuest1",3)
end
})

local Section = Tab:AddSection({
    Name = "DESERT"
})

Tab:AddButton({
	Name = "60Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","DesertQuest",1)
end
})

Tab:AddButton({
	Name = "75Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","DesertQuest",2)
end
})

local Section = Tab:AddSection({
    Name = "SNOW VILLAGE"
})

Tab:AddButton({
	Name = "90Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", "SnowQuest", 1)
end
})

Tab:AddButton({
	Name = "100Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", "SnowQuest", 2)
end
})

Tab:AddButton({
	Name = "105Lvl [BOSS]",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", "SnowQuest", 3)
end
})

local Section = Tab:AddSection({
    Name = "MARINE FORTRESS"
})

Tab:AddButton({
	Name = "120Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", "BanditQuest1", 1)
end
})

Tab:AddButton({
	Name = "130Lvl [BOSS]",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", "BanditQuest1", 1)
end
})

local Section = Tab:AddSection({
    Name = "SKY1"
})

Tab:AddButton({
	Name = "150Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","SkyQuest",1)
end
})

Tab:AddButton({
	Name = "170Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","SkyQuest",2)
end
})

local Section = Tab:AddSection({
    Name = "PRISON"
})

Tab:AddButton({
	Name = "190Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","PrisonerQuest",1)
end
})

Tab:AddButton({
	Name = "210Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","PrisonerQuest",2)
end
})

Tab:AddButton({
	Name = "220Lvl [BOSS]",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","ImpelQuest",1)
end
})

Tab:AddButton({
	Name = "230Lvl [BOS]",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","ImpelQuest",2)
end
})

Tab:AddButton({
	Name = "240Lvl [BOSS]",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","ImpelQuest",3)
end
})

local Section = Tab:AddSection({
    Name = "COLOSSEUM"
})

Tab:AddButton({
	Name = "250Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","ColosseumQuest",1)
end
})

Tab:AddButton({
	Name = "275Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","ColosseumQuest",2)
end
})

local Section = Tab:AddSection({
    Name = "MAGMA VILLAGE"
})

Tab:AddButton({
	Name = "300Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","MagmaQuest",1)
end
})

Tab:AddButton({
	Name = "325Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","MagmaQuest",2)
end
})

Tab:AddButton({
	Name = "350Lvl [BOSS]",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","MagmaQuest",3)
end
})

local Section = Tab:AddSection({
    Name = "UNDERWATER"
})

Tab:AddButton({
	Name = "375Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","FishmanQuest",1)
end
})

Tab:AddButton({
	Name = "400Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","FishmanQuest",2)
end
})

Tab:AddButton({
	Name = "425Lvl [BOSS]",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","FishmanQuest",3)
end
})

local Section = Tab:AddSection({
    Name = "SKY2-3"
})

Tab:AddButton({
	Name = "450Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","SkyExp1Quest",1)
end
})

Tab:AddButton({
	Name = "475Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","SkyExp1Quest",2)
end
})

Tab:AddButton({
	Name = "500Lvl [BOSS]",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","SkyExp1Quest",3)
end
})

Tab:AddButton({
	Name = "525Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", "SkyExp2Quest", 1)
end
})

Tab:AddButton({
	Name = "550Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", "SkyExp2Quest", 2)
end
})

Tab:AddButton({
	Name = "575Lvl [BOSS]",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", "SkyExp2Quest", 3)
end
})

local Section = Tab:AddSection({
    Name = "FOUNTAIN CITY"
})

Tab:AddButton({
	Name = "625Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","FountainQuest",1)
end
})

Tab:AddButton({
	Name = "650Lvl",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","FountainQuest",2)
end
})

Tab:AddButton({
	Name = "675Lvl [BOSS]",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","FountainQuest",3)
end
})

--мб дропдауны под секции

Tab:AddButton({
	Name = "Player Quest",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer( "PlayerHunter")
end
})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({
	Name = "Esp",
	Icon = "rbxassetid://12496239839",
	PremiumOnly = false
})

esps = {}
Tab:AddToggle({
    Name = "Fruit esp",
    Default = false,
    Callback = function(Value) 
        if Value == true then
            fruitNames = {'Fruit ','Kilo Fruit', 'Spin Fruit', 'Chop Fruit', 'Spring Fruit', 'Bomb Fruit', 'Smoke Fruit', 'Spike Fruit', 'Flame Fruit', 'Bird: Falcon Fruit', 'Ice Fruit', 'Sand Fruit', 'Dark Fruit', 'Revive Fruit', 'Diamond Fruit', 'Light Fruit', 'Love Fruit', 'Rubber Fruit', 'Barrier Fruit', 'Magma Fruit', 'Quake Fruit', 'Human: Buddha Fruit', 'Spider Fruit', 'Bird: Phoenix Fruit', 'Portal Fruit', 'Rumble Fruit', 'Paw Fruit', 'Blizzard Fruit', 'Gravity Fruit', 'Dough Fruit', 'Shadow Fruit', 'Venom Fruit', 'Control Fruit', 'Spirit Fruit', 'Dragon Fruit', 'Leopard Fruit'}
            for key, value in pairs(fruitNames) do
                fruitNames[value] = key
            end
            for _, obj in pairs(workspace:GetChildren()) do
                if fruitNames[obj.Name] then
                    local billBoard = Instance.new("BillboardGui", obj.Handle)
                    local espText = Instance.new("TextLabel", billBoard)
                    billBoard.Adornee = obj.Handle
                    billBoard.AlwaysOnTop = true
                    billBoard.Size = UDim2.new(1,200,1,30)
                    billBoard.Name = "Board"
                    espText.Size = UDim2.new(1,0,1,0)
                    espText.Text = obj.Handle.Position
                    espText.TextColor3 = Color3.fromRGB(255,160,30)
                    espText.TextStrokeTransparency = 0
                    espText.BackgroundTransparency = 1
                    espText.TextSize = 10
                    espText.Name = "Text"
                    esps[billBoard] = obj
OrionLib:MakeNotification({
	Name = obj.Name,
	Content = "This fruit was found",
	Image = "rbxassetid://12496254877",
	Time = 10
})
                end
            end
        elseif Value == false then
            for esp, obj in pairs(esps) do
                esp:Destroy()
            end
            esps = {}
        end
    end
})

Tab:AddButton({
	Name = "Tracers",
	Callback = function()
local camera = workspace.CurrentCamera
for _,v in pairs(game.Players:GetPlayers()) do
if v ~= game.Players.LocalPlayer and v.Character ~= nil and v.Character:FindFirstChild("HumanoidRootPart") ~= nil then
local vector,onScreen = camera:WorldToScreenPoint(v.Character.HumanoidRootPart.Position)
local Line = Drawing.new("Line")
Line.Visible = true
Line.From = Vector2.new(camera.ViewportSize.X / 2, camera.ViewportSize.Y / 1)
Line.To = Vector2.new(vector.X, vector.Y)
Line.Color = Color3.fromRGB(255,160,30)
Line.Thickness = 2
Line.Transparency = 1
function script()
game:GetService("RunService").RenderStepped:Connect(function(step)
if v.Character ~= nil and v.Character:FindFirstChild("HumanoidRootPart") ~= nil then
local vector,onScreen = camera:WorldToScreenPoint(v.Character.HumanoidRootPart.Position)
if onScreen == true then
Line.To = Vector2.new(vector.X, vector.Y)
Line.Visible = true
else
Line.Visible = false
end
end
end)
end
coroutine.wrap(script)()
end
v.CharacterAdded:Connect(function()
repeat wait()  until v.Character ~= nil
repeat wait()  until v.Character:FindFirstChild("HumanoidRootPart") ~= nil
local vector,onScreen = camera:WorldToScreenPoint(v.Character.HumanoidRootPart.Position)
local Line = Drawing.new("Line")
Line.Visible = true
Line.From = Vector2.new(camera.ViewportSize.X / 2, camera.ViewportSize.Y / 1)
Line.To = Vector2.new(vector.X, vector.Y)
Line.Color = Color3.fromRGB(255,160,30)
Line.Thickness = 2
Line.Transparency = 1
function script()
game:GetService("RunService").RenderStepped:Connect(function(step)
if v.Character ~= nil and v.Character:FindFirstChild("HumanoidRootPart") ~= nil then
local vector,onScreen = camera:WorldToScreenPoint(v.Character.HumanoidRootPart.Position)
if onScreen == true then
Line.To = Vector2.new(vector.X, vector.Y)
Line.Visible = true
else
Line.Visible = false
end
end
end)
end
coroutine.wrap(script)()
end)
end
end
})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({
	Name = "Fruit",
	Icon = "http://www.roblox.com/asset/?id=12496254877",
	PremiumOnly = false
})

Tab:AddToggle({
	Name = "Tp Fruit",
	Default = false,
	Callback = function(Grab)
_G.BringFruit = Grab
pcall(function()
while _G.BringFruit do wait(.1)
for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
if v:IsA("Tool") then
local OldCFrame = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame
game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = v.Handle.CFrame * CFrame.new(0,0,0)
v.Handle.CFrame = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame
wait(.1)
game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = OldCFrame
end
end
end
end)
end
})

Tab:AddButton({
	Name = "Random Fruit",
	Callback = function()
      		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Cousin", "Buy")
  	end    
})

Tab:AddButton({
	Name = "Fruit Shop",
	Callback = function()
game.Players.LocalPlayer.PlayerGui.Main.FruitShop.Visible = true
  	end
})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({
	Name = "Points soon...",
	Icon = "rbxassetid://12530069729",
	PremiumOnly = false
})

Tab:AddToggle({
	NameA = "uto Melee",
	Default = false,
	Callback = function(Melee1)
	_G.automelee = Melee1
automelee()
		end
})

Tab:AddToggle({
	Name = "Auto Defense",
	Default = false, 
	Callback = function(Defense1)
	_G.autodefense = Defense1
autodefense()
		end
})

Tab:AddToggle({
	Name = "Auto Sword",
	Default = false,
	Callback = function(Sword1)
	_G.autosword = Sword1
autosword()
		end
})

Tab:AddToggle({
	Name = "Auto Gun",
	Default = false,
	Callback = function(Gun1)
	_G.autogun = Gun1
autogun()
		end
})

Tab:AddToggle({
	Name = "Auto Devil Fruit",
	Default = false,
	Callback = function(Devil1)
	_G.autodevil = Devil1
autodevil()
		end
})

Tab:AddTextbox({
	Name = "Melee",
	Default = nil,
	TextDisappear = true,
	Callback = function(Melee)
		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Melee", Melee) 
	end	  
})

Tab:AddTextbox({
	Name = "Defense",
	Default = nil,
	TextDisappear = true,
	Callback = function(Defense)
		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Defense", Defense)
	end
})

Tab:AddTextbox({
	Name = "Sword",
	Default = nil,
	TextDisappear = true,
	Callback = function(Sword)
		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Sword", Sword)
	end
})

Tab:AddTextbox({
	Name = "Gun",
	Default = nil,
	TextDisappear = true,
	Callback = function(Gun)
		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Gun", Gun)
	end
})

Tab:AddTextbox({
	Name = "Devil Fruit",
	Default = nil,
	TextDisappear = true,
	Callback = function(Devil)
		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Demon Fruit", Devil)
	end
})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({
	Name =  "GUIs soon?..",
	Icon = "rbxassetid://12505501154",
	PremiumOnly = false
})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({
	Name =  "Any Auto soon...",
	Icon = "rbxassetid://12505499132",
	PremiumOnly = false
})

Tab:AddButton({
	Name = "Auto Sea2",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("DressrosaQuestProgress","Detective")
wait(.00001)
topos(CFrame.new(1349.4, 37.5, -1326.2))
wait(.1)
local z = game.Players.LocalPlayer.Backpack.Key
z.Parent = game.Players.LocalPlayer.Character
end
})

Tab:AddToggle({
	Name = "Auto Silver Chest",
	Default = false,
	Callback = function(Chest1)
	_G.autochest1 = Chest1
autochest1()
		end
})

Tab:AddToggle({
	Name = "Auto Gold Chest",
	Default = false,
	Callback = function(Chest2)
	_G.autochest2 = Chest2
autochest2()
		end
})

Tab:AddToggle({
	Name = "Auto Diamond Chest",
    Default = false,
	Callback = function(Chest3)
	_G.autochest3 = Chest3
autochest3()
		end
})

Tab:AddToggle({
	Name = "Auto Buso",
	Default = false,
	Callback = function(Toggle1)
	_G.autobuso = Toggle1
autobuso()
		end
})

Tab:AddToggle({
	Name = "Auto Race",
	Default = false,
	Callback = function(Toggle5)
	_G.autorace = Toggle5
autorace()
		end
})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({
	Name = "Teleport",
	Icon = "rbxassetid://12496230420",
	PremiumOnly = false
})

local Section = Tab:AddSection({
	Name = "Servers"
})

Tab:AddButton({
	Name = "Server Id",
	Callback = function()
    jobId = ''..game.JobId..''
	toClipboard(jobId)
	OrionLib:MakeNotification({
	Name = "Server ID copied to clipboard!",
	Content = "Paste this in Server Join Id",
	Image = "rbxassetid://4483345998",
	Time = 5
})
end
})

Tab:AddTextbox({
	Name = "Join Id Server",
	Default = ""..game.JobId.."",
	TextDisappear = true,
	Callback = function(Ponon)
		game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId,Ponon,game.Players.LocalPlayer)
	end
})

Tab:AddButton({
	Name = "Rejoin",
	Callback = function()
if #game.Players:GetPlayers() == 1 then
		game.Players.LocalPlayer:Kick("\nRejoin...")
		wait()
		game:GetService("TeleportService"):Teleport(game.PlaceId, game.Players.LocalPlayer)
	else
		game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId, game.JobId, game.Players.LocalPlayer)
	end
  	end
})

Tab:AddButton({
	Name = "Server Hop",
	Callback = function()
loadstring(game:HttpGet"https://raw.githubusercontent.com/LeoKholYt/roblox/main/lk_serverhop.lua")():Teleport(game.PlaceId)
  	end    
})

local Section = Tab:AddSection({
	Name = "Worlds"
})

Tab:AddButton({
	Name = "Sea1",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TravelMain")
  	end
})

Tab:AddButton({
	Name = "Sea2",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TravelDressrosa")
  	end
})

Tab:AddButton({
	Name = "Sea3",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TravelZou")
  	end    
})

local Section = Tab:AddSection({
	Name = "Settings"
})

Tab:AddButton({
	Name = "Stop Tween",
	Callback = function()
topos(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame)
end
})

local Section = Tab:AddSection({
	Name = "Islands"
})

Tab:AddButton({
	Name = "Marine Start",
	Callback = function()
topos(CFrame.new(-2566.4296875, 6.8556680679321, 2045.2561035156))
end
})

Tab:AddButton({
	Name = "Pirate Start",
	Callback = function()
topos(CFrame.new(979.79895019531, 16.516613006592, 1429.0466308594))
end
})

Tab:AddButton({
	Name = "Jungle",
	Callback = function()
topos(CFrame.new(-1612.7957763672, 36.852081298828, 149.12843322754))
end
})

Tab:AddButton({
	Name = "Pirate Village",
	Callback = function()
topos(CFrame.new(-1181.3093261719, 4.7514905929565, 3803.5456542969))
end
})

Tab:AddButton({
	Name = "Desert",
	Callback = function()
topos(CFrame.new(944.15789794922, 20.919729232788, 4373.3002929688))
end
})

Tab:AddButton({
	Name = "Snow Village",
	Callback = function()
topos(CFrame.new(1347.8067626953, 104.66806030273, -1319.7370605469))
end
})

Tab:AddButton({
	Name = "Marine Fortress",
	Callback = function()
topos(CFrame.new(-4914.8212890625, 50.963626861572, 4281.0278320313))
end
})

Tab:AddButton({
	Name = "Sky1",
	Callback = function()
topos(CFrame.new(-4869.1025390625, 733.46051025391, -2667.0180664063))
end
})

Tab:AddButton({
	Name = "Sky2",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-4607.82275, 872.54248, -1667.55688))
  	end    
})

Tab:AddButton({
	Name = "Sky3",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-7894.6176757813, 5547.1416015625, -380.29119873047))
  	end    
})

Tab:AddButton({

	Name = "Prison",
	Callback = function()
topos( CFrame.new(4875.330078125, 5.6519818305969, 734.85021972656))
end
})

Tab:AddButton({
	Name = "Colloseum",
	Callback = function()
topos( CFrame.new(-1427.6203613281, 7.2881078720093, -2792.7722167969))
end
})

Tab:AddButton({
	Name = "Magma Village",
	Callback = function()
topos(CFrame.new(-5247.7163085938, 12.883934020996, 8504.96875))
end
})

Tab:AddButton({
	Name = "Under Water City",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(61163.8515625, 11.6796875, 1819.7841796875))
end
})

Tab:AddButton({
	Name = "Fountain City",
	Callback = function()
topos(CFrame.new(5411.8, 188.9, 4281.4))
end
})

Tab:AddButton({
	Name = "Mob Island",
	Callback = function()
topos( CFrame.new(-1503.6224365234, 219.7956237793, 1369.3101806641))
end
})

Tab:AddButton({
	Name = "Shank Room",
	Callback = function()
topos(CFrame.new(-1442.16553, 29.8788261, -28.3547478))
end
})

Tab:AddButton({
	Name = "Middle Town",
	Callback = function()
topos(CFrame.new(-2850.20068, 7.39224768, 5354.99268))
end
})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({
	Name = "Boats",
	Icon = "rbxassetid://12496247656",
	PremiumOnly = false
})

local Section = Tab:AddSection({
	Name = "Pirate"
})

Tab:AddButton({
	Name = "Pirate Sloop 600$",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "PirateSloop")
  	end
})

Tab:AddButton({
	Name = "Pirate Basic 1.000$",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "PirateBasic")
   	end    
})

Tab:AddButton({
	Name = "Pirate Brigade 4.000$",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "PirateBrigade")
  	end    
})

local Section = Tab:AddSection({
	Name = "Marine"
})

Tab:AddButton({
	Name = "Marine Sloop 150$",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "MarineSloop")
  	end
})

Tab:AddButton({
	Name = "Marine Basic 600$",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "MarineBasic")
  	end
})

Tab:AddButton({
	Name = "MarineBrigade 2.000$",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "MarineBrigade")
  	end
})

local Section = Tab:AddSection({
	Name = "Luxury"
})

Tab:AddButton({
	Name = "RocketBoost 0$",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "RocketBoost")
  	end
})

Tab:AddButton({
	Name = "Enforcer 1.000$",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "Enforcer")
  	end
})

Tab:AddButton({
	Name = "Swan 5.000$",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "Swan")
  	end
})

Tab:AddButton({
	Name = "Flower 5.000$",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "Flower")
  	end    
})

Tab:AddButton({
	Name = "Sleigh 5.000$",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "Sleigh")
  	end
})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({
	Name = "Fast Cmd soon...",
	Icon = "rbxassetid://12496242729",
	PremiumOnly = false
})    

Tab:AddTextbox({
	Name = "Textbox",
	Default = "soon...",
	TextDisappear = true,
	Callback = function(Cmd)
		if Cmd == pon then
print("pon")
elseif Cmd == pon1 then
print("pon1")
end
	end
})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({
	Name = "Combat soon..",
	Icon = "rbxassetid://12496236549",
	PremiumOnly = false
})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({
	Name = "Raids",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

Tab:AddToggle({
	Name = "Killaura",
	Default = false,
	Callback = function(Killaura)
	_G.killaura = Killaura
killaura()
		end
})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({
	Name = "Troll",
	Icon = "rbxassetid://12505494337",
	PremiumOnly = false
})

Tab:AddToggle({
	Name = "Freeze",
	Default = nil,
	Callback = function(Value1)
	if Value1 == true then   game.Players.LocalPlayer.Character.HumanoidRootPart.Anchored = true
elseif Value1 == false then
game.Players.LocalPlayer.Character.HumanoidRootPart.Anchored = false
	end 
end   
})

Tab:AddButton({
	Name = "Sit",
	Callback = function()
game.Players.LocalPlayer.Character.Humanoid.Sit = true
  	end
})

Tab:AddButton({
	Name = "Lay Down",
	Callback = function()
local Human = game.Players.LocalPlayer.Character and game.Players.LocalPlayer.Character:FindFirstChildOfClass('Humanoid')
	if not Human then
		return
	end
	Human.Sit = true
	task.wait(.1)
	Human.RootPart.CFrame = Human.RootPart.CFrame * CFrame.Angles(math.pi * .5, 0, 0)
	for _, v in ipairs(Human:GetPlayingAnimationTracks()) do
		v:Stop()
	end
  	end  
})

Tab:AddTextbox({
	Name = "Spin",
	Default = nil,
	TextDisappear = true,
	Callback = function(SPINN)
		function getRoot(char)
	local rootPart = char:FindFirstChild('HumanoidRootPart') or char:FindFirstChild('Torso') or char:FindFirstChild('UpperTorso')
	return rootPart
end
local Spin = Instance.new("BodyAngularVelocity")
	Spin.Name = "Spinning"
	Spin.Parent = getRoot(game.Players.LocalPlayer.Character)
	Spin.MaxTorque = Vector3.new(0, math.huge, 0)
	Spin.AngularVelocity = Vector3.new(0, SPINN, 0)
	end
})

Tab:AddButton({
	Name = "Stop Spin",
	Callback = function()
function getRoot(char)
	local rootPart = char:FindFirstChild('HumanoidRootPart') or char:FindFirstChild('Torso') or char:FindFirstChild('UpperTorso')
	return rootPart
end
for i,v in pairs(getRoot(game.Players.LocalPlayer.Character):GetChildren()) do
		if v.Name == "Spinning" then
			v:Destroy()
		end
	end
  	end
})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({
	Name = "Codes test...",
	Icon = "rbxassetid://12496297350",
	PremiumOnly = false
})  

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({
	Name = "Player Settings",
	Icon = "rbxassetid://12496250171",
	PremiumOnly = false
})

Tab:AddTextbox({
	Name = "Chat",
	Default = "Chat",
	TextDisappear = true,
	Callback = function(Say)
		game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(Say,"All")
	end	 
})

Tab:AddDropdown({
	Name = "Buso State",
	Default = nil,
	Options = {"0", "1", "2", "3", "4", "5"},
	Callback = function(statebuso)
		if statebuso == "0" then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ChangeBusoStage",0)
elseif statebuso == "1" then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ChangeBusoStage",1)
elseif statebuso == "2" then 
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ChangeBusoStage",2)
elseif statebuso == "3" then 
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ChangeBusoStage",3)
elseif statebuso == "4" then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ChangeBusoStage",4)
elseif statebuso == "5" then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ChangeBusoStage",5)
	end
	end
})

Tab:AddTextbox({
	Name = "Ken Range",
	Default = "Ken Range(30k+ lag)",
	TextDisappear = true,
	Callback = function(KenRange)
		game.Players.LocalPlayer.VisionRadius.Value = KenRange
	end	 
})

Tab:AddButton({
	Name = "Reset",
	Callback = function()
game.Players.LocalPlayer.Character:BreakJoints()
  	end
})

Tab:AddTextbox({
	Name = "Title",
	Default = "Title",
	TextDisappear = true,
	Callback = function(title)
		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateTitle", title)
	end
})

Tab:AddButton({
	Name = "Pirates",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetTeam", "Pirates")
  	end
})

Tab:AddButton({
	Name = "Marines",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetTeam", "Marines")
  	end
})

Tab:AddDropdown({
	Name = "Buso Color",
	Default = nil,
	Options = {"Rainbow Saviour","Winter Sky", "Pure Red", "Snow White","Absolute Zero","Fiery Rose","Heat Wave","Plump Purple","Blue Jeans","Green Lizard","Slimy Green","Yellow Sunshine","Bright Yellow","Orange Soda"},
	Callback = function(busoColor)
if busoColor == "Rainbow Saviour" then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Rainbow Saviour")
   elseif busoColor == "Winter Sky" then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Winter Sky")
   elseif busoColor == "Pure Red" then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Pure Red")
   elseif busoColor == "Snow White" then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Snow White")
   elseif busoColor == "Absolute Zero" then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Absolute Zero")
   elseif busoColor == "Heat Wave" then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Heat Wave")
   elseif busoColor == "Fiery Rose" then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Fiery Rose")
   elseif busoColor == "Plump Purple" then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Plump Purple")
   elseif busoColor == "Blue Jeans" then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Blue Jeans")
   elseif busoColor == "Green Lizard" then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Green Lizard")
   elseif busoColor == "Slimy Green" then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Slimy Green")
   elseif busoColor == "Yellow Sunshine" then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Yellow Sunshine")
   elseif busoColor == "Bright Yellow" then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Bright Yellow")
   elseif busoColor == "Orange Soda" then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Orange Soda")
end
end
})

Tab:AddTextbox({
	Name = "Mastery info",
	Default = nil,
	TextDisappear = true,
	Callback = function(Namik)
     for _,obj in pairs(game.Players[Namik].Backpack:GetChildren()) do
    if obj.ClassName == 'Tool' then
        OrionLib:MakeNotification({
	Name = "Stats",
	Content = 'Name:'.. obj.Name ..'| Mastery:'.. obj.Level.Value ..'.',
	Image = "rbxassetid://4483345998",
	Time = 15
})
end	  
end
end
})

Tab:AddTextbox({
    Name = "Check Stats",
    Default = nil,
    TextDisappear = true,
    Callback = function(plrName)
        OrionLib:MakeNotification({
            Name = "Beli:"..getPlayerByNick(plrName).Data.Beli.Value.."Frags:"..getPlayerByNick(plrName).Data.Fragments.Value..'.',
            Content = "Player's stats",
            Image = "rbxassetid://12496227758",
            Time = 10
        })
    end
})

Tab:AddButton({
	Name = "Check Accessories Info",
	Callback = function()
OrionLib:MakeNotification({
	Name = ''.. game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Nerd") ..'',
	Content = "Nerd",
	Image = "rbxassetid://4483345998",
	Time = 5
})
end
})

Tab:AddButton({
	Name = "X-ray",
	Callback = function()
local sc = (debug and debug.setconstant) or setconstant
	local gc = (debug and debug.getconstants) or getconstants
local pop = game.Players.LocalPlayer.PlayerScripts.PlayerModule.CameraModule.ZoomController.Popper
	for _, v in pairs(getgc()) do
		if type(v) == 'function' and getfenv(v).script == pop then
			for i, v1 in pairs(gc(v)) do
				if tonumber(v1) == .25 then
					sc(v, i, 0)
				elseif tonumber(v1) == 0 then
					sc(v, i, .25)
				end
			end
		end
	end
end
})

Tab:AddButton({
	Name = "No Fog",
	Callback = function()
game.Lighting.FogEnd = 100000
	for i,v in pairs(Lighting:GetDescendants()) do
		if v:IsA("Atmosphere") then
			v:Destroy()
		end
	end
end
})

Tab:AddButton({
	Name = "MaxZoom inf",
	Callback = function()
game.Players.LocalPlayer.CameraMaxZoomDistance = 999999
end
})

Tab:AddButton({
	Name = "MaxZoom normal",
	Callback = function()
game.Players.LocalPlayer.CameraMaxZoomDistance = 100
end
})

elseif game.PlaceId == 4442272183 then

print("Lol")

elseif game.PlaceId == 7449423635 then

local shift = Instance.new("TextButton")
local f9 = Instance.new("TextButton")
local delete = Instance.new("TextButton")
local shift4 = Instance.new("TextButton")
local main = Instance.new("ScreenGui")
local pon = Instance.new("ScreenGui")
local vis = Instance.new("TextButton")
local rj = Instance.new("TextButton")

pon.Parent = game.CoreGui
pon.Name = "Pons"
pon.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

main.Name = "Main"
main.Parent = game.CoreGui
main.ZIndexBehavior = Enum.ZIndexBehavior.Sibling

shift.Name = "shift"
shift.Parent = main
shift.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
shift.BorderSizePixel = 1
shift.BorderColor3 = Color3.fromRGB(255, 160, 30)
shift.Position = UDim2.new(0.200683122, 0, 0, 0)
shift.Size = UDim2.new(0, 50, 0, 50)
shift.Font = Enum.Font.PermanentMarker
shift.Text = "Shift"
shift.TextColor3 = Color3.fromRGB(255, 160, 30)
shift.TextSize = 20.000
shift.TextWrapped = true
shift.MouseButton1Click:Connect(function()
	game:GetService("VirtualInputManager"):SendKeyEvent(true, "RightShift" ,false ,game)
end)

f9.Name = "f9"
f9.Parent = main
f9.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
f9.BorderSizePixel = 1
f9.BorderColor3 = Color3.fromRGB(255, 160, 30)
f9.Position = UDim2.new(0.240683122, 0, 0, 0)
f9.Size = UDim2.new(0, 50, 0, 50)
f9.Font = Enum.Font.PermanentMarker
f9.Text = "f9"
f9.TextColor3 = Color3.fromRGB(255, 160, 30)
f9.TextSize = 35.000
f9.TextWrapped = true
f9.MouseButton1Click:Connect(function()
	game:GetService("VirtualInputManager"):SendKeyEvent(true, "F9" ,false ,game)
end)

delete.Name = "delete"
delete.Parent = main
delete.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
delete.BorderSizePixel = 1
delete.BorderColor3 = Color3.fromRGB(255, 160, 30)
delete.Position = UDim2.new(0.280683122, 0, 0, 0)
delete.Size = UDim2.new(0, 50, 0, 50)
delete.Font = Enum.Font.PermanentMarker
delete.Text = "DEL"
delete.TextColor3 = Color3.fromRGB(255, 160, 30)
delete.TextSize = 35.000
delete.TextWrapped = true
delete.MouseButton1Click:Connect(function()
	main:Destroy()
	pon:Destroy()
end)

vis.Name = "Hide"
vis.Parent = pon
vis.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
vis.BorderSizePixel = 1
vis.BorderColor3 = Color3.fromRGB(255, 160, 30)
vis.Position = UDim2.new(0.320683122, 0, 0, 0)
vis.Size = UDim2.new(0, 50, 0, 50)
vis.Font = Enum.Font.PermanentMarker
vis.Text = "HIDE"
vis.TextColor3 = Color3.fromRGB(255, 160, 30)
vis.TextSize = 20.000
vis.TextWrapped = true
vis.MouseButton1Click:Connect(function()
local maine = game.CoreGui.Main.shift
local del = game.CoreGui.Main.delete
local f9 = game.CoreGui.Main.f9
local rj = game.CoreGui.Main.rj
if maine.Visible == false then
maine.Visible = true
f9.Visible = true
del.Visible = true
rj.Visible = true
		else
			maine.Visible = false
            f9.Visible = false
            del.Visible = false
            rj.Visible = false
		end
end)

rj.Name = "rj"
rj.Parent = main
rj.BackgroundColor3 = Color3.fromRGB(0, 0, 0)
rj.BorderSizePixel = 1
rj.BorderColor3 = Color3.fromRGB(255, 160, 30)
rj.Position = UDim2.new(0.360683122, 0, 0, 0)
rj.Size = UDim2.new(0, 50, 0, 50)
rj.Font = Enum.Font.PermanentMarker
rj.Text = "RJ"
rj.TextColor3 = Color3.fromRGB(255, 160, 30)
rj.TextSize = 35.000
rj.TextWrapped = true
rj.MouseButton1Click:Connect(function()
	if #game.Players:GetPlayers() == 1 then
		game.Players.LocalPlayer:Kick("\nRejoin...")
		wait()
		game:GetService("TeleportService"):Teleport(game.PlaceId, game.Players.LocalPlayer)
	else
		game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId, game.JobId, game.Players.LocalPlayer)
	end
end)

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local OrionLib = loadstring(game:HttpGet(('https://pastebin.com/raw/NDL9HYmx')))()
local Window = OrionLib:MakeWindow({Name = "PoistHub • Sea3", HidePremium = false, SaveConfig = true, ConfigFolder = "PoistHub"})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

--Значения
_G.killaura = true
_G.autochest1 = true
_G.autochest2 = true
_G.autochest3 = true
_G.hitbox = true
_G.automelee = true
_G.autodefense = true
_G.autosword = true
_G.autogun = true
_G.autodevil = true
_G.autorace = true
_G.autobuso = true

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

--Функции
if game.PlaceId == 2753915549 then
World1 = true
elseif game.PlaceId == 4442272183 then
World2 = true
elseif game.PlaceId == 7449423635 then
World3 = true
end

function CheckQuest()
MyLevel = game:GetService("Players").LocalPlayer.Data.Level.Value
if World1 then
if MyLevel == 1 or MyLevel <= 9 then
Mon = "Bandit [Lv. 5]"
LevelQuest = 1
NameQuest = "BanditQuest1"
NameMon = "Bandit"
CFrameQuest = CFrame.new(1059.37195, 15.4495068, 1550.4231, 0.939700544, -0, -0.341998369, 0, 1, -0, 0.341998369, 0, 0.939700544)
elseif MyLevel == 10 or MyLevel <= 14 then
Mon = "Monkey [Lv. 14]"
LevelQuest = 1
NameQuest = "JungleQuest"
NameMon = "Monkey"
CFrameQuest = CFrame.new(-1598.08911, 35.5501175, 153.377838, 0, 0, 1, 0, 1, -0, -1, 0, 0)
elseif MyLevel == 15 or MyLevel <= 29 then
Mon = "Gorilla [Lv. 20]"
LevelQuest = 2
NameQuest = "JungleQuest"
NameMon = "Gorilla"
CFrameQuest = CFrame.new(-1598.08911, 35.5501175, 153.377838, 0, 0, 1, 0, 1, -0, -1, 0, 0)
elseif MyLevel == 30 or MyLevel <= 39 then
Mon = "Pirate [Lv. 35]"
LevelQuest = 1
NameQuest = "BuggyQuest1"
NameMon = "Pirate"
CFrameQuest = CFrame.new(-1141.07483, 4.10001802, 3831.5498, 0.965929627, -0, -0.258804798, 0, 1, -0, 0.258804798, 0, 0.965929627)
elseif MyLevel == 40 or MyLevel <= 59 then
Mon = "Brute [Lv. 45]"
LevelQuest = 2
NameQuest = "BuggyQuest1"
NameMon = "Brute"
CFrameQuest = CFrame.new(-1141.07483, 4.10001802, 3831.5498, 0.965929627, -0, -0.258804798, 0, 1, -0, 0.258804798, 0, 0.965929627)
elseif MyLevel == 60 or MyLevel <= 74 then
Mon = "Desert Bandit [Lv. 60]"
LevelQuest = 1
NameQuest = "DesertQuest"
NameMon = "Desert Bandit"
CFrameQuest = CFrame.new(894.488647, 5.14000702, 4392.43359, 0.819155693, -0, -0.573571265, 0, 1, -0, 0.573571265, 0, 0.819155693)
elseif MyLevel == 75 or MyLevel <= 89 then
Mon = "Desert Officer [Lv. 70]"
LevelQuest = 2
NameQuest = "DesertQuest"
NameMon = "Desert Officer"
CFrameQuest = CFrame.new(894.488647, 5.14000702, 4392.43359, 0.819155693, -0, -0.573571265, 0, 1, -0, 0.573571265, 0, 0.819155693)
elseif MyLevel == 90 or MyLevel <= 99 then
Mon = "Snow Bandit [Lv. 90]"
LevelQuest = 1
NameQuest = "SnowQuest"
NameMon = "Snow Bandit"
CFrameQuest = CFrame.new(1389.74451, 88.1519318, -1298.90796, -0.342042685, 0, 0.939684391, 0, 1, 0, -0.939684391, 0, -0.342042685)
elseif MyLevel == 100 or MyLevel <= 119 then
Mon = "Snowman [Lv. 100]"
LevelQuest = 2
NameQuest = "SnowQuest"
NameMon = "Snowman"
CFrameQuest = CFrame.new(1389.74451, 88.1519318, -1298.90796, -0.342042685, 0, 0.939684391, 0, 1, 0, -0.939684391, 0, -0.342042685)
elseif MyLevel == 120 or MyLevel <= 149 then
Mon = "Chief Petty Officer [Lv. 120]"
LevelQuest = 1
NameQuest = "MarineQuest2"
NameMon = "Chief Petty Officer"
CFrameQuest = CFrame.new(-5039.58643, 27.3500385, 4324.68018, 0, 0, -1, 0, 1, 0, 1, 0, 0)
elseif MyLevel == 150 or MyLevel <= 174 then
Mon = "Sky Bandit [Lv. 150]"
LevelQuest = 1
NameQuest = "SkyQuest"
NameMon = "Sky Bandit"
CFrameQuest = CFrame.new(-4839.53027, 716.368591, -2619.44165, 0.866007268, 0, 0.500031412, 0, 1, 0, -0.500031412, 0, 0.866007268)
elseif MyLevel == 175 or MyLevel <= 189 then
Mon = "Dark Master [Lv. 175]"
LevelQuest = 2
NameQuest = "SkyQuest"
NameMon = "Dark Master"
CFrameQuest = CFrame.new(-4839.53027, 716.368591, -2619.44165, 0.866007268, 0, 0.500031412, 0, 1, 0, -0.500031412, 0, 0.866007268)
elseif MyLevel == 190 or MyLevel <= 209 then
Mon = "Prisoner [Lv. 190]"
LevelQuest = 1
NameQuest = "PrisonerQuest"
NameMon = "Prisoner"
CFrameQuest = CFrame.new(5308.93115, 1.65517521, 475.120514, -0.0894274712, -5.00292918e-09, -0.995993316, 1.60817859e-09, 1, -5.16744869e-09, 0.995993316, -2.06384709e-09, -0.0894274712)
elseif MyLevel == 210 or MyLevel <= 249 then
Mon = "Dangerous Prisoner [Lv. 210]"
LevelQuest = 2
NameQuest = "PrisonerQuest"
NameMon = "Dangerous Prisoner"
CFrameQuest = CFrame.new(5308.93115, 1.65517521, 475.120514, -0.0894274712, -5.00292918e-09, -0.995993316, 1.60817859e-09, 1, -5.16744869e-09, 0.995993316, -2.06384709e-09, -0.0894274712)
elseif MyLevel == 250 or MyLevel <= 274 then
Mon = "Toga Warrior [Lv. 250]"
LevelQuest = 1
NameQuest = "ColosseumQuest"
NameMon = "Toga Warrior"
CFrameQuest = CFrame.new(-1580.04663, 6.35000277, -2986.47534, -0.515037298, 0, -0.857167721, 0, 1, 0, 0.857167721, 0, -0.515037298)
elseif MyLevel == 275 or MyLevel <= 299 then
Mon = "Gladiator [Lv. 275]"
LevelQuest = 2
NameQuest = "ColosseumQuest"
NameMon = "Gladiator"
CFrameQuest = CFrame.new(-1580.04663, 6.35000277, -2986.47534, -0.515037298, 0, -0.857167721, 0, 1, 0, 0.857167721, 0, -0.515037298)
elseif MyLevel == 300 or MyLevel <= 324 then
Mon = "Military Soldier [Lv. 300]"
LevelQuest = 1
NameQuest = "MagmaQuest"
NameMon = "Military Soldier"
CFrameQuest = CFrame.new(-5313.37012, 10.9500084, 8515.29395, -0.499959469, 0, 0.866048813, 0, 1, 0, -0.866048813, 0, -0.499959469)
elseif MyLevel == 325 or MyLevel <= 374 then
Mon = "Military Spy [Lv. 325]"
LevelQuest = 2
NameQuest = "MagmaQuest"
NameMon = "Military Spy"
CFrameQuest = CFrame.new(-5313.37012, 10.9500084, 8515.29395, -0.499959469, 0, 0.866048813, 0, 1, 0, -0.866048813, 0, -0.499959469)
elseif MyLevel == 375 or MyLevel <= 399 then
Mon = "Fishman Warrior [Lv. 375]"
LevelQuest = 1
NameQuest = "FishmanQuest"
NameMon = "Fishman Warrior"
CFrameQuest = CFrame.new(61122.65234375, 18.497442245483, 1569.3997802734)
if _G.AutoFarm and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 10000 then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(61163.8515625, 11.6796875, 1819.7841796875))
end
elseif MyLevel == 400 or MyLevel <= 449 then
Mon = "Fishman Commando [Lv. 400]"
LevelQuest = 2
NameQuest = "FishmanQuest"
NameMon = "Fishman Commando"
CFrameQuest = CFrame.new(61122.65234375, 18.497442245483, 1569.3997802734)
if _G.AutoFarm and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 10000 then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(61163.8515625, 11.6796875, 1819.7841796875))
end
elseif MyLevel == 450 or MyLevel <= 474 then
Mon = "God's Guard [Lv. 450]"
LevelQuest = 1
NameQuest = "SkyExp1Quest"
NameMon = "God's Guard"
CFrameQuest = CFrame.new(-4721.88867, 843.874695, -1949.96643, 0.996191859, -0, -0.0871884301, 0, 1, -0, 0.0871884301, 0, 0.996191859)
if _G.AutoFarm and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 10000 then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-4607.82275, 872.54248, -1667.55688))
end
elseif MyLevel == 475 or MyLevel <= 524 then
Mon = "Shanda [Lv. 475]"
LevelQuest = 2
NameQuest = "SkyExp1Quest"
NameMon = "Shanda"
CFrameQuest = CFrame.new(-7859.09814, 5544.19043, -381.476196, -0.422592998, 0, 0.906319618, 0, 1, 0, -0.906319618, 0, -0.422592998)
if _G.AutoFarm and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 10000 then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-7894.6176757813, 5547.1416015625, -380.29119873047))
end
elseif MyLevel == 525 or MyLevel <= 549 then
Mon = "Royal Squad [Lv. 525]"
LevelQuest = 1
NameQuest = "SkyExp2Quest"
NameMon = "Royal Squad"
CFrameQuest = CFrame.new(-7906.81592, 5634.6626, -1411.99194, 0, 0, -1, 0, 1, 0, 1, 0, 0)
elseif MyLevel == 550 or MyLevel <= 624 then
Mon = "Royal Soldier [Lv. 550]"
LevelQuest = 2
NameQuest = "SkyExp2Quest"
NameMon = "Royal Soldier"
CFrameQuest = CFrame.new(-7906.81592, 5634.6626, -1411.99194, 0, 0, -1, 0, 1, 0, 1, 0, 0)
elseif MyLevel == 625 or MyLevel <= 649 then
Mon = "Galley Pirate [Lv. 625]"
LevelQuest = 1
NameQuest = "FountainQuest"
NameMon = "Galley Pirate"
CFrameQuest = CFrame.new(5259.81982, 37.3500175, 4050.0293, 0.087131381, 0, 0.996196866, 0, 1, 0, -0.996196866, 0, 0.087131381)
elseif MyLevel >= 650 then
Mon = "Galley Captain [Lv. 650]"
LevelQuest = 2
NameQuest = "FountainQuest"
NameMon = "Galley Captain"
CFrameQuest = CFrame.new(5259.81982, 37.3500175, 4050.0293, 0.087131381, 0, 0.996196866, 0, 1, 0, -0.996196866, 0, 0.087131381)
end
elseif World2 then
if MyLevel == 700 or MyLevel <= 724 then
Mon = "Raider [Lv. 700]"
LevelQuest = 1
NameQuest = "Area1Quest"
NameMon = "Raider"
CFrameQuest = CFrame.new(-429.543518, 71.7699966, 1836.18188, -0.22495985, 0, -0.974368095, 0, 1, 0, 0.974368095, 0, -0.22495985)
elseif MyLevel == 725 or MyLevel <= 774 then
Mon = "Mercenary [Lv. 725]"
LevelQuest = 2
NameQuest = "Area1Quest"
NameMon = "Mercenary"
CFrameQuest = CFrame.new(-429.543518, 71.7699966, 1836.18188, -0.22495985, 0, -0.974368095, 0, 1, 0, 0.974368095, 0, -0.22495985)
elseif MyLevel == 775 or MyLevel <= 799 then
Mon = "Swan Pirate [Lv. 775]"
LevelQuest = 1
NameQuest = "Area2Quest"
NameMon = "Swan Pirate"
CFrameQuest = CFrame.new(638.43811, 71.769989, 918.282898, 0.139203906, 0, 0.99026376, 0, 1, 0, -0.99026376, 0, 0.139203906)
elseif MyLevel == 800 or MyLevel <= 874 then
Mon = "Factory Staff [Lv. 800]"
NameQuest = "Area2Quest"
LevelQuest = 2
NameMon = "Factory Staff"
CFrameQuest = CFrame.new(632.698608, 73.1055908, 918.666321, -0.0319722369, 8.96074881e-10, -0.999488771, 1.36326533e-10, 1, 8.92172336e-10, 0.999488771, -1.07732087e-10, -0.0319722369)
elseif MyLevel == 875 or MyLevel <= 899 then
Mon = "Marine Lieutenant [Lv. 875]"
LevelQuest = 1
NameQuest = "MarineQuest3"
NameMon = "Marine Lieutenant"
CFrameQuest = CFrame.new(-2440.79639, 71.7140732, -3216.06812, 0.866007268, 0, 0.500031412, 0, 1, 0, -0.500031412, 0, 0.866007268)
elseif MyLevel == 900 or MyLevel <= 949 then
Mon = "Marine Captain [Lv. 900]"
LevelQuest = 2
NameQuest = "MarineQuest3"
NameMon = "Marine Captain"
CFrameQuest = CFrame.new(-2440.79639, 71.7140732, -3216.06812, 0.866007268, 0, 0.500031412, 0, 1, 0, -0.500031412, 0, 0.866007268)
elseif MyLevel == 950 or MyLevel <= 974 then
Mon = "Zombie [Lv. 950]"
LevelQuest = 1
NameQuest = "ZombieQuest"
NameMon = "Zombie"
CFrameQuest = CFrame.new(-5497.06152, 47.5923004, -795.237061, -0.29242146, 0, -0.95628953, 0, 1, 0, 0.95628953, 0, -0.29242146)
elseif MyLevel == 975 or MyLevel <= 999 then
Mon = "Vampire [Lv. 975]"
LevelQuest = 2
NameQuest = "ZombieQuest"
NameMon = "Vampire"
CFrameQuest = CFrame.new(-5497.06152, 47.5923004, -795.237061, -0.29242146, 0, -0.95628953, 0, 1, 0, 0.95628953, 0, -0.29242146)
elseif MyLevel == 1000 or MyLevel <= 1049 then
Mon = "Snow Trooper [Lv. 1000]"
LevelQuest = 1
NameQuest = "SnowMountainQuest"
NameMon = "Snow Trooper"
CFrameQuest = CFrame.new(609.858826, 400.119904, -5372.25928, -0.374604106, 0, 0.92718488, 0, 1, 0, -0.92718488, 0, -0.374604106)
elseif MyLevel == 1050 or MyLevel <= 1099 then
Mon = "Winter Warrior [Lv. 1050]"
LevelQuest = 2
NameQuest = "SnowMountainQuest"
NameMon = "Winter Warrior"
CFrameQuest = CFrame.new(609.858826, 400.119904, -5372.25928, -0.374604106, 0, 0.92718488, 0, 1, 0, -0.92718488, 0, -0.374604106)
elseif MyLevel == 1100 or MyLevel <= 1124 then
Mon = "Lab Subordinate [Lv. 1100]"
LevelQuest = 1
NameQuest = "IceSideQuest"
NameMon = "Lab Subordinate"
CFrameQuest = CFrame.new(-6064.06885, 15.2422857, -4902.97852, 0.453972578, -0, -0.891015649, 0, 1, -0, 0.891015649, 0, 0.453972578)
elseif MyLevel == 1125 or MyLevel <= 1174 then
Mon = "Horned Warrior [Lv. 1125]"
LevelQuest = 2
NameQuest = "IceSideQuest"
NameMon = "Horned Warrior"
CFrameQuest = CFrame.new(-6064.06885, 15.2422857, -4902.97852, 0.453972578, -0, -0.891015649, 0, 1, -0, 0.891015649, 0, 0.453972578)
elseif MyLevel == 1175 or MyLevel <= 1199 then
Mon = "Magma Ninja [Lv. 1175]"
LevelQuest = 1
NameQuest = "FireSideQuest"
NameMon = "Magma Ninja"
CFrameQuest = CFrame.new(-5428.03174, 15.0622921, -5299.43457, -0.882952213, 0, 0.469463557, 0, 1, 0, -0.469463557, 0, -0.882952213)
elseif MyLevel == 1200 or MyLevel <= 1249 then
Mon = "Lava Pirate [Lv. 1200]"
LevelQuest = 2
NameQuest = "FireSideQuest"
NameMon = "Lava Pirate"
CFrameQuest = CFrame.new(-5428.03174, 15.0622921, -5299.43457, -0.882952213, 0, 0.469463557, 0, 1, 0, -0.469463557, 0, -0.882952213)
elseif MyLevel == 1250 or MyLevel <= 1274 then
Mon = "Ship Deckhand [Lv. 1250]"
LevelQuest = 1
NameQuest = "ShipQuest1"
NameMon = "Ship Deckhand"
CFrameQuest = CFrame.new(1037.80127, 125.092171, 32911.6016)
if _G.AutoFarm and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 10000 then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(923.21252441406, 126.9760055542, 32852.83203125))
end
elseif MyLevel == 1275 or MyLevel <= 1299 then
Mon = "Ship Engineer [Lv. 1275]"
LevelQuest = 2
NameQuest = "ShipQuest1"
NameMon = "Ship Engineer"
CFrameQuest = CFrame.new(1037.80127, 125.092171, 32911.6016)
if _G.AutoFarm and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 10000 then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(923.21252441406, 126.9760055542, 32852.83203125))
end
elseif MyLevel == 1300 or MyLevel <= 1324 then
Mon = "Ship Steward [Lv. 1300]"
LevelQuest = 1
NameQuest = "ShipQuest2"
NameMon = "Ship Steward"
CFrameQuest = CFrame.new(968.80957, 125.092171, 33244.125)
if _G.AutoFarm and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 10000 then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(923.21252441406, 126.9760055542, 32852.83203125))
end
elseif MyLevel == 1325 or MyLevel <= 1349 then
Mon = "Ship Officer [Lv. 1325]"
LevelQuest = 2
NameQuest = "ShipQuest2"
NameMon = "Ship Officer"
CFrameQuest = CFrame.new(968.80957, 125.092171, 33244.125)
if _G.AutoFarm and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 10000 then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(923.21252441406, 126.9760055542, 32852.83203125))
end
elseif MyLevel == 1350 or MyLevel <= 1374 then
Mon = "Arctic Warrior [Lv. 1350]"
LevelQuest = 1
NameQuest = "FrostQuest"
NameMon = "Arctic Warrior"
CFrameQuest = CFrame.new(5667.6582, 26.7997818, -6486.08984, -0.933587909, 0, -0.358349502, 0, 1, 0, 0.358349502, 0, -0.933587909)
if _G.AutoFarm and (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude > 10000 then
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("requestEntrance",Vector3.new(-6508.5581054688, 5000.034996032715, -132.83953857422))
end
elseif MyLevel == 1375 or MyLevel <= 1424 then
Mon = "Snow Lurker [Lv. 1375]"
LevelQuest = 2
NameQuest = "FrostQuest"
NameMon = "Snow Lurker"
CFrameQuest = CFrame.new(5667.6582, 26.7997818, -6486.08984, -0.933587909, 0, -0.358349502, 0, 1, 0, 0.358349502, 0, -0.933587909)
elseif MyLevel == 1425 or MyLevel <= 1449 then
Mon = "Sea Soldier [Lv. 1425]"
LevelQuest = 1
NameQuest = "ForgottenQuest"
NameMon = "Sea Soldier"
CFrameQuest = CFrame.new(-3054.44458, 235.544281, -10142.8193, 0.990270376, -0, -0.13915664, 0, 1, -0, 0.13915664, 0, 0.990270376)
elseif MyLevel >= 1450 then
Mon = "Water Fighter [Lv. 1450]"
LevelQuest = 2
NameQuest = "ForgottenQuest"
NameMon = "Water Fighter"
CFrameQuest = CFrame.new(-3054.44458, 235.544281, -10142.8193, 0.990270376, -0, -0.13915664, 0, 1, -0, 0.13915664, 0, 0.990270376)
end
elseif World3 then
if MyLevel == 1500 or MyLevel <= 1524 then
Mon = "Pirate Millionaire [Lv. 1500]"
LevelQuest = 1
NameQuest = "PiratePortQuest"
NameMon = "Pirate Millionaire"
CFrameQuest = CFrame.new(-290.074677, 42.9034653, 5581.58984, 0.965929627, -0, -0.258804798, 0, 1, -0, 0.258804798, 0, 0.965929627)
elseif MyLevel == 1525 or MyLevel <= 1574 then
Mon = "Pistol Billionaire [Lv. 1525]"
LevelQuest = 2
NameQuest = "PiratePortQuest"
NameMon = "Pistol Billionaire"
CFrameQuest = CFrame.new(-290.074677, 42.9034653, 5581.58984, 0.965929627, -0, -0.258804798, 0, 1, -0, 0.258804798, 0, 0.965929627)
elseif MyLevel == 1575 or MyLevel <= 1599 then
Mon = "Dragon Crew Warrior [Lv. 1575]"
LevelQuest = 1
NameQuest = "AmazonQuest"
NameMon = "Dragon Crew Warrior"
CFrameQuest = CFrame.new(5832.83594, 51.6806107, -1101.51563, 0.898790359, -0, -0.438378751, 0, 1, -0, 0.438378751, 0, 0.898790359)
elseif MyLevel == 1600 or MyLevel <= 1624 then
Mon = "Dragon Crew Archer [Lv. 1600]"
NameQuest = "AmazonQuest"
LevelQuest = 2
NameMon = "Dragon Crew Archer"
CFrameQuest = CFrame.new(5833.1147460938, 51.60498046875, -1103.0693359375)
elseif MyLevel == 1625 or MyLevel <= 1649 then
Mon = "Female Islander [Lv. 1625]"
NameQuest = "AmazonQuest2"
LevelQuest = 1
NameMon = "Female Islander"
CFrameQuest = CFrame.new(5446.8793945313, 601.62945556641, 749.45672607422)
elseif MyLevel == 1650 or MyLevel <= 1699 then
Mon = "Giant Islander [Lv. 1650]"
NameQuest = "AmazonQuest2"
LevelQuest = 2
NameMon = "Giant Islander"
CFrameQuest = CFrame.new(5446.8793945313, 601.62945556641, 749.45672607422)
elseif MyLevel == 1700 or MyLevel <= 1724 then
Mon = "Marine Commodore [Lv. 1700]"
LevelQuest = 1
NameQuest = "MarineTreeIsland"
NameMon = "Marine Commodore"
CFrameQuest = CFrame.new(2180.54126, 27.8156815, -6741.5498, -0.965929747, 0, 0.258804798, 0, 1, 0, -0.258804798, 0, -0.965929747)
elseif MyLevel == 1725 or MyLevel <= 1774 then
Mon = "Marine Rear Admiral [Lv. 1725]"
NameMon = "Marine Rear Admiral"
NameQuest = "MarineTreeIsland"
LevelQuest = 2
CFrameQuest = CFrame.new(2179.98828125, 28.731239318848, -6740.0551757813)
elseif MyLevel == 1775 or MyLevel <= 1799 then
Mon = "Fishman Raider [Lv. 1775]"
LevelQuest = 1
NameQuest = "DeepForestIsland3"
NameMon = "Fishman Raider"
CFrameQuest = CFrame.new(-10581.6563, 330.872955, -8761.18652, -0.882952213, 0, 0.469463557, 0, 1, 0, -0.469463557, 0, -0.882952213)
elseif MyLevel == 1800 or MyLevel <= 1824 then
Mon = "Fishman Captain [Lv. 1800]"
LevelQuest = 2
NameQuest = "DeepForestIsland3"
NameMon = "Fishman Captain"
CFrameQuest = CFrame.new(-10581.6563, 330.872955, -8761.18652, -0.882952213, 0, 0.469463557, 0, 1, 0, -0.469463557, 0, -0.882952213)
elseif MyLevel == 1825 or MyLevel <= 1849 then
Mon = "Forest Pirate [Lv. 1825]"
LevelQuest = 1
NameQuest = "DeepForestIsland"
NameMon = "Forest Pirate"
CFrameQuest = CFrame.new(-13234.04, 331.488495, -7625.40137, 0.707134247, -0, -0.707079291, 0, 1, -0, 0.707079291, 0, 0.707134247)
elseif MyLevel == 1850 or MyLevel <= 1899 then
Mon = "Mythological Pirate [Lv. 1850]"
LevelQuest = 2
NameQuest = "DeepForestIsland"
NameMon = "Mythological Pirate"
CFrameQuest = CFrame.new(-13234.04, 331.488495, -7625.40137, 0.707134247, -0, -0.707079291, 0, 1, -0, 0.707079291, 0, 0.707134247)
elseif MyLevel == 1900 or MyLevel <= 1924 then
Mon = "Jungle Pirate [Lv. 1900]"
LevelQuest = 1
NameQuest = "DeepForestIsland2"
NameMon = "Jungle Pirate"
CFrameQuest = CFrame.new(-12680.3818, 389.971039, -9902.01953, -0.0871315002, 0, 0.996196866, 0, 1, 0, -0.996196866, 0, -0.0871315002)
elseif MyLevel == 1925 or MyLevel <= 1974 then
Mon = "Musketeer Pirate [Lv. 1925]"
LevelQuest = 2
NameQuest = "DeepForestIsland2"
NameMon = "Musketeer Pirate"
CFrameQuest = CFrame.new(-12680.3818, 389.971039, -9902.01953, -0.0871315002, 0, 0.996196866, 0, 1, 0, -0.996196866, 0, -0.0871315002)
elseif MyLevel == 1975 or MyLevel <= 1999 then
Mon = "Reborn Skeleton [Lv. 1975]"
LevelQuest = 1
NameQuest = "HauntedQuest1"
NameMon = "Reborn Skeleton"
CFrameQuest = CFrame.new(-9479.2168, 141.215088, 5566.09277, 0, 0, 1, 0, 1, -0, -1, 0, 0)
elseif MyLevel == 2000 or MyLevel <= 2024 then
Mon = "Living Zombie [Lv. 2000]"
LevelQuest = 2
NameQuest = "HauntedQuest1"
NameMon = "Living Zombie"
CFrameQuest = CFrame.new(-9479.2168, 141.215088, 5566.09277, 0, 0, 1, 0, 1, -0, -1, 0, 0)
elseif MyLevel == 2025 or MyLevel <= 2049 then
Mon = "Demonic Soul [Lv. 2025]"
LevelQuest = 1
NameQuest = "HauntedQuest2"
NameMon = "Demonic Soul"
CFrameQuest = CFrame.new(-9516.99316, 172.017181, 6078.46533, 0, 0, -1, 0, 1, 0, 1, 0, 0)
elseif MyLevel == 2050 or MyLevel <= 2074 then
Mon = "Posessed Mummy [Lv. 2050]"
LevelQuest = 2
NameQuest = "HauntedQuest2"
NameMon = "Posessed Mummy"
CFrameQuest = CFrame.new(-9516.99316, 172.017181, 6078.46533, 0, 0, -1, 0, 1, 0, 1, 0, 0)
elseif MyLevel == 2075 or MyLevel <= 2099 then
Mon = "Peanut Scout [Lv. 2075]"
LevelQuest = 1
NameQuest = "NutsIslandQuest"
NameMon = "Peanut Scout"
CFrameQuest = CFrame.new(-2104.3908691406, 38.104167938232, -10194.21875, 0, 0, -1, 0, 1, 0, 1, 0, 0)
elseif MyLevel == 2100 or MyLevel <= 2124 then
Mon = "Peanut President [Lv. 2100]"
LevelQuest = 2
NameQuest = "NutsIslandQuest"
NameMon = "Peanut President"
CFrameQuest = CFrame.new(-2104.3908691406, 38.104167938232, -10194.21875, 0, 0, -1, 0, 1, 0, 1, 0, 0)
elseif MyLevel == 2125 or MyLevel <= 2149 then
Mon = "Ice Cream Chef [Lv. 2125]"
LevelQuest = 1
NameQuest = "IceCreamIslandQuest"
NameMon = "Ice Cream Chef"
CFrameQuest = CFrame.new(-820.64825439453, 65.819526672363, -10965.795898438, 0, 0, -1, 0, 1, 0, 1, 0, 0)
elseif MyLevel == 2150 or MyLevel <= 2199 then
Mon = "Ice Cream Commander [Lv. 2150]"
LevelQuest = 2
NameQuest = "IceCreamIslandQuest"
NameMon = "Ice Cream Commander"
CFrameQuest = CFrame.new(-820.64825439453, 65.819526672363, -10965.795898438, 0, 0, -1, 0, 1, 0, 1, 0, 0)
elseif MyLevel == 2200 or MyLevel <= 2224 then
Mon = "Cookie Crafter [Lv. 2200]"
LevelQuest = 1
NameQuest = "CakeQuest1"
NameMon = "Cookie Crafter"
CFrameQuest = CFrame.new(-2021.32007, 37.7982254, -12028.7295, 0.957576931, -8.80302053e-08, 0.288177818, 6.9301187e-08, 1, 7.51931211e-08, -0.288177818, -5.2032135e-08, 0.957576931)
elseif MyLevel == 2225 or MyLevel <= 2249 then
Mon = "Cake Guard [Lv. 2225]"
LevelQuest = 2
NameQuest = "CakeQuest1"
NameMon = "Cake Guard"
CFrameQuest = CFrame.new(-2021.32007, 37.7982254, -12028.7295, 0.957576931, -8.80302053e-08, 0.288177818, 6.9301187e-08, 1, 7.51931211e-08, -0.288177818, -5.2032135e-08, 0.957576931)
elseif MyLevel == 2250 or MyLevel <= 2274 then
Mon = "Baking Staff [Lv. 2250]"
LevelQuest = 1
NameQuest = "CakeQuest2"
NameMon = "Baking Staff"
CFrameQuest = CFrame.new(-1927.91602, 37.7981339, -12842.5391, -0.96804446, 4.22142143e-08, 0.250778586, 4.74911062e-08, 1, 1.49904711e-08, -0.250778586, 2.64211941e-08, -0.96804446)
elseif MyLevel >= 2275 then
Mon = "Head Baker [Lv. 2275]"
LevelQuest = 2
NameQuest = "CakeQuest2"
NameMon = "Head Baker"
CFrameQuest = CFrame.new(-1927.91602, 37.7981339, -12842.5391, -0.96804446, 4.22142143e-08, 0.250778586, 4.74911062e-08, 1, 1.49904711e-08, -0.250778586, 2.64211941e-08, -0.96804446)
end
end
end

function isnil(thing)
return (thing == nil)
end

local function round(n)
return math.floor(tonumber(n) + 0.5)
end

function StopTween(target)
if not target then
_G.StopTween = true
wait()
topos(game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame)
wait()
if game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip") then
game:GetService("Players").LocalPlayer.Character.HumanoidRootPart:FindFirstChild("BodyClip"):Destroy()
end
_G.StopTween = false
_G.Clip = false
end
end

function UpdateEspPlayer()
if ESPPlayer then
for i,v in pairs(game:GetService("Players"):GetPlayers()) do
if not isnil(v.Character) then
if not v.Character.Head:FindFirstChild('NameEsp'..v.Name) then
local BillboardGui = Instance.new("BillboardGui")
local ESP = Instance.new("TextLabel")
local HealthESP = Instance.new("TextLabel")
BillboardGui.Parent = v.Character.Head
BillboardGui.Name = 'NameEsp'..v.Name
BillboardGui.ExtentsOffset = Vector3.new(0, 1, 0)
BillboardGui.Size = UDim2.new(1,200,1,30)
BillboardGui.Adornee = v.Character.Head
BillboardGui.AlwaysOnTop = true
ESP.Name = "ESP"
ESP.Parent = BillboardGui
ESP.TextTransparency = 0
ESP.BackgroundTransparency = 1
ESP.Size = UDim2.new(0, 200, 0, 30)
ESP.Position = UDim2.new(0,25,0,0)
ESP.Font = Enum.Font.Gotham
ESP.Text = (v.Name ..' '.."[ "..round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Character.Head.Position).Magnitude/3) ..' M'.." ]")
if v.Team == game:GetService("Players").LocalPlayer.Team then
ESP.TextColor3 = Color3.new(0, 255, 255)
else
ESP.TextColor3 = Color3.new(255, 0, 0)
end
ESP.TextSize = 14
ESP.TextStrokeTransparency = 0.500
ESP.TextWrapped = true
HealthESP.Name = "HealthESP"
HealthESP.Parent = ESP
HealthESP.TextTransparency = 0
HealthESP.BackgroundTransparency = 1
HealthESP.Position = ESP.Position + UDim2.new(0, -25, 0, 15)
HealthESP.Size = UDim2.new(0, 200, 0, 30)
HealthESP.Font = Enum.Font.Gotham
HealthESP.TextColor3 = Color3.fromRGB(255, 0, 0)
HealthESP.TextSize = 14
HealthESP.TextStrokeTransparency = 0.500
HealthESP.TextWrapped = true
HealthESP.Text = "Health "..math.floor(v.Character.Humanoid.Health).."/"..math.floor(v.Character.Humanoid.MaxHealth)
else
v.Character.Head['NameEsp'..v.Name].ESP.Text = (v.Name ..' '..round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Character.Head.Position).Magnitude/3) ..' M')
v.Character.Head['NameEsp'..v.Name].ESP.HealthESP.Text = "Health "..math.floor(v.Character.Humanoid.Health).."/"..math.floor(v.Character.Humanoid.MaxHealth)
v.Character.Head:FindFirstChild('NameEsp'..v.Name).ESP.TextTransparency = 0
v.Character.Head:FindFirstChild('NameEsp'..v.Name).ESP.HealthESP.TextTransparency = 0
end
end
end
else
for i,v in pairs(game:GetService("Players"):GetPlayers()) do
if v.Character.Head:FindFirstChild('NameEsp'..v.Name) then
v.Character.Head:FindFirstChild('NameEsp'..v.Name).ESP.TextTransparency = 1
v.Character.Head:FindFirstChild('NameEsp'..v.Name).ESP.TextStrokeTransparency = 1
v.Character.Head:FindFirstChild('NameEsp'..v.Name).ESP.HealthESP.TextTransparency = 1
v.Character.Head:FindFirstChild('NameEsp'..v.Name).ESP.HealthESP.TextStrokeTransparency = 1
end
end
end
end

function UpdateIslandESP()
for i,v in pairs(game:GetService("Workspace")["_WorldOrigin"].Locations:GetChildren()) do
pcall(function()
if IslandESP then
if v.Name ~= "Sea" then
if not v:FindFirstChild('NameEsp') then
local bill = Instance.new('BillboardGui',v)
bill.Name = 'NameEsp'
bill.ExtentsOffset = Vector3.new(0, 1, 0)
bill.Size = UDim2.new(1,200,1,30)
bill.Adornee = v
bill.AlwaysOnTop = true
local name = Instance.new('TextLabel',bill)
name.Font = "GothamBold"
name.FontSize = "Size14"
name.TextWrapped = true
name.Size = UDim2.new(1,0,1,0)
name.TextYAlignment = 'Top'
name.BackgroundTransparency = 1
name.TextStrokeTransparency = 0.5
name.TextColor3 = Color3.fromRGB(80, 245, 245)
else
v['NameEsp'].TextLabel.Text = (v.Name ..'   \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')
end
end
else
if v:FindFirstChild('NameEsp') then
v:FindFirstChild('NameEsp'):Destroy()
end
end
end)
end
end

function UpdateChestEsp()
for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
pcall(function()
if string.find(v.Name,"Chest") then
if ChestESP then
if string.find(v.Name,"Chest") then
if not v:FindFirstChild('NameEsp'..Number) then
local bill = Instance.new('BillboardGui',v)
bill.Name = 'NameEsp'..Number
bill.ExtentsOffset = Vector3.new(0, 1, 0)
bill.Size = UDim2.new(1,200,1,30)
bill.Adornee = v
bill.AlwaysOnTop = true
local name = Instance.new('TextLabel',bill)
name.Font = "GothamBold"
name.FontSize = "Size14"
name.TextWrapped = true
name.Size = UDim2.new(1,0,1,0)
name.TextYAlignment = 'Top'
name.BackgroundTransparency = 1
name.TextStrokeTransparency = 0.5
name.TextColor3 = Color3.fromRGB(255, 160, 30)
if v.Name == "Chest1" then
name.Text = ("Silver Chest" ..' \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')
end
if v.Name == "Chest2" then
name.Text = ("Gold Chest" ..' \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')
end
if v.Name == "Chest3" then
name.Text = ("Diamond Chest" ..' \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')
end
else
v['NameEsp'..Number].TextLabel.Text = (v.Name ..'   \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')
end
end
else
if v:FindFirstChild('NameEsp'..Number) then
v:FindFirstChild('NameEsp'..Number):Destroy()
end
end
end
end)
end
end

function UpdateBfEsp()
for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
pcall(function()
if DevilFruitESP then
if string.find(v.Name, "Fruit") then
if not v.Handle:FindFirstChild('NameEsp'..Number) then
local bill = Instance.new('BillboardGui',v.Handle)
bill.Name = 'NameEsp'..Number
bill.ExtentsOffset = Vector3.new(0, 1, 0)
bill.Size = UDim2.new(1,200,1,30)
bill.Adornee = v.Handle
bill.AlwaysOnTop = true
local name = Instance.new('TextLabel',bill)
name.Font = "GothamBold"
name.FontSize = "Size14"
name.TextWrapped = true
name.Size = UDim2.new(1,0,1,0)
name.TextYAlignment = 'Top'
name.BackgroundTransparency = 1
name.TextStrokeTransparency = 0.5
name.TextColor3 = Color3.fromRGB(255, 160, 30)
name.Text = (v.Name ..' \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Handle.Position).Magnitude/3) ..' M')
else
v.Handle['NameEsp'..Number].TextLabel.Text = (v.Name ..'   \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Handle.Position).Magnitude/3) ..' M')
end
end
else
if v.Handle:FindFirstChild('NameEsp'..Number) then
v.Handle:FindFirstChild('NameEsp'..Number):Destroy()
end
end
end)
end
end

function UpdateFlowerEsp()
for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
pcall(function()
if v.Name == "Flower2" or v.Name == "Flower1" then
if FlowerESP then
if not v:FindFirstChild('NameEsp'..Number) then
local bill = Instance.new('BillboardGui',v)
bill.Name = 'NameEsp'..Number
bill.ExtentsOffset = Vector3.new(0, 1, 0)
bill.Size = UDim2.new(1,200,1,30)
bill.Adornee = v
bill.AlwaysOnTop = true
local name = Instance.new('TextLabel',bill)
name.Font = "GothamBold"
name.FontSize = "Size14"
name.TextWrapped = true
name.Size = UDim2.new(1,0,1,0)
name.TextYAlignment = 'Top'
name.BackgroundTransparency = 1
name.TextStrokeTransparency = 0.5
name.TextColor3 = Color3.fromRGB(255, 0, 0)
if v.Name == "Flower1" then
name.Text = ("Blue Flower" ..' \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')
name.TextColor3 = Color3.fromRGB(0, 0, 255)
end
if v.Name == "Flower2" then
name.Text = ("Red Flower" ..' \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')
name.TextColor3 = Color3.fromRGB(255, 0, 0)
end
else
v['NameEsp'..Number].TextLabel.Text = (v.Name ..'   \n'.. round((game:GetService('Players').LocalPlayer.Character.Head.Position - v.Position).Magnitude/3) ..' M')
end
else
if v:FindFirstChild('NameEsp'..Number) then
v:FindFirstChild('NameEsp'..Number):Destroy()
end
end
end
end)
end
end

function Click()
game:GetService'VirtualUser':CaptureController()
game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
end

function UnEquipWeapon(Weapon)
if game.Players.LocalPlayer.Character:FindFirstChild(Weapon) then
_G.NotAutoEquip = true
wait(.5)
game.Players.LocalPlayer.Character:FindFirstChild(Weapon).Parent = game.Players.LocalPlayer.Backpack
wait(.1)
_G.NotAutoEquip = false
end
end

function EquipWeapon(ToolSe)
if not _G.NotAutoEquip then
if game.Players.LocalPlayer.Backpack:FindFirstChild(ToolSe) then
Tool = game.Players.LocalPlayer.Backpack:FindFirstChild(ToolSe)
wait(.1)
game.Players.LocalPlayer.Character.Humanoid:EquipTool(Tool)
end
end
end

function GetDistance(target)
return math.floor((target.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude)
end

function TP(Pos)
Distance = (Pos.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
if Distance < 250 then
Speed = 700000
elseif Distance >= 1000 then
Speed = 200
end
game:GetService("TweenService"):Create(
game:GetService("Players").LocalPlayer.Character.HumanoidRootPart,
TweenInfo.new(Distance/Speed, Enum.EasingStyle.Linear),
{CFrame = Pos}
):Play()
_G.Clip = true
wait(Distance/Speed)
_G.Clip = false
end

function topos(Pos)
Distance = (Pos.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude
if game.Players.LocalPlayer.Character.Humanoid.Sit == true then game.Players.LocalPlayer.Character.Humanoid.Sit = false end
pcall(function() tween = game:GetService("TweenService"):Create(game.Players.LocalPlayer.Character.HumanoidRootPart,TweenInfo.new(Distance/210, Enum.EasingStyle.Linear),{CFrame = Pos}) end)
tween:Play()
if Distance <= 250 then
tween:Cancel()
game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = Pos
end
if _G.StopTween == true then
tween:Cancel()
_G.Clip = false
end
end
function toClipboard(String)
	local clipBoard = setclipboard or toclipboard or set_clipboard or (Clipboard and Clipboard.set)
	if clipBoard then
		clipBoard(String)
	end
end
function getPlayerByNick(nick:string)
    local firstTry;
    local secondTry;
    local thirdTry;
    local fourthTry;
    nick = string.lower(nick)
    local playerList = game.Players:GetPlayers()
    for _,plr in pairs(playerList) do
        if string.lower(plr.Name) == nick then
            firstTry = plr
            break
        end
    end
    for _,plr in pairs(playerList) do
        if string.lower(plr.DisplayName) == nick then
            secondTry = plr
            break
        end
    end
    for _,plr in pairs(playerList) do
        if string.sub(string.lower(plr.Name), 1, #nick) == nick then
            thirdTry = plr
            break
        end
    end
    for _,plr in pairs(playerList) do
        if string.sub(string.lower(plr.DisplayName), 1, #nick) == nick then
            fourthTry = plr
            break
        end
    end
    return firstTry or nick == 'me' and game.Players.LocalPlayer or secondTry or thirdTry or fourthTry
end

function autobuso()
while _G.autobuso == true do
if not game.Players.LocalPlayer.Character:FindFirstChild('HasBuso') then
       game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Buso")
       elseif game.Players.LocalPlayer.Character:FindFirstChild('HasBuso') then
print("Buso Activates")
wait(0.5)
end
end
end

function autorace()
while _G.autorace == true do
game:GetService("ReplicatedStorage").Remotes.CommE:FireServer("ActivateAbility")
wait(0.01)
end

end



function automelee()

while _G.automelee == true do

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Melee", 1)

wait(0.01)

end

end



function autodefense()

while _G.autodefense == true do

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Defense", 1)

wait(0.01)

end

end



function autosword()

while _G.autosword == true do

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Sword", 1)

wait(0.01)

end

end



function autogun()

while _G.autogun == true do

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Gun", 1)

wait(0.01)

end

end



function autodevil()

while _G.autodevil == true do

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Demon Fruit", 1)

wait(0.01)

end

end



function autochest1()

while _G.autochest1 == true do

game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Workspace.Chest1.CFrame

wait(0.01)

end

end



function autochest2()

while _G.autochest2 == true do

game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Workspace.Chest2.CFrame

wait(0.01)

end

end



function autochest3()

while _G.autochest3 == true do

game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame = game.Workspace.Chest3.CFrame

wait(0.01)

end

end

function killaura()

while _G.killaura == true do

for _,enemy in ipairs(workspace.Enemies:GetDescendants()) do

    if enemy:FindFirstChild('HumanoidRootPart') then

z = enemy.UpperTorso
x = enemy.Head
x:Destroy()
z:Destroy()
wait(.0000001)
end
end
end
end

function hitbox()

while _G.hitbox == true do

for _,enemy in ipairs(workspace.Enemies:GetDescendants()) do

    if enemy:FindFirstChild('HumanoidRootPart') then

local z = enemy.HumanoidRootPart

local x = enemy.Humanoid

        z.Size = Vector3.new(50,50,50)

        z.Shape = "Block"

        z.Transparency = 0.2

        z.Color = Color3.fromRGB(255,160,30)

        z.Material = "ForceField"

        z.CanCollide = false

        z.Anchored = true

        x.Sit = true

wait(.000000000000001)

    end
end
end
end



----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------



local Tab = Window:MakeTab({Name = "", Icon = "", PremiumOnly = false})





----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------



local Tab = Window:MakeTab({

	Name = "Tools",

	Icon = "rbxassetid://12496252828",

	PremiumOnly = false

})



Tab:AddButton({

	Name = "Tp Tool" ,

	Callback = function()

local TpTool = Instance.new("Tool")

	TpTool.Name = "Teleport Tool"

	TpTool.RequiresHandle = false

	TpTool.Parent = game.Players.LocalPlayer.Backpack

	TpTool.Activated:Connect(function()

		local Char = game.Players.LocalPlayer.Character or workspace:FindFirstChild(game.Players.LocalPlayer.Name)

		local HRP = Char and Char:FindFirstChild("HumanoidRootPart")

		if not Char or not HRP then

			return warn("Failed to find HumanoidRootPart")

		end

		HRP.CFrame = CFrame.new(game.Players.LocalPlayer:GetMouse().Hit.X, game.Players.LocalPlayer:GetMouse().Hit.Y + 3, game.Players.LocalPlayer:GetMouse().Hit.Z, select(4, HRP.CFrame:components()))

	end)

end

})


Tab:AddButton({
	Name = "Test",
	Callback = function()
	print("\108\111\97\100\115\116\114\105\110\103\40\34\68\101\99\111\100\101\83\99\114\105\112\116\65\108\116\34\41\44\40\116\114\117\101\41\59")
	end
})


Tab:AddButton({
	Name = "Tween Tp Tool" ,
	Callback = function()
    local a = game:GetService("Players").LocalPlayer
            local b = Instance.new('Tool',a.Backpack)
            local g = game:GetService("TweenService")
            b.RequiresHandle = false
            b.Name = "TweenTp"

            b.Activated:connect(function()

            g:Create(

            a.Character:FindFirstChildOfClass("Humanoid").RootPart,

            TweenInfo.new(tonumber(2),Enum.EasingStyle.Linear),

            {CFrame = CFrame.new(a:GetMouse().Hit.Position+Vector3.new(0,5,0))}

            ):Play()

            end)

         end

})



Tab:AddButton({

	Name = "Remote Spy" ,

	Callback = function()

loadstring(game:HttpGet("https://github.com/exxtremestuffs/SimpleSpySource/raw/master/SimpleSpy.lua"))()

  	end    

})



Tab:AddButton({

	Name = "CHANGE GUIs" ,

	Callback = function()

game:GetService("CoreGui").FluxusAndroidUI.Container.ToggleBtn.Icon.BorderColor3 = Color3.fromRGB(255, 160, 30)

wait(0.1)

game:GetService("CoreGui").FluxusAndroidUI.Container.ToggleBtn.Icon.BackgroundTransparency = 0

wait(0.1)

game:GetService("CoreGui").FluxusAndroidUI.Container.ToggleBtn.Border:Destroy()

wait(0.1)

game:GetService("CoreGui").FluxusAndroidUI.Container.ToggleBtn.Icon.BackgroundColor3 = Color3.fromRGB(0, 0, 0)

wait(0.1)

game:GetService("CoreGui").FluxusAndroidUI.Container.ToggleBtn.Icon.BorderSizePixel = 5

wait(0.1)

game:GetService("CoreGui").FluxusAndroidUI.Container.ToggleBtn.ClickHandler.Text = "POISTER               CUSTOM."

wait(0.1)

game:GetService("CoreGui").FluxusAndroidUI.Container.ToggleBtn.ClickHandler.TextSize = 20

wait(0.1)

game:GetService("CoreGui").FluxusAndroidUI.Container.ToggleBtn.Icon.Rotation = 30

wait(0.1)

game.Players.LocalPlayer.PlayerGui.Main.SafeZone.Position = UDim2.new(0,680,1,-150)

wait(0.1)

game.Players.LocalPlayer.PlayerGui.Main.SafeZone.Text = "PVP - DISABLED.SAFEZONE😈👿😈"

wait(0.1)

game.Players.LocalPlayer.PlayerGui.Main.SafeZone.TextColor3 = Color3.fromRGB(255, 160, 30)

wait(0.1)

game.Players.LocalPlayer.PlayerGui.Main.Quest.Title.TextColor3 = Color3.fromRGB(255, 160, 30)

wait(0.1)

game.Players.LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.BackgroundColor3 = Color3.fromRGB(255, 160, 30)

wait(0.1)

game.Players.LocalPlayer.PlayerGui.Main.Quest.Container.BackgroundColor3 = Color3.fromRGB(0, 0, 0)

wait(0.1)

game.Players.LocalPlayer.PlayerGui.Main.Quest.BackgroundTransparency = 0

wait(0.1)

game.Players.LocalPlayer.PlayerGui.Main.Quest.Container.BackgroundTransparency = 0

wait(0.1)

game.Players.LocalPlayer.PlayerGui.Main.Skills.Title.BackgroundTransparency = 0

wait(0.1)

game.Players.LocalPlayer.PlayerGui.Main.Skills.Title.TextColor3 = Color3.fromRGB(255,160,30)

wait(0.1)

game.Players.LocalPlayer.PlayerGui.Main.Skills.Level.TextColor3 = Color3.fromRGB(255,160,30)

wait(0.1)

game.Players.LocalPlayer.PlayerGui.Main.Skills.Rage.TextColor3 = Color3.fromRGB(255, 160, 30)

wait(0.1)

game.Players.LocalPlayer.PlayerGui.Main.Skills.Level.Bar.BackgroundColor3 = Color3.fromRGB(255, 160, 30)

wait(0.1)

game.Players.LocalPlayer.PlayerGui.Main.Skills.Level.Bar2.BackgroundColor3 = Color3.fromRGB(255, 160, 30)

wait(0.1)

game.Players.LocalPlayer.PlayerGui.Main.Trade.BackgroundTransparency = 1

wait(0.1)

game.Players.LocalPlayer.PlayerGui.Main.Trade.Title.TextColor3 = Color3.fromRGB(255,160,30)

wait(0.1)

game.Players.LocalPlayer.PlayerGui.Main.Trade.Title.BackgroundTransparency = 1

wait(0.1)

game.Players.LocalPlayer.PlayerGui.Main.Trade.Title.Text = "TRADING"

wait(0.1)

game.Players.LocalPlayer.PlayerGui.Main.Trade.Container["1"].BackgroundColor3 = Color3.fromRGB(255,160,30)

wait(0.1)

game.Players.LocalPlayer.PlayerGui.Main.Trade.Container["2"].BackgroundColor3 = Color3.fromRGB(0,0,0)

wait(0.1)

game.Players.LocalPlayer.PlayerGui.Main.Trade.Container["1"].BorderColor3 = Color3.fromRGB(255,255,255)

wait(0.1)

game.Players.LocalPlayer.PlayerGui.Main.Trade.Container["2"].BorderColor3 = Color3.fromRGB(255,255,255)

wait(0.1)

game.Players.LocalPlayer.PlayerGui.Main.Trade.Info.BorderColor3 = Color3.fromRGB(255,255,255)

wait(0.1)

game.Players.LocalPlayer.PlayerGui.Main.Trade.Info.Accept.BorderColor3 = Color3.fromRGB(255,160,30)

wait(0.1)

game.Players.LocalPlayer.PlayerGui.Main.Trade.Info.Cancel.BorderColor3 = Color3.fromRGB(255,160,30)

wait(0.1)

game.Players.LocalPlayer.PlayerGui.Main.Trade.Info.Accept.BorderColor3 = Color3.fromRGB(255,160,30)

wait(0.1)

game.Players.LocalPlayer.PlayerGui.Main.Trade.Info.Accept.BackgroundColor3 = Color3.fromRGB(0,0,0)

wait(0.1)

game.Players.LocalPlayer.PlayerGui.Main.Trade.Info.Accept.BorderColor3 = Color3.fromRGB(255,160,30)

wait(0.1)

game.Players.LocalPlayer.PlayerGui.Main.Trade.Info.Accept.Trans.BackgroundColor3 = Color3.fromRGB(0,0,0)

wait(0.1)

game.Players.LocalPlayer.PlayerGui.Main.Trade.Info.Cancel.Trans.BackgroundColor3 = Color3.fromRGB(0,0,0)

wait(.1)

game.Players.LocalPlayer.PlayerGui.Main.Trade.Info.Cancel.BackgroundColor3 = Color3.fromRGB(0,0,0)

wait(.1)

game.Players.LocalPlayer.PlayerGui.Main.Trade.Info.Accept.Trans.BorderColor3 = Color3.fromRGB(255,160,30)

wait(.1)

game.Players.LocalPlayer.PlayerGui.Main.Trade.Info.Accept.TextLabel.TextColor3 = Color3.fromRGB(255,160,30)

  	end    

})



Tab:AddButton({

	Name = "Dex V3" ,

	Callback = function()

loadstring(game:HttpGet("https://raw.githubusercontent.com/Babyhamsta/RBLX_Scripts/main/Universal/BypassedDarkDexV3.lua", true))()

  	end    

})



Tab:AddButton({

	Name = "Dex V4" ,

	Callback = function()

    loadstring(game:HttpGet("https://raw.githubusercontent.com/peyton2465/Dex/master/out.lua"))()

  	end    

})

spawn(function()
while wait() do
pcall(function()
CoolLabel:Set("Beli :".." "..game:GetService("Players").LocalPlayer.Data.Beli.Value)
end)
end
end)


Tab:AddButton({

	Name = "Big Jump" ,

	Callback = function()

game.Players.LocalPlayer.PlayerGui.TouchGui.TouchControlFrame.JumpButton.Size = UDim2.new(0,200,0,200)

  	end    

})



----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------



local Tab = Window:MakeTab({

	Name = "BuyItem",

	Icon = "http://www.roblox.com/asset/?id=12496227758",

	PremiumOnly = false

})

local Section = Tab:AddSection({
	Name = "Abilities"
})

Tab:AddButton({
	Name = "Buso",
	Callback = function()
      		print("button pressed")
  	end    
})

Tab:AddButton({
	Name = "Geppo",
	Callback = function()
      		print("button pressed")
  	end    
})

Tab:AddButton({
	Name = "Soru",
	Callback = function()
      		print("button pressed")
  	end    
})

Tab:AddButton({
	Name = "Ken",
	Callback = function()
      		print("button pressed")
  	end    
})

local Section = Tab:AddSection({
	Name = "Fighting Styles"
})

Tab:AddButton({
	Name = "Dark Step 250.000$",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBlackLeg" )
  	end    
})

Tab:AddButton({
	Name = "Electro 500.000$",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyElectro" )
  	end    
})

Tab:AddButton({
	Name = "Water Kung-Fu 750.000$",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyFishmanKarate" )
  	end    
})

Tab:AddButton({
	Name = "Dragon Breath",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","DragonClaw","2")
  	end    
})

Tab:AddButton({
	Name = "Superhuman 3.000.000$",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySuperhuman" )
  	end    
})

Tab:AddButton({
	Name = "Death Step 2.500.000$ 2.500F",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyDeathStep" )
  	end    
})

Tab:AddButton({
	Name = "Electric Claw 2.500.000$ 2.500F",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyElectricClaw" )
  	end    
})

Tab:AddButton({
	Name = "Sharkman Karate 2.500.000$ 2.500F",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuySharkmanKarate" )
  	end    
})

Tab:AddButton({
	Name = "Dragon Talon 2.500.000$ 2.500F",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyDragonTalon" )
  	end    
})

Tab:AddButton({
	Name = "Godhuman 5.000.000$ 5.000F",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyGodhuman" )
  	end    
})

local Section = Tab:AddSection({
	Name = "Fragments"
})

Tab:AddButton({
	Name = "Check Color Haki Dealer",
	Callback = function()
	OrionLib:MakeNotification({
	Name = "Haki Colors Dealer",
    Content = "".. game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ColorsDealer", "1") .."",
	Image = "rbxassetid://4483345998",
	Time = 5
})
	end
})

Tab:AddButton({
	Name = "Buy Color Buso Haki",
	Callback = function()
	game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ColorsDealer", "2")
	end
})

Tab:AddButton({
	Name = "Ghoul 0F",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Ectoplasm","Change",4)
  	end    
})

Tab:AddButton({
	Name = "Cyborg 2.500F",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("CyborgTrainer","Buy")
  	end    
})

Tab:AddButton({
	Name = "Reset Stats 2.500F",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","Refund","2")
  	end    
})

Tab:AddButton({
	Name = "Race Reroll 3.000F",
	Callback = function()
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BlackbeardReward","Reroll","2")
  	end    
})

local Section = Tab:AddSection({
	Name = "Bones"
})

Tab:AddButton({
	Name = "Surprise 50bones",
	Callback = function()
      		for i = 1, 10 do
                game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Bones", "Buy", 1, 1)
            end
  	end    
})

local Section = Tab:AddSection({
	Name = "Swords"
})

local Section = Tab:AddSection({
	Name = "Guns"
})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

local Tab = Window:MakeTab({

	Name = "Farming",

	Icon = "rbxassetid://12505503302",

	PremiumOnly = false

})



Tab:AddToggle({

	Name = "HitBox",

	Default = false,

	Callback = function(lolek)

	_G.hitbox = lolek

hitbox()

		end

})

Tab:AddToggle({

	Name = "Autofarm",

	Default = false,

	Callback = function(sasa)
_G.AutoFarm = sasa
StopTween(_G.AutoFarm)
end
})


spawn(function()
while wait() do
if _G.AutoFarm then
pcall(function()
local QuestTitle = game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text
if not string.find(QuestTitle, NameMon) then
StartMagnet = false
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
end
if game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false then
StartMagnet = false
CheckQuest()
repeat wait() topos(CFrameQuest) until (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3 or not _G.AutoFarm
if (CFrameQuest.Position - game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 3 then
wait(1.2)
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest",NameQuest,LevelQuest)
wait(0.5)
end
elseif game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == true then
CheckQuest()
if game:GetService("Workspace").Enemies:FindFirstChild(Mon) then
for i,v in pairs(game:GetService("Workspace").Enemies:GetChildren()) do
if v:FindFirstChild("HumanoidRootPart") and v:FindFirstChild("Humanoid") and v.Humanoid.Health > 0 then
if v.Name == Mon then
if string.find(game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Container.QuestTitle.Title.Text, NameMon) then
repeat task.wait()
EquipWeapon(_G.SelectWeapon)
AutoHaki()
PosMon = v.HumanoidRootPart.CFrame
topos(v.HumanoidRootPart.CFrame * CFrame.new(5,10,7))
v.HumanoidRootPart.CanCollide = false
v.Humanoid.WalkSpeed = 0
v.Head.CanCollide = false
v.HumanoidRootPart.Size = Vector3.new(50,50,50)
StartMagnet = true
game:GetService'VirtualUser':CaptureController()
game:GetService'VirtualUser':Button1Down(Vector2.new(1280, 672))
until not _G.AutoFarm or v.Humanoid.Health <= 0 or not v.Parent or game:GetService("Players").LocalPlayer.PlayerGui.Main.Quest.Visible == false
else
StartMagnet = false
game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AbandonQuest")
end
end
end
end
else
StartMagnet = false
if game:GetService("ReplicatedStorage"):FindFirstChild(Mon) then
topos(game:GetService("ReplicatedStorage"):FindFirstChild(Mon).HumanoidRootPart.CFrame * CFrame.new(5,10,7))
else
if (CFrameQuest.Position - game.Players.LocalPlayer.Character.HumanoidRootPart.Position).Magnitude <= 15 then
if PosMon ~= nil then
topos(PosMon * CFrame.new(5,10,7))
else
if OldPos ~= nil then
topos(OldPos.Position)
end
end
end
end
end
end
end)
end
end
end)




local Section = Tab:AddSection({

    Name = "START"

})



Tab:AddButton({

	Name = "5Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", "BanditQuest1", 1)

end

})



local Section = Tab:AddSection({

    Name = "JUNGLE"

})



Tab:AddButton({

	Name = "10Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","JungleQuest",1)

end

})



Tab:AddButton({

	Name = "15Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","JungleQuest",2)

end

})



Tab:AddButton({

	Name = "20Lvl [BOSS]",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","JungleQuest",3)    

end

})



local Section = Tab:AddSection({

    Name = "PIRATE VILLAGE"

})



Tab:AddButton({

	Name = "30Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","BuggyQuest1",1)

end

})



Tab:AddButton({

	Name = "50Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","BuggyQuest1",2)

end

})



Tab:AddButton({

	Name = "55Lvl [BOSS]",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","BuggyQuest1",3)

end

})



local Section = Tab:AddSection({

    Name = "DESERT"

})



Tab:AddButton({

	Name = "60Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","DesertQuest",1)

end

})



Tab:AddButton({

	Name = "75Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","DesertQuest",2)

end

})



local Section = Tab:AddSection({

    Name = "SNOW VILLAGE"

})



Tab:AddButton({

	Name = "90Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", "SnowQuest", 1)

end

})



Tab:AddButton({

	Name = "100Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", "SnowQuest", 2)

end

})



Tab:AddButton({

	Name = "105Lvl [BOSS]",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", "SnowQuest", 3)

end

})



local Section = Tab:AddSection({

    Name = "MARINE FORTRESS"

})



Tab:AddButton({

	Name = "120Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", "BanditQuest1", 1)

end

})



Tab:AddButton({

	Name = "130Lvl [BOSS]",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", "BanditQuest1", 1)

end

})



local Section = Tab:AddSection({

    Name = "SKY1"

})



Tab:AddButton({

	Name = "150Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","SkyQuest",1)

end

})



Tab:AddButton({

	Name = "170Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","SkyQuest",2)

end

})



local Section = Tab:AddSection({

    Name = "PRISON"

})



Tab:AddButton({

	Name = "190Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","PrisonerQuest",1)

end

})



Tab:AddButton({

	Name = "210Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","PrisonerQuest",2)

end

})



Tab:AddButton({

	Name = "220Lvl [BOSS]",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","ImpelQuest",1)

end

})



Tab:AddButton({

	Name = "230Lvl [BOS]",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","ImpelQuest",2)

end

})



Tab:AddButton({

	Name = "240Lvl [BOSS]",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","ImpelQuest",3)

end

})



local Section = Tab:AddSection({

    Name = "COLOSSEUM"

})



Tab:AddButton({

	Name = "250Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","ColosseumQuest",1)

end

})



Tab:AddButton({

	Name = "275Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","ColosseumQuest",2)

end

})



local Section = Tab:AddSection({

    Name = "MAGMA VILLAGE"

})



Tab:AddButton({

	Name = "300Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","MagmaQuest",1)

end

})



Tab:AddButton({

	Name = "325Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","MagmaQuest",2)

end

})



Tab:AddButton({

	Name = "350Lvl [BOSS]",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","MagmaQuest",3)

end

})



local Section = Tab:AddSection({

    Name = "UNDERWATER"

})



Tab:AddButton({

	Name = "375Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","FishmanQuest",1)

end

})



Tab:AddButton({

	Name = "400Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","FishmanQuest",2)

end

})



Tab:AddButton({

	Name = "425Lvl [BOSS]",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","FishmanQuest",3)

end

})



local Section = Tab:AddSection({

    Name = "SKY2-3"

})



Tab:AddButton({

	Name = "450Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","SkyExp1Quest",1)

end

})



Tab:AddButton({

	Name = "475Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","SkyExp1Quest",2)

end

})



Tab:AddButton({

	Name = "500Lvl [BOSS]",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","SkyExp1Quest",3)

end

})



Tab:AddButton({

	Name = "525Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", "SkyExp2Quest", 1)

end

})



Tab:AddButton({

	Name = "550Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", "SkyExp2Quest", 2)

end

})



Tab:AddButton({

	Name = "575Lvl [BOSS]",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest", "SkyExp2Quest", 3)

end

})







local Section = Tab:AddSection({

    Name = "FOUNTAIN CITY"

})



Tab:AddButton({

	Name = "625Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","FountainQuest",1)

end

})



Tab:AddButton({

	Name = "650Lvl",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","FountainQuest",2)

end

})



Tab:AddButton({

	Name = "675Lvl [BOSS]",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("StartQuest","FountainQuest",3)

end

})



--мб дропдауны под секции



Tab:AddButton({

	Name = "Player Quest",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer( "PlayerHunter")

end

})



----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------



local Tab = Window:MakeTab({



	Name = "ESP",



	Icon = "rbxassetid://12496239839",



	PremiumOnly = false



})



esps = {}

Tab:AddToggle({

    Name = "Fruit ESP",

    Default = false,

    Callback = function(Value) 

        if Value == true then

            fruitNames = {'Fruit ','Kilo Fruit', 'Spin Fruit', 'Chop Fruit', 'Spring Fruit', 'Bomb Fruit', 'Smoke Fruit', 'Spike Fruit', 'Flame Fruit', 'Bird: Falcon Fruit', 'Ice Fruit', 'Sand Fruit', 'Dark Fruit', 'Revive Fruit', 'Diamond Fruit', 'Light Fruit', 'Love Fruit', 'Rubber Fruit', 'Barrier Fruit', 'Magma Fruit', 'Quake Fruit', 'Human: Buddha Fruit', 'String Fruit', 'Bird: Phoenix Fruit', 'Portal Fruit', 'Rumble Fruit', 'Paw Fruit', 'Blizzard Fruit', 'Gravity Fruit', 'Dough Fruit', 'Shadow Fruit', 'Venom Fruit', 'Control Fruit', 'Spirit Fruit', 'Dragon Fruit', 'Leopard Fruit'}

            for key, value in pairs(fruitNames) do

                fruitNames[value] = key

            end



            for _, obj in pairs(workspace:GetChildren()) do

                if fruitNames[obj.Name] then

                    local billBoard = Instance.new("BillboardGui", obj.Handle)

                    local espText = Instance.new("TextLabel", billBoard)

                    

                    billBoard.Adornee = obj.Handle

                    billBoard.AlwaysOnTop = true

                    billBoard.Size = UDim2.new(1,200,1,30)

                    billBoard.Name = "Board"

                    

                    espText.Size = UDim2.new(1,0,1,0)

                    espText.Text = obj.Name

                    espText.TextColor3 = Color3.fromRGB(255,160,30)

                    espText.TextStrokeTransparency = 0

                    espText.BackgroundTransparency = 1

                    espText.TextSize = 10

                    espText.Name = "Text"

                    esps[billBoard] = obj

OrionLib:MakeNotification({

	Name = obj.Name,

	Content = "This fruit was found",

	Image = "rbxassetid://12496254877",

	Time = 10

})

                end

            end

        elseif Value == false then

            for esp, obj in pairs(esps) do

                esp:Destroy()

            end

            esps = {}

        end

    end

})

Tab:AddToggle({
	Name = "Player ESP",
	Default = false,
	Callback = function(value)
ESPPlayer = value
while ESPPlayer do wait()
UpdateEspPlayer()
end
end
})

Tab:AddToggle({
	Name = "Chest ESP",
	Default = false,
	Callback = function(value)
ChestESP = value
while ChestESP do wait()
UpdateChestEsp()
end
end
})

Tab:AddToggle({
	Name = "Fruit2 ESP",
	Default = false,
	Callback = function(value)
DevilFruitESP = value
while DevilFruitESP do wait()
UpdateBfEsp()
end
end
})

Tab:AddToggle({
	Name = "Flower ESP",
	Default = false,
	Callback = function(value)
FlowerESP = value
while FlowerESP do wait()
UpdateFlowerEsp()
end
end
})

Tab:AddToggle({
	Name = "Island ESP",
	Default = false,
	Callback = function(value)
IslandESP = value
while IslandESP do wait()
UpdateIslandESP()
end
end
})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------



local Tab = Window:MakeTab({



	Name = "Fruit",



	Icon = "http://www.roblox.com/asset/?id=12496254877",



	PremiumOnly = false



})


Tab:AddToggle({
	Name = "Tp Fruit",
	Default = false,
	Callback = function(Grab)
_G.BringFruit = Grab
pcall(function()
while _G.BringFruit do wait(.1)
for i,v in pairs(game:GetService("Workspace"):GetChildren()) do
if v:IsA("Tool") then
local OldCFrame = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame
game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = v.Handle.CFrame * CFrame.new(0,0,0)
v.Handle.CFrame = game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame
wait(.1)
game:GetService("Players").LocalPlayer.Character.HumanoidRootPart.CFrame = OldCFrame
end
end
end
end)
end
})


Tab:AddButton({

	Name = "Random Fruit",

	Callback = function()

      		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Cousin", "Buy")

  	end    

})



Tab:AddButton({

	Name = "Fruit Shop",

	Callback = function()

game.Players.LocalPlayer.PlayerGui.Main.FruitShop.Visible = true

  	end    

})



----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------



local Tab = Window:MakeTab({



	Name = "Points soon...",



	Icon = "rbxassetid://12530069729",



	PremiumOnly = false



})



Tab:AddToggle({

	Name = "Auto Melee",

	Default = false,

	Callback = function(Melee1)

	_G.automelee = Melee1

automelee()

		end

})



Tab:AddToggle({

	Name = "Auto Defense",

	Default = false, 

	Callback = function(Defense1)

	_G.autodefense = Defense1

autodefense()

		end

})



Tab:AddToggle({

	Name = "Auto Sword",

	Default = false,

	Callback = function(Sword1)

	_G.autosword = Sword1

autosword()

		end

})



Tab:AddToggle({

	Name = "Auto Gun",

	Default = false,

	Callback = function(Gun1)

	_G.autogun = Gun1

autogun()

		end

})



Tab:AddToggle({

	Name = "Auto Devil Fruit",

	Default = false,

	Callback = function(Devil1)

	_G.autodevil = Devil1

autodevil()

		end

})





Tab:AddTextbox({

	Name = "Melee",

	Default = nil,

	TextDisappear = true,

	Callback = function(Melee)

		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Melee", Melee) 

	end	  

})



Tab:AddTextbox({

	Name = "Defense",

	Default = nil,

	TextDisappear = true,

	Callback = function(Defense)

		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Defense", Defense)

	end	  

})



Tab:AddTextbox({

	Name = "Sword",

	Default = nil,

	TextDisappear = true,

	Callback = function(Sword)

		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Sword", Sword)

	end	  

})



Tab:AddTextbox({

	Name = "Gun",

	Default = nil,

	TextDisappear = true,

	Callback = function(Gun)

		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Gun", Gun)

	end	  

})



Tab:AddTextbox({

	Name = "Devil Fruit",

	Default = nil,

	TextDisappear = true,

	Callback = function(Devil)

		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("AddPoint","Demon Fruit", Devil)

	end	  

})



----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------



local Tab = Window:MakeTab({



	Name =  "GUIs soon?..",



	Icon = "rbxassetid://12505501154",



	PremiumOnly = false



})







----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------



local Tab = Window:MakeTab({



	Name =  "Any Auto soon...",



	Icon = "rbxassetid://12505499132",



	PremiumOnly = false



})



Tab:AddToggle({

	Name = "Auto Silver Chest",

	Default = false,

	Callback = function(Chest1)

	_G.autochest1 = Chest1

autochest1()

		end

})



Tab:AddToggle({

	Name = "Auto Gold Chest",

	Default = false,

	Callback = function(Chest2)

	_G.autochest2 = Chest2

autochest2()

		end

})



Tab:AddToggle({

	Name = "Auto Diamond Chest",

	Default = false,

	Callback = function(Chest3)

	_G.autochest3 = Chest3

autochest3()

		end

})



Tab:AddToggle({

	Name = "Auto Buso",

	Default = false,

	Callback = function(Toggle1)

	_G.autobuso = Toggle1

autobuso()

		end

})





Tab:AddToggle({

	Name = "Auto Race",

	Default = false,

	Callback = function(Toggle5)

	_G.autorace = Toggle5

autorace()

		end

})



----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------



local Tab = Window:MakeTab({



	Name = "Teleport",



	Icon = "rbxassetid://12496230420",



	PremiumOnly = false



})



local Section = Tab:AddSection({

	Name = "Servers"

})





Tab:AddButton({

	Name = "Server Id",

	Callback = function()

    jobId = ''..game.JobId..''

	toClipboard(jobId)

	OrionLib:MakeNotification({

	Name = "Server ID copied to clipboard!",

	Content = "Paste this in Server Join Id",

	Image = "rbxassetid://4483345998",

	Time = 5

})

end

})



Tab:AddTextbox({

	Name = "Join Id Server",

	Default = ""..game.JobId.."",

	TextDisappear = true,

	Callback = function(Ponon)

		game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId,Ponon,game.Players.LocalPlayer)

	end	  

})



Tab:AddButton({

	Name = "Rejoin",

	Callback = function()

if #game.Players:GetPlayers() == 1 then

		game.Players.LocalPlayer:Kick("\nRejoin...")

		wait()

		game:GetService("TeleportService"):Teleport(game.PlaceId, game.Players.LocalPlayer)

	else

		game:GetService("TeleportService"):TeleportToPlaceInstance(game.PlaceId, game.JobId, game.Players.LocalPlayer)

	end

  	end    

})



Tab:AddButton({

	Name = "Server Hop",

	Callback = function()

loadstring(game:HttpGet"https://raw.githubusercontent.com/LeoKholYt/roblox/main/lk_serverhop.lua")():Teleport(game.PlaceId)

  	end    

})



local Section = Tab:AddSection({

	Name = "Worlds"

})



Tab:AddButton({

	Name = "Sea1",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TravelMain")

  	end    

})



Tab:AddButton({

	Name = "Sea2",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TravelDressrosa")

  	end    

})



Tab:AddButton({

	Name = "Sea3",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("TravelZou")


  	end    

})

local Section = Tab:AddSection({

	Name = "Settings"

})

Tab:AddButton({

	Name = "Stop Tween",

	Callback = function()
topos( CFrame.new(game.Players.LocalPlayer.Character.HumanoidRootPart.CFrame))
end
})

local Section = Tab:AddSection({

	Name = "Islands"

})


Tab:AddButton({

	Name = "Marine Start",

	Callback = function()
topos(CFrame.new(-2566.4296875, 6.8556680679321, 2045.2561035156))
end
})

Tab:AddButton({

	Name = "Pirate Start",

	Callback = function()
topos(CFrame.new(979.79895019531, 16.516613006592, 1429.0466308594))
end
})

Tab:AddButton({

	Name = "Jungle",

	Callback = function()
topos(CFrame.new(-1612.7957763672, 36.852081298828, 149.12843322754))
end
})

Tab:AddButton({

	Name = "Pirate Village",

	Callback = function()
topos(CFrame.new(-1181.3093261719, 4.7514905929565, 3803.5456542969))
end
})

Tab:AddButton({

	Name = "Desert",

	Callback = function()
topos(CFrame.new(944.15789794922, 20.919729232788, 4373.3002929688))
end
})

Tab:AddButton({

	Name = "Snow Village",

	Callback = function()
topos(CFrame.new(1347.8067626953, 104.66806030273, -1319.7370605469))
end
})

Tab:AddButton({

	Name = "Marine Fortress",

	Callback = function()
topos(CFrame.new(-4914.8212890625, 50.963626861572, 4281.0278320313))
end
})

Tab:AddButton({

	Name = "Great Tree",

	Callback = function()
topos(CFrame.new(2946.0, 2281.5, -7219.6))
end
})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------



local Tab = Window:MakeTab({



	Name = "Boats",



	Icon = "rbxassetid://12496247656",



	PremiumOnly = false



})



local Section = Tab:AddSection({

	Name = "Pirate"

})



Tab:AddButton({

	Name = "Pirate Sloop 600$",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "PirateSloop")

  	end    

})



Tab:AddButton({

	Name = "Pirate Basic 1.000$",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "PirateBasic")

  	end    

})



Tab:AddButton({

	Name = "Pirate Brigade 4.000$",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "PirateBrigade")

  	end    

})



local Section = Tab:AddSection({

	Name = "Marine"

})



Tab:AddButton({

	Name = "Marine Sloop 150$",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "MarineSloop")

  	end    

})



Tab:AddButton({

	Name = "Marine Basic 600$",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "MarineBasic")

  	end    

})



Tab:AddButton({

	Name = "MarineBrigade 2.000$",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "MarineBrigade")

  	end    

})



local Section = Tab:AddSection({

	Name = "Luxury"

})



Tab:AddButton({

	Name = "RocketBoost 0$",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "RocketBoost")

  	end    

})



Tab:AddButton({

	Name = "Enforcer 1.000$",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "Enforcer")

  	end    

})



Tab:AddButton({

	Name = "Swan 5.000$",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "Swan")

  	end    

})



Tab:AddButton({

	Name = "Flower 5.000$",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "Flower")

  	end    

})



Tab:AddButton({

	Name = "Sleigh 5.000$",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("BuyBoat", "Sleigh")

  	end    

})

    

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------



local Tab = Window:MakeTab({



	Name = "Fast Cmd soon...",



	Icon = "rbxassetid://12496242729",



	PremiumOnly = false



})    



Tab:AddTextbox({

	Name = "Textbox",

	Default = "soon...",

	TextDisappear = true,

	Callback = function(Cmd)

		if Cmd == pon then

print("pon")

elseif Cmd == pon1 then

print("pon1")

end

	end	 

})



----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------



local Tab = Window:MakeTab({
	Name = "Combat",
	Icon = "rbxassetid://12496236549",
	PremiumOnly = false
})

local walkto = false
local waypointwalkto = false
Tab:AddButton({
	Name = "Walk To Player",
	Callback = function()
	local players = getPlayer(xbxJIE7EHDAxdx, game.Players.LocalPlayer)
	for i,v in pairs(players)do
		if players[v].Character ~= nil then
			if game.Players.LocalPlayer.Character:FindFirstChildOfClass('Humanoid') and game.Players.LocalPlayer.Character:FindFirstChildOfClass('Humanoid').SeatPart then
				game.Players.LocalPlayer.Character:FindFirstChildOfClass('Humanoid').Sit = false
				wait(.1)
			end
			walkto = true
			repeat wait()
				game.Players.LocalPlayer.Character:FindFirstChildOfClass('Humanoid'):MoveTo(getRoot(players[v].Character).Position)
			until players[v].Character == nil or not getRoot(players[v].Character) or walkto == false
		end
	end
end
})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------


local Tab = Window:MakeTab({
	Name = "Raids",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

Tab:AddToggle({

	Name = "Killaura",

	Default = false,

	Callback = function(Killaura)

	_G.killaura = Killaura

killaura()

		end

})

----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------



local Tab = Window:MakeTab({



	Name = "Troll",



	Icon = "rbxassetid://12505494337",



	PremiumOnly = false



})



Tab:AddToggle({

	Name = "Freeze",

	Default = nil,

	Callback = function(Value1)

	if Value1 == true then   game.Players.LocalPlayer.Character.HumanoidRootPart.Anchored = true

elseif Value1 == false then

game.Players.LocalPlayer.Character.HumanoidRootPart.Anchored = false

	end 

end   

})



Tab:AddButton({

	Name = "Sit",

	Callback = function()

game.Players.LocalPlayer.Character.Humanoid.Sit = true

  	end    

})



Tab:AddButton({

	Name = "Lay Down",

	Callback = function()

local Human = game.Players.LocalPlayer.Character and game.Players.LocalPlayer.Character:FindFirstChildOfClass('Humanoid')

	if not Human then

		return

	end

	Human.Sit = true

	task.wait(.1)

	Human.RootPart.CFrame = Human.RootPart.CFrame * CFrame.Angles(math.pi * .5, 0, 0)

	for _, v in ipairs(Human:GetPlayingAnimationTracks()) do

		v:Stop()

	end

  	end    

})



Tab:AddTextbox({

	Name = "Spin SPEED:",

	Default = nil,

	TextDisappear = true,

	Callback = function(SPINN)

		function getRoot(char)

	local rootPart = char:FindFirstChild('HumanoidRootPart') or char:FindFirstChild('Torso') or char:FindFirstChild('UpperTorso')

	return rootPart

end

local Spin = Instance.new("BodyAngularVelocity")

	Spin.Name = "Spinning"

	Spin.Parent = getRoot(game.Players.LocalPlayer.Character)

	Spin.MaxTorque = Vector3.new(0, math.huge, 0)

	Spin.AngularVelocity = Vector3.new(0, SPINN, 0)

	end	  

})



Tab:AddButton({

	Name = "Stop Spin",

	Callback = function()

function getRoot(char)

	local rootPart = char:FindFirstChild('HumanoidRootPart') or char:FindFirstChild('Torso') or char:FindFirstChild('UpperTorso')

	return rootPart

end

for i,v in pairs(getRoot(game.Players.LocalPlayer.Character):GetChildren()) do

		if v.Name == "Spinning" then

			v:Destroy()

		end

	end

  	end    

})





----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------



local Tab = Window:MakeTab({



	Name = "Codes test...",



	Icon = "rbxassetid://12496297350",



	PremiumOnly = false



})  



----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------



local Tab = Window:MakeTab({



	Name = "Player Settings",



	Icon = "rbxassetid://12496250171",



	PremiumOnly = false



})



Tab:AddTextbox({

	Name = "Chat",

	Default = "Chat",

	TextDisappear = true,

	Callback = function(Say)

		game:GetService("ReplicatedStorage").DefaultChatSystemChatEvents.SayMessageRequest:FireServer(Say,"All")

	end	 

})



Tab:AddDropdown({

	Name = "Buso State",

	Default = nil,

	Options = {"0", "1", "2", "3", "4", "5"},

	Callback = function(statebuso)

		if statebuso == "0" then

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ChangeBusoStage",0)

elseif statebuso == "1" then

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ChangeBusoStage",1)

elseif statebuso == "2" then 

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ChangeBusoStage",2)

elseif statebuso == "3" then 

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ChangeBusoStage",3)

elseif statebuso == "4" then

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ChangeBusoStage",4)

elseif statebuso == "5" then

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("ChangeBusoStage",5)

	end    

	end

})



Tab:AddTextbox({

	Name = "Ken Range",

	Default = "Ken Range(30k+ lag)",

	TextDisappear = true,

	Callback = function(KenRange)

		game.Players.LocalPlayer.VisionRadius.Value = KenRange

	end	 

})



Tab:AddButton({

	Name = "Reset",

	Callback = function()

game.Players.LocalPlayer.Character:BreakJoints()

  	end    

})



Tab:AddTextbox({

	Name = "Title",

	Default = "Title",

	TextDisappear = true,

	Callback = function(title)

		game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateTitle", title)

	end	 

})





Tab:AddButton({

	Name = "Pirates",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetTeam", "Pirates")

  	end    

})



Tab:AddButton({

	Name = "Marines",

	Callback = function()

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("SetTeam", "Marines")

  	end    

})



Tab:AddDropdown({

	Name = "Buso Color",

	Default = nil,

	Options = {"Rainbow Saviour","Winter Sky", "Pure Red", "Snow White","Absolute Zero","Fiery Rose","Heat Wave","Plump Purple","Blue Jeans","Green Lizard","Slimy Green","Yellow Sunshine","Bright Yellow","Orange Soda"},

	Callback = function(busoColor)

if busoColor == "Rainbow Saviour" then

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Rainbow Saviour")

   elseif busoColor == "Winter Sky" then

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Winter Sky")

   elseif busoColor == "Pure Red" then

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Pure Red")

   elseif busoColor == "Snow White" then

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Snow White")

   elseif busoColor == "Absolute Zero" then

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Absolute Zero")

   elseif busoColor == "Heat Wave" then

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Heat Wave")

   elseif busoColor == "Fiery Rose" then

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Fiery Rose")

   elseif busoColor == "Plump Purple" then

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Plump Purple")

   elseif busoColor == "Blue Jeans" then

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Blue Jeans")

   elseif busoColor == "Green Lizard" then

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Green Lizard")

   elseif busoColor == "Slimy Green" then

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Slimy Green")

   elseif busoColor == "Yellow Sunshine" then

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Yellow Sunshine")

   elseif busoColor == "Bright Yellow" then

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Bright Yellow")

   elseif busoColor == "Orange Soda" then

game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("activateColor", "Orange Soda")

end

end

})





Tab:AddTextbox({

	Name = "Mastery info",

	Default = nil,

	TextDisappear = true,

	Callback = function(Namik)
     for _,obj in pairs(game.Players[Namik].Backpack:GetChildren()) do

    if obj.ClassName == 'Tool' then
        OrionLib:MakeNotification({

	Name = "Stats",

	Content = 'Name:'.. obj.Name ..'| Mastery:'.. obj.Level.Value ..'.',

	Image = "rbxassetid://4483345998",

	Time = 15

})

end	  
end
end

})



Tab:AddTextbox({

    Name = "Check Stats",

    Default = nil,

    TextDisappear = true,

    Callback = function(plrName)

        OrionLib:MakeNotification({

            Name = "Beli:"..getPlayerByNick(plrName).Data.Beli.Value.."Frags:"..getPlayerByNick(plrName).Data.Fragments.Value..'.',

            Content = "Player's stats",

            Image = "rbxassetid://12496227758",

            Time = 10

        })


    end

})


Tab:AddButton({
	Name = "Check Accessories Info",
	Callback = function()
OrionLib:MakeNotification({
	Name = ''.. game:GetService("ReplicatedStorage").Remotes.CommF_:InvokeServer("Nerd") ..'',
	Content = "Nerd",
	Image = "rbxassetid://4483345998",
	Time = 5
})
end
})

Tab:AddButton({

	Name = "X-ray",

	Callback = function()

local sc = (debug and debug.setconstant) or setconstant

	local gc = (debug and debug.getconstants) or getconstants

local pop = game.Players.LocalPlayer.PlayerScripts.PlayerModule.CameraModule.ZoomController.Popper

	for _, v in pairs(getgc()) do

		if type(v) == 'function' and getfenv(v).script == pop then

			for i, v1 in pairs(gc(v)) do

				if tonumber(v1) == .25 then

					sc(v, i, 0)

				elseif tonumber(v1) == 0 then

					sc(v, i, .25)

				end

			end

		end

	end

end
})

Tab:AddButton({

	Name = "Tp",

	Callback = function()
topos( CFrame.new(-1503.6224365234, 219.7956237793, 1369.3101806641))
end
})

Tab:AddButton({

	Name = "No Fog",

	Callback = function()

game.Lighting.FogEnd = 100000

	for i,v in pairs(Lighting:GetDescendants()) do

		if v:IsA("Atmosphere") then

			v:Destroy()

		end

	end

end

})



Tab:AddButton({

	Name = "MaxZoom inf",

	Callback = function()

game.Players.LocalPlayer.CameraMaxZoomDistance = 999999

end

})



Tab:AddButton({

	Name = "MaxZoom normal",

	Callback = function()

game.Players.LocalPlayer.CameraMaxZoomDistance = 100

end

})

end
