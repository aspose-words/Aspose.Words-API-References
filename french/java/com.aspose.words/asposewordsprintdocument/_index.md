---
title: "AsposeWordsPrintDocument"
linktitle: "AsposeWordsPrintDocument"
second_title: "Aspose.Words pour Java"
description: "Fournit une implémentation par défaut pour l'impression d'un Document dans le framework d'impression Java."
type: docs
weight: 20
url: /fr/java/com.aspose.words/asposewordsprintdocument/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.awt.print.Pageable, java.awt.print.Printable
```
public class AsposeWordsPrintDocument implements Pageable, Printable
```

Fournit une implémentation par défaut pour l'impression d'un [Document](../../com.aspose.words/document/) dans le framework d'impression Java.

Pour en savoir plus, consultez l'article de documentation [ Printing a Document Programmatically or Using Dialogs ][Printing a Document Programmatically or Using Dialogs].

 **Remarks:** 

[AsposeWordsPrintDocument](../../com.aspose.words/asposewordsprintdocument/) overrides both **java.awt.print.Printable** and **java.awt.print.Pageable**.

Un seul document Aspose.Words peut être composé de plusieurs sections qui spécifient des pages avec différentes tailles, orientations et bacs à papier. [AsposeWordsPrintDocument](../../com.aspose.words/asposewordsprintdocument/) doit être utilisé comme **java.awt.print.Pageable** pour imprimer correctement chaque taille de papier, orientation, etc.

En revanche, si le document ne comporte qu'une seule section, le développeur peut utiliser [AsposeWordsPrintDocument](../../com.aspose.words/asposewordsprintdocument/) comme **java.awt.print.Printable** pour améliorer les performances d'impression.

 **Examples:** 

Montre comment surveiller la progression de l'impression.

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

Présente une classe d'exemple pour le suivi de la progression de l'impression.

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
## Constructors

