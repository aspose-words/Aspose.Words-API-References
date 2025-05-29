---
title: PdfLoadOptions.PageIndex
linktitle: PageIndex
articleTitle: PageIndex
second_title: Aspose.Words per .NET
description: Scopri PdfLoadOptions PageIndex. Imposta facilmente l'indice della pagina iniziale per la lettura dei PDF con questa proprietà flessibile. Ottimizza la gestione dei tuoi PDF oggi stesso!
type: docs
weight: 30
url: /it/net/aspose.words.loading/pdfloadoptions/pageindex/
---
## PdfLoadOptions.PageIndex property

Ottiene o imposta l'indice a partire da 0 della prima pagina da leggere. Il valore predefinito è 0.

```csharp
public int PageIndex { get; set; }
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
