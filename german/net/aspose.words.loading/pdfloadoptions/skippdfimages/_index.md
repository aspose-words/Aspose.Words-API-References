---
title: PdfLoadOptions.SkipPdfImages
linktitle: SkipPdfImages
articleTitle: SkipPdfImages
second_title: Aspose.Words für .NET
description: PdfLoadOptions SkipPdfImages eigendom. Ruft das Flag ab oder setzt es das angibt ob Bilder beim Laden eines PDFDokuments übersprungen werden müssen. Standard istFALSCH  in C#.
type: docs
weight: 40
url: /de/net/aspose.words.loading/pdfloadoptions/skippdfimages/
---
## PdfLoadOptions.SkipPdfImages property

Ruft das Flag ab oder setzt es, das angibt, ob Bilder beim Laden eines PDF-Dokuments übersprungen werden müssen. Standard ist`FALSCH` .

```csharp
public bool SkipPdfImages { get; set; }
```

## Beispiele

Zeigt, wie Bilder beim Laden von PDF-Dateien übersprungen werden.

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

### Siehe auch

* class [PdfLoadOptions](../)
* namensraum [Aspose.Words.Loading](../../../aspose.words.loading/)
* Montage [Aspose.Words](../../../)
