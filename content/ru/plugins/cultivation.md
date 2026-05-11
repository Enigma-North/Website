---
title: "Enigma Cultivation"
weight: 3
summary: "Cultivation — аддон для Slimefun4, добавляющий множество растений, кустов и деревьев в Minecraft, а также уникальную кухню с большим выбором блюд. С помощью Display Entities растения и блоки отображаются так, как вы никогда раньше не видели."
version: "Minecraft 26.1.2 / Paper 26.1.2 / Java 21 · Требует Enigma Slimefun4"
download: "https://github.com/Repulsiveprogress/Enigma-Slimefun-Cultivation/releases"
github: "https://github.com/Repulsiveprogress/Enigma-Slimefun-Cultivation"
addon: true
---

![Cultivation](https://user-images.githubusercontent.com/20646323/231161480-7b6bd303-cec9-4555-aa40-5c502aaa031b.png)

> **Форк EnigmaticMP** — портирован на Minecraft 26.1.2 / Paper 26.1.2 / Java 21 со встроенной русской локализацией.  
> **Требует**: [Enigma Slimefun4](https://github.com/Repulsiveprogress/Enigma-Slimefun4-new)

Cultivation — аддон для Slimefun4, добавляющий множество растений, кустов и деревьев в Minecraft, а также уникальную кухню с большим выбором блюд. Благодаря Display Entities растения и блоки выглядят совершенно по-новому.

> **Примечание:** Аддон использует BLOCK_DISPLAY, ITEM_DISPLAY, TEXT_DISPLAY. Они не нагружают сервер, но некоторые плагины очистки лагов могут их удалять. Добавьте эти типы в список исключений.

![Обзор](https://user-images.githubusercontent.com/20646323/231163325-3749560b-f998-4399-8a60-a4bb5c0b6fcd.png)

## Локализация

После первого запуска создаются файлы:

```
plugins/Cultivation/config.yml
plugins/Cultivation/lang/en.yml
plugins/Cultivation/lang/ru.yml
```

Установите язык в `config.yml`:

```yaml
language: ru   # en | ru | <custom>
```

## Растения Cultivation

![Растения](https://user-images.githubusercontent.com/20646323/231164447-be56b8b1-cc92-486d-a2ec-97cec27a438d.png)

Растения — основной источник ресурсов аддона. Каждый тип растения периодически производит ванильные предметы.

- Растениям нужны **рядковые вешки** для роста.
- Два растения с двойными вешками пытаются **скрещиваться** с соседними.
- Добейтесь **10/10/10** для максимальных дропов, скорости роста и силы скрещивания.
- **90 растений** для открытия через скрещивание; Странствующие торговцы продают подсказки.

## Garden Cloche

![Garden Cloche](https://user-images.githubusercontent.com/20646323/231168642-9208af2b-d40a-4d75-8da8-c8deeed1703e.png)

Garden Cloche автоматизирует производство растений. Немного медленнее ручного сбора урожая, но работает постоянно и поддерживает Slimefun Cargo и Networks.

## Кусты Cultivation

![Кусты](https://user-images.githubusercontent.com/20646323/231167783-3749560b-f998-4399-8a60-a4bb5c0b6fcd.png)

Кусты проще растений — они не скрещиваются и не прокачиваются. Их задача — производство продуктов для кухни. Покупаются у **деревенских фермеров**.

## Деревья Cultivation

![Деревья](https://user-images.githubusercontent.com/20646323/231168164-fa57deee-e4fb-4463-9439-56b729cd4229.png)

Деревья вырастают в красивые кастомные постройки с сочными плодами. Ломание листьев даёт **20% шанс** выпадения саженца. Покупаются у **деревенских лучников**.

## Кухня

![Кухня](https://user-images.githubusercontent.com/20646323/231169938-c94116a1-2064-4cb1-85e8-2ecd14b6d61e.png)

На кухне готовятся все ваши продукты. Почти все предметы Cultivation (и большинство ванильной еды) можно:

- Нарезать / Порубить / Сварить
- Перемолоть / Обжарить / Размять

Затем из заготовок приготовить блюдо через **Выпекание** или **Финальную обработку**.

Каждая еда имеет **уникальный эффект** при употреблении длительностью **10 минут**.

## Лицензия

Форк наследует лицензию [оригинального Cultivation](https://github.com/Sefiraat/Cultivation).
