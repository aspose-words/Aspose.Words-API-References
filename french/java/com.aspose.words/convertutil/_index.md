---
title: "ConvertUtil"
linktitle: "ConvertUtil"
second_title: "Aspose.Words pour Java"
description: "Fournit des fonctions d'aide pour convertir entre différentes unités de mesure en Java."
type: docs
weight: 131
url: /fr/java/com.aspose.words/convertutil/
---

**Inheritance:**
java.lang.Object
```
public class ConvertUtil
```

Fournit des fonctions d'aide pour convertir entre différentes unités de mesure.

Pour en savoir plus, consultez l'article de documentation [ Convert Between Measurement Units ][Convert Between Measurement Units].

 **Examples:** 

Montre comment ajuster la taille du papier, l'orientation, les marges, ainsi que d'autres paramètres pour une section.

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

Montre comment spécifier les propriétés de la page en pouces.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [inchToPoint(double inches)](#inchToPoint-double) | Convertit les pouces en points. |
| [millimeterToPoint(double millimeters)](#millimeterToPoint-double) | Convertit les millimètres en points. |
| [pixelToNewDpi(double pixels, double oldDpi, double newDpi)](#pixelToNewDpi-double-double-double) | Convertit les pixels d'une résolution à une autre. |
| [pixelToPoint(double pixels)](#pixelToPoint-double) | Convertit les pixels en points. |
| [pixelToPoint(double pixels, double resolution)](#pixelToPoint-double-double) | Convertit les pixels en points à la résolution de pixel spécifiée. |
| [pointToInch(double points)](#pointToInch-double) | Convertit les points en pouces. |
| [pointToPixel(double points)](#pointToPixel-double) | Convertit les points en pixels. |
| [pointToPixel(double points, double resolution)](#pointToPixel-double-double) | Convertit les points en pixels à la résolution de pixel spécifiée. |
### inchToPoint(double inches) {#inchToPoint-double}
```
public static double inchToPoint(double inches)
```


Convertit les pouces en points.

 **Remarks:** 

1 pouce équivaut à 72 points.

 **Examples:** 

Montre comment ajuster la taille du papier, l'orientation, les marges, ainsi que d'autres paramètres pour une section.

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

Montre comment spécifier les propriétés de la page en pouces.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| pouces | double | La valeur à convertir. |

**Returns:**
double
### millimeterToPoint(double millimeters) {#millimeterToPoint-double}
```
public static double millimeterToPoint(double millimeters)
```


Convertit les millimètres en points.

 **Remarks:** 

1 pouce équivaut à 25,4 millimètres. 1 pouce équivaut à 72 points.

 **Examples:** 

Montre comment spécifier les propriétés de la page en millimètres.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| millimètres | double | La valeur à convertir. |

**Returns:**
double
### pixelToNewDpi(double pixels, double oldDpi, double newDpi) {#pixelToNewDpi-double-double-double}
```
public static int pixelToNewDpi(double pixels, double oldDpi, double newDpi)
```


Convertit les pixels d'une résolution à une autre.

 **Examples:** 

Montre comment utiliser la conversion de points en pixels avec une résolution par défaut et personnalisée.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| pixels | double | La valeur à convertir. |
| oldDpi | double | La résolution dpi (points par pouce) actuelle. |
| newDpi | double | La nouvelle résolution dpi (points par pouce). |

**Returns:**
int
### pixelToPoint(double pixels) {#pixelToPoint-double}
```
public static double pixelToPoint(double pixels)
```


Convertit les pixels en points.  Convertit les pixels en points à 96 dpi.

 **Remarks:** 

1 pouce équivaut à 72 points.

 **Examples:** 

Montre comment spécifier les propriétés de page en pixels.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| pixels | double | La valeur à convertir. |

**Returns:**
double
### pixelToPoint(double pixels, double resolution) {#pixelToPoint-double-double}
```
public static double pixelToPoint(double pixels, double resolution)
```


Convertit les pixels en points à la résolution de pixel spécifiée.

 **Remarks:** 

1 pouce équivaut à 72 points.

 **Examples:** 

Montre comment utiliser la conversion de points en pixels avec une résolution par défaut et personnalisée.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| pixels | double | La valeur à convertir. |
| résolution | double | La résolution dpi (points par pouce). |

**Returns:**
double
### pointToInch(double points) {#pointToInch-double}
```
public static double pointToInch(double points)
```


Convertit les points en pouces.

 **Remarks:** 

1 pouce équivaut à 72 points.

 **Examples:** 

Montre comment spécifier les propriétés de la page en pouces.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| points | double | La valeur à convertir. |

**Returns:**
double
### pointToPixel(double points) {#pointToPixel-double}
```
public static double pointToPixel(double points)
```


Convertit les points en pixels.  Convertit les points en pixels à 96 dpi.

 **Remarks:** 

1 pouce équivaut à 72 points.

 **Examples:** 

Montre comment spécifier les propriétés de page en pixels.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| points | double | La valeur à convertir. |

**Returns:**
double
### pointToPixel(double points, double resolution) {#pointToPixel-double-double}
```
public static double pointToPixel(double points, double resolution)
```


Convertit les points en pixels à la résolution de pixel spécifiée.

 **Remarks:** 

1 pouce équivaut à 72 points.

 **Examples:** 

Montre comment utiliser la conversion de points en pixels avec une résolution par défaut et personnalisée.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| points | double | La valeur à convertir. |
| résolution | double | La résolution dpi (points par pouce). |

**Returns:**
double
