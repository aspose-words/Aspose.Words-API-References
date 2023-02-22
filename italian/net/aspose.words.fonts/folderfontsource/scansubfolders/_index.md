---
title: FolderFontSource.ScanSubfolders
second_title: Aspose.Words per .NET API Reference
description: FolderFontSource proprietà. Determina se scansionare o meno le sottocartelle.
type: docs
weight: 30
url: /it/net/aspose.words.fonts/folderfontsource/scansubfolders/
---
## FolderFontSource.ScanSubfolders property

Determina se scansionare o meno le sottocartelle.

```csharp
public bool ScanSubfolders { get; }
```

### Esempi

Mostra come utilizzare una cartella di sistema locale che contiene i caratteri come origine dei caratteri.

```csharp
// Crea una fonte di font da una cartella che contiene file di font.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false, 1);

Document doc = new Document();
doc.FontSettings = new FontSettings();
doc.FontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

Assert.AreEqual(FontsDir, folderFontSource.FolderPath);
Assert.AreEqual(false, folderFontSource.ScanSubfolders);
Assert.AreEqual(FontSourceType.FontsFolder, folderFontSource.Type);
Assert.AreEqual(1, folderFontSource.Priority);
```

### Guarda anche

* class [FolderFontSource](../)
* spazio dei nomi [Aspose.Words.Fonts](../../folderfontsource/)
* assemblea [Aspose.Words](../../../)


