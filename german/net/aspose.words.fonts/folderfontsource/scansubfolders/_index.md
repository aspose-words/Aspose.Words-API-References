---
title: FolderFontSource.ScanSubfolders
linktitle: ScanSubfolders
articleTitle: ScanSubfolders
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „FolderFontSource ScanSubfolders“, um die Schriftartenorganisation einfach zu verwalten, indem Sie zur Verbesserung der Effizienz das Scannen von Unterordnern auswählen.
type: docs
weight: 30
url: /de/net/aspose.words.fonts/folderfontsource/scansubfolders/
---
## FolderFontSource.ScanSubfolders property

Legt fest, ob die Unterordner gescannt werden sollen oder nicht.

```csharp
public bool ScanSubfolders { get; }
```

## Beispiele

Zeigt, wie ein lokaler Systemordner, der Schriftarten enthält, als Schriftartenquelle verwendet wird.

```csharp
// Erstellen Sie eine Schriftartquelle aus einem Ordner, der Schriftartdateien enthält.
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
