---
title: ImportFormatOptions.MergePastedLists
linktitle: MergePastedLists
articleTitle: MergePastedLists
second_title: Aspose.Words per .NET
description: Controlla l'unione degli elenchi con la proprietà MergePastedLists di ImportFormatOptions. Gestisci facilmente gli elenchi incollati per migliorare la formattazione del documento. Valore predefinito: false.
type: docs
weight: 70
url: /it/net/aspose.words/importformatoptions/mergepastedlists/
---
## ImportFormatOptions.MergePastedLists property

Ottiene o imposta un valore booleano che specifica se gli elenchi incollati verranno uniti agli elenchi circostanti. Il valore predefinito è`falso` .

```csharp
public bool MergePastedLists { get; set; }
```

## Esempi

Mostra come unire gli elenchi di un documento.

```csharp
Document srcDoc = new Document(MyDir + "List item.docx");
Document dstDoc = new Document(MyDir + "List destination.docx");

ImportFormatOptions options = new ImportFormatOptions { MergePastedLists = true };

// Imposta la proprietà "MergePastedLists" su "true". Gli elenchi incollati verranno uniti agli elenchi circostanti.
dstDoc.AppendDocument(srcDoc, ImportFormatMode.UseDestinationStyles, options);

dstDoc.Save(ArtifactsDir + "Document.MergePastedLists.docx");
```

### Guarda anche

* class [ImportFormatOptions](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
