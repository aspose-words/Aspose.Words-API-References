---
title: PdfLoadOptions.SkipPdfImages
second_title: Aspose.Words per .NET API Reference
description: PdfLoadOptions proprietà. Ottiene o imposta il flag che indica se le immagini devono essere saltate durante il caricamento del documento PDF. Limpostazione predefinita è False.
type: docs
weight: 40
url: /it/net/aspose.words.loading/pdfloadoptions/skippdfimages/
---
## PdfLoadOptions.SkipPdfImages property

Ottiene o imposta il flag che indica se le immagini devono essere saltate durante il caricamento del documento PDF. L'impostazione predefinita è False.

```csharp
public bool SkipPdfImages { get; set; }
```

### Esempi

Mostra come saltare le immagini durante il caricamento di file PDF.

```csharp
PdfLoadOptions options = new PdfLoadOptions();
options.SkipPdfImages = isSkipPdfImages;

Document doc = new Document(MyDir + "Images.pdf", options);
NodeCollection shapeCollection = doc.GetChildNodes(NodeType.Shape, true);

if (isSkipPdfImages)
{
    Assert.AreEqual(shapeCollection.Count, 0);
}
else
{
    Assert.AreNotEqual(shapeCollection.Count, 0);
}
```

### Guarda anche

* class [PdfLoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../pdfloadoptions/)
* assemblea [Aspose.Words](../../../)


