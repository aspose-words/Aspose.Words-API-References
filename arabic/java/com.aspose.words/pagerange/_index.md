---
title: "PageRange"
linktitle: "PageRange"
second_title: "Aspose.Words لـ Java"
description: "يمثل نطاقًا مستمرًا من الصفحات في Java."
type: docs
weight: 516
url: /ar/java/com.aspose.words/pagerange/
---

**Inheritance:**
java.lang.Object
```
public class PageRange
```

يمثل نطاقًا مستمرًا من الصفحات.

لمزيد من المعلومات، زر مقالة الوثائق [ Programming with Documents ][Programming with Documents].

 **Examples:** 

يعرض كيفية استخراج الصفحات بناءً على نطاقات صفحات دقيقة.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.TIFF);
 PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3), new PageRange(2, 4), new PageRange(1, 1));

 imageOptions.setPageSet(pageSet);
 doc.save(getArtifactsDir() + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
 
```


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [PageRange(int from, int to)](#PageRange-int-int) | ينشئ كائن نطاق صفحات جديد. |
### PageRange(int from, int to) {#PageRange-int-int}
```
public PageRange(int from, int to)
```


ينشئ كائن نطاق صفحات جديد.

 **Remarks:** 

**Integer.MAX\_VALUE** means the last page in the document.

 **Examples:** 

يعرض كيفية استخراج الصفحات بناءً على نطاقات صفحات دقيقة.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.TIFF);
 PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3), new PageRange(2, 4), new PageRange(1, 1));

 imageOptions.setPageSet(pageSet);
 doc.save(getArtifactsDir() + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| من | int | فهرس الصفحة الابتدائية يبدأ من الصفر. |
| إلى | int | فهرس الصفحة النهائية صفر-مبني. إذا تجاوز فهرس آخر صفحة في المستند، يتم تقصيره ليتناسب مع المستند عند العرض. |

