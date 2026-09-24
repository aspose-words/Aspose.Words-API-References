---
title: "PageSet"
linktitle: "PageSet"
second_title: "Aspose.Words Java için"
description: "Java'da rastgele bir sayfa kümesini açıklar."
type: docs
weight: 518
url: /tr/java/com.aspose.words/pageset/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class PageSet implements Iterable
```

Rastgele bir sayfa kümesini tanımlar.

Daha fazla bilgi için, [ Programming with Documents ][Programming with Documents] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Bir belgeden tek bir sayfayı JPEG görüntüsüne nasıl render edeceğinizi gösterir.

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
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [PageSet(int page)](#PageSet-int) | Tam sayfa indeksine dayalı tek sayfalık bir küme oluşturur. |
| [PageSet(int[] pages)](#PageSet-int...) | Tam sayfa indekslerine dayalı bir sayfa kümesi oluşturur. |
| [PageSet(PageRange[] ranges)](#PageSet-com.aspose.words.PageRange...) | Aralıklara dayalı bir sayfa kümesi oluşturur. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getAll()](#getAll) | Belgenin tüm sayfalarını orijinal sıralarında içeren bir küme alır. |
| [getEven()](#getEven) | Belgenin tüm çift sayfalarını orijinal sıralarında içeren bir küme alır. |
| [getOdd()](#getOdd) | Belgenin tüm tek sayfalarını orijinal sıralarında içeren bir küme alır. |
| [iterator()](#iterator) |  |
### PageSet(int page) {#PageSet-int}
```
public PageSet(int page)
```


Tam sayfa indeksine dayalı tek sayfalık bir küme oluşturur.

 **Remarks:** 

Belgede bulunmayan bir sayfa ile karşılaşılırsa, renderleme sırasında bir istisna fırlatılır. **Integer.MAX\_VALUE** belgedeki son sayfayı ifade eder.

 **Examples:** 

Bir belgeden tek bir sayfayı JPEG görüntüsüne nasıl render edeceğinizi gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sayfa | int | Sayfanın sıfır tabanlı indeksi. |

### PageSet(int[] pages) {#PageSet-int...}
```
public PageSet(int[] pages)
```


Tam sayfa indekslerine dayalı bir sayfa kümesi oluşturur.

 **Remarks:** 

Belgede bulunmayan bir sayfa ile karşılaşılırsa, renderleme sırasında bir istisna fırlatılır. **Integer.MAX\_VALUE** belgedeki son sayfayı ifade eder.

 **Examples:** 

Tam sayfa indekslerine dayalı sayfaları nasıl çıkaracağınızı gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sayfalar | int[] | Sayfaların sıfır tabanlı indeksleri. |

### PageSet(PageRange[] ranges) {#PageSet-com.aspose.words.PageRange...}
```
public PageSet(PageRange[] ranges)
```


Aralıklara dayalı bir sayfa kümesi oluşturur.

 **Remarks:** 

Belgedeki son sayfadan sonra başlayan bir aralıkla karşılaşılırsa, renderleme sırasında bir istisna fırlatılır. Son sayfadan sonra biten tüm aralıklar belgeye sığacak şekilde kırpılır.

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
| ranges | [PageRange\[\]](../../com.aspose.words/pagerange/) | Sayfa aralıkları dizisi. |

### getAll() {#getAll}
```
public static PageSet getAll()
```


Belgenin tüm sayfalarını orijinal sıralarında içeren bir küme alır.

 **Examples:** 

Belgeden tek sayfaları nasıl dışa aktaracağınızı gösterir.

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


Belgenin tüm çift sayfalarını orijinal sıralarında içeren bir küme alır.

 **Remarks:** 

Çift sayfaların indeksleri tek sayıdır çünkü sayfa indeksleri sıfır tabanlıdır.

 **Examples:** 

Belgeden tek sayfaları nasıl dışa aktaracağınızı gösterir.

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


Belgenin tüm tek sayfalarını orijinal sıralarında içeren bir küme alır.

 **Remarks:** 

Tek sayfaların indeksleri çift sayıdır çünkü sayfa indeksleri sıfır tabanlıdır.

 **Examples:** 

Belgeden tek sayfaları nasıl dışa aktaracağınızı gösterir.

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
