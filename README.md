# Data Crack Mini-Game

Made by **utku#9999**

Thanks **Danistheman262** from GTA5-Mods.com for showing me the right native functions.

## Installation

Simply put "datacrack" to your resources folder and start it from server.cfg

## Usage

- To start the mini-game use this in your code:

```lua
exports["datacrack"]:Start(difficulty) -- this will start the hack
```

Difficulties: ranging form 2 to 5 and can take float numbers. 5 is the hardest one and 2 is the easiest one. For example:

```lua
exports["datacrack"]:Start(2)
exports["datacrack"]:Start(2.5)
exports["datacrack"]:Start(3.7)
exports["datacrack"]:Start(4)
exports["datacrack"]:Start(4.5)
```

- To catch the hack outcome use this in your code: output == true means success, else is fail(abort)

```lua
AddEventHandler("datacrack", function(output) -- this event will be triggered when the player finished hacking
    -- your code here, for example:
    if output then
        ESX.ShowHelpNotification('Hack complete!', false, true, 5000)
    else
        ESX.ShowHelpNotification('Hack failed!', false, true, 5000)
    end
end)
```

- Alternative way to trigger datacrack, where difficulty is a float or integer ranging from 2 to 5, see example below:

```lua
TriggerEvent("datacrack:start", 3, function(output)
    if output == true then
    -- some code
    else
    -- some code
    end
end)
```
