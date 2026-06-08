---
title: "Enigma Storage"
weight: 2
summary: "Mass item storage reimagined as a Paper plugin. Store millions of items in a single block, wire them into a wireless mesh network, and access your storage from anywhere — no mods or client install required."
version: "Minecraft 26.1.2 / Paper 26.1.2"
download: "https://github.com/Enigma-North/Enigma-Storage/releases"
github: "https://github.com/Enigma-North/Enigma-Storage"
---

**Mass item storage, reimagined as a Paper plugin.** Store millions of items in a single block, wire them into a wireless mesh network, and pull anything from anywhere — no mods, no client install. Inspired by Applied Energistics 2.

Every Server Rack (DSU) stores its contents in item NBT, so nothing is ever lost on restart. Build a Server Rack, drop in a Wireless Router or two, mount a terminal on the wall — and your entire base storage becomes one sortable, hopper-automatable grid.

---

## The Hardware

Enigma Storage is built around a handful of physical blocks you place, link, and grow into a network.

### Server Rack
Your storage core. Slot in storage cells, add trusted players, and hook up hoppers for fully automated I/O. Each rack projects a **16-block mesh zone** around itself — the foundation of your network.

### Wireless Router
Need more reach? Drop a Wireless Router. It extends the mesh with a **64-block coverage cube** and chains off your existing network — place it so its zone overlaps the rack's, and your range grows organically across the base. Link enough of them and scale it across your entire base.

### Wall Terminal
A flush terminal that mounts right on the wall. Walk up, open it, and browse your linked rack's contents in-place — perfect for a clean, panel-lined storage room.

### Wireless Terminal
The same storage grid, in your hotbar. Bind it with a Link Module and access your Server Rack from anywhere inside the mesh — mine, fight, build, and deposit loot without ever walking home.

---

## Features

**Storage**
- 6 cell sizes: 1K / 4K / 16K / 64K / 256K / 1M items per Server Rack
- Sort by name, count, container order, or ID
- Lock a rack to its owner and add trusted players
- Hopper I/O with adjustable speed and Speed Upgrades

**Mesh Network**
- Coverage is a real, in-world **cube** around every node — no abstract "range numbers" to guess
- Server Racks anchor the network (16-block zone); Wireless Routers extend it (64-block zone)
- Routers must overlap an existing zone to connect, so networks grow outward from the rack the way you build them
- The path from each router back to the rack is rebuilt from scratch on every check (BFS) — it's a true mesh, not a fixed chain
- Self-healing: if a router has a backup path to the rack, the network reroutes automatically when one node is removed. Double up your routers and avoid single-bridge bottlenecks
- One rack = one network — neighbouring racks stay independent and never merge
- Tune both radii in the config (`rack-range`, `router-range`)

**Terminals**
- **Wall Terminal** — mounted, in-place access for storage rooms
- **Wireless Terminal** — bind with a Link Module and reach your storage from anywhere in the mesh

**Custom Recipes**
- Craft Enigma gear at a special workbench (dispenser)
- Browse every recipe in an in-game recipe book with page navigation

**Languages**
- Ships with: ru, en, de, fr, es, pl, cn
- Drop a `.json` into `languages/` and point the config at it to add your own

**WorldGuard integration** *(optional)*
- Soft-dependency — works fine without it, no errors if WorldGuard isn't installed
- Blocks placement, break, terminal linking, and storage access inside protected regions
- Region members and owners always have access; outsiders are denied
- Storage access is checked at the **rack's** location, not the player's — a terminal can't reach into a rack sitting in someone else's protected region
- Custom region flag `enigma-storage-use` for fine-grained per-region control: `/rg flag <region> enigma-storage-use deny` (unset falls back to region membership)
- Plays nicely with GriefPrevention, Towny, Lands and similar — Sorter creation also respects their block-protection
- Fails **closed** by default — a broken WorldGuard check denies access rather than silently letting griefers through

---

## Installation

