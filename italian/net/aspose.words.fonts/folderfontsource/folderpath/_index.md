---
title: FolderFontSource.FolderPath
second_title: Aspose.Words per .NET API Reference
description: FolderFontSource proprietà. Percorso della cartella.
type: docs
weight: 20
url: /it/net/aspose.words.fonts/folderfontsource/folderpath/
---
## FolderFontSource.FolderPath property

Percorso della cartella.

```csharp
public string FolderPath { get; }
```

### Esempi

Mostra come utilizzare una cartella di sistema locale che contiene i caratteri come origine dei caratteri.

```csharp
// Crea un'origine carattere da una cartella che contiene file di caratteri.
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


