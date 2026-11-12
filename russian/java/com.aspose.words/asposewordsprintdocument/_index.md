---
title: "AsposeWordsPrintDocument"
linktitle: "AsposeWordsPrintDocument"
second_title: "Aspose.Words для Java"
description: "Предоставляет реализацию по умолчанию для печати Document в рамках Java‑печатающего фреймворка."
type: docs
weight: 20
url: /ru/java/com.aspose.words/asposewordsprintdocument/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.awt.print.Pageable, java.awt.print.Printable
```
public class AsposeWordsPrintDocument implements Pageable, Printable
```

Предоставляет реализацию по умолчанию для печати [Document](../../com.aspose.words/document/) в рамках Java‑печатающего фреймворка.

Чтобы узнать больше, посетите статью документации [ Printing a Document Programmatically or Using Dialogs ][Printing a Document Programmatically or Using Dialogs].

 **Remarks:** 

[AsposeWordsPrintDocument](../../com.aspose.words/asposewordsprintdocument/) overrides both **java.awt.print.Printable** and **java.awt.print.Pageable**.

Один документ Aspose.Words может состоять из нескольких разделов, которые задают страницы с разными размерами, ориентацией и лотками для бумаги. [AsposeWordsPrintDocument](../../com.aspose.words/asposewordsprintdocument/) следует использовать как **java.awt.print.Pageable**, чтобы корректно печатать каждый из разных размеров страниц, ориентацию и т.д.

С другой стороны, если документ состоит только из одного раздела, разработчик может использовать [AsposeWordsPrintDocument](../../com.aspose.words/asposewordsprintdocument/) как **java.awt.print.Printable**, чтобы повысить производительность печати.

 **Examples:** 

Показывает, как отслеживать прогресс печати.

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

Показывает пример класса для мониторинга прогресса печати.

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
## Конструкторы

