---
title: "Enigma Storage"
weight: 2
summary: "A compact terminal storage system for Minecraft Paper/Spigot servers, inspired by Applied Energistics 2 (AE2). Adds Deep Storage Units with massive capacity, a wireless terminal, and SQLite-backed persistence."
version: "Minecraft 26.1.2 / Paper 26.1.2"
download: "https://github.com/Enigma-North/Enigma-Storage/releases"
github: "https://github.com/Enigma-North/Enigma-Storage"
---

**Enigma Storage** is a bulk item storage plugin for Paper/Spigot, forked from DeepStoragePlus and updated for the current Minecraft version — 26.1.2.

Store millions of items in a single block. DSU data is saved in SQLite so nothing is lost on restart. Access your storage wirelessly from anywhere and automate transfers with hoppers.

---

## Installation

1. Put `EnigmaStorage.jar` in `plugins/`.
2. Start the server.
3. Edit `plugins/EnigmaStorage/config.yml` if needed.

There's an optional resource pack — players see a download link on join. You can turn it off in the config.

---

## Features

**Storage**
- 6 sizes: 1K / 4K / 16K / 64K / 256K / 1M items per DSU
- Sort by name, count, container order, or ID
- Lock your DSU and add trusted players
- Hopper I/O with adjustable speed and upgrades

**Wireless Terminal**
- Use your DSU from anywhere on the map
- Bind it with a Link Module, set a range limit or remove it entirely

**Custom Recipes**
- Craft at a special workbench (dispenser)
- Browse all recipes in a recipe book with page navigation

**Languages**
- Ships with: ru, en, de, fr, es, pl, cn
- Drop a `.json` into `languages/` and set it in config to add your own

---

## Commands

All commands use `/es` — aliases `/enigmastorage` and `/dsp` also work.

| Command | What it does |
|---|---|
| `/es give <item> [amount]` | Give yourself an item |
| `/es give <player> <item> [amount]` | Give a player an item |
| `/es items` | Show all plugin items |
| `/es migrate` | Re-run DSU data migration to SQLite |
| `/es recipe book` | Open the recipe book |
| `/es recipe give <player> <name> [amount]` | Give a recipe result item |
| `/es recipe items` | List all recipe names |

---

## Permissions

All permissions default to `op`. The only exception is `enigmastorage.recipe.craft` which is enabled for everyone so players can craft out of the box.

| Permission | What it allows | Default |
|---|---|---|
| `enigmastorage.create` | Build DSUs | **everyone** |
| `enigmastorage.wireless` | Use the wireless terminal | **everyone** |
| `enigmastorage.recipe` | Access `/es recipe` | **everyone** |
| `enigmastorage.recipe.book` | Open the recipe book | **everyone** |
| `enigmastorage.recipe.craft` | Craft at the workbench | **everyone** |
| `enigmastorage.recipe.craft.<name>` | Craft one specific recipe | **everyone** |
| `enigmastorage.recipe.craftall` | Craft everything without individual perms | **everyone** |
| `enigmastorage.adminopen` | Open locked DSUs | op |
| `enigmastorage.give` | `/es give` and `/es items` | op |
| `enigmastorage.recipe.giveitem` | Right-click items in the recipe book to receive them | op |
| `enigmastorage.recipe.give` | `/es recipe give` and `/es recipe items` | op |
| `enigmastorage.recipe.op` | See permission names in the recipe book | op |

---

## Config

```yaml
language: "en"           # en, ru, de, fr, es, pl, cn — or a custom file in languages/
loadresourcepack: true   # show resource pack link on join
prefix: "&f&l[&9&lEnigmaStorage&f&l]"
range: 500               # wireless terminal range in blocks (-1 = no limit)
countinstacks: false     # if true, storage limits count stacks instead of items
1kmax: 1
4kmax: 4
16kmax: 16
64kmax: 64
256kmax: 256
1mmax: 1024
```

---

Made by EnigmaticMP. Based on DeepStoragePlus by Darkolythe. GNU GPL v3.
