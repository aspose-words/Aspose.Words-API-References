---
title: FontSourceBase Class
linktitle: FontSourceBase
articleTitle: FontSourceBase
second_title: Aspose.Words для .NET
description: Откройте для себя Aspose.Words.Fonts.FontSourceBase, необходимый абстрактный класс для определения различных источников шрифтов в ваших приложениях. Улучшите форматирование ваших документов!
type: docs
weight: 3410
url: /ru/net/aspose.words.fonts/fontsourcebase/
---
## FontSourceBase class

Это абстрактный базовый класс для классов, которые позволяют пользователю указывать различные источники шрифтов.

Чтобы узнать больше, посетите[Работа со шрифтами](https://docs.aspose.com/words/net/working-with-fonts/) документальная статья.

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

* пространство имен [Aspose.Words.Fonts](../../aspose.words.fonts/)
* сборка [Aspose.Words](../../)
