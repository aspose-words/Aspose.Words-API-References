---
title: MemoryFontSource.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words for .NET
description: Discover the MemoryFontSource Type property that reveals your font source type, enhancing your design precision and creativity. Unlock your font potential!
type: docs
weight: 40
url: /net/aspose.words.fonts/memoryfontsource/type/
---
## MemoryFontSource.Type property

Returns the type of the font source.

```csharp
public override FontSourceType Type { get; }
```

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

* enum [FontSourceType](../../fontsourcetype/)
* class [MemoryFontSource](../)
* namespace [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assembly [Aspose.Words](../../../)
