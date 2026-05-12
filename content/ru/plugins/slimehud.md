---
title: "Enigma SlimeHUD"
weight: 4
summary: "SlimeHUD добавляет WAILA-HUD (What Am I Looking At) для блоков Slimefun. Смотрите название предмета, генерацию энергии, канал карго и размер сети с первого взгляда — без взлома блоков и открытия меню."
version: "Требует Enigma Slimefun4"
download: "https://github.com/Enigma-North/Enigma-Slimefun-SlimeHUD/releases"
github: "https://github.com/Enigma-North/Enigma-Slimefun-SlimeHUD"
addon: true
---

> **Требует**: [Enigma Slimefun4](https://github.com/Enigma-North/Enigma-Slimefun4-new)

**Enigma SlimeHUD** добавляет WAILA (**W**hat **A**m **I** **L**ooking **A**t) HUD для блоков Slimefun. Наведите прицел на любой блок Slimefun — и сразу увидите его название и дополнительную информацию, не ломая блок и не открывая меню.

## Возможности

- **Название блока** — отображает название предмета Slimefun, на который вы смотрите.
- **Информация об энергии** — показывает генерацию или потребление энергии для машин.
- **Информация о карго** — отображает канал карго-узлов.
- **Информация о сети** — показывает размер сети для подключённых компонентов.
- **Два режима отображения** — боссбар или над хотбаром (настраивается в `config.yml`).
- **Индивидуальное переключение** — каждый игрок может включить или выключить HUD командой `/slimehud toggle`.

## Команды

| Команда | Описание |
|---|---|
| `/slimehud toggle` | Включить или выключить свой HUD |

## Конфигурация

После первого запуска создаётся `plugins/SlimeHUD/config.yml`. Выберите режим отображения:

```yaml
# Режим отображения: bossbar | hotbar
display-mode: hotbar
# Показывать информацию об энергии
show-energy: true
# Показывать информацию о канале карго
show-cargo: true
```

> **Примечание:** Боссбар поддерживает только 7 цветов против 16 у хотбара.

## PlaceholderAPI

| Плейсхолдер | Описание |
|---|---|
| `%slimehud_toggle%` | Текущее состояние переключателя игрока (`true` / `false`) |
| `%slimehud_hud%` | Полный HUD — название блока и дополнительная информация |
| `%slimehud_hud_block%` | Только название блока |
| `%slimehud_hud_block_info%` | Только дополнительная информация |

## Требования

- Spigot или его производные (рекомендуется Paper)
- [Enigma Slimefun4](https://github.com/Enigma-North/Enigma-Slimefun4-new)

## Авторы

- **Sefiraat** — оригинальный дизайн и создание API.
- *InfinityLib* by Mooy1.
- *Lombok* by Project Lombok.
