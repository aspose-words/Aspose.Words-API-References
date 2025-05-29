---
title: FolderFontSource.FolderPath
linktitle: FolderPath
articleTitle: FolderPath
second_title: Aspose.Words per .NET
description: Scopri la proprietà FolderFontSource FolderPath per accedere facilmente alla cartella dei tuoi font. Semplifica il tuo flusso di lavoro di progettazione oggi stesso!
type: docs
weight: 20
url: /it/net/aspose.words.fonts/folderfontsource/folderpath/
---
## FolderFontSource.FolderPath property

Percorso della cartella.

```csharp
public string FolderPath { get; }
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
