---
title: StreamFontSource.OpenFontDataStream
linktitle: OpenFontDataStream
articleTitle: OpenFontDataStream
second_title: Aspose.Words для .NET
description: Откройте для себя метод StreamFontSource OpenFontDataStream для эффективного доступа к потокам данных шрифтов по требованию, что улучшит ваш рабочий процесс проектирования.
type: docs
weight: 30
url: /ru/net/aspose.words.fonts/streamfontsource/openfontdatastream/
---
## StreamFontSource.OpenFontDataStream method

Этот метод должен открывать поток с данными шрифта по требованию.

```csharp
public abstract Stream OpenFontDataStream()
```

### Возвращаемое значение

Поток данных шрифта.

## Примечания

Поток будет закрыт после прочтения. Нет необходимости закрывать его явно.

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

* class [StreamFontSource](../)
* пространство имен [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* сборка [Aspose.Words](../../../)
