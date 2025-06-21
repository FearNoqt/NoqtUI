
--[[ Noqt UI Library
A fully featured Roblox UI Library designed for clean interfaces, custom themes, and easy usage.
Inspired by Orion and CMCD, but optimized to be lightweight, flexible, and loadstring compatible.

Features
Full Themes (Dark, Sky, Cyber, Light) — extend with your own styles!
Draggable UI – all windows can be moved freely.
Config System Structure – easy to expand with file save/load.
All UI Elements ready to use:
AddLabel
AddToggle
AddTextbox
AddSlider
AddDropdown
AddKeybind
Loadstring Compatible – use with loadstring(game:HttpGet(...))().
Live Theme Switching – Noqt:ApplyTheme("Sky")

Example Usage
--]]

local Noqt = loadstring(game:HttpGet("https://raw.githubusercontent.com/FearNoqt/NoqtUI/refs/heads/main/Documations"))()
local UI = Noqt():MakeWindow({ Name = "Noqt UI Hub" })

UI:AddLabel("Welcome to Noqt UI")

UI:AddToggle({
    Name = "Enable Feature",
    Default = true,
    Callback = function(state)
        print("Toggle State:", state)
    end
})

UI:AddTextbox({
    PlaceholderText = "Type something...",
    Callback = function(text)
        print("User input:", text)
    end
})

UI:AddDropdown({
    Name = "Select Option",
    Options = {"Option A", "Option B", "Option C"},
    Callback = function(opt)
        print("Selected:", opt)
    end
})

UI:AddSlider({
    Name = "Volume",
    Min = 0,
    Max = 100,
    Default = 50,
    Callback = function(value)
        print("Slider Value:", value)
    end
})

UI:AddKeybind({
    Name = "Quick Key",
    Default = Enum.KeyCode.E,
    Callback = function(key)
        print("Pressed:", key)
    end
})

 --[[
 Theme Switching

Noqt:ApplyTheme("Cyber") -- Available: Dark, Sky, Cyber, Light
Setup Instructions
local Noqt = loadstring(game:HttpGet("https://raw.githubusercontent.com/FearNoqt/NoqtUI/refs/heads/main/Documations"))()
Custom Themes

Noqt:AddTheme("Neon", {
    Background = Color3.fromRGB(25, 25, 25),
    Foreground = Color3.fromRGB(0, 255, 170),
    Accent = Color3.fromRGB(255, 0, 128),
    Button = Color3.fromRGB(0, 255, 128),
    Toggle = Color3.fromRGB(0, 170, 255),
    Slider = Color3.fromRGB(200, 200, 255),
    Dropdown = Color3.fromRGB(255, 200, 100),
    Textbox = Color3.fromRGB(255, 255, 255)
})
Then call:

Noqt:ApplyTheme("Neon")
Made by NoqtHub
]]
