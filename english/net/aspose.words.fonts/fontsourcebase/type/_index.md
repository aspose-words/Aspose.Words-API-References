---
title: FontSourceBase.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words for .NET
description: Discover the FontSourceBase Type property: easily retrieve font source types to enhance your web design and optimize user experience.
type: docs
weight: 20
url: /net/aspose.words.fonts/fontsourcebase/type/
---
## FontSourceBase.Type property

Returns the type of the font source.

```csharp
public abstract FontSourceType Type { get; }
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
* class [FontSourceBase](../)
* namespace [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assembly [Aspose.Words](../../../)
