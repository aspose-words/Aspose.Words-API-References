---
title: "معلومات الصفحة"
linktitle: "معلومات الصفحة"
second_title: "Aspose.Words لـ Java"
description: "يمثل معلومات حول صفحة مستند معينة في جافا."
type: docs
weight: 513
url: /ar/java/com.aspose.words/pageinfo/
---

**Inheritance:**
java.lang.Object
```
public class PageInfo
```

يمثل معلومات حول صفحة مستند معينة.

لمزيد من المعلومات، زر مقالة الوثائق [ Rendering ][Rendering].

 **Remarks:** 

عرض وارتفاع الصفحة التي تُرجعها هذه الكائن تمثل الحجم "النهائي" للصفحة، على سبيل المثال تم تدويرها بالفعل إلى الاتجاه الصحيح.


[Rendering]: https://docs.aspose.com/words/java/rendering/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getColored()](#getColored) | يرجع  true  إذا كانت الصفحة تحتوي على محتوى ملون. |
| [getHeightInPoints()](#getHeightInPoints) | يحصل على ارتفاع الصفحة بالنقاط. |
| [getLandscape()](#getLandscape) | يرجع  true  إذا كان اتجاه الصفحة المحدد في المستند لهذه الصفحة هو أفقي. |
| [getPaperSize()](#getPaperSize) | يحصل على حجم الورق كقيمة تعداد. |
| [getPaperTray()](#getPaperTray) | يحصل على صينية الورق (الدرج) لهذه الصفحة كما هو محدد في المستند. |
| [getSizeInPixels(float scale, float dpi)](#getSizeInPixels-float-float) | يحسب حجم الصفحة بالبكسل لعامل تكبير ودقة محددين. |
| [getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)](#getSizeInPixels-float-float-float) | يحسب حجم الصفحة بالبكسل لعامل تكبير ودقة محددين. |
| [getSizeInPoints()](#getSizeInPoints) | يحصل على حجم الصفحة بالنقاط. |
| [getWidthInPoints()](#getWidthInPoints) | يحصل على عرض الصفحة بالنقاط. |
### getColored() {#getColored}
```
public boolean getColored()
```


يرجع  true  إذا كانت الصفحة تحتوي على محتوى ملون.

 **Examples:** 

يعرض كيفية التحقق مما إذا كانت الصفحة ملونة أم لا.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 // Check that the first page of the document is not colored.
 Assert.assertFalse(doc.getPageInfo(0).getColored());
 
```

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
boolean - true إذا كان يجب تخطي الصفحة؛ وإلا، false. /
### getHeightInPoints() {#getHeightInPoints}
```
public float getHeightInPoints()
```


يحصل على ارتفاع الصفحة بالنقاط.

**Returns:**
float - ارتفاع الصفحة بالنقاط.
### getLandscape() {#getLandscape}
```
public boolean getLandscape()
```


يرجع  true  إذا كان اتجاه الصفحة المحدد في المستند لهذه الصفحة هو أفقي.

**Returns:**
boolean -  true إذا كان اتجاه الصفحة المحدد في المستند لهذه الصفحة هو أفقي.
### getPaperSize() {#getPaperSize}
```
public int getPaperSize()
```


يحصل على حجم الورق كقيمة تعداد.

**Returns:**
int - حجم الورق كعدد تعداد. القيمة المرجعة هي واحدة من ثوابت [PaperSize](../../com.aspose.words/papersize/).
### getPaperTray() {#getPaperTray}
```
public int getPaperTray()
```


يحصل على صينية الورق (bin) لهذه الصفحة كما هو محدد في المستند. القيمة خاصة بتنفيذ (الطابعة).

**Returns:**
int - صينية الورق (bin) لهذه الصفحة كما هو محدد في المستند.
### getSizeInPixels(float scale, float dpi) {#getSizeInPixels-float-float}
```
public Dimension getSizeInPixels(float scale, float dpi)
```


يحسب حجم الصفحة بالبكسل لعامل تكبير ودقة محددين.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| المقياس | float | عامل التكبير (1.0 يساوي 100%). |
| dpi | float | الدقة (الأفقية والعمودية) لتحويل النقاط إلى بكسل (نقطة في البوصة). |

**Returns:**
java.awt.Dimension - حجم الصفحة بالبكسل.
### getSizeInPixels(float scale, float horizontalDpi, float verticalDpi) {#getSizeInPixels-float-float-float}
```
public Dimension getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)
```


يحسب حجم الصفحة بالبكسل لعامل تكبير ودقة محددين.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| المقياس | float | عامل التكبير (1.0 يساوي 100%). |
| horizontalDpi | float | الدقة الأفقية لتحويل النقاط إلى بكسل (نقطة في البوصة). |
| verticalDpi | float | الدقة العمودية لتحويل النقاط إلى بكسل (نقطة في البوصة). |

**Returns:**
java.awt.Dimension - حجم الصفحة بالبكسل.
### getSizeInPoints() {#getSizeInPoints}
```
public Point2D.Float getSizeInPoints()
```


يحصل على حجم الصفحة بالنقاط.

**Returns:**
java.awt.geom.Point2D.Float - حجم الصفحة بالنقاط.
### getWidthInPoints() {#getWidthInPoints}
```
public float getWidthInPoints()
```


يحصل على عرض الصفحة بالنقاط.

**Returns:**
float - عرض الصفحة بالنقاط.
