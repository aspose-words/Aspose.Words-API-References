---
title: ImportFormatOptions.MergePastedLists
second_title: Aspose.Words per .NET API Reference
description: ImportFormatOptions proprietà. Ottiene o imposta un valore booleano che specifica se gli elenchi incollati verranno uniti con gli elenchi circostanti. Il valore predefinito èfalso .
type: docs
weight: 70
url: /it/net/aspose.words/importformatoptions/mergepastedlists/
---
## ImportFormatOptions.MergePastedLists property

Ottiene o imposta un valore booleano che specifica se gli elenchi incollati verranno uniti con gli elenchi circostanti. Il valore predefinito è`falso` .

```csharp
public bool MergePastedLists { get; set; }
```

### Esempi

Mostra come unire elenchi da documenti.

```csharp
Document srcDoc = new Document(MyDir + "List item.docx");
Document dstDoc = new Document(MyDir + "List destination.docx");

ImportFormatOptions options = new ImportFormatOptions { MergePastedLists = true };

// Imposta la proprietà "MergePastedLists" su "vero": gli elenchi incollati verranno uniti con gli elenchi circostanti.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, options);

dstDoc.Save(ArtifactsDir + "Document.MergePastedLists.docx");
```

### Guarda anche

* class [ImportFormatOptions](../)
* spazio dei nomi [Aspose.Words](../../importformatoptions/)
* assemblea [Aspose.Words](../../../)


