---
title: "PageRange"
linktitle: "PageRange"
second_title: "Aspose.Words Java için"
description: "Java'da sürekli bir sayfa aralığını temsil eder."
type: docs
weight: 516
url: /tr/java/com.aspose.words/pagerange/
---

**Inheritance:**
java.lang.Object
```
public class PageRange
```

Sürekli bir sayfa aralığını temsil eder.

Daha fazla bilgi için, [ Programming with Documents ][Programming with Documents] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Tam sayfa aralıklarına göre sayfaların nasıl çıkarılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.TIFF);
 PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3), new PageRange(2, 4), new PageRange(1, 1));

 imageOptions.setPageSet(pageSet);
 doc.save(getArtifactsDir() + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
 
```


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [PageRange(int from, int to)](#PageRange-int-int) | Yeni bir sayfa aralığı nesnesi oluşturur. |
### PageRange(int from, int to) {#PageRange-int-int}
```
public PageRange(int from, int to)
```


Yeni bir sayfa aralığı nesnesi oluşturur.

 **Remarks:** 

**Integer.MAX\_VALUE** means the last page in the document.

 **Examples:** 

Tam sayfa aralıklarına göre sayfaların nasıl çıkarılacağını gösterir.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.TIFF);
 PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3), new PageRange(2, 4), new PageRange(1, 1));

 imageOptions.setPageSet(pageSet);
 doc.save(getArtifactsDir() + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| den | int | Başlangıç sayfasının sıfır tabanlı indeksi. |
| e | int | Bitiş sayfasının sıfır tabanlı indeksi. Belge içindeki son sayfanın indeksini aşarsa, render sırasında belgeye sığacak şekilde kırpılır. |

