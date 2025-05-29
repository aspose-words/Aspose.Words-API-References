---
title: PdfLoadOptions.PageCount
linktitle: PageCount
articleTitle: PageCount
second_title: .NET için Aspose.Words
description: PdfLoadOptions' PageCount özelliğiyle sayfa okumayı kontrol edin. Okunacak sayfa sayısını kolayca ayarlayın, böylece verimli belge işleme sağlayın.
type: docs
weight: 20
url: /tr/net/aspose.words.loading/pdfloadoptions/pagecount/
---
## PdfLoadOptions.PageCount property

Okunacak sayfa sayısını alır veya ayarlar. Varsayılan değer MaxValue'dur, bu da belgenin tüm sayfalarının okunacağı anlamına gelir.

```csharp
public int PageCount { get; set; }
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
