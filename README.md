# XIV Planner

A Dalamud plugin that levels a crafter, Miner or Botanist for you. Pick a class and a target level, press Go, and it
plans the cheapest way there from what you already hold, then does it: fetches from your retainers, gathers what your
Miner or Botanist can reach, buys vendor items, gives you one market board list to buy by hand, crafts with Artisan,
does the class quests with Questionable, sells what it crafts, puts on gear upgrades, and re-plans as you level.

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
| GatherBuddy Reborn (optional) | buying vendor items, gathering | `https://raw.githubusercontent.com/FFXIV-CombatReborn/CombatRebornRepo/main/pluginmaster.json` |
| AutoRetainer (optional) | selling crafted items to vendors | `https://love.puni.sh/ment.json` |
| Gearsetter (optional) | putting on gear upgrades | `https://puni.sh/api/repository/vera` |

## Worth knowing first

- **It automates a lot**: crafting, gathering, travel, vendor buying, selling, quests. All of that is against the game's
  terms of service, like any automation plugin, and you use it at your own risk. Stay at the keyboard while it runs.
- **The market board is always by hand.** The plugin never buys there. Each shopping list covers the next 10 levels
  (change it in the window) and shows, per item, how many, HQ or not, the most to pay and the cheapest seen; rows go
  green as your bags fill and the run carries on by itself. "Gil max per shopping list" caps vendor spending: raise it
  for a 10-level list.
- **Where it goes**: vendor items first (GatherBuddy Reborn goes wherever they're sold), then a bell in whatever zone
  that leaves you, and it crafts there. If the zone has none, it uses the hub from Hub settings in the
  window: a housing ward on your current world (Lavender Beds ward 1 by default) or Old Gridania.
- **New crafter, Miner or Botanist?** Pick it and press Go: it does the unlock quests, equips the tool and makes a
  gearset first. Gatherers stay in A Realm Reborn zones (no flying needed), so up to level 50.
- **Gathering for crafting**: mats your Miner or Botanist can reach are gathered through GatherBuddy Reborn before
  anything is bought. It never unlocks a gatherer just for that.
- **First crafts**: recipes you've never made give a big one-off bonus, so it makes cheap new recipes once before
  grinding one.
- **Grand Company supply missions**: open your GC's supply window once a day and the run crafts that class's request
  first; you hand it in yourself.
- **Use up my mats** crafts whatever your bags can make on the class, best XP first, buying only small vendor bits
  (rivets and the like) to finish off mats you can't rebuy. It sells as it goes to keep room in your bags.
- **Live XP**: the Run tab shows your XP bar, XP an hour lately and time to the next level and the target.
- **It crafts the ingredients it can** (lumber, cloth, yarn, ingots...) from base mats instead of buying them, and their XP
  counts towards the level. Cheaper in gil, more crafts. "Craft ingredients myself" in the window turns it off.
- **Class quest hand-ins** it can craft at your level get crafted (two tries for HQ) before anything is bought.
- **Selling**: crafted items worth listing on the market board (by recent sales on Universalis) are kept and shown in the
  window; the rest go to a vendor through AutoRetainer.
- **Repairs**: if your gear is under 70%, it crafts next to a mender so Artisan can repair there. In Artisan, tick
  "Prioritize Repair NPC".
- **Copy report** in the window copies what the run did, for sending to whoever's helping you.
- **Known issue in Artisan 4.0.5.21**: crafts that need it to pick HQ or NQ ingredients fail inside Artisan
  (NightmareXIV/ECommons#182, PunishXIV/Artisan#299). The plugin leaves such recipes out and plans around them.
- **Housing district vendors**: GatherBuddy Reborn can't reach a district you haven't unlocked ("Where the Heart Is"
  quests). The plugin picks another vendor, or tells you which quest unlocks it.

## Credits

Built on ECommons (MIT). Ideas, not code, from Artisan, MarketMafioso, HaselCommon and LazyCrafter. Class quest hand-in
counts come from Questionable's quest data.

MIT licence: see LICENSE.
