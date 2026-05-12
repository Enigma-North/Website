---
title: "Enigma Cultivation"
weight: 3
summary: "Cultivation is a Slimefun4 addon that adds a plethora of plants, bushes and trees to Minecraft as well as an amazing food selection made via a unique, fully featured kitchen! Using Display Entities, plants and blocks are displayed like you've never seen before."
version: "Minecraft 26.1.2 / Paper 26.1.2 / Java 21 · Requires Enigma Slimefun4"
download: "https://github.com/Enigma-North/Enigma-Slimefun-Cultivation/releases"
github: "https://github.com/Enigma-North/Enigma-Slimefun-Cultivation"
addon: true
---

![Cultivation](https://user-images.githubusercontent.com/20646323/231161480-7b6bd303-cec9-4555-aa40-5c502aaa031b.png)

> **EnigmaticMP Fork** — ported to Minecraft 26.1.2 / Paper 26.1.2 / Java 21 with built-in Russian localisation.  
> **Requires**: [Enigma Slimefun4](https://github.com/Enigma-North/Enigma-Slimefun4-new)

Cultivation is a Slimefun4 addon that adds a plethora of plants, bushes and trees to Minecraft as well as an amazing food selection to be made via a unique, fully featured kitchen! Using Display Entities we are able to display plants and blocks like you've never seen before.

> **Note on Display Entities:** This addon uses BLOCK_DISPLAY, ITEM_DISPLAY and TEXT_DISPLAY entities. They add no performance overhead, but some lag-clearing plugins may remove them. Add these entity types to your exclusion list to avoid errors.

![Overview](https://user-images.githubusercontent.com/20646323/231163325-3749560b-f998-4399-8a60-a4bb5c0b6fcd.png)

## Localisation

After first launch, the following files are created:

```
plugins/Cultivation/config.yml
plugins/Cultivation/lang/en.yml
plugins/Cultivation/lang/ru.yml
```

Set your language in `config.yml`:

```yaml
language: ru   # en | ru | <custom>
```

**Adding a community translation:** copy `lang/en.yml` to `lang/<code>.yml`, translate the values, set `language: <code>` and restart. Missing keys fall back to English automatically.

## Cultivation Plants

![Plants](https://user-images.githubusercontent.com/20646323/231164447-be56b8b1-cc92-486d-a2ec-97cec27a438d.png)

Plants are Cultivation's resource-generating flora. Each plant type grows vanilla Minecraft items periodically.

- Plants require **crop sticks** to grow.
- Double crop-sticked plants attempt to **breed** with nearby plants.
- Breeding produces a new plant type or a stronger version of the parent plants.
- Try to reach **10/10/10** on a plant for maximum drops, growth speed and breed strength.
- **90 plants** to discover via breeding; Wandering Traders sell documents with breeding hints.

## Garden Cloche

![Garden Cloche](https://user-images.githubusercontent.com/20646323/231168642-9208af2b-d40a-4d75-8da8-c8deeed1703e.png)

The Garden Cloche automates the production of Cultivation Plants. Slightly slower than manual harvesting, it produces constantly and supports Slimefun Cargo and Networks access.

## Cultivation Bushes

![Bushes](https://user-images.githubusercontent.com/20646323/231167783-3749560b-f998-4399-8a60-a4bb5c0b6fcd.png)

Bushes are simpler than plants — they don't breed or level up. Their sole purpose is producing foodstuffs ("Produce") that can be used in the kitchen. Bushes are purchased from **Farmer villagers**.

## Cultivation Trees

![Trees](https://user-images.githubusercontent.com/20646323/231168164-fa57deee-e4fb-4463-9439-56b729cd4229.png)

Trees grow into beautiful, custom-built structures bearing ripe fruits. Fruits can be used in cooking and smoothie making. Breaking a tree's leaves has a **20% chance** to drop a sapling. Trees are purchased from **Fletching Villagers**.

## The Kitchen

![Kitchen](https://user-images.githubusercontent.com/20646323/231169938-c94116a1-2064-4cb1-85e8-2ecd14b6d61e.png)

The Kitchen is where you cook all your wonderful produce. Nearly all Cultivation products (and most vanilla foods) can be:

- Chopped / Sliced / Boiled
- Blended / Ground
- Fried / Mashed

Then combine by-products into a meal via **Oven Cooking / Baking** or **Finishing**.

Each food item has a **custom effect** when eaten. Most effects last for **10 minutes** and prevent eating again during that time.

## License

This fork inherits the license from the [original Cultivation](https://github.com/Sefiraat/Cultivation).
