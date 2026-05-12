---
title: "Enigma SlimeHUD"
weight: 4
summary: "SlimeHUD adds a WAILA (What Am I Looking At) HUD for Slimefun items. See item names, energy generation, cargo channels and network size at a glance — without breaking blocks or opening menus."
version: "Requires Enigma Slimefun4"
download: "https://github.com/Enigma-North/Enigma-Slimefun-SlimeHUD/releases"
github: "https://github.com/Enigma-North/Enigma-Slimefun-SlimeHUD"
addon: true
---

> **Requires**: [Enigma Slimefun4](https://github.com/Enigma-North/Enigma-Slimefun4-new)

**Enigma SlimeHUD** adds a WAILA (**W**hat **A**m **I** **L**ooking **A**t) HUD for Slimefun blocks. Point your crosshair at any Slimefun block to instantly see its name and additional details — no need to break it or open its menu.

## Features

- **Block name display** — shows the Slimefun item name of the block you're looking at.
- **Energy info** — displays energy generation or consumption for machines.
- **Cargo info** — shows the cargo channel of cargo nodes.
- **Network info** — displays the network size for connected components.
- **Two display modes** — bossbar or above the hotbar (configured in `config.yml`).
- **Per-player toggle** — each player can show or hide the HUD with `/slimehud toggle`.

## Commands

| Command | Description |
|---|---|
| `/slimehud toggle` | Toggle your personal HUD on or off |

## Configuration

After first launch, `plugins/SlimeHUD/config.yml` is created. Set the display mode:

```yaml
# Display mode: bossbar | hotbar
display-mode: hotbar
# Show energy information
show-energy: true
# Show cargo channel information
show-cargo: true
```

> **Note:** The bossbar supports only 7 colors compared to 16 for hotbar display.

## PlaceholderAPI

| Placeholder | Description |
|---|---|
| `%slimehud_toggle%` | Player's current toggle state (`true` / `false`) |
| `%slimehud_hud%` | Full HUD — block name and additional info |
| `%slimehud_hud_block%` | Block display name only |
| `%slimehud_hud_block_info%` | Additional information only |

## Requirements

- Spigot or its derivatives (Paper recommended)
- [Enigma Slimefun4](https://github.com/Enigma-North/Enigma-Slimefun4-new)

## Credits

- **Sefiraat** — original API design and creation.
- *InfinityLib* by Mooy1.
- *Lombok* by Project Lombok.
