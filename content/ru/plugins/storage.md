---
title: "Enigma Storage"
weight: 2
summary: "Компактная система терминального хранения предметов для Paper/Spigot серверов Minecraft, вдохновлённая Applied Energistics 2. Добавляет Deep Storage Units огромной ёмкости, беспроводной терминал и хранение данных в SQLite."
version: "Minecraft 26.1.2 / Paper 26.1.2"
download: "https://github.com/Enigma-North/Enigma-Storage/releases"
github: "https://github.com/Enigma-North/Enigma-Storage"
---

**Enigma Storage** — плагин массового хранения предметов для Paper/Spigot, форк DeepStoragePlus, обновлённый для актуальной версии Minecraft — 26.1.2.

## Возможности

- **Deep Storage Units (DSU)** огромной ёмкости с переносимыми Storage Containers.
- **Беспроводной терминал** — управляйте DSU из любой точки мира.
- **SQLite-хранилище** — содержимое DSU сохраняется после перезапусков и миграций.
- **Пользовательские рецепты** через встроенный CustomRecipeAPI.
- **Гибкая система прав** для всех команд и функций.

## Установка

1. Скопируйте `EnigmaStorage.jar` в папку `plugins/` вашего сервера.
2. Запустите сервер, чтобы сгенерировался файл `plugins/EnigmaStorage/config.yml`.
3. Перезагрузите или перезапустите сервер.

## Команды

### Enigma Storage

| Команда | Описание |
|---|---|
| `/es items` | Список зарегистрированных предметов |
| `/es give <игрок> <предмет> <кол-во>` | Выдать предмет игроку |
| `/es give <предмет> <кол-во>` | Выдать предмет себе |
| `/es migrate` | Принудительная миграция DSU из lore в SQLite |

> Алиасы: `enigmastorage`, `dsp`

### CustomRecipeAPI

| Команда | Описание |
|---|---|
| `/crapi book` | Открыть книгу рецептов |
| `/crapi new` | Создать рецепт в игровом интерфейсе |
| `/crapi setworkbench` | Открыть редактор верстака |
| `/crapi workbench` | Просмотреть текущий рецепт верстака |
| `/crapi items` | Показать доступные рецепты |
| `/crapi give <игрок> <предмет> <кол-во>` | Выдать результат рецепта |

## Разрешения

### Enigma Storage

| Право | Описание |
|---|---|
| `enigmastorage.create` | Создавать DSU |
| `enigmastorage.adminopen` | Открывать заблокированные DSU |
| `enigmastorage.wireless` | Использовать беспроводной терминал |
| `enigmastorage.give` | Использовать `/es give` |

### CustomRecipeAPI

| Право | Описание |
|---|---|
| `crapi.command` | Использовать команду `/crapi` |
| `crapi.book` | Открывать книгу рецептов |
| `crapi.new` | Создавать рецепты в игре |
| `crapi.craft` | Крафтить пользовательские рецепты |
| `crapi.give` | Использовать `/crapi give` и `/crapi items` |

## Авторы

- **EnigmaticMP** — автор этого проекта.
- **Darkolythe** — оригинальный DeepStoragePlus и CustomRecipeAPI.

## Лицензия

Проект распространяется под [GNU GPL v3](https://github.com/Enigma-North/Enigma-Storage/blob/main/LICENSE).
