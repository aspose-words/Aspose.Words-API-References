---
title: FolderFontSource.FolderPath
linktitle: FolderPath
articleTitle: FolderPath
second_title: Aspose.Words für .NET
description: FolderFontSource FolderPath eigendom. Pfad zum Ordner in C#.
type: docs
weight: 20
url: /de/net/aspose.words.fonts/folderfontsource/folderpath/
---
## FolderFontSource.FolderPath property

Pfad zum Ordner.

```csharp
public string FolderPath { get; }
```

## Beispiele

Zeigt, wie ein lokaler Systemordner, der Schriftarten enthält, als Schriftartenquelle verwendet wird.

```csharp
// Erstellen Sie eine Schriftartenquelle aus einem Ordner, der Schriftartendateien enthält.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false, 1);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

Assert.AreEqual(FontsDir, folderFontSource.FolderPath);
Assert.AreEqual(false, folderFontSource.ScanSubfolders);
Assert.AreEqual(FontSourceType.FontsFolder, folderFontSource.Type);
Assert.AreEqual(1, folderFontSource.Priority);
```

### Siehe auch

* class [FolderFontSource](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
