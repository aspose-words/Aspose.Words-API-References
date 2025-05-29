---
title: PdfLoadOptions.PageIndex
linktitle: PageIndex
articleTitle: PageIndex
second_title: Aspose.Words für .NET
description: Entdecken Sie PdfLoadOptions PageIndex. Mit dieser flexiblen Eigenschaft legen Sie ganz einfach den Index der Startseite für das Lesen von PDF-Dateien fest. Optimieren Sie noch heute Ihre PDF-Verarbeitung!
type: docs
weight: 30
url: /de/net/aspose.words.loading/pdfloadoptions/pageindex/
---
## PdfLoadOptions.PageIndex property

Ruft den 0-basierten Index der ersten zu lesenden Seite ab oder legt ihn fest. Der Standardwert ist 0.

```csharp
public int PageIndex { get; set; }
```

## Beispiele

Zeigt, wie Bilder beim Laden von PDF-Dateien übersprungen werden.

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

### Siehe auch

* class [PdfLoadOptions](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
