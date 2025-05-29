---
title: HtmlLoadOptions.BlockImportMode
linktitle: BlockImportMode
articleTitle: BlockImportMode
second_title: Aspose.Words per .NET
description: Scopri la proprietà BlockImportMode di HtmlLoadOptions per personalizzare l'importazione di elementi a livello di blocco. Controlla l'unione per una gestione ottimale dei contenuti!
type: docs
weight: 20
url: /it/net/aspose.words.loading/htmlloadoptions/blockimportmode/
---
## HtmlLoadOptions.BlockImportMode property

Ottiene o imposta un valore che specifica come vengono importate le proprietà degli elementi a livello di blocco. Il valore predefinito èMerge .

```csharp
public BlockImportMode BlockImportMode { get; set; }
```

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
// Imposta la nuova modalità di importazione degli elementi HTML a livello di blocco.
loadOptions.BlockImportMode = blockImportMode;

Document doc = new Document(stream, loadOptions);
doc.Save(ArtifactsDir + "HtmlLoadOptions.BlockImport.docx");
```

### Guarda anche

* enum [BlockImportMode](../../blockimportmode/)
* class [HtmlLoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)
