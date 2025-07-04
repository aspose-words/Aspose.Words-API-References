---
title: FolderFontSource.ScanSubfolders
linktitle: ScanSubfolders
articleTitle: ScanSubfolders
second_title: Aspose.Words for .NET
description: Discover the FolderFontSource ScanSubfolders property to easily manage font organization by choosing to scan subfolders for enhanced efficiency.
type: docs
weight: 30
url: /net/aspose.words.fonts/folderfontsource/scansubfolders/
---
## FolderFontSource.ScanSubfolders property

Determines whether or not to scan the subfolders.

```csharp
public bool ScanSubfolders { get; }
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

* class [FolderFontSource](../)
* namespace [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assembly [Aspose.Words](../../../)
