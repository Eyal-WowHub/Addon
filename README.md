# Addon

A library that facilitates object creation and event handling, providing essential infrastructure for addons.

### Example:

```lua
-- Main.lua
local addon = LibStub("Addon-1.0"):New(...)

function addon:OnInitialized()
    print("Hello from " .. addon:GetName())
end

-- Foo.lua
local _, addon = ...
local Foo = addon:NewObject("Foo")

Foo:RegisterEvent("PLAYER_LOGIN", function(_, eventName)
    print("Hello from " .. eventName)
end)
```







