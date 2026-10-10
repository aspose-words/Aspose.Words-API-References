---
title: "AsposeWordsPrintDocument"
linktitle: "AsposeWordsPrintDocument"
second_title: "Aspose.Words لـ Java"
description: "يوفر تنفيذًا افتراضيًا لطباعة مستند داخل إطار الطباعة في Java."
type: docs
weight: 20
url: /ar/java/com.aspose.words/asposewordsprintdocument/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.awt.print.Pageable, java.awt.print.Printable
```
public class AsposeWordsPrintDocument implements Pageable, Printable
```

يوفر تنفيذًا افتراضيًا لطباعة [Document](../../com.aspose.words/document/) داخل إطار الطباعة في Java.

لمزيد من المعلومات، زر مقالة الوثائق [ Printing a Document Programmatically or Using Dialogs ][Printing a Document Programmatically or Using Dialogs].

 **Remarks:** 

[AsposeWordsPrintDocument](../../com.aspose.words/asposewordsprintdocument/) overrides both **java.awt.print.Printable** and **java.awt.print.Pageable**.

يمكن أن يتكون مستند Aspose.Words واحد من عدة أقسام تحدد صفحات بأحجام مختلفة، واتجاهات وصواني ورق. يجب استخدام [AsposeWordsPrintDocument](../../com.aspose.words/asposewordsprintdocument/) كـ **java.awt.print.Pageable** لطباعة كل حجم ورقة مختلف، واتجاهه، إلخ.

من ناحية أخرى، إذا كان المستند يتكون من قسم واحد فقط، يمكن للمطور استخدام [AsposeWordsPrintDocument](../../com.aspose.words/asposewordsprintdocument/) كـ **java.awt.print.Printable** لتحسين أداء الطباعة.

 **Examples:** 

يعرض كيفية مراقبة تقدم الطباعة.

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

