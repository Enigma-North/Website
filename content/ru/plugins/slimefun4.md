---
title: "Enigma Slimefun4"
weight: 1
summary: "Slimefun — плагин, который превращает ванильный Minecraft-сервер в опыт, похожий на модпак, без установки модов. Более 500 новых предметов и рецептов: от рюкзаков и джетпаков до ядерных реакторов, магических алтарей, энергосетей и систем транспортировки предметов."
version: "Minecraft 26.1.2 / Paper 26.1.2 / Java 25"
download: "https://github.com/Enigma-North/Enigma-Slimefun4-new/releases"
github: "https://github.com/Enigma-North/Enigma-Slimefun4-new"
---

Это **неофициальный форк Slimefun 4**, портированный на Paper 26.1.2 / Java 25.

> Форк не является официальным релизом Slimefun, не поддерживается командой Slimefun и **не принимает баг-репорты в оригинальный репозиторий**. Все проблемы следует сообщать только в этом репозитории.

## Что это такое

Slimefun — плагин, превращающий ванильный Minecraft-сервер в опыт, похожий на модпак, без установки модов. Более **500 новых предметов и рецептов**: от рюкзаков и джетпаков до ядерных реакторов, магических алтарей, энергосетей и систем транспортировки предметов.

Форк создан для работы плагина на актуальной версии Minecraft.

## Совместимость

| | Этот форк | Оригинальный Slimefun |
|---|---|---|
| **Minecraft** | 26.1.2 | 1.16 – 1.21 |
| **Сервер** | Paper 26.1.2 | Paper / Spigot |
| **Java** | **Java 25** | Java 16+ |

> Minecraft 26.1 — первая версия, использующая новую схему версионирования Mojang `YY.D.H`, и первая, требующая **Java 25**. Работа на Java 21 и ниже невозможна.

## Установка

1. Установите Paper 26.1.2 и убедитесь, что сервер запускается на Java 25.
2. Скачайте `.jar` из [Releases](https://github.com/Enigma-North/Enigma-Slimefun4-new/releases).
3. Поместите `.jar` в папку `plugins/` сервера.
4. Запустите сервер — файлы конфигурации создадутся в `plugins/Slimefun/`.

## Сборка из исходников

Требования: JDK 25, Maven 3.9+

```bash
git clone https://github.com/Enigma-North/Enigma-Slimefun4-new
cd Enigma-Slimefun4-new
mvn clean package
```

Готовый `.jar` будет в `target/Slimefun v4.9-UNOFFICIAL.jar`.

## Отличия от оригинала

- Совместимость с Paper 26.1.2 (Mojang mappings, новый формат `api-version`).
- Java 25 как цель компиляции (ранее Java 16/17).
- Обновлённые зависимости для нового Paper API.
- Исправления кода для breaking changes в Paper API между 1.21 и 26.1.

Никаких изменений в геймплее, рецептах и балансе — это исключительно технический порт.

## Лицензия

Slimefun 4 лицензирован под [GNU GPLv3](https://github.com/Enigma-North/Enigma-Slimefun4-new/blob/master/LICENSE).  
Оригинальный проект: [Slimefun/Slimefun4](https://github.com/Slimefun/Slimefun4)