| Конструктор | Описание |
| --- | --- |
| [AsposeWordsPrintDocument(Document document)](#AsposeWordsPrintDocument-com.aspose.words.Document) | Инициализирует новый экземпляр этого класса. |
## Методы

| Метод | Описание |
| --- | --- |
| [getColorMode()](#getColorMode) | Получает информацию о том, как печатаются нечёрные страницы, если устройство поддерживает цветную печать. |
| [getColorPagesPrinted()](#getColorPagesPrinted) | Получает количество страниц, напечатанных в цвете (т.е. |
| [getNumberOfPages()](#getNumberOfPages) |  |
| [getPageFormat(int pageIndex)](#getPageFormat-int) |  |
| [getPageIndexFilter()](#getPageIndexFilter) | Получает фильтр индекса, начинающегося с нуля, используемый для определения, какие страницы пропустить при печати. |
| [getPagesRemaining()](#getPagesRemaining) | Получает количество оставшихся страниц в текущем активном задании печати. |
| [getPrintable(int pageIndex)](#getPrintable-int) |  |
| [getTotalPagesPrinted()](#getTotalPagesPrinted) | Получает общее количество страниц, фактически напечатанных за время сеанса печати. |
| [print(Graphics graphics, PageFormat pageFormat, int pageIndex)](#print-java.awt.Graphics-java.awt.print.PageFormat-int) |  |
| [setColorMode(int value)](#setColorMode-int) | Устанавливает способ печати страниц без цвета, если устройство поддерживает цветную печать. |
| [setPageIndexFilter(IIndexFilter value)](#setPageIndexFilter-com.aspose.words.IIndexFilter) | Устанавливает фильтр индекса, начинающегося с нуля, используемый для определения, какие страницы пропустить при печати. |
### AsposeWordsPrintDocument(Document document) {#AsposeWordsPrintDocument-com.aspose.words.Document}
```
public AsposeWordsPrintDocument(Document document)
```


Инициализирует новый экземпляр этого класса.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document/) | Документ для печати. |

### getColorMode() {#getColorMode}
```
public int getColorMode()
```


Получает информацию о том, как печатаются нечёрные страницы, если устройство поддерживает цветную печать.

 **Remarks:** 

Не влияет на печать буклета.

**Returns:**
int — Как печатаются страницы без цвета, если устройство поддерживает цветную печать. Возвращаемое значение является одной из констант [ColorPrintMode](../../com.aspose.words/colorprintmode/).
### getColorPagesPrinted() {#getColorPagesPrinted}
```
public int getColorPagesPrinted()
```


Получает количество страниц, напечатанных в цвете (т.е. с PageSettings\#getColor().getColor() / PageSettings\#setColor(boolean).setColor(boolean) установленным в true).

**Returns:**
int — Количество страниц, напечатанных в цвете (т.е.
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| pageIndex | int |  |

**Returns:**
java.awt.print.PageFormat
### getPageIndexFilter() {#getPageIndexFilter}
```
public IIndexFilter getPageIndexFilter()
```


Получает фильтр индекса, начинающегося с нуля, используемый для определения, какие страницы пропустить при печати.

 **Remarks:** 

Обратите внимание, что если некоторые страницы пропущены, фактическое общее количество страниц для печати будет неизвестно до завершения процесса печати. Это может повлиять на отслеживание процесса печати, если изначально ожидаемое количество страниц превышает фактическое количество напечатанных.

 **Examples:** 

Показывает, как фильтровать страницы с использованием списка номеров страниц.

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


Получает количество оставшихся страниц в текущем активном задании печати.

 **Remarks:** 

Это значение обновляется автоматически по мере печати страниц, отражая текущий прогресс задания печати. Вне времени печати и в случае ошибок или прерываний задания печати значение может не соответствовать фактическому количеству ожидающих страниц.

 **Examples:** 

Показывает, как отслеживать прогресс печати.

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

Показывает пример класса для мониторинга прогресса печати.

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
int — Текущий номер печатаемой страницы. / public int getPrintingPage() \{ return printingPage; \} /\*\* Получает общее количество страниц для печати. Возвращает 0, когда печать не выполняется.
### getPrintable(int pageIndex) {#getPrintable-int}
```
public Printable getPrintable(int pageIndex)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| pageIndex | int |  |

**Returns:**
java.awt.print.Printable
### getTotalPagesPrinted() {#getTotalPagesPrinted}
```
public int getTotalPagesPrinted()
```


Получает общее количество страниц, фактически напечатанных за время сеанса печати.

 **Remarks:** 

Обновляется после завершения печати. Возвращает 0 до начала печати.

 **Examples:** 

Показывает, как фильтровать страницы в зависимости от их цвета.

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
int — true, если страницу следует пропустить; иначе false. /
### print(Graphics graphics, PageFormat pageFormat, int pageIndex) {#print-java.awt.Graphics-java.awt.print.PageFormat-int}
```
public int print(Graphics graphics, PageFormat pageFormat, int pageIndex)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| графика | java.awt.Graphics |  |
| pageFormat | java.awt.print.PageFormat |  |
| pageIndex | int |  |

**Returns:**
int
### setColorMode(int value) {#setColorMode-int}
```
public void setColorMode(int value)
```


Устанавливает способ печати страниц без цвета, если устройство поддерживает цветную печать.

 **Remarks:** 

Не влияет на печать буклета.

**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | int | Как печатаются страницы без цвета, если устройство поддерживает цветную печать. Значение должно быть одной из констант [ColorPrintMode](../../com.aspose.words/colorprintmode/). |

### setPageIndexFilter(IIndexFilter value) {#setPageIndexFilter-com.aspose.words.IIndexFilter}
```
public void setPageIndexFilter(IIndexFilter value)
```


Устанавливает фильтр индекса, начинающегося с нуля, используемый для определения, какие страницы пропустить при печати.

 **Remarks:** 

Обратите внимание, что если некоторые страницы пропущены, фактическое общее количество страниц для печати будет неизвестно до завершения процесса печати. Это может повлиять на отслеживание процесса печати, если изначально ожидаемое количество страниц превышает фактическое количество напечатанных.

 **Examples:** 

Показывает, как фильтровать страницы с использованием списка номеров страниц.

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
| Параметр | Тип | Описание |
| --- | --- | --- |
| value | [IIndexFilter](../../com.aspose.words/iindexfilter/) | Фильтр индекса, начинающегося с нуля, используемый для определения, какие страницы пропустить при печати. |