يعرض فئة مثال لمراقبة تقدم الطباعة.

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
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [AsposeWordsPrintDocument(Document document)](#AsposeWordsPrintDocument-com.aspose.words.Document) | يقوم بتهيئة نسخة جديدة من هذه الفئة. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getColorMode()](#getColorMode) | يحصل على طريقة طباعة الصفحات غير الملونة إذا كان الجهاز يدعم الطباعة بالألوان. |
| [getColorPagesPrinted()](#getColorPagesPrinted) | يحصل على عدد الصفحات المطبوعة بالألوان (i.e. |
| [getNumberOfPages()](#getNumberOfPages) |  |
| [getPageFormat(int pageIndex)](#getPageFormat-int) |  |
| [getPageIndexFilter()](#getPageIndexFilter) | يحصل على مرشح الفهرس الصفري المستخدم لتحديد الصفحات التي يجب تخطيها أثناء الطباعة. |
| [getPagesRemaining()](#getPagesRemaining) | يحصل على عدد الصفحات المتبقية في مهمة الطباعة النشطة حاليًا. |
| [getPrintable(int pageIndex)](#getPrintable-int) |  |
| [getTotalPagesPrinted()](#getTotalPagesPrinted) | يحصل على إجمالي عدد الصفحات التي تم طباعتها فعليًا خلال جلسة الطباعة. |
| [print(Graphics graphics, PageFormat pageFormat, int pageIndex)](#print-java.awt.Graphics-java.awt.print.PageFormat-int) |  |
| [setColorMode(int value)](#setColorMode-int) | يضبط كيفية طباعة الصفحات غير الملونة إذا كان الجهاز يدعم الطباعة بالألوان. |
| [setPageIndexFilter(IIndexFilter value)](#setPageIndexFilter-com.aspose.words.IIndexFilter) | يضبط مرشح الفهرس الصفري المستخدم لتحديد الصفحات التي يجب تخطيها أثناء الطباعة. |
### AsposeWordsPrintDocument(Document document) {#AsposeWordsPrintDocument-com.aspose.words.Document}
```
public AsposeWordsPrintDocument(Document document)
```


يقوم بتهيئة نسخة جديدة من هذه الفئة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document/) | المستند للطباعة. |

### getColorMode() {#getColorMode}
```
public int getColorMode()
```


يحصل على طريقة طباعة الصفحات غير الملونة إذا كان الجهاز يدعم الطباعة بالألوان.

 **Remarks:** 

لا يؤثر على طباعة الكتيب.

**Returns:**
int - كيفية طباعة الصفحات غير الملونة إذا كان الجهاز يدعم الطباعة بالألوان. القيمة المرجعة هي واحدة من ثوابت [ColorPrintMode](../../com.aspose.words/colorprintmode/).
### getColorPagesPrinted() {#getColorPagesPrinted}
```
public int getColorPagesPrinted()
```


يحصل على عدد الصفحات المطبوعة بالألوان (أي باستخدام PageSettings\#getColor().getColor() / PageSettings\#setColor(boolean).setColor(boolean) تم تعيينه إلى true).

**Returns:**
int - عدد الصفحات المطبوعة بالألوان (أي
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| pageIndex | int |  |

**Returns:**
java.awt.print.PageFormat
### getPageIndexFilter() {#getPageIndexFilter}
```
public IIndexFilter getPageIndexFilter()
```


يحصل على مرشح الفهرس الصفري المستخدم لتحديد الصفحات التي يجب تخطيها أثناء الطباعة.

 **Remarks:** 

يرجى ملاحظة أنه إذا تم تخطي بعض الصفحات، فلن يُعرف العدد الإجمالي الفعلي للصفحات التي يجب طباعتها حتى يكتمل عملية الطباعة. قد يؤثر ذلك على تتبع عملية الطباعة إذا كان عدد الصفحات المتوقع في البداية أكبر من العدد الفعلي المطبع.

 **Examples:** 

يوضح كيفية تصفية الصفحات باستخدام قائمة أرقام الصفحات.

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


يحصل على عدد الصفحات المتبقية في مهمة الطباعة النشطة حاليًا.

 **Remarks:** 

يتم تحديث هذه القيمة تلقائيًا مع طباعة الصفحات، مما يعكس تقدم مهمة الطباعة الحالية. خارج وقت الطباعة وفي حالة حدوث أخطاء أو انقطاعات في مهمة الطباعة، قد لا تعكس القيمة العدد الفعلي للصفحات المتبقية.

 **Examples:** 

يعرض كيفية مراقبة تقدم الطباعة.

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

يعرض فئة مثال لمراقبة تقدم الطباعة.

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
int - رقم الصفحة الحالية التي يتم طباعتها. / public int getPrintingPage() \{ return printingPage; \} /\*\* يحصل على إجمالي عدد الصفحات للطباعة. يُرجع 0 عندما لا تكون هناك عملية طباعة جارية.
### getPrintable(int pageIndex) {#getPrintable-int}
```
public Printable getPrintable(int pageIndex)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| pageIndex | int |  |

**Returns:**
java.awt.print.Printable
### getTotalPagesPrinted() {#getTotalPagesPrinted}
```
public int getTotalPagesPrinted()
```


يحصل على إجمالي عدد الصفحات التي تم طباعتها فعليًا خلال جلسة الطباعة.

 **Remarks:** 

يتم تحديثه بعد اكتمال الطباعة. يُرجع 0 قبل بدء الطباعة.

 **Examples:** 

يعرض كيفية تصفية الصفحات بناءً على لون الصفحة.

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
int - true إذا يجب تخطي الصفحة؛ وإلا false. /
### print(Graphics graphics, PageFormat pageFormat, int pageIndex) {#print-java.awt.Graphics-java.awt.print.PageFormat-int}
```
public int print(Graphics graphics, PageFormat pageFormat, int pageIndex)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الرسومات | java.awt.Graphics |  |
| pageFormat | java.awt.print.PageFormat |  |
| pageIndex | int |  |

**Returns:**
int
### setColorMode(int value) {#setColorMode-int}
```
public void setColorMode(int value)
```


يضبط كيفية طباعة الصفحات غير الملونة إذا كان الجهاز يدعم الطباعة بالألوان.

 **Remarks:** 

لا يؤثر على طباعة الكتيب.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | int | كيفية طباعة الصفحات غير الملونة إذا كان الجهاز يدعم الطباعة بالألوان. يجب أن تكون القيمة واحدة من ثوابت [ColorPrintMode](../../com.aspose.words/colorprintmode/). |

### setPageIndexFilter(IIndexFilter value) {#setPageIndexFilter-com.aspose.words.IIndexFilter}
```
public void setPageIndexFilter(IIndexFilter value)
```


يضبط مرشح الفهرس الصفري المستخدم لتحديد الصفحات التي يجب تخطيها أثناء الطباعة.

 **Remarks:** 

يرجى ملاحظة أنه إذا تم تخطي بعض الصفحات، فلن يُعرف العدد الإجمالي الفعلي للصفحات التي يجب طباعتها حتى يكتمل عملية الطباعة. قد يؤثر ذلك على تتبع عملية الطباعة إذا كان عدد الصفحات المتوقع في البداية أكبر من العدد الفعلي المطبع.

 **Examples:** 

يوضح كيفية تصفية الصفحات باستخدام قائمة أرقام الصفحات.

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
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [IIndexFilter](../../com.aspose.words/iindexfilter/) | مرشح الفهرس الصفري المستخدم لتحديد الصفحات التي يجب تخطيها أثناء الطباعة. |

