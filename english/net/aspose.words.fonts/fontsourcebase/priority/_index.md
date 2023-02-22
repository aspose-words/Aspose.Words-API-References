---
title: Priority
second_title: Aspose.Words for .NET API Reference
description: FontSourceBase property. Returns the font source priority in C#.
type: docs
weight: 10
url: /net/aspose.words.fonts/fontsourcebase/priority/
---
## FontSourceBase.Priority property

Returns the font source priority.

```csharp
public int Priority { get; }
```

## Remarks

This value is used when there are fonts with the same family name and style in different font sources. In this case Aspose.Words selects the font from the source with the higher priority value.

The default value is 0.

## Examples

Shows how to use a font file in the local file system as a font source.

```csharp
FileFontSource fileFontSource = new FileFontSource(MyDir + "Alte DIN 1451 Mittelschrift.ttf", 0);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {fileFontSource});

Assert.AreEqual(MyDir + "Alte DIN 1451 Mittelschrift.ttf", fileFontSource.FilePath);
Assert.AreEqual(FontSourceType.FontFile, fileFontSource.Type);
Assert.AreEqual(0, fileFontSource.Priority);
```

### See Also

* class [FontSourceBase](../)
* namespace [Aspose.Words.Fonts](../../fontsourcebase/)
* assembly [Aspose.Words](../../../)
