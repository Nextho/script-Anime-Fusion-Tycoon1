local library = loadstring(game:HttpGet("https://raw.githubusercontent.com/NiceBBMBThai12/NBTScript/main/UI-Library-Robloxx"))()
local window = library:Win()
local tap1 = window:addtap("main")
local tap2 = window:addtap("-")
local page1 = tap1:addpage()
local page2 = tap1:addpage()
local page3 = tap1:addpage()
local page4 = tap1:addpage()
page1:Ti("autofarm NEXIz")

page1:Toggle("Auto Farm",_false, function(value)
_G.autofarm = value
end)

spawn(function()
    while wait() do
        if _G.autofarm then
local A_1 = "Agarrado"
local A_2 = "Values"
local A_3 = "10"
local Event = game:GetService("ReplicatedStorage").Remotes.Pasante
Event:FireServer(A_1, A_2, A_3)
        end
    end
end)

page1:Toggle("Auto sell",_false, function(value)
    _G.autosell = value
    end)
    
    spawn(function()
        while wait() do
            if _G.autosell then
                local A_1 = "Depositar"
local Event = game:GetService("ReplicatedStorage").Remotes.Pasante
Event:FireServer(A_1)
            end
        end
    end)

page1:Toggle("Auto upgrade Hero",_false, function(value)
    _G.autoupgrade = value
    end)
        
    spawn(function()
         while wait() do
             if _G.autoupgrade then
                local A_1 = "Comprar1"
local Event = game:GetService("ReplicatedStorage").Remotes.Pasante
Event:FireServer(A_1)                    
            end
        end
    end)

page1:Toggle("Auto fusion",_false, function(value)
    _G.autofusion = value
     end)
        
    spawn(function()
        while wait() do
            if _G.autofusion then
                local A_1 = "Fusionar"
                local Event = game:GetService("ReplicatedStorage").Remotes.Pasante
                Event:FireServer(A_1)                
            end
        end
     end)
