# XIV Planner

A Dalamud plugin that levels a crafter for you. Pick a class and a target level, press Go, and it plans the cheapest way
there from what you already hold, then does it: fetches from your retainers, buys vendor items, crafts with Artisan, does
the class quests with Questionable, sells what it crafts, puts on gear upgrades, and re-plans every few levels.

There's also a Quests tab: type a quest's name (or what it rewards, like a mount), see the chain from where you are,
and Go hands it to Questionable quest by quest.

This repository only holds the plugin's releases. The source isn't public.

## Install

1. In game, `/xlsettings`, Experimental tab, Custom Plugin Repositories. Add:
   `https://raw.githubusercontent.com/Tacodille/xiv-planner-releases/main/repo.json`
   then tick it, Save and close.
2. `/xlplugins`, search for **XIV Planner**, install.
3. `/xivplan` opens the window. Its **Plugins** section lists anything missing, with a button to find each one and the
   repository link to add for the ones outside Dalamud's own list.

## What it needs

| Plugin | What for | Where it comes from |
|---|---|---|
| Artisan | every craft | `https://love.puni.sh/ment.json` |
| vnavmesh | walking to bells, boards and vendors | `https://puni.sh/api/repository/veyn` |
| Lifestream | getting to the hub and the aethernet | `https://github.com/NightmareXIV/MyDalamudPlugins/raw/main/pluginmaster.json` |
| Allagan Tools | counting what your retainers hold | Dalamud's own list |
| Questionable (optional) | class quests and quest chains | `https://love.puni.sh/ment.json` |
| GatherBuddy Reborn (optional) | buying vendor items | `https://raw.githubusercontent.com/FFXIV-CombatReborn/CombatRebornRepo/main/pluginmaster.json` |
| AutoRetainer (optional) | selling crafted items to vendors | `https://love.puni.sh/ment.json` |
| Gearsetter (optional) | putting on gear upgrades | `https://puni.sh/api/repository/vera` |

## Worth knowing first

- **It automates a lot**: crafting, travel, buying, selling, quests. All of that is against the game's terms of
  service, like any automation plugin, and you use it at your own risk.
- **The market board is off by default.** Tick "Buy market board items for me" to let it buy, and it stays within two
  caps you set: a percentage over the planned price and a gil limit per stretch. It only presses Yes when the game's
  own prompt shows the quantity and price it expected.
- **English game client only** for market board buying. On another language every purchase safely answers No.
- **The hub** (Hub settings in the window) is where it goes for bells, boards and vendors: a housing district ward on
  your current world, or Old Gridania. Defaults to the Lavender Beds, ward 1.
- **Known issue in Artisan 4.0.5.21**: crafts that need it to pick HQ or NQ ingredients fail inside Artisan
  (NightmareXIV/ECommons#182, PunishXIV/Artisan#299). The plugin leaves such recipes out and plans around them.
- **GatherBuddy Reborn's route to Mist** can get stuck at the Limsa aetheryte menu. If an item keeps sending you there,
  pick another vendor for it in GBR's buy list.

## Credits

Built on ECommons (MIT). Ideas, not code, from Artisan, MarketMafioso, HaselCommon and LazyCrafter. Class quest hand-in
counts come from Questionable's quest data.

MIT licence: see LICENSE.
