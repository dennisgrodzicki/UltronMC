# UltronMC — SkyBlock Server

A fully configured **Paper 1.8.8 SkyBlock** Minecraft server built under the name **UltronMC**, designed for a competitive multiplayer experience with economy, progression, and player-vs-player systems.

---

## Overview

UltronMC is a custom SkyBlock server where players start on a small floating island and expand it by completing challenges, levelling up, and participating in the server economy. It supports up to **200 players**, runs in **survival mode with PvP enabled**, and includes cross-platform play via Geyser (Bedrock + Java).

---

## Server Details

| Property | Value |
|---|---|
| Software | Paper 1.8.8 (build 445) |
| Game Mode | Survival (SkyBlock) |
| Max Players | 200 |
| PvP | Enabled |
| Difficulty | Easy |
| Whitelist | Enabled |
| Cross-play | Java + Bedrock (Geyser/Floodgate) |
| JVM RAM | ~6–7.5 GB allocated |

---

## Plugin Stack

### Core Gameplay
| Plugin | Purpose |
|---|---|
| **FabledSkyBlock** | The main SkyBlock engine — islands, challenges, generators, biomes, levelling, schematics |
| **EssentialsX** | Core server commands (home, warp, teleport, economy base) |
| **Vault** | Economy API bridge between plugins |
| **WorldEdit / WorldGuard** | Region editing and protection |

### Economy & Shops
| Plugin | Purpose |
|---|---|
| **EconomyShopGUI** | Chest-shop style GUI shop for buying/selling items |
| **AuctionHouse** (Retro) | Player-to-player auction listing system |
| **MoneyPouch** | Droppable/redeemable money pouches |
| **CoinFlip** | Gambling minigame — bet coins in a coin flip against other players |

### Progression & Rewards
| Plugin | Purpose |
|---|---|
| **Battlepass** | Season battlepass with tiered rewards |
| **UltimateKits** | Starter and donor kit system with cooldowns |
| **AdvancedCrates / CratesPlus / ExcellentCrates / SynthCrates** | Multiple crate systems with key-based loot |
| **EpicEnchantments** | Custom enchantments beyond vanilla |
| **AdvancedEnchantments** | Additional custom enchant system |

### Spawners & Mobs
| Plugin | Purpose |
|---|---|
| **EpicSpawners** | Stackable mob spawners with upgrade system |
| **StackMob** | Stacks nearby mobs into a single entity to reduce lag |
| **MashsBlockStacker** | Block stacker integration (linked to island levelling via custom plugin) |
| **SilkSpawners** | Allows picking up spawners with Silk Touch |
| **PassiveMobs** | Manages passive mob spawning on islands |
| **CustomOreGen** | Custom ore generation rates per island/biome |

### Moderation & Anti-Cheat
| Plugin | Purpose |
|---|---|
| **Verus** | Anti-cheat (movement, combat, inventory) |
| **LiteBans** | Ban, mute, kick, and warn system |
| **UltimateModeration** | Staff moderation toolkit |
| **CoreProtect** | Block logging and rollback for grief detection |
| **JetsAntiFKPro** | Anti-AFK / anti-farm-key detection |

### Permissions & Display
| Plugin | Purpose |
|---|---|
| **LuckPerms** | Permission management with rank groups |
| **TAB** | Custom tab list and scoreboard formatting |
| **SupremeTags** | Cosmetic chat tags for players |
| **LPC** | Prefix/suffix formatting in chat |
| **PlaceholderAPI** | Shared placeholder system across plugins |
| **Holograms** | Floating text display holograms |

### Utility & QoL
| Plugin | Purpose |
|---|---|
| **ViaVersion** | Allows newer Minecraft clients to connect to 1.8.8 |
| **Geyser + Floodgate** | Bedrock Edition cross-play support |
| **AutoRestart** | Scheduled automatic server restarts |
| **ClearLag** | Removes excess entities/items to reduce lag |
| **VoidTeleport** | Teleports players who fall into the void back to safety |
| **SimpleRename** | Rename items in-game with an anvil-like GUI |
| **NoCraftThat** | Disables specific crafting recipes |
| **PlugMan** | Load/unload/reload plugins without restarting |
| **Votifier / GAListener** | Vote reward system tied to Minecraft server lists |
| **BuycraftX** | Donation store integration |
| **EditDrops** | Customize mob/block drop tables |
| **UltimateClaims** | Land claiming system outside of islands |

---

## Custom Plugins

Several plugins in this server were **built in-house** (see the `eclipse-workspace/` projects):

- **CollectionChest** — Per-chunk chest that automatically collects nearby item drops and displays a hologram above it
- **Daily Rewards** — GUI-based daily reward system with a 16-hour cooldown; player data stored in `playerdata.yml`
- **StackLevelBridge** — Bridges FabledSkyBlock island levelling with MashsBlockStacker so block counts contribute to island level
- **UndeadHero** — Hero/God Kit system with GUI menus and per-kit cooldowns

---

## World Structure

```
world/              — Main overworld (SkyBlock islands)
world_nether/       — Nether dimension
world_the_end/      — End dimension
island_normal_world/  — FabledSkyBlock island world
island_nether_world/  — FabledSkyBlock island nether
island_end_world/     — FabledSkyBlock island end
```

---

## Starting the Server

```bat
start.bat
```

Launches the server with approximately 6–7.5 GB of RAM:

```bat
java -Xms6192M -Xmx7692M -jar paper-1.8.8-445.jar
```

---

## Notes

- The server was in **Open Beta** phase at the time of this snapshot (Feb 2026), as indicated by the MOTD: `UltronMC >> Open Beta Soon! Join Discord!`
- Whitelist was active during development/testing
- Cross-play was supported from day one via Geyser + Floodgate
