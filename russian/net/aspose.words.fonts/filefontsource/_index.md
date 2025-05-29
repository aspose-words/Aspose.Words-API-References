---
title: FileFontSource Class
linktitle: FileFontSource
articleTitle: FileFontSource
second_title: Aspose.Words для .NET
description: Откройте для себя Aspose.Words.Fonts.FileFontSource. Легко управляйте файлами шрифтов TrueType в вашей системе для улучшенного форматирования документов и гибкости дизайна.
type: docs
weight: 3280
url: /ru/net/aspose.words.fonts/filefontsource/
---
## FileFontSource class

Представляет один файл шрифта TrueType, хранящийся в файловой системе.

Чтобы узнать больше, посетите[Работа со шрифтами](https://docs.aspose.com/words/net/working-with-fonts/) документальная статья.

```csharp
public class FileFontSource : FontSourceBase
```

## Конструкторы

| Имя | Описание |
| --- | --- |
| [FileFontSource](filefontsource/#constructor)(*string*) | Ctor. |
| [FileFontSource](filefontsource/#constructor_1)(*string, int*) | Ctor. |
| [FileFontSource](filefontsource/#constructor_2)(*string, int, string*) | Ctor. |

## Характеристики

| Имя | Описание |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/filefontsource/cachekey/) { get; } | Ключ этого источника в кэше. |
| [FilePath](../../aspose.words.fonts/filefontsource/filepath/) { get; } | Путь к файлу шрифта. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Возвращает приоритет источника шрифта. |
| override [Type](../../aspose.words.fonts/filefontsource/type/) { get; } | Возвращает тип источника шрифта. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Вызывается во время обработки источника шрифта при обнаружении проблемы, которая может привести к потере точности форматирования. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Возвращает список шрифтов, доступных через этот источник. |

## Примеры

Показывает, как использовать файл шрифта в локальной файловой системе в качестве источника шрифта.

```csharp
FileFontSource fileFontSource = new FileFontSource(MyDir + "Alte DIN 1451 Mittelschrift.ttf", 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {fileFontSource});

Assert.AreEqual(MyDir + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.FilePath);
Assert.AreEqual(FontSourceType.FontFile, fileFontSource.Type);
Assert.AreEqual(0, fileFontSource.Priority);
```

### Смотрите также

* class [FontSourceBase](../fontsourcebase/)
* пространство имен [Aspose.Words.Fonts](../../aspose.words.fonts/)
* сборка [Aspose.Words](../../)
