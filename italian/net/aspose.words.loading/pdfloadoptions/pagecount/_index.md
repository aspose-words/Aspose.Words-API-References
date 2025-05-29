---
title: PdfLoadOptions.PageCount
linktitle: PageCount
articleTitle: PageCount
second_title: Aspose.Words per .NET
description: Controlla la lettura delle pagine con la proprietà PageCount di PdfLoadOptions. Imposta facilmente il numero di pagine da leggere, garantendo una gestione efficiente dei documenti.
type: docs
weight: 20
url: /it/net/aspose.words.loading/pdfloadoptions/pagecount/
---
## PdfLoadOptions.PageCount property

Ottiene o imposta il numero di pagine da leggere. Il valore predefinito è MaxValue, che significa che verranno lette tutte le pagine del documento.

```csharp
public int PageCount { get; set; }
```

## Esempi

Mostra come saltare le immagini durante il caricamento dei file PDF.

```csharp
PdfLoadOptions options = new PdfLoadOptions();
options.SkipPdfImages = isSkipPdfImages;
options.PageIndex = 0;
options.PageCount = 1;

Document doc = new Document(MyDir + "Images.pdf", options);
NodeCollection shapeCollection = doc.GetChildNodes(NodeType.Shape, true);

if (isSkipPdfImages)
    Assert.AreEqual(shapeCollection.Count, 0);
else
    Assert.AreNotEqual(shapeCollection.Count, 0);
```

### Guarda anche

* class [PdfLoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../../aspose.words.loading/)
* assemblea [Aspose.Words](../../../)