1. Drop `EnigmaStorage.jar` into `plugins/`.
2. Start the server.
3. Tweak `plugins/EnigmaStorage/config.yml` to taste.

There's an optional resource pack — players see a download link on join (toggle it in the config).

---

## Commands

All commands use `/es` — aliases `/enigmastorage` and `/dsu` work too.

| Command | What it does |
|---|---|
| `/es help` | Show the command list |
| `/es book` | Open the recipe book |
| `/es give <item> [qty]` | Give yourself an item |
| `/es give <player> <item> [qty]` | Give a player an item |
| `/es items [page]` | List all plugin item keys |
| `/es craft <recipe> [qty]` | Give yourself a recipe result item |
| `/es craft <player> <recipe> [qty]` | Give a player a recipe result item |
| `/es recipes [page]` | List all recipe names |
| `/es migrate` | Run the one-time SQLite → NBT data migration |
| `/es reload` | Reload config and language files |

Item keys for `/es give` include: `server_rack`, `router`, `wall_terminal`, `terminal`, `link_module`, `receiver`, `sorter_wrench`, `speed_upgrade`, `creative_storage_container`, and the `storage_cell_*` / `storage_container_*` families.

---

## Permissions

The player-facing permissions below default to everyone so people can build out of the box; the rest default to `op`.

| Permission | What it allows | Default |
|---|---|---|
| `enigmastorage.use` | Run `/es` at all | **everyone** |
| `enigmastorage.create` | Build Server Rack | **everyone** |
| `enigmastorage.wireless` | Use the wireless terminal | **everyone** |
| `enigmastorage.wallterminal` | Open the wall terminal | **everyone** |
| `enigmastorage.recipe` | Access `/es` recipe features | **everyone** |
| `enigmastorage.recipe.book` | Open the recipe book (`/es book`) | **everyone** |
| `enigmastorage.recipe.craft` | Craft custom recipes at the workbench | **everyone** |
| `enigmastorage.recipe.craft.<name>` | Craft one specific recipe | **everyone** |
| `enigmastorage.adminopen` | Open locked DSUs | op |
| `enigmastorage.give` | `/es give` and `/es items` | op |
| `enigmastorage.migrate` | Run `/es migrate` | op |
| `enigmastorage.reload` | Run `/es reload` | op |
| `enigmastorage.recipe.giveitem` | Right-click items in the recipe book to receive them | op |
| `enigmastorage.recipe.give` | `/es craft` and `/es recipes` | op |
| `enigmastorage.recipe.craftall` | Craft everything without per-recipe perms | op |
| `enigmastorage.recipe.new` | Create new custom recipes via the recipe book | op |
| `enigmastorage.recipe.op` | See permission names in the recipe book | op |

---

## Config

```yaml
loadresourcepack: true   # show the resource pack link on join
resourcepackmessage: true
prefix: "&f&l[&9&lEnigmaStorage&f&l]"
range: 500               # legacy wireless terminal range in blocks (-1 = no limit)

# Mesh network coverage (cube radius per axis, in blocks)
rack-range: 16           # Server Rack base zone
router-range: 64         # Wireless Router zone (must overlap an existing zone to link)

# Resource pack download URL
resourcepack:
  url: "https://cdn.ltht.app/EnigmaNorth/EnigmaStorage-v1010.zip"

language: "en"           # en, ru, de, fr, es, pl, cn — or a custom file in languages/

# WorldGuard anti-grief (optional)
worldguard:
  enabled: true
  protect-build: true    # protect placing/breaking Enigma blocks
  protect-access: true   # protect opening GUIs, upgrades, terminal linking, hopper I/O
  fail-open: false       # false = deny on internal WG error (recommended)

# Storage limits (applied at craft time)
countinstacks: false     # count limits in stacks instead of single items
1kmax: 1
4kmax: 4
16kmax: 16
64kmax: 64
256kmax: 256
1mmax: 1024
```

---

Made by Enigma North. Based on DeepStoragePlus by Darkolythe. GNU GPL v3.
