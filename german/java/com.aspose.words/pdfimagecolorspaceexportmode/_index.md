---
title: "PdfImageColorSpaceExportMode"
linktitle: "PdfImageColorSpaceExportMode"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie der Farbraum für die Bilder in einem PDF-Dokument in Java ausgewählt wird."
type: docs
weight: 536
url: /de/java/com.aspose.words/pdfimagecolorspaceexportmode/
---

**Inheritance:**
java.lang.Object
```
public class PdfImageColorSpaceExportMode
```

Gibt an, wie der Farbraum für die Bilder im PDF-Dokument ausgewählt wird.

 **Examples:** 

Zeigt, wie man für Bilder in einem Dokument beim Exportieren in PDF einen anderen Farbraum festlegt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("Jpeg image:");
 builder.insertImage(getImageDir() + "Logo.jpg");
 builder.insertParagraph();
 builder.writeln("Png image:");
 builder.insertImage(getImageDir() + "Transparent background logo.png");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();

 // Set the "ImageColorSpaceExportMode" property to "PdfImageColorSpaceExportMode.Auto" to get Aspose.Words to
 // automatically select the color space for images in the document that it converts to PDF.
 // In most cases, the color space will be RGB.
 // Set the "ImageColorSpaceExportMode" property to "PdfImageColorSpaceExportMode.SimpleCmyk"
 // to use the CMYK color space for all images in the saved PDF.
 // Aspose.Words will also apply Flate compression to all images and ignore the "ImageCompression" property's value.
 pdfSaveOptions.setImageColorSpaceExportMode(pdfImageColorSpaceExportMode);

 doc.save(getArtifactsDir() + "PdfSaveOptions.ImageColorSpaceExportMode.pdf", pdfSaveOptions);
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [AUTO](#AUTO) | Aspose.Words wählt automatisch den am besten geeigneten Farbraum für jedes Bild aus. |
| [SIMPLE_CMYK](#SIMPLE-CMYK) | Aspose.Words konvertiert RGB-Bilder mithilfe einer einfachen Formel in den CMYK-Farbraum. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String pdfImageColorSpaceExportModeName)](#fromName-java.lang.String) |  |
| [getName(int pdfImageColorSpaceExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfImageColorSpaceExportMode)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Aspose.Words wählt automatisch den am besten geeigneten Farbraum für jedes Bild aus.

 **Remarks:** 

Die meisten Bilder werden im RGB-Farbraum gespeichert. Auch indizierte und Graustufen-Farbräume können verwendet werden. Der CMYK-Farbraum wird niemals verwendet.

Bei einigen Bildern kann der Farbraum auf verschiedenen Plattformen unterschiedlich sein.

### SIMPLE_CMYK {#SIMPLE-CMYK}
```
public static int SIMPLE_CMYK
```


Aspose.Words konvertiert RGB-Bilder mithilfe einer einfachen Formel in den CMYK-Farbraum.

 **Remarks:** 

Bilder im RGB-Farbraum werden mithilfe der Formel in CMYK konvertiert: Black = minimum(1-Red,1-Green,1-Blue). Cyan = (1-Red-Black)/(1-Black). Magenta = (1-Green-Black)/(1-Black). Yellow = (1-Blue-Black)/(1-Black). RGB-Werte werden normalisiert – sie liegen zwischen 0 und 1,0.

### length {#length}
```
public static int length
```


### fromName(String pdfImageColorSpaceExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String pdfImageColorSpaceExportModeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pdfImageColorSpaceExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int pdfImageColorSpaceExportMode) {#getName-int}
```
public static String getName(int pdfImageColorSpaceExportMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pdfImageColorSpaceExportMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pdfImageColorSpaceExportMode) {#toString-int}
```
public static String toString(int pdfImageColorSpaceExportMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pdfImageColorSpaceExportMode | int |  |

**Returns:**
java.lang.String
