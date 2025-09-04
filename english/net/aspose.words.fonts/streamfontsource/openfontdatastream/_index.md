---
title: StreamFontSource.OpenFontDataStream
linktitle: OpenFontDataStream
articleTitle: OpenFontDataStream
second_title: Aspose.Words for .NET
description: Discover the StreamFontSource OpenFontDataStream method to efficiently access font data streams on demand, enhancing your design workflow.
type: docs
weight: 40
url: /net/aspose.words.fonts/streamfontsource/openfontdatastream/
---
## StreamFontSource.OpenFontDataStream method

This method should open the stream with font data on demand.

```csharp
public abstract Stream OpenFontDataStream()
```

### Return Value

Font data stream.

## Remarks

The stream will be closed after reading. There is no need to close it explicitly.

## Examples

Shows how to load fonts from stream.

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
/// Load the font data only when required instead of storing it in the memory
/// for the entire lifetime of the "FontSettings" object.
/// </summary>
private class StreamFontSourceFile : StreamFontSource
{
    public override Stream OpenFontDataStream()
    {
        return File.OpenRead(FontsDir + "Kreon-Regular.ttf");
    }
}
```

### See Also

* class [StreamFontSource](../)
* namespace [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assembly [Aspose.Words](../../../)
