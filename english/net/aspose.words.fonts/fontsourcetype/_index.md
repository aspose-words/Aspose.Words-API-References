---
title: FontSourceType Enum
linktitle: FontSourceType
articleTitle: FontSourceType
second_title: Aspose.Words for .NET
description: Discover Aspose.Words.Fonts.FontSourceType enum for efficient font source management. Optimize your document processing with flexible font options.
type: docs
weight: 3420
url: /net/aspose.words.fonts/fontsourcetype/
---
## FontSourceType enumeration

Specifies the type of font source.

```csharp
public enum FontSourceType
```

### Values

| Name | Value | Description |
| --- | --- | --- |
| FontFile | `0` | A [`FileFontSource`](../filefontsource/) object that represents single font file. |
| FontsFolder | `1` | A [`FolderFontSource`](../folderfontsource/) object that represents folder with font files. |
| MemoryFont | `2` | A [`MemoryFontSource`](../memoryfontsource/) object that represents single font in memory. |
| SystemFonts | `3` | A [`SystemFontSource`](../systemfontsource/) object that represents all fonts installed to the system. |
| FontStream | `4` | A [`StreamFontSource`](../streamfontsource/) object that represents a stream with font data. |

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

* namespace [Aspose.Words.Fonts](../../aspose.words.fonts/)
* assembly [Aspose.Words](../../)
