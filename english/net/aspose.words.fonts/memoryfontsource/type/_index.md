---
title: Type
second_title: Aspose.Words for .NET API Reference
description: MemoryFontSource property. Returns the type of the font source in C#.
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

Assert.AreEqual(FontSourceType.MemoryFont, memoryFontSource.Type);
Assert.AreEqual(0, memoryFontSource.Priority);
```

### See Also

* enum [FontSourceType](../../fontsourcetype/)
* class [MemoryFontSource](../)
* namespace [Aspose.Words.Fonts](../../memoryfontsource/)
* assembly [Aspose.Words](../../../)