| Constructor | Description |
| --- | --- |
| [AsposeWordsPrintDocument(Document document)](#AsposeWordsPrintDocument-com.aspose.words.Document) | Initialise une nouvelle instance de cette classe. |
## Méthodes

| Méthode | Description |
| --- | --- |
| [getColorMode()](#getColorMode) | Obtient la façon dont les pages non colorées sont imprimées si l'appareil prend en charge l'impression couleur. |
| [getColorPagesPrinted()](#getColorPagesPrinted) | Obtient le nombre de pages imprimées en couleur (c.-à-d. |
| [getNumberOfPages()](#getNumberOfPages) |  |
| [getPageFormat(int pageIndex)](#getPageFormat-int) |  |
| [getPageIndexFilter()](#getPageIndexFilter) | Obtient le filtre d'index basé sur zéro utilisé pour déterminer quelles pages sauter lors de l'impression. |
| [getPagesRemaining()](#getPagesRemaining) | Obtient le nombre de pages restantes dans le travail d'impression actuellement actif. |
| [getPrintable(int pageIndex)](#getPrintable-int) |  |
| [getTotalPagesPrinted()](#getTotalPagesPrinted) | Obtient le nombre total de pages réellement imprimées pendant la session d'impression. |
| [print(Graphics graphics, PageFormat pageFormat, int pageIndex)](#print-java.awt.Graphics-java.awt.print.PageFormat-int) |  |
| [setColorMode(int value)](#setColorMode-int) | Définit comment les pages non colorées sont imprimées si l’appareil prend en charge l’impression couleur. |
| [setPageIndexFilter(IIndexFilter value)](#setPageIndexFilter-com.aspose.words.IIndexFilter) | Définit le filtre d’index basé sur zéro utilisé pour déterminer quelles pages ignorer lors de l’impression. |
### AsposeWordsPrintDocument(Document document) {#AsposeWordsPrintDocument-com.aspose.words.Document}
```
public AsposeWordsPrintDocument(Document document)
```


Initialise une nouvelle instance de cette classe.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document/) | Le document à imprimer. |

### getColorMode() {#getColorMode}
```
public int getColorMode()
```


Obtient la façon dont les pages non colorées sont imprimées si l'appareil prend en charge l'impression couleur.

 **Remarks:** 

N’affecte pas l’impression de livret.

**Returns:**
int - Comment les pages non colorées sont imprimées si l’appareil prend en charge l’impression couleur. La valeur retournée est l’une des constantes [ColorPrintMode](../../com.aspose.words/colorprintmode/).
### getColorPagesPrinted() {#getColorPagesPrinted}
```
public int getColorPagesPrinted()
```


Obtient le nombre de pages imprimées en couleur (c.-à-d. avec PageSettings\#getColor().getColor() / PageSettings\#setColor(boolean).setColor(boolean) réglé sur true).

**Returns:**
int - Le nombre de pages imprimées en couleur (c.-à-d.
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
| Paramètre | Type | Description |
| --- | --- | --- |
| pageIndex | int |  |

**Returns:**
java.awt.print.PageFormat
### getPageIndexFilter() {#getPageIndexFilter}
```
public IIndexFilter getPageIndexFilter()
```


Obtient le filtre d'index basé sur zéro utilisé pour déterminer quelles pages sauter lors de l'impression.

 **Remarks:** 

Veuillez noter que si certaines pages sont ignorées, le nombre total réel de pages à imprimer ne sera pas connu avant la fin du processus d’impression. Cela peut affecter le suivi du processus d’impression si le nombre de pages prévu initialement est supérieur au nombre réellement imprimé.

 **Examples:** 

Montre comment filtrer les pages à l’aide d’une liste de numéros de pages.

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


Obtient le nombre de pages restantes dans le travail d'impression actuellement actif.

 **Remarks:** 

Cette valeur est mise à jour automatiquement au fur et à mesure que les pages sont imprimées, reflétant la progression du travail d’impression en cours. En dehors du temps d’impression et en cas d’erreurs ou d’interruptions du travail d’impression, la valeur peut ne pas refléter le nombre réel de pages en attente.

 **Examples:** 

Montre comment surveiller la progression de l'impression.

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

Présente une classe d'exemple pour le suivi de la progression de l'impression.

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
int - Le numéro de page actuel en cours d’impression. / public int getPrintingPage() \{ return printingPage; \} /\*\* Obtient le nombre total de pages à imprimer. Retourne 0 lorsqu’aucune impression n’est en cours.
### getPrintable(int pageIndex) {#getPrintable-int}
```
public Printable getPrintable(int pageIndex)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| pageIndex | int |  |

**Returns:**
java.awt.print.Printable
### getTotalPagesPrinted() {#getTotalPagesPrinted}
```
public int getTotalPagesPrinted()
```


Obtient le nombre total de pages réellement imprimées pendant la session d'impression.

 **Remarks:** 

Mis à jour après la fin de l’impression. Retourne 0 avant le démarrage de l’impression.

 **Examples:** 

Montre comment filtrer les pages en fonction de la couleur de la page.

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
int - true si la page doit être ignorée ; sinon, false. /
### print(Graphics graphics, PageFormat pageFormat, int pageIndex) {#print-java.awt.Graphics-java.awt.print.PageFormat-int}
```
public int print(Graphics graphics, PageFormat pageFormat, int pageIndex)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| graphismes | java.awt.Graphics |  |
| pageFormat | java.awt.print.PageFormat |  |
| pageIndex | int |  |

**Returns:**
int
### setColorMode(int value) {#setColorMode-int}
```
public void setColorMode(int value)
```


Définit comment les pages non colorées sont imprimées si l’appareil prend en charge l’impression couleur.

 **Remarks:** 

N’affecte pas l’impression de livret.

**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| value | int | Comment les pages non colorées sont imprimées si l’appareil prend en charge l’impression couleur. La valeur doit être l’une des constantes [ColorPrintMode](../../com.aspose.words/colorprintmode/). |

### setPageIndexFilter(IIndexFilter value) {#setPageIndexFilter-com.aspose.words.IIndexFilter}
```
public void setPageIndexFilter(IIndexFilter value)
```


Définit le filtre d’index basé sur zéro utilisé pour déterminer quelles pages ignorer lors de l’impression.

 **Remarks:** 

Veuillez noter que si certaines pages sont ignorées, le nombre total réel de pages à imprimer ne sera pas connu avant la fin du processus d’impression. Cela peut affecter le suivi du processus d’impression si le nombre de pages prévu initialement est supérieur au nombre réellement imprimé.

 **Examples:** 

Montre comment filtrer les pages à l’aide d’une liste de numéros de pages.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| value | [IIndexFilter](../../com.aspose.words/iindexfilter/) | Le filtre d’index basé sur zéro utilisé pour déterminer quelles pages ignorer lors de l’impression. |

