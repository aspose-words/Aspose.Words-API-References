---
title: "AsposeWordsPrintDocument"
linktitle: "AsposeWordsPrintDocument"
second_title: "Aspose.Words für Java"
description: "Stellt eine Standardimplementierung für das Drucken eines Dokuments innerhalb des Java-Druckframeworks bereit."
type: docs
weight: 20
url: /de/java/com.aspose.words/asposewordsprintdocument/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.awt.print.Pageable, java.awt.print.Printable
```
public class AsposeWordsPrintDocument implements Pageable, Printable
```

Stellt eine Standardimplementierung für das Drucken eines [Document](../../com.aspose.words/document/) innerhalb des Java-Druckframeworks bereit.

Weitere Informationen finden Sie im Dokumentationsartikel [ Printing a Document Programmatically or Using Dialogs ][Printing a Document Programmatically or Using Dialogs].

 **Remarks:** 

[AsposeWordsPrintDocument](../../com.aspose.words/asposewordsprintdocument/) overrides both **java.awt.print.Printable** and **java.awt.print.Pageable**.

Ein einzelnes Aspose.Words-Dokument kann aus mehreren Abschnitten bestehen, die Seiten mit unterschiedlichen Größen, Ausrichtungen und Papierfächern festlegen. [AsposeWordsPrintDocument](../../com.aspose.words/asposewordsprintdocument/) sollte als **java.awt.print.Pageable** verwendet werden, um jede der verschiedenen Papiergrößen, Ausrichtungen usw. korrekt zu drucken.

Andererseits, wenn das Dokument nur aus einem einzigen Abschnitt besteht, kann der Entwickler [AsposeWordsPrintDocument](../../com.aspose.words/asposewordsprintdocument/) als **java.awt.print.Printable** verwenden, um die Druckleistung zu verbessern.

 **Examples:** 

Zeigt, wie der Druckfortschritt überwacht wird.

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

