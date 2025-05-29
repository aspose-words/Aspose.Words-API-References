---
title: PdfLoadOptions.SkipPdfImages
linktitle: SkipPdfImages
articleTitle: SkipPdfImages
second_title: .NET için Aspose.Words
description: PDF'lerde resim yüklemeyi kontrol etmek için PdfLoadOptions' SkipPdfImages özelliğini keşfedin. Daha hızlı belge işleme için resimleri atlayarak performansı artırın.
type: docs
weight: 40
url: /tr/net/aspose.words.loading/pdfloadoptions/skippdfimages/
---
## PdfLoadOptions.SkipPdfImages property

PDF belgesi yüklenirken resimlerin atlanması gerekip gerekmediğini belirten bayrağı alır veya ayarlar. Varsayılan:`YANLIŞ` .

```csharp
public bool SkipPdfImages { get; set; }
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
