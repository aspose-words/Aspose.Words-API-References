---
title: Type
second_title: Aspose.Words for .NET API Reference
description: Returns the type of the font source.
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

* enum [FontSourceType](../../fontsourcetype)
* class [FontSourceBase](../../fontsourcebase)
* namespace [Aspose.Words.Fonts](../../fontsourcebase)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
