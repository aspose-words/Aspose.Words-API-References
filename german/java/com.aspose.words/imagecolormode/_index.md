---
title: "ImageColorMode"
linktitle: "ImageColorMode"
second_title: "Aspose.Words für Java"
description: "Gibt den Farbmodus für die in Java erzeugten Bilder von Dokumentseiten an."
type: docs
weight: 390
url: /de/java/com.aspose.words/imagecolormode/
---

**Inheritance:**
java.lang.Object
```
public class ImageColorMode
```

Gibt den Farbmodus für die erzeugten Bilder der Dokumentseiten an.

 **Examples:** 

Zeigt, wie man beim Rendern von Dokumenten einen Farbmodus festlegt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 Assert.assertTrue(new File(getImageDir() + "Logo.jpg").length() < 20200);

 // When we save the document as an image, we can pass a SaveOptions object to
 // select a color mode for the image that the saving operation will generate.
 // If we set the "ImageColorMode" property to "ImageColorMode.BlackAndWhite",
 // the saving operation will apply grayscale color reduction while rendering the document.
 // If we set the "ImageColorMode" property to "ImageColorMode.Grayscale",
 // the saving operation will render the document into a monochrome image.
 // If we set the "ImageColorMode" property to "None", the saving operation will apply the default method
 // and preserve all the document's colors in the output image.
 ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.PNG);
 imageSaveOptions.setImageColorMode(imageColorMode);

 doc.save(getArtifactsDir() + "ImageSaveOptions.ColorMode.png", imageSaveOptions);
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [BLACK_AND_WHITE](#BLACK-AND-WHITE) | Die Seiten des Dokuments werden als Schwarz‑weiß‑Bilder gerendert. |
| [GRAYSCALE](#GRAYSCALE) | Die Seiten des Dokuments werden als Graustufen‑Bilder gerendert. |
| [NONE](#NONE) | Die Seiten des Dokuments werden als Farbbilder gerendert. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String imageColorModeName)](#fromName-java.lang.String) |  |
| [getName(int imageColorMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int imageColorMode)](#toString-int) |  |
### BLACK_AND_WHITE {#BLACK-AND-WHITE}
```
public static int BLACK_AND_WHITE
```


Die Seiten des Dokuments werden als Schwarz‑weiß‑Bilder gerendert.

### GRAYSCALE {#GRAYSCALE}
```
public static int GRAYSCALE
```


Die Seiten des Dokuments werden als Graustufen‑Bilder gerendert.

### NONE {#NONE}
```
public static int NONE
```


Die Seiten des Dokuments werden als Farbbilder gerendert.

### length {#length}
```
public static int length
```


### fromName(String imageColorModeName) {#fromName-java.lang.String}
```
public static int fromName(String imageColorModeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| imageColorModeName | java.lang.String |  |

**Returns:**
int
### getName(int imageColorMode) {#getName-int}
```
public static String getName(int imageColorMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| imageColorMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int imageColorMode) {#toString-int}
```
public static String toString(int imageColorMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| imageColorMode | int |  |

**Returns:**
java.lang.String
