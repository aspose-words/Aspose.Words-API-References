---
title: StreamFontSource Class
linktitle: StreamFontSource
articleTitle: StreamFontSource
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Fonts.StreamFontSource class, your go-to solution for custom stream font sources that enhance document flexibility and design.
type: docs
weight: 3480
url: /net/aspose.words.fonts/streamfontsource/
---
## StreamFontSource class

Base class for user-defined stream font source.

To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/net/working-with-fonts/) documentation article.

```csharp
public abstract class StreamFontSource : FontSourceBase,   
```

## Properties

| Name | Description |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/streamfontsource/cachekey/) { get; } | The key of this source in the cache. |
| [IsEmbedded](../../aspose.words.fonts/streamfontsource/isembedded/) { get; } |  |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Returns the font source priority. |
| [Type](../../aspose.words.fonts/streamfontsource/type/) { get; } | Returns the type of the font source. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Called during processing of font source when an issue is detected that might result in formatting fidelity loss. |

## Methods

| Name | Description |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Returns list of fonts available via this source. |
| abstract [OpenFontDataStream](../../aspose.words.fonts/streamfontsource/openfontdatastream/)() | This method should open the stream with font data on demand. |

## Remarks

In order to use the stream font source you should create a derived class from the `StreamFontSource` and provide implementation of the [`OpenFontDataStream`](./openfontdatastream/) method.

[`OpenFontDataStream`](./openfontdatastream/) method could be called several times. For the first time it will be called when Aspose.Words scans the provided font sources to get the list of available fonts. Later it may be called if the font is used in the document to parse the font data and to embed the font data to some output formats.

`StreamFontSource` may be useful because it allows to load the font data only when it is required and not to store it in the memory for the [`FontSettings`](../fontsettings/) lifetime.

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

* class [FontSourceBase](../fontsourcebase/)
* interface [  ](../../global/%02  /)
* namespace [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assembly [Aspose.Words](../../)
