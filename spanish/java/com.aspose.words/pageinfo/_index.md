---
title: "PageInfo"
linktitle: "PageInfo"
second_title: "Aspose.Words para Java"
description: "Representa información sobre una página de documento particular en Java."
type: docs
weight: 513
url: /es/java/com.aspose.words/pageinfo/
---

**Inheritance:**
java.lang.Object
```
public class PageInfo
```

Representa información sobre una página de documento específica.

Para obtener más información, visite el artículo de documentación [ Rendering ][Rendering].

 **Remarks:** 

El ancho y alto de página devueltos por este objeto representan el tamaño "final" de la página, por ejemplo, ya están rotados a la orientación correcta.


[Rendering]: https://docs.aspose.com/words/java/rendering/
## Métodos

| Método | Descripción |
| --- | --- |
| [getColored()](#getColored) | Devuelve  true  si la página contiene contenido coloreado. |
| [getHeightInPoints()](#getHeightInPoints) | Obtiene la altura de la página en puntos. |
| [getLandscape()](#getLandscape) | Devuelve  true  si la orientación de la página especificada en el documento para esta página es horizontal. |
| [getPaperSize()](#getPaperSize) | Obtiene el tamaño del papel como enumeración. |
| [getPaperTray()](#getPaperTray) | Obtiene la bandeja de papel (cajón) para esta página según lo especificado en el documento. |
| [getSizeInPixels(float scale, float dpi)](#getSizeInPixels-float-float) | Calcula el tamaño de la página en píxeles para un factor de zoom y resolución especificados. |
| [getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)](#getSizeInPixels-float-float-float) | Calcula el tamaño de la página en píxeles para un factor de zoom y resolución especificados. |
| [getSizeInPoints()](#getSizeInPoints) | Obtiene el tamaño de la página en puntos. |
| [getWidthInPoints()](#getWidthInPoints) | Obtiene el ancho de la página en puntos. |
### getColored() {#getColored}
```
public boolean getColored()
```


Devuelve  true  si la página contiene contenido coloreado.

 **Examples:** 

Muestra cómo comprobar si la página está en color o no.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 // Check that the first page of the document is not colored.
 Assert.assertFalse(doc.getPageInfo(0).getColored());
 
```

Muestra cómo filtrar páginas según el color de la página.

```
{@code
 public void colorMode() throws Exception
 {
     // Load the document with 3 color pages and 2 black and white pages.
     Document doc = new Document("Colored pages.docx");

     // Print color pages to 'color' printer.
     int colorPagesPrinted = printPages(doc, "Microsoft Print to PDF", true);

     // Print black-and-white pages to 'black-and-white' printer.
     int nonColorPagesPrinted = printPages(doc, "Microsoft XPS Document Writer", false);

     // Verify that correct number of pages were printed in each case.
     Assert.assertEquals(3, colorPagesPrinted);
     Assert.assertEquals(3, nonColorPagesPrinted);
 }

 /// 
 /// Prints document pages filtered by color requirements.
 /// 
 /// The document to print.
 /// The name of the target printer.
 /// 
 /// true to print only color pages;
 /// false to print only black and white pages.
 /// 
 /// The number of pages actually printed.
 private int printPages(Document doc, String printerName, boolean colored) throws Exception
 {
     // Configure printer settings.
     PrinterJob printerJob = PrinterJob.getPrinterJob();

     // Select target printer.
     for (PrintService service : PrinterJob.lookupPrintServices()) {
         if (service.getName().equalsIgnoreCase(printerName)) {
             printerJob.setPrintService(service);
             break;
         }
     }

     // Create print document with color mode set to Normal.
     AsposeWordsPrintDocument printDoc = new AsposeWordsPrintDocument(doc);
     printDoc.setColorMode(ColorPrintMode.NORMAL);

     // Filter pages: skip color pages when printing black and white, and vice versa.
     printDoc.setPageIndexFilter(new ColorPagesFilter(doc, !colored));

     printerJob.setPrintable(printDoc);
     printerJob.print();

     return printDoc.getTotalPagesPrinted();
 }

 /// 
 /// A filter that selectively skips color or black-and-white pages during printing
 /// based on the document's page information and specified filtering mode.
 /// 
 /// 
 /// This filter implements the IIndexFilter interface to provide custom page selection
 /// logic for printing operations. It can be configured to either skip color pages
 /// (when printing only black-and-white content) or skip black-and-white pages
 /// (when printing only color content).
 /// 
 static class ColorPagesFilter implements IIndexFilter
 {
     private final Document doc;
     private final boolean skipColorPages;

     /**
 Initializes a new instance of the ColorPagesFilter class.
```

**Returns:**
boolean - verdadero si la página debe omitirse; de lo contrario, falso. /
### getHeightInPoints() {#getHeightInPoints}
```
public float getHeightInPoints()
```


Obtiene la altura de la página en puntos.

**Returns:**
float - La altura de la página en puntos.
### getLandscape() {#getLandscape}
```
public boolean getLandscape()
```


Devuelve  true  si la orientación de la página especificada en el documento para esta página es horizontal.

**Returns:**
boolean -  verdadero  si la orientación de la página especificada en el documento para esta página es horizontal.
### getPaperSize() {#getPaperSize}
```
public int getPaperSize()
```


Obtiene el tamaño del papel como enumeración.

**Returns:**
int - El tamaño del papel como enumeración. El valor devuelto es una de las constantes de [PaperSize](../../com.aspose.words/papersize/).
### getPaperTray() {#getPaperTray}
```
public int getPaperTray()
```


Obtiene la bandeja de papel (cajón) para esta página según lo especificado en el documento. El valor es específico de la implementación (impresora).

**Returns:**
int - La bandeja de papel (cajón) para esta página según lo especificado en el documento.
### getSizeInPixels(float scale, float dpi) {#getSizeInPixels-float-float}
```
public Dimension getSizeInPixels(float scale, float dpi)
```


Calcula el tamaño de la página en píxeles para un factor de zoom y resolución especificados.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| escala | float | El factor de zoom (1.0 es 100%). |
| dpi | float | La resolución (horizontal y vertical) para convertir de puntos a píxeles (puntos por pulgada). |

**Returns:**
java.awt.Dimension - El tamaño de la página en píxeles.
### getSizeInPixels(float scale, float horizontalDpi, float verticalDpi) {#getSizeInPixels-float-float-float}
```
public Dimension getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)
```


Calcula el tamaño de la página en píxeles para un factor de zoom y resolución especificados.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| escala | float | El factor de zoom (1.0 es 100%). |
| horizontalDpi | float | La resolución horizontal para convertir de puntos a píxeles (puntos por pulgada). |
| verticalDpi | float | La resolución vertical para convertir de puntos a píxeles (puntos por pulgada). |

**Returns:**
java.awt.Dimension - El tamaño de la página en píxeles.
### getSizeInPoints() {#getSizeInPoints}
```
public Point2D.Float getSizeInPoints()
```


Obtiene el tamaño de la página en puntos.

**Returns:**
java.awt.geom.Point2D.Float - El tamaño de la página en puntos.
### getWidthInPoints() {#getWidthInPoints}
```
public float getWidthInPoints()
```


Obtiene el ancho de la página en puntos.

**Returns:**
float - El ancho de la página en puntos.
