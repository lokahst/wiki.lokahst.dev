---
title: Commands
updated: July 19, 2026
---

| Command | Aliases | Description | Permission |
|---------|---------|-------------|------------|
| `/valentines` | `/val`, `/vgui` | Open the main interface | `valentines.use` |
| `/vreload` | None | Reload the plugin configuration | `valentines.reload` |

## Player Commands

| Command | Aliases | Description | Permission |
|---------|-----------------------------|-------------|------------|
| `/lotn` | `/legends`, `/legendsofthenorth`, `/lotn menu` | Opens the main LOTN menu | `lotn.use` |
| `/lotn stats` | `/stats`, `/character`, `/lotn character` | Opens character statistics | `lotn.use` |
| `/lotn attributes` | `/attributes` | Opens the attributes menu | `lotn.use` |
| `/lotn skills` | `/skills`, `/lotn perks`, `/perks` | Opens the skill categories and perk trees | `lotn.use` |
| `/lotn journal` | `/journal` | Opens the quest journal | `lotn.use` |
| `/lotn quests` | `/quests` | Opens the available quests page | `lotn.use` |
| `/lotn contracts` | `/contracts` | Opens available contracts | `lotn.use` |
| `/lotn codex` | `/codex` | Opens the codex | `lotn.use` |
| `/lotn fishdex` | `/fishdex` | Opens the fish collection | `lotn.use` |
| `/lotn factions` | `/factions`, `/lotn reputation`, `/reputation` | Opens factions and reputation | `lotn.use` |
| `/lotn enchants` | `/enchants` | Opens the custom enchantments menu | `lotn.use` |
| `/lotn alchemy` | `/alchemy` | Opens the custom alchemy workbench | `lotn.use`, `lotn.alchemy` |
| `/lotn fish` | `/fish` | Opens the fish shop | `lotn.use` |
| `/lotn travel` | `/travel`, `/lotn fasttravel`, `/fasttravel` | Opens the fast-travel menu | `lotn.use` |
| `/lotn sellfish` | `/sellfish`, `/lotn sellall`, `/sellall` | Sells all LOTN fish in the player's inventory | `lotn.use` |

## Administration Commands

| Command | Description | Permission |
|---------|-------------|------------|
| `/lotn reload` | Reloads LOTN configuration | `lotn.use`, `lotn.admin` |
| `/lotn givexp <player> <amount>` | Gives player-level XP to an online player | `lotn.use`, `lotn.admin` |
| `/lotn givepoints <player> <amount>` | Gives perk points to an online player | `lotn.use`, `lotn.admin` |
| `/lotn unlockenchant <player> <enchant>` | Unlocks a custom enchantment for an online player | `lotn.use`, `lotn.admin` |
| `/lotn character setname <player> <name>` | Changes an online player's LOTN character name | `lotn.use`, `lotn.admin.character` |
| `/lotn character reset <player>` | Resets character creation while preserving progression | `lotn.use`, `lotn.admin.character` |
| `/lotn character info <player>` | Displays an online player's character information | `lotn.use`, `lotn.admin.character` |
| `/lotn character complete <player>` | Completes character creation for an online player | `lotn.use`, `lotn.admin.character` |
| `/lotna` | Displays administration help | `lotn.admin` |
| `/lotna help` | Displays administration help | `lotn.admin` |
| `/lotna reload` | Reloads all LOTN configuration and content | `lotn.admin` |

## Early Access Commands

| Command | Description | Permission |
|---------|-------------|------------|
| `/lotnea` | Opens the Shout administration menu | `lotn.admin` |
| `/lotnea help` | Displays Early Access command help | `lotn.admin` |
| `/lotnea maxpoints` | Gives the player 1,000 perk points | `lotn.admin` |
| `/lotnea maxupgrades` | Gives the player 1,000 upgrade points | `lotn.admin` |
| `/lotnea unlockall` | Unlocks all currently eligible configured perk ranks | `lotn.admin` |
| `/lotnea unlockallforce` | Sets every configured perk to its maximum rank, ignoring requirements | `lotn.admin` |
| `/lotnea resetnodes` | Clears all perk ranks and legacy unlocked nodes | `lotn.admin` |
| `/lotnea maxlevel` | Sets all enabled skills to their configured maximum level | `lotn.admin` |
| `/lotnea unlockallenchants` | Unlocks every custom enchantment | `lotn.admin` |
| `/lotnea menu` | Opens the skill category menu | `lotn.admin` |
| `/lotnea shouts` | Opens the Shout selection menu | `lotn.admin` |
| `/lotnea resetall` | Resets levels, skill XP, attributes, perks, enchantments and progression points while preserving quests and collections | `lotn.admin` |
| `/lotnea breakleg [player]` | Gives the specified player a broken leg; targets the sender when omitted | `lotn.admin`, `lotn.admin.breakleg` |
| `/lotnea healleg [player]` | Heals the specified player's broken leg; targets the sender when omitted | `lotn.admin`, `lotn.admin.healleg` |