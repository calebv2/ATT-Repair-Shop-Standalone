# ATT Repair Shop Standalone

A standalone repair-shop building for **A Township Tale PC**, with a shopkeeper, blacksmith, item intake, coin payment, and repair storage. Repairs use the forge, anvil, and wood-working station.

## Download

Download the ZIP from [Releases](https://github.com/calebv2/ATT-Repair-Shop-Standalone/releases/latest). It contains separate client and server versions of `RepairShop.dll`.

## Installation

Requires **MelonLoader** and **SyncLib** on the server and clients.

- Players: put `Client/RepairShop.dll` in your existing client mod folder, then restart the game.
- Server: put `Server/RepairShop.dll` in the server mod folder during a planned update. The server loads it when it next starts.
- Install only the correct role DLL in each process.

This is the **building-only** package. It shares its DLL and mod identity with the combined full-islands RepairShop package; choose one package. Existing combined map instances are not automatically converted. Preserve world data, `UserData/RepairShop`, and the SyncLib registry when updating.

## Place and use the shop

The prefab is `ATT_RepairShop_Standalone`. Find it using the server's admin spawn tools:

```text
spawn find ATT_RepairShop_Standalone
```

Place the building on a clear site at floor elevation. Deposit a damaged weapon or tool at intake, follow the sign and coin-payment instructions, and collect the finished item from its assigned shelf.

## NPC cosmetics

These commands work on any server running the server mod. Run them in that server's admin console with console permissions, while the source player is online on that server. Use their exact username and quote names containing spaces.

```text
repairshop outfit copy keeper "PlayerName"
repairshop outfit copy blacksmith "PlayerName"
repairshop outfit status
repairshop outfit reload
repairshop outfit reset keeper
repairshop outfit reset blacksmith
```

Each worker has its own saved appearance, including body type. Change the player's outfit between copy commands to dress the two workers differently. Settings are saved separately on the hosting server in `UserData/RepairShop/worker-outfits.json` and apply to its current workers. Use `reload` after manually editing that file. Outfit commands do not require a server restart.

## Version 0.2.30

- Standalone building with both repair workers.
- Metal and wooden-part work at the appropriate stations.
- Correct body-type application and open NPC eyes.
- Server shop registry replaces recurring scene-wide shop discovery.

The worker rig moves between stations without a legged walking animation.