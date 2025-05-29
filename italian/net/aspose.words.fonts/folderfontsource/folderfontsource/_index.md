---
title: FolderFontSource
linktitle: FolderFontSource
articleTitle: FolderFontSource
second_title: Aspose.Words per .NET
description: Scopri il costruttore FolderFontSource per una gestione impeccabile dei font. Migliora i tuoi progetti web con un efficiente sourcing di font oggi stesso!
type: docs
weight: 10
url: /it/net/aspose.words.fonts/folderfontsource/folderfontsource/
---
## FolderFontSource(*string, bool*) {#constructor}

Ctor.

```csharp
public FolderFontSource(string folderPath, bool scanSubfolders)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| folderPath | String | Percorso alla cartella. |
| scanSubfolders | Boolean | Determina se analizzare o meno le sottocartelle. |

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

---

## FolderFontSource(*string, bool, int*) {#constructor_1}

Ctor.

```csharp
public FolderFontSource(string folderPath, bool scanSubfolders, int priority)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| folderPath | String | Percorso alla cartella. |
| scanSubfolders | Boolean | Determina se analizzare o meno le sottocartelle. |
| priority | Int32 | Priorità della sorgente del font. Vedi[`Priority`](../../fontsourcebase/priority/) descrizione della proprietà per maggiori informazioni. |

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
