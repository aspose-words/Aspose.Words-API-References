---
title: MemoryFontSource.FontData
linktitle: FontData
articleTitle: FontData
second_title: Aspose.Words for .NET
description: Discover MemoryFontSource's FontData property for seamless binary font integration. Enhance your projects with efficient font management solutions.
type: docs
weight: 30
url: /net/aspose.words.fonts/memoryfontsource/fontdata/
---
## MemoryFontSource.FontData property

Binary font data.

```csharp
public byte[] FontData { get; }
```

## Examples

Shows how to use a byte array with data from a font file as a font source.

```csharp
byte[] fontBytes = File.ReadAllBytes(MyDir + "Alte DIN 1451 Mittelschrift.ttf");
MemoryFontSource memoryFontSource = new MemoryFontSource(fontBytes, 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {memoryFontSource});

Assert.AreEqual(FontSourceType.MemoryFont, memoryFontSource.Type);
Assert.AreEqual(0, memoryFontSource.Priority);
```

### See Also

* class [MemoryFontSource](../)
* namespace [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assembly [Aspose.Words](../../../)
