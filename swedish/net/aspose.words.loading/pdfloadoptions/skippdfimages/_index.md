---
title: PdfLoadOptions.SkipPdfImages
second_title: Aspose.Words för .NET API Referens
description: PdfLoadOptions fast egendom. Hämtar eller ställer in flaggan som anger om bilder måste hoppas över när PDFdokument laddas. Standard ärfalsk .
type: docs
weight: 40
url: /sv/net/aspose.words.loading/pdfloadoptions/skippdfimages/
---
## PdfLoadOptions.SkipPdfImages property

Hämtar eller ställer in flaggan som anger om bilder måste hoppas över när PDF-dokument laddas. Standard är`falsk` .

```csharp
public bool SkipPdfImages { get; set; }
```

### Exempel

Visar hur du hoppar över bilder när du laddar PDF-filer.

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

### Se även

* class [PdfLoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../pdfloadoptions/)
* hopsättning [Aspose.Words](../../../)