Zeigt eine Beispielklasse zur Überwachung des Druckfortschritts.

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
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [AsposeWordsPrintDocument(Document document)](#AsposeWordsPrintDocument-com.aspose.words.Document) | Initialisiert eine neue Instanz dieser Klasse. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getColorMode()](#getColorMode) | Ermittelt, wie nichtfarbige Seiten gedruckt werden, wenn das Gerät Farbdruck unterstützt. |
| [getColorPagesPrinted()](#getColorPagesPrinted) | Ermittelt die Anzahl der farbig gedruckten Seiten (d.h. |
| [getNumberOfPages()](#getNumberOfPages) |  |
| [getPageFormat(int pageIndex)](#getPageFormat-int) |  |
| [getPageIndexFilter()](#getPageIndexFilter) | Ermittelt den nullbasierten Indexfilter, der verwendet wird, um zu bestimmen, welche Seiten beim Drucken übersprungen werden. |
| [getPagesRemaining()](#getPagesRemaining) | Ermittelt die verbleibende Seitenzahl im aktuell aktiven Druckauftrag. |
| [getPrintable(int pageIndex)](#getPrintable-int) |  |
| [getTotalPagesPrinted()](#getTotalPagesPrinted) | Ermittelt die Gesamtzahl der tatsächlich während der Drucksitzung gedruckten Seiten. |
| [print(Graphics graphics, PageFormat pageFormat, int pageIndex)](#print-java.awt.Graphics-java.awt.print.PageFormat-int) |  |
| [setColorMode(int value)](#setColorMode-int) | Legt fest, wie nichtfarbige Seiten gedruckt werden, wenn das Gerät Farbdruck unterstützt. |
| [setPageIndexFilter(IIndexFilter value)](#setPageIndexFilter-com.aspose.words.IIndexFilter) | Legt den nullbasierten Indexfilter fest, der verwendet wird, um zu bestimmen, welche Seiten beim Drucken übersprungen werden. |
### AsposeWordsPrintDocument(Document document) {#AsposeWordsPrintDocument-com.aspose.words.Document}
```
public AsposeWordsPrintDocument(Document document)
```


Initialisiert eine neue Instanz dieser Klasse.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document/) | Das zu druckende Dokument. |

### getColorMode() {#getColorMode}
```
public int getColorMode()
```


Ermittelt, wie nichtfarbige Seiten gedruckt werden, wenn das Gerät Farbdruck unterstützt.

 **Remarks:** 

Beeinflusst den Heftdruck nicht.

**Returns:**
int - Wie nichtfarbige Seiten gedruckt werden, wenn das Gerät Farbdruck unterstützt. Der zurückgegebene Wert ist einer der Konstanten von [ColorPrintMode](../../com.aspose.words/colorprintmode/).
### getColorPagesPrinted() {#getColorPagesPrinted}
```
public int getColorPagesPrinted()
```


Ermittelt die Anzahl der farbig gedruckten Seiten (d.h. mit PageSettings\#getColor().getColor() / PageSettings\#setColor(boolean).setColor(boolean) auf true gesetzt).

**Returns:**
int - Die Anzahl der farbig gedruckten Seiten (d.h.
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pageIndex | int |  |

**Returns:**
java.awt.print.PageFormat
### getPageIndexFilter() {#getPageIndexFilter}
```
public IIndexFilter getPageIndexFilter()
```


Ermittelt den nullbasierten Indexfilter, der verwendet wird, um zu bestimmen, welche Seiten beim Drucken übersprungen werden.

 **Remarks:** 

Bitte beachten Sie, dass, wenn einige Seiten übersprungen werden, die tatsächliche Gesamtzahl der zu druckenden Seiten erst bekannt ist, wenn der Druckvorgang abgeschlossen ist. Dies kann die Verfolgung des Druckprozesses beeinträchtigen, wenn die ursprünglich erwartete Seitenzahl größer ist als die tatsächlich gedruckte.

 **Examples:** 

Zeigt, wie Seiten mithilfe einer Seitenzahlenliste gefiltert werden.

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


Ermittelt die verbleibende Seitenzahl im aktuell aktiven Druckauftrag.

 **Remarks:** 

Dieser Wert wird automatisch aktualisiert, während Seiten gedruckt werden, und spiegelt den Fortschritt des aktuellen Druckauftrags wider. Außerhalb der Druckzeit und im Falle von Druckauftragsfehlern oder Unterbrechungen kann der Wert die tatsächliche Anzahl ausstehender Seiten nicht widerspiegeln.

 **Examples:** 

Zeigt, wie der Druckfortschritt überwacht wird.

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

Zeigt eine Beispielklasse zur Überwachung des Druckfortschritts.

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
int - Die aktuelle zu druckende Seitenzahl. / public int getPrintingPage() \{ return printingPage; \} /\*\* Ermittelt die Gesamtzahl der zu druckenden Seiten. Gibt 0 zurück, wenn kein Druckvorgang läuft.
### getPrintable(int pageIndex) {#getPrintable-int}
```
public Printable getPrintable(int pageIndex)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pageIndex | int |  |

**Returns:**
java.awt.print.Printable
### getTotalPagesPrinted() {#getTotalPagesPrinted}
```
public int getTotalPagesPrinted()
```


Ermittelt die Gesamtzahl der tatsächlich während der Drucksitzung gedruckten Seiten.

 **Remarks:** 

Wird aktualisiert, nachdem der Druck abgeschlossen ist. Gibt 0 zurück, bevor der Druck beginnt.

 **Examples:** 

Zeigt, wie Seiten basierend auf ihrer Farbe gefiltert werden.

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
int - true, wenn die Seite übersprungen werden soll; andernfalls false. /
### print(Graphics graphics, PageFormat pageFormat, int pageIndex) {#print-java.awt.Graphics-java.awt.print.PageFormat-int}
```
public int print(Graphics graphics, PageFormat pageFormat, int pageIndex)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Grafik | java.awt.Graphics |  |
| pageFormat | java.awt.print.PageFormat |  |
| pageIndex | int |  |

**Returns:**
int
### setColorMode(int value) {#setColorMode-int}
```
public void setColorMode(int value)
```


Legt fest, wie nichtfarbige Seiten gedruckt werden, wenn das Gerät Farbdruck unterstützt.

 **Remarks:** 

Beeinflusst den Heftdruck nicht.

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Wie nicht‑farbige Seiten gedruckt werden, wenn das Gerät Farbdruck unterstützt. Der Wert muss einer der Konstanten von [ColorPrintMode](../../com.aspose.words/colorprintmode/) sein. |

### setPageIndexFilter(IIndexFilter value) {#setPageIndexFilter-com.aspose.words.IIndexFilter}
```
public void setPageIndexFilter(IIndexFilter value)
```


Legt den nullbasierten Indexfilter fest, der verwendet wird, um zu bestimmen, welche Seiten beim Drucken übersprungen werden.

 **Remarks:** 

Bitte beachten Sie, dass, wenn einige Seiten übersprungen werden, die tatsächliche Gesamtzahl der zu druckenden Seiten erst bekannt ist, wenn der Druckvorgang abgeschlossen ist. Dies kann die Verfolgung des Druckprozesses beeinträchtigen, wenn die ursprünglich erwartete Seitenzahl größer ist als die tatsächlich gedruckte.

 **Examples:** 

Zeigt, wie Seiten mithilfe einer Seitenzahlenliste gefiltert werden.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | [IIndexFilter](../../com.aspose.words/iindexfilter/) | Der nullbasierte Indexfilter, der verwendet wird, um zu bestimmen, welche Seiten beim Drucken übersprungen werden sollen. |

