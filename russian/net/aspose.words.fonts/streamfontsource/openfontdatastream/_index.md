---
title: StreamFontSource.OpenFontDataStream
second_title: Справочник по API Aspose.Words для .NET
description: StreamFontSource метод. Этот метод должен открывать поток с данными шрифта по запросу.
type: docs
weight: 30
url: /ru/net/aspose.words.fonts/streamfontsource/openfontdatastream/
---
## StreamFontSource.OpenFontDataStream method

Этот метод должен открывать поток с данными шрифта по запросу.

```csharp
public abstract Stream OpenFontDataStream()
```

### Возвращаемое значение

Поток данных шрифта.

### Примечания

Поток будет закрыт после чтения. Нет необходимости закрывать его явно.

### Примеры

Показывает, как загружать шрифты из потока.

```csharp
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
/// Загружаем данные шрифта только при необходимости, а не сохраняем их в памяти
/// на все время жизни объекта FontSettings.
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
* пространство имен [Aspose.Words.Fonts](../../streamfontsource/)
* сборка [Aspose.Words](../../../)


