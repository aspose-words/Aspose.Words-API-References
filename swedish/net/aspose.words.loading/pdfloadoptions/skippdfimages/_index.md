---
title: PdfLoadOptions.SkipPdfImages
linktitle: SkipPdfImages
articleTitle: SkipPdfImages
second_title: Aspose.Words för .NET
description: Upptäck PdfLoadOptions egenskap SkipPdfImages för att styra bildinläsning i PDF-filer. Förbättra prestandan genom att hoppa över bilder för snabbare dokumentbehandling.
type: docs
weight: 40
url: /sv/net/aspose.words.loading/pdfloadoptions/skippdfimages/
---
## PdfLoadOptions.SkipPdfImages property

Hämtar eller ställer in flaggan som anger om bilder måste hoppas över när PDF-dokumentet laddas. Standard är`falsk` .

```csharp
public bool SkipPdfImages { get; set; }
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
