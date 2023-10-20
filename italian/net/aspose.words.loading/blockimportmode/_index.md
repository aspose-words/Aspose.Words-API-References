---
title: BlockImportMode Enum
linktitle: BlockImportMode
articleTitle: BlockImportMode
second_title: Aspose.Words per .NET
description: Aspose.Words.Loading.BlockImportMode enum. Specifica il modo in cui le proprietà degli elementi a livello di blocco vengono importate da documenti basati su HTML in C#.
type: docs
weight: 3560
url: /it/net/aspose.words.loading/blockimportmode/
---
## BlockImportMode enumeration

Specifica il modo in cui le proprietà degli elementi a livello di blocco vengono importate da documenti basati su HTML.

```csharp
public enum BlockImportMode
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| Merge | `0` | Le proprietà dei blocchi principali vengono unite e archiviate negli elementi secondari (ad esempio paragrafi o tabelle). |
| Preserve | `1` | Le proprietà dei blocchi genitori vengono importate in una struttura logica speciale e vengono archiviate separatamente dai nodi del documento. |

## Esempi

Mostra come le proprietà degli elementi a livello di blocco vengono importate da documenti basati su HTML.

```csharp
const string html = @"
<html>
    <div style='border:dotted'>
        <div style='border:solid'>
            <p>paragraph 1</p>
            <p>paragraph 2</p>
        </div>
    </div>
</html>";
MemoryStream stream = new MemoryStream(Encoding.UTF8.GetBytes(html));

HtmlLoadOptions loadOptions = new HtmlLoadOptions();
// Imposta la nuova modalità di importazione di elementi HTML a livello di blocco.
loadOptions.BlockImportMode = blockImportMode;

Document doc = new Document(stream, loadOptions);
doc.Save(ArtifactsDir + "HtmlLoadOptions.BlockImport.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Loading](../../aspose.words.loading/)
* assemblea [Aspose.Words](../../)
