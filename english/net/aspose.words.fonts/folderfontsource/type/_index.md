---
title: FolderFontSource.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words for .NET
description: Discover the FolderFontSource Type property. Easily identify font source types to enhance your design projects and streamline your workflow.
type: docs
weight: 40
url: /net/aspose.words.fonts/folderfontsource/type/
---
## FolderFontSource.Type property

Returns the type of the font source.

```csharp
public override FontSourceType Type { get; }
```

## Examples

Shows how to use a local system folder which contains fonts as a font source.

```csharp
// Create a font source from a folder that contains font files.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false, 1);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

Assert.That(folderFontSource.FolderPath, Is.EqualTo(FontsDir));
Assert.That(folderFontSource.ScanSubfolders, Is.EqualTo(false));
Assert.That(folderFontSource.Type, Is.EqualTo(FontSourceType.FontsFolder));
Assert.That(folderFontSource.Priority, Is.EqualTo(1));
```

### See Also

* enum [FontSourceType](../../fontsourcetype/)
* class [FolderFontSource](../)
* namespace [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assembly [Aspose.Words](../../../)
