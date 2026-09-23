---
title: "ImageBinarizationMethod"
linktitle: "ImageBinarizationMethod"
second_title: "Aspose.Words für Java"
description: "Gibt die Methode an, die zum Binarisieren von Bildern in Java verwendet wird."
type: docs
weight: 389
url: /de/java/com.aspose.words/imagebinarizationmethod/
---

**Inheritance:**
java.lang.Object
```
public class ImageBinarizationMethod
```

Gibt die Methode an, die zum Binarisieren von Bildern verwendet wird.

 **Examples:** 

Zeigt, wie man den Binärschwellenwert für TIFF festlegt, wenn man die Floyd‑Steinberg‑Methode zum Rendern eines TIFF‑Bildes verwendet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 // When we save the document as a TIFF, we can pass a SaveOptions object to
 // adjust the dithering that Aspose.Words will apply when rendering this image.
 // The default value of the "ThresholdForFloydSteinbergDithering" property is 128.
 // Higher values tend to produce darker images.
 ImageSaveOptions options = new ImageSaveOptions(SaveFormat.TIFF);
 options.setTiffCompression(TiffCompression.CCITT_3);
 options.setTiffBinarizationMethod(ImageBinarizationMethod.FLOYD_STEINBERG_DITHERING);
 options.setThresholdForFloydSteinbergDithering((byte) 240);

 doc.save(getArtifactsDir() + "ImageSaveOptions.FloydSteinbergDithering.tiff", options);
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [FLOYD_STEINBERG_DITHERING](#FLOYD-STEINBERG-DITHERING) | Gibt das Dithering unter Verwendung der Floyd‑Steinberg-Fehlerdiffusionsmethode an. |
| [THRESHOLD](#THRESHOLD) | Gibt die Schwellenwertmethode an. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String imageBinarizationMethodName)](#fromName-java.lang.String) |  |
| [getName(int imageBinarizationMethod)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int imageBinarizationMethod)](#toString-int) |  |
### FLOYD_STEINBERG_DITHERING {#FLOYD-STEINBERG-DITHERING}
```
public static int FLOYD_STEINBERG_DITHERING
```


Gibt das Dithering unter Verwendung der Floyd‑Steinberg-Fehlerdiffusionsmethode an.

### THRESHOLD {#THRESHOLD}
```
public static int THRESHOLD
```


Gibt die Schwellenwertmethode an.

### length {#length}
```
public static int length
```


### fromName(String imageBinarizationMethodName) {#fromName-java.lang.String}
```
public static int fromName(String imageBinarizationMethodName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| imageBinarizationMethodName | java.lang.String |  |

**Returns:**
int
### getName(int imageBinarizationMethod) {#getName-int}
```
public static String getName(int imageBinarizationMethod)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| imageBinarizationMethod | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int imageBinarizationMethod) {#toString-int}
```
public static String toString(int imageBinarizationMethod)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| imageBinarizationMethod | int |  |

**Returns:**
java.lang.String
