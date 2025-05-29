---
title: PdfLoadOptions.PageCount
linktitle: PageCount
articleTitle: PageCount
second_title: Aspose.Words für .NET
description: Steuern Sie das Lesen von Seiten mit der PageCount-Eigenschaft von PdfLoadOptions. Legen Sie einfach die Anzahl der zu lesenden Seiten fest und gewährleisten Sie so eine effiziente Dokumentenverarbeitung.
type: docs
weight: 20
url: /de/net/aspose.words.loading/pdfloadoptions/pagecount/
---
## PdfLoadOptions.PageCount property

Ruft die Anzahl der zu lesenden Seiten ab oder legt sie fest. Der Standardwert ist MaxValue, d. h., es werden alle Seiten des Dokuments gelesen.

```csharp
public int PageCount { get; set; }
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
