---
title: FileFontSource Class
linktitle: FileFontSource
articleTitle: FileFontSource
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.Fonts.FileFontSource. Easily manage TrueType font files on your system for enhanced document formatting and design flexibility.
type: docs
weight: 3270
url: /net/aspose.words.fonts/filefontsource/
---
## FileFontSource class

Represents the single TrueType font file stored in the file system.

To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/net/working-with-fonts/) documentation article.

```csharp
public class FileFontSource : FontSourceBase
```

## Constructors

| Name | Description |
| --- | --- |
| [FileFontSource](filefontsource/#constructor)(*string*) | Ctor. |
| [FileFontSource](filefontsource/#constructor_1)(*string, int*) | Ctor. |
| [FileFontSource](filefontsource/#constructor_2)(*string, int, string*) | Ctor. |

## Properties

| Name | Description |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/filefontsource/cachekey/) { get; } | The key of this source in the cache. |
| [FilePath](../../aspose.words.fonts/filefontsource/filepath/) { get; } | Path to the font file. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Returns the font source priority. |
| override [Type](../../aspose.words.fonts/filefontsource/type/) { get; } | Returns the type of the font source. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Called during processing of font source when an issue is detected that might result in formatting fidelity loss. |

## Methods

| Name | Description |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Returns list of fonts available via this source. |

## Examples

Shows how to use a font file in the local file system as a font source.

```csharp
FileFontSource fileFontSource = new FileFontSource(MyDir + "Alte DIN 1451 Mittelschrift.ttf", 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {fileFontSource});

Assert.That(fileFontSource.FilePath, Is.EqualTo(MyDir + "Alte DIN 1451 Mittelschrift.ttf"));
Assert.That(fileFontSource.Type, Is.EqualTo(FontSourceType.FontFile));
Assert.That(fileFontSource.Priority, Is.EqualTo(0));
```

### See Also

* class [FontSourceBase](../fontsourcebase/)
* namespace [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assembly [Aspose.Words](../../)
