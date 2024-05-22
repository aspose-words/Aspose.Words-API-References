---
title: ConvertUtil
linktitle: ConvertUtil
second_title: Aspose.Words for Java
description: Provides helper functions to convert between various measurement units in Java.
type: docs
weight: 119
url: /java/com.aspose.words/convertutil/
---

**Inheritance:**
java.lang.Object
```
public class ConvertUtil
```

Provides helper functions to convert between various measurement units.

To learn more, visit the [ Convert Between Measurement Units ][Convert Between Measurement Units] documentation article.

 **Examples:** 

Shows how to adjust paper size, orientation, margins, along with other settings for a section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

Shows how to specify page properties in inches.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A section's "Page Setup" defines the size of the page margins in points.
 // We can also use the "ConvertUtil" class to use a more familiar measurement unit,
 // such as inches when defining boundaries.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setTopMargin(ConvertUtil.inchToPoint(1.0));
 pageSetup.setBottomMargin(ConvertUtil.inchToPoint(2.0));
 pageSetup.setLeftMargin(ConvertUtil.inchToPoint(2.5));
 pageSetup.setRightMargin(ConvertUtil.inchToPoint(1.5));

 // An inch is 72 points.
 Assert.assertEquals(72.0d, ConvertUtil.inchToPoint(1.0));
 Assert.assertEquals(1.0d, ConvertUtil.pointToInch(72.0));

 // Add content to demonstrate the new margins.
 builder.writeln(MessageFormat.format("This Text is {0} points/{1} inches from the left, ",
         pageSetup.getLeftMargin(), ConvertUtil.pointToInch(pageSetup.getLeftMargin())) +
         MessageFormat.format("{0} points/{1} inches from the right, ",
                 pageSetup.getRightMargin(), ConvertUtil.pointToInch(pageSetup.getRightMargin())) +
         MessageFormat.format("{0} points/{1} inches from the top, ",
                 pageSetup.getTopMargin(), ConvertUtil.pointToInch(pageSetup.getTopMargin())) +
         MessageFormat.format("and {0} points/{1} inches from the bottom of the page.",
                 pageSetup.getBottomMargin(), ConvertUtil.pointToInch(pageSetup.getBottomMargin())));

 doc.save(getArtifactsDir() + "UtilityClasses.PointsAndInches.docx");
 
```


[Convert Between Measurement Units]: https://docs.aspose.com/words/java/convert-between-measurement-units/
## Methods

| Method | Description |
| --- | --- |
| [inchToPoint(double inches)](#inchToPoint-double) | Converts inches to points. |
| [millimeterToPoint(double millimeters)](#millimeterToPoint-double) | Converts millimeters to points. |
| [pixelToNewDpi(double pixels, double oldDpi, double newDpi)](#pixelToNewDpi-double-double-double) | Converts pixels from one resolution to another. |
| [pixelToPoint(double pixels)](#pixelToPoint-double) | Converts pixels to points. |
| [pixelToPoint(double pixels, double resolution)](#pixelToPoint-double-double) | Converts pixels to points at the specified pixel resolution. |
| [pointToInch(double points)](#pointToInch-double) | Converts points to inches. |
| [pointToPixel(double points)](#pointToPixel-double) | Converts points to pixels. |
| [pointToPixel(double points, double resolution)](#pointToPixel-double-double) | Converts points to pixels at the specified pixel resolution. |
### inchToPoint(double inches) {#inchToPoint-double}
```
public static double inchToPoint(double inches)
```


Converts inches to points.

 **Remarks:** 

1 inch equals 72 points.

 **Examples:** 

Shows how to adjust paper size, orientation, margins, along with other settings for a section.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getPageSetup().setPaperSize(PaperSize.LEGAL);
 builder.getPageSetup().setOrientation(Orientation.LANDSCAPE);
 builder.getPageSetup().setTopMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setBottomMargin(ConvertUtil.inchToPoint(1.0));
 builder.getPageSetup().setLeftMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setRightMargin(ConvertUtil.inchToPoint(1.5));
 builder.getPageSetup().setHeaderDistance(ConvertUtil.inchToPoint(0.2));
 builder.getPageSetup().setFooterDistance(ConvertUtil.inchToPoint(0.2));

 builder.writeln("Hello world!");

 doc.save(getArtifactsDir() + "PageSetup.PageMargins.docx");
 
```

