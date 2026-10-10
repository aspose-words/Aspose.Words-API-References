---
title: "AsposeWordsPrintDocument"
linktitle: "AsposeWordsPrintDocument"
second_title: "Aspose.Words para Java"
description: "Proporciona una implementación predeterminada para la impresión de un Document dentro del framework de impresión de Java."
type: docs
weight: 20
url: /es/java/com.aspose.words/asposewordsprintdocument/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.awt.print.Pageable, java.awt.print.Printable
```
public class AsposeWordsPrintDocument implements Pageable, Printable
```

Proporciona una implementación predeterminada para la impresión de un [Document](../../com.aspose.words/document/) dentro del framework de impresión de Java.

Para obtener más información, visite el artículo de documentación [ Printing a Document Programmatically or Using Dialogs ][Printing a Document Programmatically or Using Dialogs].

 **Remarks:** 

[AsposeWordsPrintDocument](../../com.aspose.words/asposewordsprintdocument/) overrides both **java.awt.print.Printable** and **java.awt.print.Pageable**.

Un solo documento Aspose.Words puede constar de varias secciones que especifican páginas con diferentes tamaños, orientación y bandejas de papel. [AsposeWordsPrintDocument](../../com.aspose.words/asposewordsprintdocument/) debe usarse como **java.awt.print.Pageable** para imprimir correctamente cada uno de los diferentes tamaños de papel, orientación, etc.

Por otro lado, si el documento consta de una sola sección, el desarrollador puede usar [AsposeWordsPrintDocument](../../com.aspose.words/asposewordsprintdocument/) como **java.awt.print.Printable** para mejorar el rendimiento de la impresión.

 **Examples:** 

Muestra cómo monitorear el progreso de la impresión.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Create a special Aspose.Words implementation of the Java PrintDocument class
 AsposeWordsPrintDocument printDoc = new AsposeWordsPrintDocument(doc);

 // In Java, printer settings are handled through PrinterJob.
 PrinterJob printerJob = PrinterJob.getPrinterJob();
 printerJob.setPrintable(printDoc);

 // Initialize the custom printing tracker.
 PrintTracker printTracker = new PrintTracker(printDoc);

 printerJob.print();

 // Write the event log.
 for (String eventString : printTracker.getEventLog()) {
     System.out.println(eventString);
 }
 
