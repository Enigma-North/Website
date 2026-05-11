---
title: "Enigma Storage"
weight: 2
summary: "A compact terminal storage system for Minecraft Paper/Spigot servers, inspired by Applied Energistics 2 (AE2). Adds Deep Storage Units with massive capacity, a wireless terminal, and SQLite-backed persistence."
version: "Minecraft 26.1.2 / Paper 26.1.2"
download: "https://github.com/Repulsiveprogress/Enigma-Storage/releases"
github: "https://github.com/Repulsiveprogress/Enigma-Storage"
---

**Enigma Storage** is a bulk item storage plugin for Paper/Spigot, forked from DeepStoragePlus and updated for the current Minecraft version — 26.1.2.

## Features

- **Deep Storage Units (DSU)** with massive item capacity and portable Storage Containers.
- **Wireless terminal** linked to your DSUs from anywhere.
- **SQLite persistence** — DSU contents survive restarts and migrations.
- **Custom recipes** via the built-in CustomRecipeAPI.
- **Fine-grained permissions** for all commands and features.

## Installation

1. Copy `EnigmaStorage.jar` into your server's `plugins/` folder.
2. Start the server to generate `plugins/EnigmaStorage/config.yml`.
3. Reload or restart the server.

## Commands

### Enigma Storage

| Command | Description |
|---|---|
| `/es items` | List all registered Enigma Storage items |
| `/es give <player> <item> <amount>` | Give an item to a player |
| `/es give <item> <amount>` | Give an item to yourself |
| `/es migrate` | Force-migrate DSU data from lore to SQLite |

> Aliases: `enigmastorage`, `dsp`

### CustomRecipeAPI

| Command | Description |
|---|---|
| `/crapi book` | Open the recipe book |
| `/crapi new` | Create a new recipe in-game |
| `/crapi setworkbench` | Open the workbench editor |
| `/crapi workbench` | View the current workbench recipe |
| `/crapi items` | Show available CustomRecipeAPI recipes |
| `/crapi give <player> <item> <amount>` | Give a recipe result |

## Permissions

### Enigma Storage

| Permission | Description |
|---|---|
| `enigmastorage.create` | Allows creating DSUs |
| `enigmastorage.adminopen` | Allows opening locked DSUs |
| `enigmastorage.wireless` | Allows using the wireless terminal |
| `enigmastorage.give` | Allows using `/es give` |

### CustomRecipeAPI

| Permission | Description |
|---|---|
| `crapi.command` | Use the `/crapi` command |
| `crapi.book` | Open the recipe book and workbench |
| `crapi.new` | Create new recipes in-game |
| `crapi.craft` | Craft custom recipes |
| `crapi.give` | Use `/crapi give` and `/crapi items` |

## Credits

- **EnigmaticMP** — author of this project.
- **Darkolythe** — original DeepStoragePlus and CustomRecipeAPI.

## License

Distributed under [GNU GPL v3](https://github.com/Repulsiveprogress/Enigma-Storage/blob/main/LICENSE).
