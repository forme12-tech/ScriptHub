local OrionLib = loadstring(game:HttpGet(('https://raw.githubusercontent.com/shlexware/Orion/main/source')))()
local Player = game.Players.LocalPlayer
local Window = OrionLib:MakeWindow({Name = "SpeedHUB Key System", HidePremium = true, SaveConfig = true, ConfigFolder = "Key System"})

OrionLib:MakeNotification({
	Name = "Logged In!",
	Content = "Welcome to SpeedHUB Key System! "..Player.Name..".",
	Image = "rbxassetid://4483345998",
	Time = 5
})

_G.Key = cLCkMTHHkLmzFEtsNXPiYjSsU
_G.KeyInput = "string"

function MakeScriptHub()
       if game.PlaceId == 7560156054
       local Window = OrionLib:MakeWindow({Name = "SpeedHUB", HidePremium = true, SaveConfig = true, ConfigFolder = "SpeedHUB"})
       

end

function CorrectKeyNotification()
       OrionLib:MakeNotification({
	Name = "Correct Key!",
	Content = "You have entered the correct key!",
	Image = "rbxassetid://4483345998",
	Time = 5
})

function IncorrectKeyNotification()
       OrionLib:MakeNotification({
	Name = "Incorrect Key!",
	Content = "You have entered the Incorrect key!",
	Image = "rbxassetid://4483345998",
	Time = 5
})

local Tab = Window:MakeTab({
	Name = "Key System",
	Icon = "rbxassetid://4483345998",
	PremiumOnly = false
})

Tab:AddTextbox({
	Name = "Key",
	Default = "Enter Key Here",
	TextDisappear = true,
	Callback = function(Value)
		_G.KeyInput = Value
	end	  
})

Tab:AddButton({
	Name = "Enter Key",
	Callback = function()
      		if _G.KeyInput == _G.Key then
      		MakeScriptHub()
      		CorrectKeyNotification()
      		else
      		      IncorrectKeyNotification()
      		end
  	end    
})
