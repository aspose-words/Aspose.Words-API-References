---
title: Document.PageCount
linktitle: PageCount
articleTitle: PageCount
second_title: Aspose.Words per .NET
description: Scopri la proprietà Document PageCount, che rivela il numero totale di pagine in base al layout più recente, garantendo una gestione accurata dei documenti e informazioni dettagliate.
type: docs
weight: 330
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
// Questa operazione non dovrà essere ripetuta quando si esegue il rendering del documento in un formato di salvataggio della pagina fisso,
// come .pdf. Così puoi risparmiare tempo, soprattutto con i documenti più complessi.
doc.Save(ArtifactsDir + "Document.GetPageCount.pdf");
```

### Guarda anche

* method [UpdatePageLayout](../updatepagelayout/)
* class [Document](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
