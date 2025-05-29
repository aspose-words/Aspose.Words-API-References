---
title: FolderFontSource.Type
linktitle: Type
articleTitle: Type
second_title: Aspose.Words für .NET
description: Entdecken Sie die Eigenschaft „FolderFontSourceType“. Identifizieren Sie mühelos Schriftarten, um Ihre Designprojekte zu verbessern und Ihren Workflow zu optimieren.
type: docs
weight: 40
url: /de/net/aspose.words.fonts/folderfontsource/type/
---
## FolderFontSource.Type property

Gibt den Typ der Schriftartquelle zurück.

```csharp
public override FontSourceType Type { get; }
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

* enum [FontSourceType](../../fontsourcetype/)
* class [FolderFontSource](../)
* namensraum [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* Montage [Aspose.Words](../../../)
