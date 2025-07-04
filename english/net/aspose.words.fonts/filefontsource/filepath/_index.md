---
title: FileFontSource.FilePath
linktitle: FilePath
articleTitle: FilePath
second_title: Aspose.Words for .NET
description: Discover the FileFontSource FilePath property for easy access to your font files. Streamline your design process with this essential tool!
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

Assert.That(fileFontSource.FilePath, Is.EqualTo(MyDir + "Alte DIN 1451 Mittelschrift.ttf"));
Assert.That(fileFontSource.Type, Is.EqualTo(FontSourceType.FontFile));
Assert.That(fileFontSource.Priority, Is.EqualTo(0));
```

### See Also

* class [FileFontSource](../)
* namespace [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assembly [Aspose.Words](../../../)