```

Muestra una clase de ejemplo para monitorear el progreso de la impresión.

```
{@code
 /// 
 /// Tracks printing progress of an Aspose.Words document and logs printing events.
 /// 
 /**
 Tracks printing progress of an Aspose.Words document and logs printing events.
 Note: Java version doesn't have the same event system as .NET, so this implementation
 wraps the AsposeWordsPrintDocument to provide similar functionality.
 /
 class PrintTracker implements Printable {
     private final AsposeWordsPrintDocument printDocument;
     private int printingPage = -1;
     private int totalPages = 0;
     private final List eventLog = new ArrayList<>();
     private boolean isPrinting = false;

     /**
 Initializes a new instance of the PrintTracker class
 and wraps the specified Aspose.Words print document.
```


[Printing a Document Programmatically or Using Dialogs]: https://docs.aspose.com/words/java/print-a-document-programmatically-or-using-dialogs/
## Constructores

| Constructor | Descripción |
| --- | --- |
| [AsposeWordsPrintDocument(Document document)](#AsposeWordsPrintDocument-com.aspose.words.Document) | Inicializa una nueva instancia de esta clase. |
## Métodos

| Método | Descripción |
| --- | --- |
| [getColorMode()](#getColorMode) | Obtiene cómo se imprimen las páginas sin color si el dispositivo admite impresión en color. |
| [getColorPagesPrinted()](#getColorPagesPrinted) | Obtiene el número de páginas impresas en color (es decir, |
| [getNumberOfPages()](#getNumberOfPages) |  |
| [getPageFormat(int pageIndex)](#getPageFormat-int) |  |
| [getPageIndexFilter()](#getPageIndexFilter) | Obtiene el filtro de índice basado en cero usado para determinar qué páginas omitir durante la impresión. |
| [getPagesRemaining()](#getPagesRemaining) | Obtiene el número de páginas restantes en el trabajo de impresión actualmente activo. |
| [getPrintable(int pageIndex)](#getPrintable-int) |  |
| [getTotalPagesPrinted()](#getTotalPagesPrinted) | Obtiene el número total de páginas realmente impresas durante la sesión de impresión. |
| [print(Graphics graphics, PageFormat pageFormat, int pageIndex)](#print-java.awt.Graphics-java.awt.print.PageFormat-int) |  |
| [setColorMode(int value)](#setColorMode-int) | Establece cómo se imprimen las páginas sin color si el dispositivo admite impresión a color. |
| [setPageIndexFilter(IIndexFilter value)](#setPageIndexFilter-com.aspose.words.IIndexFilter) | Establece el filtro de índice basado en cero utilizado para determinar qué páginas omitir durante la impresión. |
### AsposeWordsPrintDocument(Document document) {#AsposeWordsPrintDocument-com.aspose.words.Document}
```
public AsposeWordsPrintDocument(Document document)
```


Inicializa una nueva instancia de esta clase.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document/) | El documento a imprimir. |

### getColorMode() {#getColorMode}
```
public int getColorMode()
```


Obtiene cómo se imprimen las páginas sin color si el dispositivo admite impresión en color.

 **Remarks:** 

No afecta la impresión de folletos.

**Returns:**
int - Cómo se imprimen las páginas sin color si el dispositivo admite impresión a color. El valor devuelto es una de las constantes de [ColorPrintMode](../../com.aspose.words/colorprintmode/).
### getColorPagesPrinted() {#getColorPagesPrinted}
```
public int getColorPagesPrinted()
```


Obtiene el número de páginas impresas en color (es decir, con PageSettings\#getColor().getColor() / PageSettings\#setColor(boolean).setColor(boolean) establecido en true).

**Returns:**
int - El número de páginas impresas en color (es decir,
### getNumberOfPages() {#getNumberOfPages}
```
public int getNumberOfPages()
```




**Returns:**
int
### getPageFormat(int pageIndex) {#getPageFormat-int}
```
public PageFormat getPageFormat(int pageIndex)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pageIndex | int |  |

**Returns:**
java.awt.print.PageFormat
### getPageIndexFilter() {#getPageIndexFilter}
```
public IIndexFilter getPageIndexFilter()
```


Obtiene el filtro de índice basado en cero usado para determinar qué páginas omitir durante la impresión.

 **Remarks:** 

Tenga en cuenta que si se omiten algunas páginas, el número total real de páginas a imprimir no se conocerá hasta que se complete el proceso de impresión. Esto puede afectar el seguimiento del proceso de impresión si el número de páginas esperado inicialmente es mayor que el número realmente impreso.

 **Examples:** 

Muestra cómo filtrar páginas usando una lista de números de página.

```
{@code
 public void pageIndexFilter() throws Exception
 {
     Document doc = new Document("Rendering.docx");

     // Configure printer settings and create print document.
     PrinterJob printerJob = PrinterJob.getPrinterJob();
     printerJob.setPrintService(printerJob.getPrintService());

     // Create Aspose.Words print document.
     AsposeWordsPrintDocument printDoc = new AsposeWordsPrintDocument(doc);

     // Set the printer name.
     PrintService[] printServices = PrinterJob.lookupPrintServices();
     for (PrintService service : printServices) {
         if (service.getName().equalsIgnoreCase("Microsoft Print to PDF")) {
             printerJob.setPrintService(service);
             break;
         }
     }

     // The test document has 5 pages. To skip pages 2, 4, and 5,
     // specify the zero-based indices of pages to exclude.
     HashSet pagesToSkip = new HashSet<>(Arrays.asList(1, 3, 4));

     // Apply the page filter to skip specified pages.
     printDoc.setPageIndexFilter(new PrintPagesFilter(pagesToSkip));

     // Initialize custom printing tracker (optional).
     PrintTracker printTracker = new PrintTracker(printDoc);

     // Print the document (only pages 1 and 3 will be printed).
     printerJob.setPrintable(printDoc);
     printerJob.print();
 }

 /// 
 /// Filter for skipping specified pages during printing.
 /// 
 public final class PrintPagesFilter implements IIndexFilter {
     private final HashSet pagesToSkip;

     /// 
     /// Initializes a new instance of the  class.
     /// 
     /// The collection of page indices to skip.
     public PrintPagesFilter(HashSet pagesToSkip) {
         if (pagesToSkip == null)
             throw new IllegalArgumentException("pagesToSkip cannot be null.");
         this.pagesToSkip = pagesToSkip;
     }
```

**Returns:**
[IIndexFilter](../../com.aspose.words/iindexfilter/) - true if the page should be skipped; otherwise, false. /
### getPagesRemaining() {#getPagesRemaining}
```
public int getPagesRemaining()
```


Obtiene el número de páginas restantes en el trabajo de impresión actualmente activo.

 **Remarks:** 

Este valor se actualiza automáticamente a medida que se imprimen las páginas, reflejando el progreso actual del trabajo de impresión. Fuera del tiempo de impresión y en caso de errores o interrupciones del trabajo de impresión, el valor puede no reflejar el número real de páginas pendientes.

 **Examples:** 

Muestra cómo monitorear el progreso de la impresión.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 // Create a special Aspose.Words implementation of the Java PrintDocument class
 AsposeWordsPrintDocument printDoc = new AsposeWordsPrintDocument(doc);

 // In Java, printer settings are handled through PrinterJob.
 PrinterJob printerJob = PrinterJob.getPrinterJob();
 printerJob.setPrintable(printDoc);

 // Initialize the custom printing tracker.
 PrintTracker printTracker = new PrintTracker(printDoc);

 printerJob.print();

 // Write the event log.
 for (String eventString : printTracker.getEventLog()) {
     System.out.println(eventString);
 }
 
```

Muestra una clase de ejemplo para monitorear el progreso de la impresión.

```
{@code
 /// 
 /// Tracks printing progress of an Aspose.Words document and logs printing events.
 /// 
 /**
 Tracks printing progress of an Aspose.Words document and logs printing events.
 Note: Java version doesn't have the same event system as .NET, so this implementation
 wraps the AsposeWordsPrintDocument to provide similar functionality.
 /
 class PrintTracker implements Printable {
     private final AsposeWordsPrintDocument printDocument;
     private int printingPage = -1;
     private int totalPages = 0;
     private final List eventLog = new ArrayList<>();
     private boolean isPrinting = false;

     /**
 Initializes a new instance of the PrintTracker class
 and wraps the specified Aspose.Words print document.
```

**Returns:**
int - El número de página actual que se está imprimiendo. / public int getPrintingPage() \{ return printingPage; \} /\*\* Obtiene el número total de páginas a imprimir. Devuelve 0 cuando no hay impresión en curso.
### getPrintable(int pageIndex) {#getPrintable-int}
```
public Printable getPrintable(int pageIndex)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pageIndex | int |  |

**Returns:**
java.awt.print.Printable
### getTotalPagesPrinted() {#getTotalPagesPrinted}
```
public int getTotalPagesPrinted()
```


Obtiene el número total de páginas realmente impresas durante la sesión de impresión.

 **Remarks:** 

Actualizado después de que la impresión se complete. Devuelve 0 antes de que comience la impresión.

 **Examples:** 

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
int - true si la página debe omitirse; de lo contrario, false. /
### print(Graphics graphics, PageFormat pageFormat, int pageIndex) {#print-java.awt.Graphics-java.awt.print.PageFormat-int}
```
public int print(Graphics graphics, PageFormat pageFormat, int pageIndex)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| gráficos | java.awt.Graphics |  |
| pageFormat | java.awt.print.PageFormat |  |
| pageIndex | int |  |

**Returns:**
int
### setColorMode(int value) {#setColorMode-int}
```
public void setColorMode(int value)
```


Establece cómo se imprimen las páginas sin color si el dispositivo admite impresión a color.

 **Remarks:** 

No afecta la impresión de folletos.

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | int | Cómo se imprimen las páginas sin color si el dispositivo admite impresión a color. El valor debe ser una de las constantes de [ColorPrintMode](../../com.aspose.words/colorprintmode/). |

### setPageIndexFilter(IIndexFilter value) {#setPageIndexFilter-com.aspose.words.IIndexFilter}
```
public void setPageIndexFilter(IIndexFilter value)
```


Establece el filtro de índice basado en cero utilizado para determinar qué páginas omitir durante la impresión.

 **Remarks:** 

Tenga en cuenta que si se omiten algunas páginas, el número total real de páginas a imprimir no se conocerá hasta que se complete el proceso de impresión. Esto puede afectar el seguimiento del proceso de impresión si el número de páginas esperado inicialmente es mayor que el número realmente impreso.

 **Examples:** 

Muestra cómo filtrar páginas usando una lista de números de página.

```
{@code
 public void pageIndexFilter() throws Exception
 {
     Document doc = new Document("Rendering.docx");

     // Configure printer settings and create print document.
     PrinterJob printerJob = PrinterJob.getPrinterJob();
     printerJob.setPrintService(printerJob.getPrintService());

     // Create Aspose.Words print document.
     AsposeWordsPrintDocument printDoc = new AsposeWordsPrintDocument(doc);

     // Set the printer name.
     PrintService[] printServices = PrinterJob.lookupPrintServices();
     for (PrintService service : printServices) {
         if (service.getName().equalsIgnoreCase("Microsoft Print to PDF")) {
             printerJob.setPrintService(service);
             break;
         }
     }

     // The test document has 5 pages. To skip pages 2, 4, and 5,
     // specify the zero-based indices of pages to exclude.
     HashSet pagesToSkip = new HashSet<>(Arrays.asList(1, 3, 4));

     // Apply the page filter to skip specified pages.
     printDoc.setPageIndexFilter(new PrintPagesFilter(pagesToSkip));

     // Initialize custom printing tracker (optional).
     PrintTracker printTracker = new PrintTracker(printDoc);

     // Print the document (only pages 1 and 3 will be printed).
     printerJob.setPrintable(printDoc);
     printerJob.print();
 }

 /// 
 /// Filter for skipping specified pages during printing.
 /// 
 public final class PrintPagesFilter implements IIndexFilter {
     private final HashSet pagesToSkip;

     /// 
     /// Initializes a new instance of the  class.
     /// 
     /// The collection of page indices to skip.
     public PrintPagesFilter(HashSet pagesToSkip) {
         if (pagesToSkip == null)
             throw new IllegalArgumentException("pagesToSkip cannot be null.");
         this.pagesToSkip = pagesToSkip;
     }
```

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| value | [IIndexFilter](../../com.aspose.words/iindexfilter/) | El filtro de índice basado en cero utilizado para determinar qué páginas omitir durante la impresión. |

