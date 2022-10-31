-- KEY | HWID

_G.Key = "KEY-A"


HWID = "HELLO1"

local Server =  syn.request({
    Url = "http://127.0.0.1/Whitelist/Server.php?Key=".. _G.Key .."&HWID="..HWID,
    Method = "GET"
}).Body

if Server == "WHITELIST !" then
    print("SCRIPT")
elseif Server == "Invaid HWID !" then
    game.Players.LocalPlayer:kick("Invaid HWID")
elseif Server == "Invaid Key" then
    game.Players.LocalPlayer:kick("Invaid Key")
else
    game.Players.LocalPlayer:kick("Invaid Key")
end
