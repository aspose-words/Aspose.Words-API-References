---
title: StreamFontSource Class
linktitle: StreamFontSource
articleTitle: StreamFontSource
second_title: Aspose.Words для .NET
description: Откройте для себя класс Aspose.Words.Fonts.StreamFontSource — ваше идеальное решение для создания пользовательских потоковых источников шрифтов, повышающих гибкость и дизайн документов.
type: docs
weight: 3470
url: /ru/net/aspose.words.fonts/streamfontsource/
---
## StreamFontSource class

Базовый класс для определяемого пользователем источника потокового шрифта.

Чтобы узнать больше, посетите[Работа со шрифтами](https://docs.aspose.com/words/net/working-with-fonts/) документальная статья.

```csharp
public abstract class StreamFontSource : FontSourceBase,   
```

## Характеристики

| Имя | Описание |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/streamfontsource/cachekey/) { get; } | Ключ этого источника в кэше. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Возвращает приоритет источника шрифта. |
| [Type](../../aspose.words.fonts/streamfontsource/type/) { get; } | Возвращает тип источника шрифта. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Вызывается во время обработки источника шрифта при обнаружении проблемы, которая может привести к потере точности форматирования. |

## Методы

| Имя | Описание |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Возвращает список шрифтов, доступных через этот источник. |
| abstract [OpenFontDataStream](../../aspose.words.fonts/streamfontsource/openfontdatastream/)() | Этот метод должен открывать поток с данными шрифта по требованию. |

## Примечания

Для использования потокового источника шрифта необходимо создать производный класс от`StreamFontSource` и обеспечить реализацию[`OpenFontDataStream`](./openfontdatastream/) метод.

[`OpenFontDataStream`](./openfontdatastream/)Метод может быть вызван несколько раз. В первый раз он будет вызван , когда Aspose.Words сканирует предоставленные источники шрифтов, чтобы получить список доступных шрифтов. Позже он может быть вызван, если шрифт используется в документе для анализа данных шрифта и внедрения данных шрифта в некоторые выходные форматы.

`StreamFontSource` может быть полезным, поскольку позволяет загружать данные шрифта только тогда, когда это необходимо , а не сохранять их в памяти для[`FontSettings`](../fontsettings/) продолжительность жизни.

## Примеры

Показывает, как загружать шрифты из потока.

```csharp
public void StreamFontSourceFileRendering()
{
    FontSettings fontSettings = new FontSettings();
    fontSettings.SetFontsSources(new FontSourceBase[] {new StreamFontSourceFile()});

    DocumentBuilder builder = new DocumentBuilder();
    builder.Document.FontSettings = fontSettings;
    builder.Font.Name = "Kreon-Regular";
    builder.Writeln("Test aspose text when saving to PDF.");

    builder.Document.Save(ArtifactsDir + "FontSettings.StreamFontSourceFileRendering.pdf");
}

/// <summary>
/// Загружать данные шрифта только при необходимости, а не сохранять их в памяти
/// на все время существования объекта "FontSettings".
/// </summary>
private class StreamFontSourceFile : StreamFontSource
{
    public override Stream OpenFontDataStream()
    {
        return File.OpenRead(FontsDir + "Kreon-Regular.ttf");
    }
}
```

### Смотрите также

* class [FontSourceBase](../fontsourcebase/)
* interface [  ](../../global/%02  /)
* пространство имен [Aspose.Words.Fonts](../../aspose.words.fonts/)
* сборка [Aspose.Words](../../)