Shows how to specify page properties in inches.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A section's "Page Setup" defines the size of the page margins in points.
 // We can also use the "ConvertUtil" class to use a more familiar measurement unit,
 // such as inches when defining boundaries.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setTopMargin(ConvertUtil.inchToPoint(1.0));
 pageSetup.setBottomMargin(ConvertUtil.inchToPoint(2.0));
 pageSetup.setLeftMargin(ConvertUtil.inchToPoint(2.5));
 pageSetup.setRightMargin(ConvertUtil.inchToPoint(1.5));

 // An inch is 72 points.
 Assert.assertEquals(72.0d, ConvertUtil.inchToPoint(1.0));
 Assert.assertEquals(1.0d, ConvertUtil.pointToInch(72.0));

 // Add content to demonstrate the new margins.
 builder.writeln(MessageFormat.format("This Text is {0} points/{1} inches from the left, ",
         pageSetup.getLeftMargin(), ConvertUtil.pointToInch(pageSetup.getLeftMargin())) +
         MessageFormat.format("{0} points/{1} inches from the right, ",
                 pageSetup.getRightMargin(), ConvertUtil.pointToInch(pageSetup.getRightMargin())) +
         MessageFormat.format("{0} points/{1} inches from the top, ",
                 pageSetup.getTopMargin(), ConvertUtil.pointToInch(pageSetup.getTopMargin())) +
         MessageFormat.format("and {0} points/{1} inches from the bottom of the page.",
                 pageSetup.getBottomMargin(), ConvertUtil.pointToInch(pageSetup.getBottomMargin())));

 doc.save(getArtifactsDir() + "UtilityClasses.PointsAndInches.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| inches | double | The value to convert. |

**Returns:**
double
### millimeterToPoint(double millimeters) {#millimeterToPoint-double}
```
public static double millimeterToPoint(double millimeters)
```


Converts millimeters to points.

 **Remarks:** 

1 inch equals 25.4 millimeters. 1 inch equals 72 points.

 **Examples:** 

Shows how to specify page properties in millimeters.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A section's "Page Setup" defines the size of the page margins in points.
 // We can also use the "ConvertUtil" class to use a more familiar measurement unit,
 // such as millimeters when defining boundaries.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setTopMargin(ConvertUtil.millimeterToPoint(30.0));
 pageSetup.setBottomMargin(ConvertUtil.millimeterToPoint(50.0));
 pageSetup.setLeftMargin(ConvertUtil.millimeterToPoint(80.0));
 pageSetup.setRightMargin(ConvertUtil.millimeterToPoint(40.0));

 // A centimeter is approximately 28.3 points.
 Assert.assertEquals(28.34d, ConvertUtil.millimeterToPoint(10.0), 0.01d);

 // Add content to demonstrate the new margins.
 builder.writeln(MessageFormat.format("This Text is {0} points from the left, ", pageSetup.getLeftMargin()) +
         MessageFormat.format("{0} points from the right, ", pageSetup.getRightMargin()) +
         MessageFormat.format("{0} points from the top, ", pageSetup.getTopMargin()) +
         MessageFormat.format("and {0} points from the bottom of the page.", pageSetup.getBottomMargin()));

 doc.save(getArtifactsDir() + "UtilityClasses.PointsAndMillimeters.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| millimeters | double | The value to convert. |

**Returns:**
double
### pixelToNewDpi(double pixels, double oldDpi, double newDpi) {#pixelToNewDpi-double-double-double}
```
public static int pixelToNewDpi(double pixels, double oldDpi, double newDpi)
```


Converts pixels from one resolution to another.

 **Examples:** 

Shows how to use convert points to pixels with default and custom resolution.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define the size of the top margin of this section in pixels, according to a custom DPI.
 double myDpi = 192.0;

 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setTopMargin(ConvertUtil.pixelToPoint(100.0, myDpi));
 Assert.assertEquals(37.5d, pageSetup.getTopMargin(), 0.01d);

 // At the default DPI of 96, a pixel is 0.75 points.
 Assert.assertEquals(0.75d, ConvertUtil.pixelToPoint(1.0));

 builder.writeln(MessageFormat.format("This Text is {0} points/{1} ",
         pageSetup.getTopMargin(), ConvertUtil.pointToPixel(pageSetup.getTopMargin(), myDpi)) +
         MessageFormat.format("pixels (at a DPI of {0}) from the top of the page.", myDpi));

 // Set a new DPI and adjust the top margin value accordingly.
 double newDpi = 300.0;
 pageSetup.setTopMargin(ConvertUtil.pixelToNewDpi(pageSetup.getTopMargin(), myDpi, newDpi));
 Assert.assertEquals(59.0d, pageSetup.getTopMargin(), 0.01d);

 builder.writeln(MessageFormat.format("At a DPI of {0}, the text is now {1} points/{2} ",
         newDpi, pageSetup.getTopMargin(), ConvertUtil.pointToPixel(pageSetup.getTopMargin(), myDpi)) +
         "pixels from the top of the page.");

 doc.save(getArtifactsDir() + "UtilityClasses.PointsAndPixelsDpi.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pixels | double | The value to convert. |
| oldDpi | double | The current dpi (dots per inch) resolution. |
| newDpi | double | The new dpi (dots per inch) resolution. |

**Returns:**
int
### pixelToPoint(double pixels) {#pixelToPoint-double}
```
public static double pixelToPoint(double pixels)
```


Converts pixels to points.  Converts pixels to points at 96 dpi.

 **Remarks:** 

1 inch equals 72 points.

 **Examples:** 

Shows how to specify page properties in pixels.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A section's "Page Setup" defines the size of the page margins in points.
 // We can also use the "ConvertUtil" class to use a different measurement unit,
 // such as pixels when defining boundaries.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setTopMargin(ConvertUtil.pixelToPoint(100.0));
 pageSetup.setBottomMargin(ConvertUtil.pixelToPoint(200.0));
 pageSetup.setLeftMargin(ConvertUtil.pixelToPoint(225.0));
 pageSetup.setRightMargin(ConvertUtil.pixelToPoint(125.0));

 // A pixel is 0.75 points.
 Assert.assertEquals(0.75d, ConvertUtil.pixelToPoint(1.0));
 Assert.assertEquals(1.0d, ConvertUtil.pointToPixel(0.75));

 // The default DPI value used is 96.
 Assert.assertEquals(0.75d, ConvertUtil.pixelToPoint(1.0, 96.0));

 // Add content to demonstrate the new margins.
 builder.writeln(MessageFormat.format("This Text is {0} points/{1} inches from the left, ",
         pageSetup.getLeftMargin(), ConvertUtil.pointToInch(pageSetup.getLeftMargin())) +
         MessageFormat.format("{0} points/{1} inches from the right, ",
                 pageSetup.getRightMargin(), ConvertUtil.pointToInch(pageSetup.getRightMargin())) +
         MessageFormat.format("{0} points/{1} inches from the top, ",
                 pageSetup.getTopMargin(), ConvertUtil.pointToInch(pageSetup.getTopMargin())) +
         MessageFormat.format("and {0} points/{1} inches from the bottom of the page.",
                 pageSetup.getBottomMargin(), ConvertUtil.pointToInch(pageSetup.getBottomMargin())));

 doc.save(getArtifactsDir() + "UtilityClasses.PointsAndPixels.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pixels | double | The value to convert. |

**Returns:**
double
### pixelToPoint(double pixels, double resolution) {#pixelToPoint-double-double}
```
public static double pixelToPoint(double pixels, double resolution)
```


Converts pixels to points at the specified pixel resolution.

 **Remarks:** 

1 inch equals 72 points.

 **Examples:** 

Shows how to use convert points to pixels with default and custom resolution.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define the size of the top margin of this section in pixels, according to a custom DPI.
 double myDpi = 192.0;

 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setTopMargin(ConvertUtil.pixelToPoint(100.0, myDpi));
 Assert.assertEquals(37.5d, pageSetup.getTopMargin(), 0.01d);

 // At the default DPI of 96, a pixel is 0.75 points.
 Assert.assertEquals(0.75d, ConvertUtil.pixelToPoint(1.0));

 builder.writeln(MessageFormat.format("This Text is {0} points/{1} ",
         pageSetup.getTopMargin(), ConvertUtil.pointToPixel(pageSetup.getTopMargin(), myDpi)) +
         MessageFormat.format("pixels (at a DPI of {0}) from the top of the page.", myDpi));

 // Set a new DPI and adjust the top margin value accordingly.
 double newDpi = 300.0;
 pageSetup.setTopMargin(ConvertUtil.pixelToNewDpi(pageSetup.getTopMargin(), myDpi, newDpi));
 Assert.assertEquals(59.0d, pageSetup.getTopMargin(), 0.01d);

 builder.writeln(MessageFormat.format("At a DPI of {0}, the text is now {1} points/{2} ",
         newDpi, pageSetup.getTopMargin(), ConvertUtil.pointToPixel(pageSetup.getTopMargin(), myDpi)) +
         "pixels from the top of the page.");

 doc.save(getArtifactsDir() + "UtilityClasses.PointsAndPixelsDpi.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pixels | double | The value to convert. |
| resolution | double | The dpi (dots per inch) resolution. |

**Returns:**
double
### pointToInch(double points) {#pointToInch-double}
```
public static double pointToInch(double points)
```


Converts points to inches.

 **Remarks:** 

1 inch equals 72 points.

 **Examples:** 

Shows how to specify page properties in inches.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A section's "Page Setup" defines the size of the page margins in points.
 // We can also use the "ConvertUtil" class to use a more familiar measurement unit,
 // such as inches when defining boundaries.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setTopMargin(ConvertUtil.inchToPoint(1.0));
 pageSetup.setBottomMargin(ConvertUtil.inchToPoint(2.0));
 pageSetup.setLeftMargin(ConvertUtil.inchToPoint(2.5));
 pageSetup.setRightMargin(ConvertUtil.inchToPoint(1.5));

 // An inch is 72 points.
 Assert.assertEquals(72.0d, ConvertUtil.inchToPoint(1.0));
 Assert.assertEquals(1.0d, ConvertUtil.pointToInch(72.0));

 // Add content to demonstrate the new margins.
 builder.writeln(MessageFormat.format("This Text is {0} points/{1} inches from the left, ",
         pageSetup.getLeftMargin(), ConvertUtil.pointToInch(pageSetup.getLeftMargin())) +
         MessageFormat.format("{0} points/{1} inches from the right, ",
                 pageSetup.getRightMargin(), ConvertUtil.pointToInch(pageSetup.getRightMargin())) +
         MessageFormat.format("{0} points/{1} inches from the top, ",
                 pageSetup.getTopMargin(), ConvertUtil.pointToInch(pageSetup.getTopMargin())) +
         MessageFormat.format("and {0} points/{1} inches from the bottom of the page.",
                 pageSetup.getBottomMargin(), ConvertUtil.pointToInch(pageSetup.getBottomMargin())));

 doc.save(getArtifactsDir() + "UtilityClasses.PointsAndInches.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| points | double | The value to convert. |

**Returns:**
double
### pointToPixel(double points) {#pointToPixel-double}
```
public static double pointToPixel(double points)
```


Converts points to pixels.  Converts points to pixels at 96 dpi.

 **Remarks:** 

1 inch equals 72 points.

 **Examples:** 

Shows how to specify page properties in pixels.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // A section's "Page Setup" defines the size of the page margins in points.
 // We can also use the "ConvertUtil" class to use a different measurement unit,
 // such as pixels when defining boundaries.
 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setTopMargin(ConvertUtil.pixelToPoint(100.0));
 pageSetup.setBottomMargin(ConvertUtil.pixelToPoint(200.0));
 pageSetup.setLeftMargin(ConvertUtil.pixelToPoint(225.0));
 pageSetup.setRightMargin(ConvertUtil.pixelToPoint(125.0));

 // A pixel is 0.75 points.
 Assert.assertEquals(0.75d, ConvertUtil.pixelToPoint(1.0));
 Assert.assertEquals(1.0d, ConvertUtil.pointToPixel(0.75));

 // The default DPI value used is 96.
 Assert.assertEquals(0.75d, ConvertUtil.pixelToPoint(1.0, 96.0));

 // Add content to demonstrate the new margins.
 builder.writeln(MessageFormat.format("This Text is {0} points/{1} inches from the left, ",
         pageSetup.getLeftMargin(), ConvertUtil.pointToInch(pageSetup.getLeftMargin())) +
         MessageFormat.format("{0} points/{1} inches from the right, ",
                 pageSetup.getRightMargin(), ConvertUtil.pointToInch(pageSetup.getRightMargin())) +
         MessageFormat.format("{0} points/{1} inches from the top, ",
                 pageSetup.getTopMargin(), ConvertUtil.pointToInch(pageSetup.getTopMargin())) +
         MessageFormat.format("and {0} points/{1} inches from the bottom of the page.",
                 pageSetup.getBottomMargin(), ConvertUtil.pointToInch(pageSetup.getBottomMargin())));

 doc.save(getArtifactsDir() + "UtilityClasses.PointsAndPixels.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| points | double | The value to convert. |

**Returns:**
double
### pointToPixel(double points, double resolution) {#pointToPixel-double-double}
```
public static double pointToPixel(double points, double resolution)
```


Converts points to pixels at the specified pixel resolution.

 **Remarks:** 

1 inch equals 72 points.

 **Examples:** 

Shows how to use convert points to pixels with default and custom resolution.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Define the size of the top margin of this section in pixels, according to a custom DPI.
 double myDpi = 192.0;

 PageSetup pageSetup = builder.getPageSetup();
 pageSetup.setTopMargin(ConvertUtil.pixelToPoint(100.0, myDpi));
 Assert.assertEquals(37.5d, pageSetup.getTopMargin(), 0.01d);

 // At the default DPI of 96, a pixel is 0.75 points.
 Assert.assertEquals(0.75d, ConvertUtil.pixelToPoint(1.0));

 builder.writeln(MessageFormat.format("This Text is {0} points/{1} ",
         pageSetup.getTopMargin(), ConvertUtil.pointToPixel(pageSetup.getTopMargin(), myDpi)) +
         MessageFormat.format("pixels (at a DPI of {0}) from the top of the page.", myDpi));

 // Set a new DPI and adjust the top margin value accordingly.
 double newDpi = 300.0;
 pageSetup.setTopMargin(ConvertUtil.pixelToNewDpi(pageSetup.getTopMargin(), myDpi, newDpi));
 Assert.assertEquals(59.0d, pageSetup.getTopMargin(), 0.01d);

 builder.writeln(MessageFormat.format("At a DPI of {0}, the text is now {1} points/{2} ",
         newDpi, pageSetup.getTopMargin(), ConvertUtil.pointToPixel(pageSetup.getTopMargin(), myDpi)) +
         "pixels from the top of the page.");

 doc.save(getArtifactsDir() + "UtilityClasses.PointsAndPixelsDpi.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| points | double | The value to convert. |
| resolution | double | The dpi (dots per inch) resolution. |

**Returns:**
double
