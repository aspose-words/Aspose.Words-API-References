---
title: PageRange Class
linktitle: PageRange
articleTitle: PageRange
second_title: .NET için Aspose.Words
description: Sürekli sayfa aralıklarını kolayca tanımlamak için Aspose.Words.Saving.PageRange sınıfını keşfedin. Belge işlemenizi hassasiyet ve verimlilikle geliştirin.
type: docs
weight: 6150
url: /tr/net/aspose.words.saving/pagerange/
---
## PageRange class

Sürekli bir sayfa aralığını temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Belgelerle Programlama](https://docs.aspose.com/words/net/programming-with-documents/) belgeleme makalesi.

```csharp
public sealed class PageRange
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [PageRange](pagerange/)(*int, int*) | Yeni bir sayfa aralığı nesnesi oluşturur. |

## Örnekler

Sayfaların tam sayfa aralıklarına göre nasıl çıkarılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Images.docx");

ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Tiff);
PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3),
    new PageRange(2, 4), new PageRange(1, 1));

imageOptions.PageSet = pageSet;
doc.Save(ArtifactsDir + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Saving](../../aspose.words.saving/)
* toplantı [Aspose.Words](../../)
