---
title: FolderFontSource.FolderFontSource
second_title: Aspose.Words per .NET API Reference
description: FolderFontSource costruttore. Tor.
type: docs
weight: 10
url: /it/net/aspose.words.fonts/folderfontsource/folderfontsource/
---
## FolderFontSource(string, bool) {#constructor}

Tor.

```csharp
public FolderFontSource(string folderPath, bool scanSubfolders)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| folderPath | String | Percorso della cartella. |
| scanSubfolders | Boolean | Determina se scansionare o meno le sottocartelle. |

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

---

## FolderFontSource(string, bool, int) {#constructor_1}

Tor.

```csharp
public FolderFontSource(string folderPath, bool scanSubfolders, int priority)
```

| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| folderPath | String | Percorso della cartella. |
| scanSubfolders | Boolean | Determina se scansionare o meno le sottocartelle. |
| priority | Int32 | Priorità origine carattere. Vedi il[`Priority`](../../fontsourcebase/priority/) descrizione della struttura per ulteriori informazioni. |

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


