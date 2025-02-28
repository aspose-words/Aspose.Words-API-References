---
title: PdfLoadOptions.SkipPdfImages
linktitle: SkipPdfImages
articleTitle: SkipPdfImages
second_title: Aspose.Words for .NET
description: Discover PdfLoadOptions' SkipPdfImages property to control image loading in PDFs. Enhance performance by skipping images for faster document processing.
type: docs
weight: 40
url: /net/aspose.words.loading/pdfloadoptions/skippdfimages/
---
## PdfLoadOptions.SkipPdfImages property

Gets or sets the flag indicating whether images must be skipped while loading PDF document. Default is `false`.

```csharp
public bool SkipPdfImages { get; set; }
```

## Examples

Shows how to skip images during loading PDF files.

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

### See Also

* class [PdfLoadOptions](../)
* namespace [Aspose.Words.Loading](../../../aspose.words.loading/)
* assembly [Aspose.Words](../../../)
