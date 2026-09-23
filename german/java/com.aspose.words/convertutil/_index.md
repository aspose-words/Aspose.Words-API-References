---
title: "ConvertUtil"
linktitle: "ConvertUtil"
second_title: "Aspose.Words für Java"
description: "Stellt Hilfsfunktionen bereit, um zwischen verschiedenen Maßeinheiten in Java zu konvertieren."
type: docs
weight: 131
url: /de/java/com.aspose.words/convertutil/
---

**Inheritance:**
java.lang.Object
```
public class ConvertUtil
```

Bietet Hilfsfunktionen zum Konvertieren zwischen verschiedenen Maßeinheiten.

Um mehr zu erfahren, besuchen Sie den Dokumentationsartikel [ Convert Between Measurement Units ][Convert Between Measurement Units].

 **Examples:** 

Zeigt, wie man Papiergröße, Ausrichtung, Ränder und weitere Einstellungen für einen Abschnitt anpasst.

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

Zeigt, wie man Seiteneigenschaften in Zoll angibt.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [inchToPoint(double inches)](#inchToPoint-double) | Konvertiert Zoll in Punkte. |
| [millimeterToPoint(double millimeters)](#millimeterToPoint-double) | Konvertiert Millimeter in Punkte. |
| [pixelToNewDpi(double pixels, double oldDpi, double newDpi)](#pixelToNewDpi-double-double-double) | Konvertiert Pixel von einer Auflösung zur anderen. |
| [pixelToPoint(double pixels)](#pixelToPoint-double) | Konvertiert Pixel in Punkte. |
| [pixelToPoint(double pixels, double resolution)](#pixelToPoint-double-double) | Konvertiert Pixel in Punkte bei der angegebenen Pixelauflösung. |
| [pointToInch(double points)](#pointToInch-double) | Konvertiert Punkte in Zoll. |
| [pointToPixel(double points)](#pointToPixel-double) | Konvertiert Punkte in Pixel. |
| [pointToPixel(double points, double resolution)](#pointToPixel-double-double) | Konvertiert Punkte in Pixel bei der angegebenen Pixelauflösung. |
### inchToPoint(double inches) {#inchToPoint-double}
```
public static double inchToPoint(double inches)
```


Konvertiert Zoll in Punkte.

 **Remarks:** 

1 Zoll entspricht 72 Punkten.

 **Examples:** 

Zeigt, wie man Papiergröße, Ausrichtung, Ränder und weitere Einstellungen für einen Abschnitt anpasst.

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

Zeigt, wie man Seiteneigenschaften in Zoll angibt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Zoll | double | Der zu konvertierende Wert. |

**Returns:**
double
### millimeterToPoint(double millimeters) {#millimeterToPoint-double}
```
public static double millimeterToPoint(double millimeters)
```


Konvertiert Millimeter in Punkte.

 **Remarks:** 

1 Zoll entspricht 25,4 Millimetern. 1 Zoll entspricht 72 Punkten.

 **Examples:** 

Zeigt, wie man Seiteneigenschaften in Millimetern angibt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Millimeter | double | Der zu konvertierende Wert. |

**Returns:**
double
### pixelToNewDpi(double pixels, double oldDpi, double newDpi) {#pixelToNewDpi-double-double-double}
```
public static int pixelToNewDpi(double pixels, double oldDpi, double newDpi)
```


Konvertiert Pixel von einer Auflösung zur anderen.

 **Examples:** 

Zeigt, wie man Punkte in Pixel umwandelt, mit Standard- und benutzerdefinierter Auflösung.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Pixel | double | Der zu konvertierende Wert. |
| oldDpi | double | Die aktuelle DPI (dots per inch)-Auflösung. |
| newDpi | double | Die neue DPI (dots per inch)-Auflösung. |

**Returns:**
int
### pixelToPoint(double pixels) {#pixelToPoint-double}
```
public static double pixelToPoint(double pixels)
```


Wandelt Pixel in Punkte um.  Wandelt Pixel bei 96 DPI in Punkte um.

 **Remarks:** 

1 Zoll entspricht 72 Punkten.

 **Examples:** 

Zeigt, wie man Seiten­eigenschaften in Pixeln angibt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Pixel | double | Der zu konvertierende Wert. |

**Returns:**
double
### pixelToPoint(double pixels, double resolution) {#pixelToPoint-double-double}
```
public static double pixelToPoint(double pixels, double resolution)
```


Konvertiert Pixel in Punkte bei der angegebenen Pixelauflösung.

 **Remarks:** 

1 Zoll entspricht 72 Punkten.

 **Examples:** 

Zeigt, wie man Punkte in Pixel umwandelt, mit Standard- und benutzerdefinierter Auflösung.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Pixel | double | Der zu konvertierende Wert. |
| Auflösung | double | Die DPI (dots per inch)-Auflösung. |

**Returns:**
double
### pointToInch(double points) {#pointToInch-double}
```
public static double pointToInch(double points)
```


Konvertiert Punkte in Zoll.

 **Remarks:** 

1 Zoll entspricht 72 Punkten.

 **Examples:** 

Zeigt, wie man Seiteneigenschaften in Zoll angibt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Punkte | double | Der zu konvertierende Wert. |

**Returns:**
double
### pointToPixel(double points) {#pointToPixel-double}
```
public static double pointToPixel(double points)
```


Wandelt Punkte in Pixel um.  Wandelt Punkte bei 96 DPI in Pixel um.

 **Remarks:** 

1 Zoll entspricht 72 Punkten.

 **Examples:** 

Zeigt, wie man Seiten­eigenschaften in Pixeln angibt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Punkte | double | Der zu konvertierende Wert. |

**Returns:**
double
### pointToPixel(double points, double resolution) {#pointToPixel-double-double}
```
public static double pointToPixel(double points, double resolution)
```


Konvertiert Punkte in Pixel bei der angegebenen Pixelauflösung.

 **Remarks:** 

1 Zoll entspricht 72 Punkten.

 **Examples:** 

Zeigt, wie man Punkte in Pixel umwandelt, mit Standard- und benutzerdefinierter Auflösung.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Punkte | double | Der zu konvertierende Wert. |
| Auflösung | double | Die DPI (dots per inch)-Auflösung. |

**Returns:**
double
