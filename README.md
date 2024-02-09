<h1 align="center"><a href="https://discord.gg/brocode" target="_blank" rel="noopener noreferrer">Brocode Wounding</a></h1>

As of right now, only Bro Code Version of ox_inventory is only compatible with this script. It is a bridge and storage box used to compute player injuries. You could improve your roleplay server's Medical Services by carefully using the Exports. Additionally, we intend to write a medic script to guarantee greater compatibility and extensive resource support for this script. To enable you to incorporate it into your script, callbacks and exports will be offered.

## Installation

1. Download the ox_inventory-brocode from https://github.com/TeamBroCode/ox_inventory-brocode.
2. Add the scripts (ox_inventory and BC_Wounding) to your resources folder.
3. Edit the Config for your framework. (Currently only supports QBCore / QBOX / ESX)
4. Please only edit the client_open if you understand with its working structure and can adjust it to your specifications. (Optional)
5. Add the following to your server.cfg file:

```lua
ensure BC_Wounding
ensure ox_inventory
```

6. Start the server and enjoy!

## Exports

### Client Side

```lua
    local PlayerDamage = exports.BC_Wounding:GetPlayerDamage() -- Returns the player's damage. Returns a table.
    -- Result
    PlayerDamage = {
        ['HEAD'] = { bullet = 0, severity = false, broken = false, bleeding = false },
        ['NECK'] = { bullet = 0, severity = false, broken = false, bleeding = false },
        ['SPINE'] = { bullet = 0, severity = false, broken = false, bleeding = false },
        ['UPPER_BODY'] = { bullet = 0, severity = false, broken = false, bleeding = false },
        ['LOWER_BODY'] = { bullet = 0, severity = false, broken = false, bleeding = false },
        ['LARM'] = { bullet = 0, severity = false, broken = false, bleeding = false },
        ['LHAND'] = { bullet = 0, severity = false, broken = false, bleeding = false },
        ['LFINGER'] = { bullet = 0, severity = false, broken = false, bleeding = false },
        ['LLEG'] = { bullet = 0, severity = false, broken = false, bleeding = false },
        ['LFOOT'] = { bullet = 0, severity = false, broken = false, bleeding = false },
        ['RARM'] = { bullet = 0, severity = false, broken = false, bleeding = false },
        ['RHAND'] = { bullet = 0, severity = false, broken = false, bleeding = false },
        ['RFINGER'] = { bullet = 0, severity = false, broken = false, bleeding = false },
        ['RLEG'] = { bullet = 0, severity = false, broken = false, bleeding = false },
        ['RFOOT'] = { bullet = 0, severity = false, broken = false, bleeding = false },
    }

    exports.BC_Wounding:ResetAll() -- Resets the player's damage completely.

    -- BodyPart: string (Refer Config.Bones), bullet: int, severity: bool, broken: bool, bleeding: bool
    exports.BC_Wounding:UpdatePlayerDamage(bodyPart, bullet, severity, broken, bleeding) -- Updates the player's damage.

    -- Example
    exports.BC_Wounding:UpdatePlayerDamage('HEAD', 10, true, true, true) -- Updates the player's head damage.
```

### Server Side

```lua
    local PlayerDamage = exports.BC_Wounding:GetPlayerDamage(source) -- Returns the player's damage. Returns a table.
    -- Result
    PlayerDamage = {
        ['HEAD'] = { bullet = 0, severity = false, broken = false, bleeding = false },
        ['NECK'] = { bullet = 0, severity = false, broken = false, bleeding = false },
        ['SPINE'] = { bullet = 0, severity = false, broken = false, bleeding = false },
        ['UPPER_BODY'] = { bullet = 0, severity = false, broken = false, bleeding = false },
        ['LOWER_BODY'] = { bullet = 0, severity = false, broken = false, bleeding = false },
        ['LARM'] = { bullet = 0, severity = false, broken = false, bleeding = false },
        ['LHAND'] = { bullet = 0, severity = false, broken = false, bleeding = false },
        ['LFINGER'] = { bullet = 0, severity = false, broken = false, bleeding = false },
        ['LLEG'] = { bullet = 0, severity = false, broken = false, bleeding = false },
        ['LFOOT'] = { bullet = 0, severity = false, broken = false, bleeding = false },
        ['RARM'] = { bullet = 0, severity = false, broken = false, bleeding = false },
        ['RHAND'] = { bullet = 0, severity = false, broken = false, bleeding = false },
        ['RFINGER'] = { bullet = 0, severity = false, broken = false, bleeding = false },
        ['RLEG'] = { bullet = 0, severity = false, broken = false, bleeding = false },
        ['RFOOT'] = { bullet = 0, severity = false, broken = false, bleeding = false },
    }
```
