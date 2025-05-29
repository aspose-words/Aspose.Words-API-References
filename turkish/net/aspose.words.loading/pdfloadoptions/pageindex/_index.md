---
title: PdfLoadOptions.PageIndex
linktitle: PageIndex
articleTitle: PageIndex
second_title: .NET için Aspose.Words
description: PdfLoadOptions PageIndex'i keşfedin. Bu esnek özellik ile PDF okuma için başlangıç sayfası dizinini kolayca ayarlayın. PDF işlemenizi bugün optimize edin!
type: docs
weight: 30
url: /tr/net/aspose.words.loading/pdfloadoptions/pageindex/
---
## PdfLoadOptions.PageIndex property

Okunacak ilk sayfanın 0 tabanlı dizinini alır veya ayarlar. Varsayılan 0'dır.

```csharp
public int PageIndex { get; set; }
```

## Örnekler

PDF dosyaları yüklenirken resimlerin nasıl atlanacağını gösterir.

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

### Ayrıca bakınız

* class [PdfLoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
