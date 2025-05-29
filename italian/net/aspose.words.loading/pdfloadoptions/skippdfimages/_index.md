---
title: PdfLoadOptions.SkipPdfImages
linktitle: SkipPdfImages
articleTitle: SkipPdfImages
second_title: Aspose.Words per .NET
description: Scopri la proprietà SkipPdfImages di PdfLoadOptions per controllare il caricamento delle immagini nei PDF. Migliora le prestazioni saltando le immagini per un'elaborazione più rapida dei documenti.
type: docs
weight: 40
url: /it/net/aspose.words.loading/pdfloadoptions/skippdfimages/
---
## PdfLoadOptions.SkipPdfImages property

Ottiene o imposta il flag che indica se le immagini devono essere saltate durante il caricamento del documento PDF. Il valore predefinito è`falso` .

```csharp
public bool SkipPdfImages { get; set; }
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
