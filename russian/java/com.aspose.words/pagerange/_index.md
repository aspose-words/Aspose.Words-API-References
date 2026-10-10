---
title: "PageRange"
linktitle: "PageRange"
second_title: "Aspose.Words для Java"
description: "Представляет непрерывный диапазон страниц в Java."
type: docs
weight: 516
url: /ru/java/com.aspose.words/pagerange/
---

**Inheritance:**
java.lang.Object
```
public class PageRange
```

Представляет непрерывный диапазон страниц.

Чтобы узнать больше, посетите статью документации [ Programming with Documents ][Programming with Documents].

 **Examples:** 

Показывает, как извлекать страницы на основе точных диапазонов страниц.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.TIFF);
 PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3), new PageRange(2, 4), new PageRange(1, 1));

 imageOptions.setPageSet(pageSet);
 doc.save(getArtifactsDir() + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
 
```


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [PageRange(int from, int to)](#PageRange-int-int) | Создаёт новый объект диапазона страниц. |
### PageRange(int from, int to) {#PageRange-int-int}
```
public PageRange(int from, int to)
```


Создаёт новый объект диапазона страниц.

 **Remarks:** 

**Integer.MAX\_VALUE** means the last page in the document.

 **Examples:** 

Показывает, как извлекать страницы на основе точных диапазонов страниц.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.TIFF);
 PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3), new PageRange(2, 4), new PageRange(1, 1));

 imageOptions.setPageSet(pageSet);
 doc.save(getArtifactsDir() + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
 
```

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| от | int | Начальный индекс страницы, начиная с нуля. |
| до | int | Конечный индекс страницы, начиная с нуля. Если он превышает индекс последней страницы в документе, он обрезается, чтобы соответствовать документу при рендеринге. |

