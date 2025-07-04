---
title: MemoryFontSource Class
linktitle: MemoryFontSource
articleTitle: MemoryFontSource
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Fonts.MemoryFontSource class, enabling seamless access to TrueType fonts stored in memory for enhanced document processing.
type: docs
weight: 3440
url: /net/aspose.words.fonts/memoryfontsource/
---
## MemoryFontSource class

Represents the single TrueType font file stored in memory.

To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/net/working-with-fonts/) documentation article.

```csharp
public class MemoryFontSource : FontSourceBase
```

## Constructors

| Name | Description |
| --- | --- |
| [MemoryFontSource](memoryfontsource/#constructor)(*byte[]*) | Ctor. |
| [MemoryFontSource](memoryfontsource/#constructor_1)(*byte[], int*) | Ctor. |
| [MemoryFontSource](memoryfontsource/#constructor_2)(*byte[], int, string*) | Ctor. |

## Properties

| Name | Description |
| --- | --- |
| [CacheKey](../../aspose.words.fonts/memoryfontsource/cachekey/) { get; } | The key of this source in the cache. |
| [FontData](../../aspose.words.fonts/memoryfontsource/fontdata/) { get; } | Binary font data. |
| [Priority](../../aspose.words.fonts/fontsourcebase/priority/) { get; } | Returns the font source priority. |
| override [Type](../../aspose.words.fonts/memoryfontsource/type/) { get; } | Returns the type of the font source. |
| [WarningCallback](../../aspose.words.fonts/fontsourcebase/warningcallback/) { get; set; } | Called during processing of font source when an issue is detected that might result in formatting fidelity loss. |

## Methods

| Name | Description |
| --- | --- |
| [GetAvailableFonts](../../aspose.words.fonts/fontsourcebase/getavailablefonts/)() | Returns list of fonts available via this source. |

## Examples

Shows how to use a byte array with data from a font file as a font source.

```csharp
byte[] fontBytes = File.ReadAllBytes(MyDir + "Alte DIN 1451 Mittelschrift.ttf");
MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {memoryFontSource});

Assert.That(memoryFontSource.Type, Is.EqualTo(FontSourceType.MemoryFont));
Assert.That(memoryFontSource.Priority, Is.EqualTo(0));
```

### See Also

* class [FontSourceBase](../fontsourcebase/)
* namespace [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assembly [Aspose.Words](../../)
