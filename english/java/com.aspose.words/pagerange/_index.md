---
title: PageRange
linktitle: PageRange
second_title: Aspose.Words for Java
description: Represents a continuous range of pages in Java.
type: docs
weight: 515
url: /java/com.aspose.words/pagerange/
---

**Inheritance:**
java.lang.Object
```
public class PageRange
```

Represents a continuous range of pages.

To learn more, visit the [ Programming with Documents ][Programming with Documents] documentation article.

 **Examples:** 

Shows how to extract pages based on exact page ranges.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.TIFF);
 PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3), new PageRange(2, 4), new PageRange(1, 1));

 imageOptions.setPageSet(pageSet);
 doc.save(getArtifactsDir() + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
 
```


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## Constructors

| Constructor | Description |
| --- | --- |
| [PageRange(int from, int to)](#PageRange-int-int) | Creates a new page range object. |
### PageRange(int from, int to) {#PageRange-int-int}
```
public PageRange(int from, int to)
```


Creates a new page range object.

 **Remarks:** 

**Integer.MAX\_VALUE** means the last page in the document.

 **Examples:** 

Shows how to extract pages based on exact page ranges.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.TIFF);
 PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3), new PageRange(2, 4), new PageRange(1, 1));

 imageOptions.setPageSet(pageSet);
 doc.save(getArtifactsDir() + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| from | int | The starting page zero-based index. |
| to | int | The ending page zero-based index. If it exceeds the index of the last page in the document, it is truncated to fit in the document on rendering. |

