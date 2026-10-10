---
title: "PageSet"
linktitle: "PageSet"
second_title: "Aspose.Words para Java"
description: "Describe un conjunto aleatorio de páginas en Java."
type: docs
weight: 518
url: /es/java/com.aspose.words/pageset/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class PageSet implements Iterable
```

Describe un conjunto aleatorio de páginas.

Para obtener más información, visite el artículo de documentación [ Programming with Documents ][Programming with Documents].

 **Examples:** 

Muestra cómo renderizar una página de un documento a una imagen JPEG.

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
## Constructores

| Constructor | Descripción |
| --- | --- |
| [PageSet(int page)](#PageSet-int) | Crea un conjunto de una página basado en el índice exacto de la página. |
| [PageSet(int[] pages)](#PageSet-int...) | Crea un conjunto de páginas basado en índices exactos de página. |
| [PageSet(PageRange[] ranges)](#PageSet-com.aspose.words.PageRange...) | Crea un conjunto de páginas basado en rangos. |
## Métodos

| Método | Descripción |
| --- | --- |
| [getAll()](#getAll) | Obtiene un conjunto con todas las páginas del documento en su orden original. |
| [getEven()](#getEven) | Obtiene un conjunto con todas las páginas pares del documento en su orden original. |
| [getOdd()](#getOdd) | Obtiene un conjunto con todas las páginas impares del documento en su orden original. |
| [iterator()](#iterator) |  |
### PageSet(int page) {#PageSet-int}
```
public PageSet(int page)
```


Crea un conjunto de una página basado en el índice exacto de la página.

 **Remarks:** 

Si se encuentra una página que no está en el documento, se lanzará una excepción durante el renderizado. **Integer.MAX\_VALUE** significa la última página del documento.

 **Examples:** 

Muestra cómo renderizar una página de un documento a una imagen JPEG.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| página | int | Índice basado en cero de la página. |

### PageSet(int[] pages) {#PageSet-int...}
```
public PageSet(int[] pages)
```


Crea un conjunto de páginas basado en índices exactos de página.

 **Remarks:** 

Si se encuentra una página que no está en el documento, se lanzará una excepción durante el renderizado. **Integer.MAX\_VALUE** significa la última página del documento.

 **Examples:** 

Muestra cómo extraer páginas basándose en índices exactos de página.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| páginas | int[] | Índices basados en cero de las páginas. |

### PageSet(PageRange[] ranges) {#PageSet-com.aspose.words.PageRange...}
```
public PageSet(PageRange[] ranges)
```


Crea un conjunto de páginas basado en rangos.

 **Remarks:** 

Si se encuentra un rango que comienza después de la última página del documento, se lanzará una excepción durante el renderizado. Todos los rangos que terminan después de la última página se truncan para ajustarse al documento.

 **Examples:** 

Muestra cómo extraer páginas basándose en rangos de página exactos.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 ImageSaveOptions imageOptions = new ImageSaveOptions(SaveFormat.TIFF);
 PageSet pageSet = new PageSet(new PageRange(1, 1), new PageRange(2, 3), new PageRange(1, 3), new PageRange(2, 4), new PageRange(1, 1));

 imageOptions.setPageSet(pageSet);
 doc.save(getArtifactsDir() + "ImageSaveOptions.ExportVariousPageRanges.tiff", imageOptions);
 
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| ranges | [PageRange\[\]](../../com.aspose.words/pagerange/) | Arreglo de rangos de página. |

### getAll() {#getAll}
```
public static PageSet getAll()
```


Obtiene un conjunto con todas las páginas del documento en su orden original.

 **Examples:** 

Muestra cómo exportar páginas impares del documento.

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


Obtiene un conjunto con todas las páginas pares del documento en su orden original.

 **Remarks:** 

Las páginas pares tienen índices impares ya que los índices de página comienzan en cero.

 **Examples:** 

Muestra cómo exportar páginas impares del documento.

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


Obtiene un conjunto con todas las páginas impares del documento en su orden original.

 **Remarks:** 

Las páginas impares tienen índices pares ya que los índices de página comienzan en cero.

 **Examples:** 

Muestra cómo exportar páginas impares del documento.

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
