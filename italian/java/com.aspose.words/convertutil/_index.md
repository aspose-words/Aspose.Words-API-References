---
title: "ConvertUtil"
linktitle: "ConvertUtil"
second_title: "Aspose.Words per Java"
description: "Fornisce funzioni di supporto per convertire tra varie unità di misura in Java."
type: docs
weight: 131
url: /it/java/com.aspose.words/convertutil/
---

**Inheritance:**
java.lang.Object
```
public class ConvertUtil
```

Fornisce funzioni di supporto per convertire tra varie unità di misura.

Per saperne di più, visita l'articolo di documentazione [ Convert Between Measurement Units ][Convert Between Measurement Units].

 **Examples:** 

Mostra come regolare la dimensione della carta, l'orientamento, i margini, insieme ad altre impostazioni per una sezione.

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

Mostra come specificare le proprietà della pagina in pollici.

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
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [inchToPoint(double inches)](#inchToPoint-double) | Converte i pollici in punti. |
| [millimeterToPoint(double millimeters)](#millimeterToPoint-double) | Converte i millimetri in punti. |
| [pixelToNewDpi(double pixels, double oldDpi, double newDpi)](#pixelToNewDpi-double-double-double) | Converte i pixel da una risoluzione all'altra. |
| [pixelToPoint(double pixels)](#pixelToPoint-double) | Converte i pixel in punti. |
| [pixelToPoint(double pixels, double resolution)](#pixelToPoint-double-double) | Converte i pixel in punti alla risoluzione pixel specificata. |
| [pointToInch(double points)](#pointToInch-double) | Converte i punti in pollici. |
| [pointToPixel(double points)](#pointToPixel-double) | Converte i punti in pixel. |
| [pointToPixel(double points, double resolution)](#pointToPixel-double-double) | Converte i punti in pixel alla risoluzione pixel specificata. |
### inchToPoint(double inches) {#inchToPoint-double}
```
public static double inchToPoint(double inches)
```


Converte i pollici in punti.

 **Remarks:** 

1 pollice equivale a 72 punti.

 **Examples:** 

Mostra come regolare la dimensione della carta, l'orientamento, i margini, insieme ad altre impostazioni per una sezione.

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

Mostra come specificare le proprietà della pagina in pollici.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pollici | double | Il valore da convertire. |

**Returns:**
double
### millimeterToPoint(double millimeters) {#millimeterToPoint-double}
```
public static double millimeterToPoint(double millimeters)
```


Converte i millimetri in punti.

 **Remarks:** 

1 pollice equivale a 25,4 millimetri. 1 pollice equivale a 72 punti.

 **Examples:** 

Mostra come specificare le proprietà della pagina in millimetri.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| millimetri | double | Il valore da convertire. |

**Returns:**
double
### pixelToNewDpi(double pixels, double oldDpi, double newDpi) {#pixelToNewDpi-double-double-double}
```
public static int pixelToNewDpi(double pixels, double oldDpi, double newDpi)
```


Converte i pixel da una risoluzione all'altra.

 **Examples:** 

Mostra come utilizzare la conversione da punti a pixel con risoluzione predefinita e personalizzata.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pixel | double | Il valore da convertire. |
| oldDpi | double | La risoluzione dpi corrente (punti per pollice). |
| newDpi | double | La nuova risoluzione dpi (punti per pollice). |

**Returns:**
int
### pixelToPoint(double pixels) {#pixelToPoint-double}
```
public static double pixelToPoint(double pixels)
```


Converte i pixel in punti.  Converte i pixel in punti a 96 dpi.

 **Remarks:** 

1 pollice equivale a 72 punti.

 **Examples:** 

Mostra come specificare le proprietà della pagina in pixel.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pixel | double | Il valore da convertire. |

**Returns:**
double
### pixelToPoint(double pixels, double resolution) {#pixelToPoint-double-double}
```
public static double pixelToPoint(double pixels, double resolution)
```


Converte i pixel in punti alla risoluzione pixel specificata.

 **Remarks:** 

1 pollice equivale a 72 punti.

 **Examples:** 

Mostra come utilizzare la conversione da punti a pixel con risoluzione predefinita e personalizzata.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pixel | double | Il valore da convertire. |
| risoluzione | double | La risoluzione dpi (punti per pollice). |

**Returns:**
double
### pointToInch(double points) {#pointToInch-double}
```
public static double pointToInch(double points)
```


Converte i punti in pollici.

 **Remarks:** 

1 pollice equivale a 72 punti.

 **Examples:** 

Mostra come specificare le proprietà della pagina in pollici.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| punti | double | Il valore da convertire. |

**Returns:**
double
### pointToPixel(double points) {#pointToPixel-double}
```
public static double pointToPixel(double points)
```


Converte i punti in pixel.  Converte i punti in pixel a 96 dpi.

 **Remarks:** 

1 pollice equivale a 72 punti.

 **Examples:** 

Mostra come specificare le proprietà della pagina in pixel.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| punti | double | Il valore da convertire. |

**Returns:**
double
### pointToPixel(double points, double resolution) {#pointToPixel-double-double}
```
public static double pointToPixel(double points, double resolution)
```


Converte i punti in pixel alla risoluzione pixel specificata.

 **Remarks:** 

1 pollice equivale a 72 punti.

 **Examples:** 

Mostra come utilizzare la conversione da punti a pixel con risoluzione predefinita e personalizzata.

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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| punti | double | Il valore da convertire. |
| risoluzione | double | La risoluzione dpi (punti per pollice). |

**Returns:**
double
