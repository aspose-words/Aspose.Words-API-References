---
title: PageRange
linktitle: PageRange
articleTitle: PageRange
second_title: Aspose.Words for .NET
description: PageRange inşaatçı. Yeni bir sayfa aralığı nesnesi oluşturur C#'da.
type: docs
weight: 10
url: /tr/net/aspose.words.saving/pagerange/pagerange/
---
## PageRange constructor

Yeni bir sayfa aralığı nesnesi oluşturur.

```csharp
public PageRange(int from, int to)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| from | Int32 | Başlangıç sayfası sıfır tabanlı dizin. |
| to | Int32 | Bitiş sayfası sıfır tabanlı dizin. Belgedeki son sayfanın indeksini aşarsa, oluşturma sırasında belgeye sığacak şekilde kesilir. |

## Notlar

MaxValue belgedeki son sayfa anlamına gelir.

## Örnekler

Tam sayfa aralıklarına göre sayfaların nasıl çıkarılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Images.docx");

ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.Tiff);
PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3),
    new PageRange(2, 4), new PageRange(1, 1));

imageOptions.PageSet = pageSet;
doc.Save(ArtifactsDir + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
```

### Ayrıca bakınız

* class [PageRange](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
