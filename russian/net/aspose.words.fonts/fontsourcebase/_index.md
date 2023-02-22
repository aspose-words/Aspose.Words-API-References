---
title: Class FontSourceBase
second_title: Справочник по API Aspose.Words для .NET
description: Aspose.Words.Fonts.FontSourceBase сорт. Это абстрактный базовый класс для классов которые позволяют пользователю указывать различные источники шрифтов.
type: docs
weight: 2800
url: /ru/net/aspose.words.fonts/fontsourcebase/
---
## FontSourceBase class

Это абстрактный базовый класс для классов, которые позволяют пользователю указывать различные источники шрифтов.

```csharp
public abstract class FontSourceBase
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Возвращает приоритет источника шрифта. |
| abstract [Type](../../aspose.words.fonts/fontsourcebase/type/) { get; } | Возвращает тип источника шрифта. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Вызывается во время обработки источника шрифта при обнаружении проблемы, которая может привести к потере точности форматирования. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Возвращает список шрифтов, доступных через этот источник. |

### Примеры

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

* пространство имен [Aspose.Words.Fonts](../../aspose.words.fonts/)
* сборка [Aspose.Words](../../)


