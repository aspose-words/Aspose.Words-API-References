---
title: "ImageColorMode"
linktitle: "ImageColorMode"
second_title: "Aspose.Words per Java"
description: "Specifica la modalità colore per le immagini generate delle pagine del documento in Java."
type: docs
weight: 390
url: /it/java/com.aspose.words/imagecolormode/
---

**Inheritance:**
java.lang.Object
```
public class ImageColorMode
```

Specifica la modalità colore per le immagini generate delle pagine del documento.

 **Examples:** 

Mostra come impostare una modalità colore durante il rendering dei documenti.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [BLACK_AND_WHITE](#BLACK-AND-WHITE) | Le pagine del documento verranno renderizzate come immagini in bianco e nero. |
| [GRAYSCALE](#GRAYSCALE) | Le pagine del documento verranno renderizzate come immagini in scala di grigi. |
| [NONE](#NONE) | Le pagine del documento verranno renderizzate come immagini a colori. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String imageColorModeName)](#fromName-java.lang.String) |  |
| [getName(int imageColorMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int imageColorMode)](#toString-int) |  |
### BLACK_AND_WHITE {#BLACK-AND-WHITE}
```
public static int BLACK_AND_WHITE
```


Le pagine del documento verranno renderizzate come immagini in bianco e nero.

### GRAYSCALE {#GRAYSCALE}
```
public static int GRAYSCALE
```


Le pagine del documento verranno renderizzate come immagini in scala di grigi.

### NONE {#NONE}
```
public static int NONE
```


Le pagine del documento verranno renderizzate come immagini a colori.

### length {#length}
```
public static int length
```


### fromName(String imageColorModeName) {#fromName-java.lang.String}
```
public static int fromName(String imageColorModeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| imageColorModeName | java.lang.String |  |

**Returns:**
int
### getName(int imageColorMode) {#getName-int}
```
public static String getName(int imageColorMode)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| imageColorMode | int |  |

**Returns:**
java.lang.String
