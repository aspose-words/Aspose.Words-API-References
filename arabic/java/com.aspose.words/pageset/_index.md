---
title: "PageSet"
linktitle: "PageSet"
second_title: "Aspose.Words لـ Java"
description: "يصف مجموعة عشوائية من الصفحات في Java."
type: docs
weight: 518
url: /ar/java/com.aspose.words/pageset/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class PageSet implements Iterable
```

يصف مجموعة عشوائية من الصفحات.

لمزيد من المعلومات، زر مقالة الوثائق [ Programming with Documents ][Programming with Documents].

 **Examples:** 

يوضح كيفية تحويل صفحة واحدة من مستند إلى صورة JPEG.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 2.");
 builder.insertImage(getImageDir() + "Logo.jpg");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 3.");

 // Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
 // to modify the way in which that method renders the document into an image.
 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.JPEG);
 // Set the "PageSet" to "1" to select the second page via
 // the zero-based index to start rendering the document from.
 options.setPageSet(new PageSet(1));

 // When we save the document to the JPEG format, Aspose.Words only renders one page.
 // This image will contain one page starting from page two,
 // which will just be the second page of the original document.
 doc.save(getArtifactsDir() + "ImageSaveOptions.OnePage.jpg", options);
 
```


[Programming with Documents]: https://docs.aspose.com/words/java/programming-with-documents/
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [PageSet(int page)](#PageSet-int) | ينشئ مجموعة صفحة واحدة بناءً على فهرس الصفحة الدقيق. |
| [PageSet(int[] pages)](#PageSet-int...) | ينشئ مجموعة صفحات بناءً على فهارس الصفحات الدقيقة. |
| [PageSet(PageRange[] ranges)](#PageSet-com.aspose.words.PageRange...) | ينشئ مجموعة صفحات بناءً على النطاقات. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getAll()](#getAll) | يحصل على مجموعة تحتوي على جميع صفحات المستند بترتيبها الأصلي. |
| [getEven()](#getEven) | يحصل على مجموعة تحتوي على جميع الصفحات الزوجية للمستند بترتيبها الأصلي. |
| [getOdd()](#getOdd) | يحصل على مجموعة تحتوي على جميع الصفحات الفردية للمستند بترتيبها الأصلي. |
| [iterator()](#iterator) |  |
### PageSet(int page) {#PageSet-int}
```
public PageSet(int page)
```


ينشئ مجموعة صفحة واحدة بناءً على فهرس الصفحة الدقيق.

 **Remarks:** 

إذا تم العثور على صفحة غير موجودة في المستند، سيتم رمي استثناء أثناء عملية العرض. **Integer.MAX\_VALUE** يعني آخر صفحة في المستند.

 **Examples:** 

يوضح كيفية تحويل صفحة واحدة من مستند إلى صورة JPEG.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Page 1.");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 2.");
 builder.insertImage(getImageDir() + "Logo.jpg");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page 3.");

 // Create an "ImageSaveOptions" object which we can pass to the document's "Save" method
 // to modify the way in which that method renders the document into an image.
 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.JPEG);
 // Set the "PageSet" to "1" to select the second page via
 // the zero-based index to start rendering the document from.
 options.setPageSet(new PageSet(1));

 // When we save the document to the JPEG format, Aspose.Words only renders one page.
 // This image will contain one page starting from page two,
 // which will just be the second page of the original document.
 doc.save(getArtifactsDir() + "ImageSaveOptions.OnePage.jpg", options);
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| صفحة | int | الفهرس الصفري للصفحة. |

### PageSet(int[] pages) {#PageSet-int...}
```
public PageSet(int[] pages)
```


ينشئ مجموعة صفحات بناءً على فهارس الصفحات الدقيقة.

 **Remarks:** 

إذا تم العثور على صفحة غير موجودة في المستند، سيتم رمي استثناء أثناء عملية العرض. **Integer.MAX\_VALUE** يعني آخر صفحة في المستند.

 **Examples:** 

يوضح كيفية استخراج الصفحات بناءً على فهارس الصفحات الدقيقة.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| صفحات | int[] | فهارس الصفحات الصفرية. |

### PageSet(PageRange[] ranges) {#PageSet-com.aspose.words.PageRange...}
```
public PageSet(PageRange[] ranges)
```


ينشئ مجموعة صفحات بناءً على النطاقات.

 **Remarks:** 

إذا تم العثور على نطاق يبدأ بعد آخر صفحة في المستند، سيتم رمي استثناء أثناء عملية العرض. جميع النطاقات التي تنتهي بعد آخر صفحة يتم قصها لتتناسب مع المستند.

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
| ranges | [PageRange\[\]](../../com.aspose.words/pagerange/) | مصفوفة من نطاقات الصفحات. |

### getAll() {#getAll}
```
public static PageSet getAll()
```


يحصل على مجموعة تحتوي على جميع صفحات المستند بترتيبها الأصلي.

 **Examples:** 

يوضح كيفية تصدير الصفحات الفردية من المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 for (int i = 0; i < 5; i++) {
     builder.writeln(MessageFormat.format("Page {0} ({1})", i + 1, (i % 2 == 0 ? "odd" : "even")));
     if (i < 4)
         builder.insertBreak(BreakType.PAGE_BREAK);
 }

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Below are three PageSet properties that we can use to filter out a set of pages from
 // our document to save in an output PDF document based on the parity of their page numbers.
 // 1 -  Save only the even-numbered pages:
 options.setPageSet(PageSet.getEven());

 doc.save(getArtifactsDir() + "PdfSaveOptions.ExportPageSet.Even.pdf", options);

 // 2 -  Save only the odd-numbered pages:
 options.setPageSet(PageSet.getOdd());

 doc.save(getArtifactsDir() + "PdfSaveOptions.ExportPageSet.Odd.pdf", options);

 // 3 -  Save every page:
 options.setPageSet(PageSet.getAll());

 doc.save(getArtifactsDir() + "PdfSaveOptions.ExportPageSet.All.pdf", options);
 
```

**Returns:**
[PageSet](../../com.aspose.words/pageset/) - A set with all the pages of the document in their original order.
### getEven() {#getEven}
```
public static PageSet getEven()
```


يحصل على مجموعة تحتوي على جميع الصفحات الزوجية للمستند بترتيبها الأصلي.

 **Remarks:** 

الصفحات الزوجية لها فهارس فردية لأن فهارس الصفحات صفرية.

 **Examples:** 

يوضح كيفية تصدير الصفحات الفردية من المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 for (int i = 0; i < 5; i++) {
     builder.writeln(MessageFormat.format("Page {0} ({1})", i + 1, (i % 2 == 0 ? "odd" : "even")));
     if (i < 4)
         builder.insertBreak(BreakType.PAGE_BREAK);
 }

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Below are three PageSet properties that we can use to filter out a set of pages from
 // our document to save in an output PDF document based on the parity of their page numbers.
 // 1 -  Save only the even-numbered pages:
 options.setPageSet(PageSet.getEven());

 doc.save(getArtifactsDir() + "PdfSaveOptions.ExportPageSet.Even.pdf", options);

 // 2 -  Save only the odd-numbered pages:
 options.setPageSet(PageSet.getOdd());

 doc.save(getArtifactsDir() + "PdfSaveOptions.ExportPageSet.Odd.pdf", options);

 // 3 -  Save every page:
 options.setPageSet(PageSet.getAll());

 doc.save(getArtifactsDir() + "PdfSaveOptions.ExportPageSet.All.pdf", options);
 
```

**Returns:**
[PageSet](../../com.aspose.words/pageset/) - A set with all the even pages of the document in their original order.
### getOdd() {#getOdd}
```
public static PageSet getOdd()
```


يحصل على مجموعة تحتوي على جميع الصفحات الفردية للمستند بترتيبها الأصلي.

 **Remarks:** 

الصفحات الفردية لها فهارس زوجية لأن فهارس الصفحات صفرية.

 **Examples:** 

يوضح كيفية تصدير الصفحات الفردية من المستند.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 for (int i = 0; i < 5; i++) {
     builder.writeln(MessageFormat.format("Page {0} ({1})", i + 1, (i % 2 == 0 ? "odd" : "even")));
     if (i < 4)
         builder.insertBreak(BreakType.PAGE_BREAK);
 }

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Below are three PageSet properties that we can use to filter out a set of pages from
 // our document to save in an output PDF document based on the parity of their page numbers.
 // 1 -  Save only the even-numbered pages:
 options.setPageSet(PageSet.getEven());

 doc.save(getArtifactsDir() + "PdfSaveOptions.ExportPageSet.Even.pdf", options);

 // 2 -  Save only the odd-numbered pages:
 options.setPageSet(PageSet.getOdd());

 doc.save(getArtifactsDir() + "PdfSaveOptions.ExportPageSet.Odd.pdf", options);

 // 3 -  Save every page:
 options.setPageSet(PageSet.getAll());

 doc.save(getArtifactsDir() + "PdfSaveOptions.ExportPageSet.All.pdf", options);
 
```

**Returns:**
[PageSet](../../com.aspose.words/pageset/) - A set with all the odd pages of the document in their original order.
### iterator() {#iterator}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator
