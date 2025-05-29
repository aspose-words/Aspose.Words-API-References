---
title: PdfLoadOptions.PageIndex
linktitle: PageIndex
articleTitle: PageIndex
second_title: Aspose.Words för .NET
description: Upptäck PdfLoadOptions PageIndex. Ställ enkelt in startsidans index för PDF-läsning med den här flexibla egenskapen. Optimera din PDF-hantering idag!
type: docs
weight: 30
url: /sv/net/aspose.words.loading/pdfloadoptions/pageindex/
---
## PdfLoadOptions.PageIndex property

Hämtar eller ställer in det 0-baserade indexet för den första sidan som ska läsas. Standardvärdet är 0.

```csharp
public int PageIndex { get; set; }
```

## Exempel

Visar hur man hoppar över bilder när man laddar PDF-filer.

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

### Se även

* class [PdfLoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
