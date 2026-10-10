---
title: "PageSet"
linktitle: "PageSet"
second_title: "Aspose.Words für Java"
description: "Beschreibt eine zufällige Menge von Seiten in Java."
type: docs
weight: 518
url: /de/java/com.aspose.words/pageset/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class PageSet implements Iterable
```

Beschreibt eine zufällige Menge von Seiten.

Weitere Informationen finden Sie im Dokumentationsartikel [ Programming with Documents ][Programming with Documents].

 **Examples:** 

Zeigt, wie eine Seite aus einem Dokument in ein JPEG-Bild gerendert wird.

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
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [PageSet(int page)](#PageSet-int) | Erstellt ein einseitiges Set basierend auf dem genauen Seitenindex. |
| [PageSet(int[] pages)](#PageSet-int...) | Erstellt ein Seitenset basierend auf den genauen Seitenindizes. |
| [PageSet(PageRange[] ranges)](#PageSet-com.aspose.words.PageRange...) | Erstellt ein Seitenset basierend auf Bereichen. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getAll()](#getAll) | Erhält ein Set mit allen Seiten des Dokuments in ihrer ursprünglichen Reihenfolge. |
| [getEven()](#getEven) | Erhält ein Set mit allen geraden Seiten des Dokuments in ihrer ursprünglichen Reihenfolge. |
| [getOdd()](#getOdd) | Erhält ein Set mit allen ungeraden Seiten des Dokuments in ihrer ursprünglichen Reihenfolge. |
| [iterator()](#iterator) |  |
### PageSet(int page) {#PageSet-int}
```
public PageSet(int page)
```


Erstellt ein einseitiges Set basierend auf dem genauen Seitenindex.

 **Remarks:** 

Wenn eine Seite gefunden wird, die nicht im Dokument enthalten ist, wird während des Renderns eine Ausnahme ausgelöst. **Integer.MAX\_VALUE** bedeutet die letzte Seite im Dokument.

 **Examples:** 

Zeigt, wie eine Seite aus einem Dokument in ein JPEG-Bild gerendert wird.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Seite | int | Nullbasierter Index der Seite. |

### PageSet(int[] pages) {#PageSet-int...}
```
public PageSet(int[] pages)
```


Erstellt ein Seitenset basierend auf den genauen Seitenindizes.

 **Remarks:** 

Wenn eine Seite gefunden wird, die nicht im Dokument enthalten ist, wird während des Renderns eine Ausnahme ausgelöst. **Integer.MAX\_VALUE** bedeutet die letzte Seite im Dokument.

 **Examples:** 

Zeigt, wie man Seiten basierend auf genauen Seitenindizes extrahiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Seiten | int[] | Nullbasierte Indizes der Seiten. |

### PageSet(PageRange[] ranges) {#PageSet-com.aspose.words.PageRange...}
```
public PageSet(PageRange[] ranges)
```


Erstellt ein Seitenset basierend auf Bereichen.

 **Remarks:** 

Wenn ein Bereich gefunden wird, der nach der letzten Seite im Dokument beginnt, wird während des Renderns eine Ausnahme ausgelöst. Alle Bereiche, die nach der letzten Seite enden, werden gekürzt, um in das Dokument zu passen.

 **Examples:** 

Zeigt, wie man Seiten basierend auf genauen Seitenbereichen extrahiert.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.TIFF);
 PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3), new PageRange(2, 4), new PageRange(1, 1));

 imageOptions.setPageSet(pageSet);
 doc.save(getArtifactsDir() + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| ranges | [PageRange\[\]](../../com.aspose.words/pagerange/) | Array von Seitenbereichen. |

### getAll() {#getAll}
```
public static PageSet getAll()
```


Erhält ein Set mit allen Seiten des Dokuments in ihrer ursprünglichen Reihenfolge.

 **Examples:** 

Zeigt, wie man ungerade Seiten aus dem Dokument exportiert.

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


Erhält ein Set mit allen geraden Seiten des Dokuments in ihrer ursprünglichen Reihenfolge.

 **Remarks:** 

Gerade Seiten haben ungerade Indizes, da Seitenindizes nullbasiert sind.

 **Examples:** 

Zeigt, wie man ungerade Seiten aus dem Dokument exportiert.

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


Erhält ein Set mit allen ungeraden Seiten des Dokuments in ihrer ursprünglichen Reihenfolge.

 **Remarks:** 

Ungerade Seiten haben gerade Indizes, da Seitenindizes nullbasiert sind.

 **Examples:** 

Zeigt, wie man ungerade Seiten aus dem Dokument exportiert.

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
