local Material = loadstring(game:HttpGet("https://raw.githubusercontent.com/Kinlei/MaterialLua/master/Module.lua"))()

local X = Material.Load({
	Title = "K3R3N DUPE ",
	Style = 3,
	SizeX = 500,
	SizeY = 350,
	Theme = "Dark",
	ColorOverrides = {
		MainFrame = Color3.fromRGB(35,35,35)
	}
})
 
local Y = X.New({
	Title = "Main"
})

local A = Y.Button({
	Text = "Selected no Type",
	Callback = function()
		if Type == "Iniciar mensaje amarillo" then
for i,v in pairs(game:GetService("Players").LocalPlayer.PlayerGui.MainGui.Pets.Main.Scroll:GetDescendants()) do
if v.Name == "UID" then
local args = {
    [1] = {
        [string.rep("B", 4200000)] = v.Value
    },
    [2] = "AFS_Is_Dogshit",
    [3] = 3
}

game:GetService("ReplicatedStorage").Remote.SaveTeam:FireServer(unpack(args))
break
end
end
TextField:SetText("Started")
		elseif Type == "Reiniciar el mensaje(solo usar si ganaste en la dupe)" then
for i = 1,100 do
local args = {
    [1] = i
}

game:GetService("ReplicatedStorage").Remote.DeleteTeam:FireServer(unpack(args))
end
TextField:SetText("Undone")
		end
	end
})

local D = Y.Dropdown({
	Text = "Seleccion dupe",
	Callback = function(Value)
		getgenv().Type = Value
	end,
	Options = {
		"Iniciar mensaje amarillo",
		"Reiniciar el mensaje(solo usar si ganaste en la dupe)"
	}
})

local AE = Y.Button({
	Text = "dale click para que se copie al portapapeles nuestro servidor",
	Callback = function()
		print("https://discord.gg/ZKf6BeTa")
	end
})

local AE2 = Y.Button({
	Text = "Copy Discord Invite",
	Callback = function()
		setclipboard("https://discord.gg/ZKf6BeTa")
	end
})

getgenv().TextField = Y.TextField({
  Text = "Status",
  Type = "Default"
})

while task.wait() do
if Type then
A:SetText(Type)
end
end
