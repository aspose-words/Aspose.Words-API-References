---
title: PageSet
linktitle: PageSet
second_title: Aspose.Words for Java
description: Describes a random set of pages in Java.
type: docs
weight: 472
url: /java/com.aspose.words/pageset/
---

**Inheritance:**
java.lang.Object
```
public class PageSet
```

Describes a random set of pages.

To learn more, visit the [ Programming with Documents ][Programming with Documents] documentation article.


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## Constructors

| Constructor | Description |
| --- | --- |
| [PageSet(int page)](#PageSet-int) | Creates an one-page set based on exact page index. |
| [PageSet(int[] pages)](#PageSet-int...) | Creates a page set based on exact page indices. |
| [PageSet(PageRange[] ranges)](#PageSet-com.aspose.words.PageRange...) | Creates a page set based on ranges. |
## Methods

| Method | Description |
| --- | --- |
| [getAll()](#getAll) | Gets a set with all the pages of the document in their original order. |
| [getEven()](#getEven) | Gets a set with all the even pages of the document in their original order. |
| [getOdd()](#getOdd) | Gets a set with all the odd pages of the document in their original order. |
### PageSet(int page) {#PageSet-int}
```
public PageSet(int page)
```


Creates an one-page set based on exact page index.

 **Remarks:** 

If a page is encountered that is not in the document, an exception will be thrown during rendering. **Integer.MAX\_VALUE** means the last page in the document.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| page | int | Zero-based index of the page. |

### PageSet(int[] pages) {#PageSet-int...}
```
public PageSet(int[] pages)
```


Creates a page set based on exact page indices.

 **Remarks:** 

If a page is encountered that is not in the document, an exception will be thrown during rendering. **Integer.MAX\_VALUE** means the last page in the document.

 **Examples:** 

Shows how to extract pages based on exact page indices.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add five pages to the document.
 for (int i = 1; i < 6; i++) {
     builder.write("Page " + i);
     builder.insertBreak(BreakType.PAGE_BREAK);
 }

 // Create an "XpsSaveOptions" object, which we can pass to the document's "Save" method
 // to modify how that method converts the document to .XPS.
 XpsSaveOptions xpsOptions = new XpsSaveOptions();

 // Use the "PageSet" property to select a set of the document's pages to save to output XPS.
 // In this case, we will choose, via a zero-based index, only three pages: page 1, page 2, and page 4.
 xpsOptions.setPageSet(new PageSet(0, 1, 3));

 doc.save(getArtifactsDir() + "XpsSaveOptions.ExportExactPages.xps", xpsOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pages | int[] | Zero-based indices of pages. |

### PageSet(PageRange[] ranges) {#PageSet-com.aspose.words.PageRange...}
```
public PageSet(PageRange[] ranges)
```


Creates a page set based on ranges.

 **Remarks:** 

If a range is encountered that starts after the last page in the document, an exception will be thrown during rendering. All ranges that end after the last page are truncated to fit in the document.

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
| ranges | [PageRange\[\]](../../com.aspose.words/pagerange/) | Array of page ranges. |

### getAll() {#getAll}
```
public static PageSet getAll()
```


Gets a set with all the pages of the document in their original order.

**Returns:**
[PageSet](../../com.aspose.words/pageset/) - A set with all the pages of the document in their original order.
### getEven() {#getEven}
```
public static PageSet getEven()
```


Gets a set with all the even pages of the document in their original order.

 **Remarks:** 

Even pages have odd indices since page indices are zero-based.

**Returns:**
[PageSet](../../com.aspose.words/pageset/) - A set with all the even pages of the document in their original order.
### getOdd() {#getOdd}
```
public static PageSet getOdd()
```


Gets a set with all the odd pages of the document in their original order.

 **Remarks:** 

Odd pages have even indices since page indices are zero-based.

**Returns:**
[PageSet](../../com.aspose.words/pageset/) - A set with all the odd pages of the document in their original order.
