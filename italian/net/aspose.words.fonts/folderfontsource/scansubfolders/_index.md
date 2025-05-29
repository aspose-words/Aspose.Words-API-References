---
title: FolderFontSource.ScanSubfolders
linktitle: ScanSubfolders
articleTitle: ScanSubfolders
second_title: Aspose.Words per .NET
description: Scopri la proprietà FolderFontSource ScanSubfolders per gestire facilmente l'organizzazione dei font scegliendo di eseguire la scansione delle sottocartelle per una maggiore efficienza.
type: docs
weight: 30
url: /it/net/aspose.words.fonts/folderfontsource/scansubfolders/
---
## FolderFontSource.ScanSubfolders property

Determina se eseguire o meno la scansione delle sottocartelle.

```csharp
public bool ScanSubfolders { get; }
```

## Esempi

Mostra come utilizzare una cartella di sistema locale contenente i font come origine dei font.

```csharp
// Crea una sorgente font da una cartella che contiene file font.
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
* spazio dei nomi [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* assemblea [Aspose.Words](../../../)
