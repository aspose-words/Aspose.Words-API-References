---
title: FolderFontSource.ScanSubfolders
second_title: Aspose.Words für .NET-API-Referenz
description: FolderFontSource eigendom. Legt fest ob die Unterordner gescannt werden sollen oder nicht.
type: docs
weight: 30
url: /de/net/aspose.words.fonts/folderfontsource/scansubfolders/
---
## FolderFontSource.ScanSubfolders property

Legt fest, ob die Unterordner gescannt werden sollen oder nicht.

```csharp
public bool ScanSubfolders { get; }
```

### Beispiele

Zeigt, wie ein lokaler Systemordner, der Schriftarten enthält, als Schriftartquelle verwendet wird.

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
* namensraum [Aspose.Words.Fonts](../../folderfontsource/)
* Montage [Aspose.Words](../../../)


