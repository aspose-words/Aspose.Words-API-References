---
title: MemoryFontSource Class
linktitle: MemoryFontSource
articleTitle: MemoryFontSource
second_title: Aspose.Words для .NET
description: Aspose.Words.Fonts.MemoryFontSource сорт. Представляет один файл шрифта TrueType хранящийся в памяти на С#.
type: docs
weight: 3020
url: /ru/net/aspose.words.fonts/memoryfontsource/
---
## MemoryFontSource class

Представляет один файл шрифта TrueType, хранящийся в памяти.

Чтобы узнать больше, посетите[Работа со шрифтами](https://docs.aspose.com/words/net/working-with-fonts/) статья документации.

```csharp
public class MemoryFontSource : FontSourceBase
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [MemoryFontSource](memoryfontsource/#constructor)(*byte[]*) | Cтор. |
| [MemoryFontSource](memoryfontsource/#constructor_1)(*byte[], int*) | Cтор. |
| [MemoryFontSource](memoryfontsource/#constructor_2)(*byte[], int, string*) | Cтор. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/memoryfontsource/cachekey/) { get; } | Ключ этого источника в кеше. |
| [FontData](../../aspose.words.fonts/memoryfontsource/fontdata/) { get; } | Двоичные данные шрифта. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Возвращает приоритет источника шрифта. |
| override [Type](../../aspose.words.fonts/memoryfontsource/type/) { get; } | Возвращает тип источника шрифта. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Вызывается во время обработки источника шрифта при обнаружении проблемы, которая может привести к потере точности форматирования. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Возвращает список шрифтов, доступных через этот источник. |

## Примеры

Показывает, как использовать массив байтов с данными из файла шрифта в качестве источника шрифта.

```csharp
byte[] fontBytes = File.ReadAllBytes(MyDir + "Alte DIN 1451 Mittelschrift.ttf");
MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {memoryFontSource});

Assert.AreEqual(FontSourceType.MemoryFont, memoryFontSource.Type);
Assert.AreEqual(0, memoryFontSource.Priority);
```

### Смотрите также

* class [FontSourceBase](../fontsourcebase/)
* пространство имен [Aspose.Words.Fonts](../../aspose.words.fonts/)
* сборка [Aspose.Words](../../)
