---
title: PdfLoadOptions.PageCount
linktitle: PageCount
articleTitle: PageCount
second_title: Aspose.Words för .NET
description: Styr sidläsning med PdfLoadOptions PageCount-egenskap. Ställ enkelt in antalet sidor som ska läsas, vilket säkerställer effektiv dokumenthantering.
type: docs
weight: 20
url: /sv/net/aspose.words.loading/pdfloadoptions/pagecount/
---
## PdfLoadOptions.PageCount property

Hämtar eller ställer in antalet sidor som ska läsas. Standardvärdet är MaxValue vilket innebär att alla sidor i dokumentet kommer att läsas.

```csharp
public int PageCount { get; set; }
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
