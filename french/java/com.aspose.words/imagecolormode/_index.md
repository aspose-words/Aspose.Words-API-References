---
title: "ImageColorMode"
linktitle: "ImageColorMode"
second_title: "Aspose.Words pour Java"
description: "Spécifie le mode couleur pour les images générées des pages de document en Java."
type: docs
weight: 390
url: /fr/java/com.aspose.words/imagecolormode/
---

**Inheritance:**
java.lang.Object
```
public class ImageColorMode
```

Spécifie le mode couleur pour les images générées des pages du document.

 **Examples:** 

Montre comment définir un mode couleur lors du rendu des documents.

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
## Champs

| Champ | Description |
| --- | --- |
| [BLACK_AND_WHITE](#BLACK-AND-WHITE) | Les pages du document seront rendues en images noir et blanc. |
| [GRAYSCALE](#GRAYSCALE) | Les pages du document seront rendues en images en niveaux de gris. |
| [NONE](#NONE) | Les pages du document seront rendues en images couleur. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String imageColorModeName)](#fromName-java.lang.String) |  |
| [getName(int imageColorMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int imageColorMode)](#toString-int) |  |
### BLACK_AND_WHITE {#BLACK-AND-WHITE}
```
public static int BLACK_AND_WHITE
```


Les pages du document seront rendues en images noir et blanc.

### GRAYSCALE {#GRAYSCALE}
```
public static int GRAYSCALE
```


Les pages du document seront rendues en images en niveaux de gris.

### NONE {#NONE}
```
public static int NONE
```


Les pages du document seront rendues en images couleur.

### length {#length}
```
public static int length
```


### fromName(String imageColorModeName) {#fromName-java.lang.String}
```
public static int fromName(String imageColorModeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| imageColorModeName | java.lang.String |  |

**Returns:**
int
### getName(int imageColorMode) {#getName-int}
```
public static String getName(int imageColorMode)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| imageColorMode | int |  |

**Returns:**
java.lang.String
