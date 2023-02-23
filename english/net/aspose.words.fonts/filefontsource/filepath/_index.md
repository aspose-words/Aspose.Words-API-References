---
title: FileFontSource.FilePath
linktitle: FilePath
second_title: Aspose.Words for .NET API Reference
description: FileFontSource property. Path to the font file in C#.
type: docs
weight: 30
url: /net/aspose.words.fonts/filefontsource/filepath/
---
## FileFontSource.FilePath property

Path to the font file.

```csharp
public string FilePath { get; }
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

* class [FileFontSource](../)
* namespace [Aspose.Words.Fonts](../../filefontsource/)
* assembly [Aspose.Words](../../../)
