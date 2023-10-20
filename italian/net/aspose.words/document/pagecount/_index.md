---
title: Document.PageCount
linktitle: PageCount
articleTitle: PageCount
second_title: Aspose.Words per .NET
description: Document PageCount proprietà. Ottiene il numero di pagine nel documento calcolato dalloperazione di impaginazione più recente in C#.
type: docs
weight: 320
url: /it/net/aspose.words/document/pagecount/
---
## Document.PageCount property

Ottiene il numero di pagine nel documento calcolato dall'operazione di impaginazione più recente.

```csharp
public int PageCount { get; }
```

## Esempi

Mostra come contare il numero di pagine nel documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Page 1");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Page 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Write("Page 3");

// Verifica il numero di pagine previsto del documento.
Assert.AreEqual(3, doc.PageCount);

// L'ottenimento della proprietà PageCount ha richiamato il layout di pagina del documento per calcolare il valore.
// Non sarà necessario ripetere questa operazione quando si esegue il rendering del documento in un formato di salvataggio della pagina fisso,
// come .pdf. In questo modo puoi risparmiare tempo, soprattutto con documenti più complessi.
doc.Save(ArtifactsDir + "Document.GetPageCount.pdf");
```

### Guarda anche

* method [UpdatePageLayout](../updatepagelayout/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
