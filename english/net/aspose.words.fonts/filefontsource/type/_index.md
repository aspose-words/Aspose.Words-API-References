---
title: FileFontSource.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words for .NET
description: Discover the FileFontSource Type property to easily identify font source types, enhancing your design projects with precise typography solutions.
type: docs
weight: 40
url: /net/aspose.words.fonts/filefontsource/type/
---
## FileFontSource.Type property

Returns the type of the font source.

```csharp
public override FontSourceType Type { get; }
```

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

* enum [FontSourceType](../../fontsourcetype/)
* class [FileFontSource](../)
* namespace [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assembly [Aspose.Words](../../../)
