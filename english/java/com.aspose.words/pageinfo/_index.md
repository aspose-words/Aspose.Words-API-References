---
title: PageInfo
linktitle: PageInfo
second_title: Aspose.Words for Java
description: Represents information about a particular document page in Java.
type: docs
weight: 511
url: /java/com.aspose.words/pageinfo/
---

**Inheritance:**
java.lang.Object
```
public class PageInfo
```

Represents information about a particular document page.

To learn more, visit the [ Rendering ][Rendering] documentation article.

 **Remarks:** 

The page width and height returned by this object represent the "final" size of the page e.g. they are already rotated to the correct orientation.


[Rendering]: https://docs.aspose.com/words/java/rendering/
## Methods

| Method | Description |
| --- | --- |
| [getColored()](#getColored) | Returns  true  if the page contains colored content. |
| [getHeightInPoints()](#getHeightInPoints) | Gets the height of the page in points. |
| [getLandscape()](#getLandscape) | Returns  true  if the page orientation specified in the document for this page is landscape. |
| [getPaperSize()](#getPaperSize) | Gets the paper size as enumeration. |
| [getPaperTray()](#getPaperTray) | Gets the paper tray (bin) for this page as specified in the document. |
| [getSizeInPixels(float scale, float dpi)](#getSizeInPixels-float-float) | Calculates the page size in pixels for a specified zoom factor and resolution. |
| [getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)](#getSizeInPixels-float-float-float) | Calculates the page size in pixels for a specified zoom factor and resolution. |
| [getSizeInPoints()](#getSizeInPoints) | Gets the page size in points. |
| [getWidthInPoints()](#getWidthInPoints) | Gets the width of the page in points. |
### getColored() {#getColored}
```
public boolean getColored()
```


Returns  true  if the page contains colored content.

 **Examples:** 

Shows how to check whether the page is in color or not.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 // Check that the first page of the document is not colored.
 Assert.assertFalse(doc.getPageInfo(0).getColored());
 
```

Shows how to filtering pages base on page color.

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
boolean - true if the page should be skipped; otherwise, false. /
### getHeightInPoints() {#getHeightInPoints}
```
public float getHeightInPoints()
```


Gets the height of the page in points.

**Returns:**
float - The height of the page in points.
### getLandscape() {#getLandscape}
```
public boolean getLandscape()
```


Returns  true  if the page orientation specified in the document for this page is landscape.

**Returns:**
boolean -  true  if the page orientation specified in the document for this page is landscape.
### getPaperSize() {#getPaperSize}
```
public int getPaperSize()
```


Gets the paper size as enumeration.

**Returns:**
int - The paper size as enumeration. The returned value is one of [PaperSize](../../com.aspose.words/papersize/) constants.
### getPaperTray() {#getPaperTray}
```
public int getPaperTray()
```


Gets the paper tray (bin) for this page as specified in the document. The value is implementation (printer) specific.

**Returns:**
int - The paper tray (bin) for this page as specified in the document.
### getSizeInPixels(float scale, float dpi) {#getSizeInPixels-float-float}
```
public Dimension getSizeInPixels(float scale, float dpi)
```


Calculates the page size in pixels for a specified zoom factor and resolution.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| scale | float | The zoom factor (1.0 is 100%). |
| dpi | float | The resolution (horizontal and vertical) to convert from points to pixels (dots per inch). |

**Returns:**
java.awt.Dimension - The size of the page in pixels.
### getSizeInPixels(float scale, float horizontalDpi, float verticalDpi) {#getSizeInPixels-float-float-float}
```
public Dimension getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)
```


Calculates the page size in pixels for a specified zoom factor and resolution.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| scale | float | The zoom factor (1.0 is 100%). |
| horizontalDpi | float | The horizontal resolution to convert from points to pixels (dots per inch). |
| verticalDpi | float | The vertical resolution to convert from points to pixels (dots per inch). |

**Returns:**
java.awt.Dimension - The size of the page in pixels.
### getSizeInPoints() {#getSizeInPoints}
```
public Point2D.Float getSizeInPoints()
```


Gets the page size in points.

**Returns:**
java.awt.geom.Point2D.Float - The page size in points.
### getWidthInPoints() {#getWidthInPoints}
```
public float getWidthInPoints()
```


Gets the width of the page in points.

**Returns:**
float - The width of the page in points.
