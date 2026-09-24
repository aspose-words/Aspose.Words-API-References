---
title: "ImageColorMode"
linktitle: "ImageColorMode"
second_title: "Aspose.Words para Java"
description: "Especifica el modo de color para las imágenes generadas de las páginas del documento en Java."
type: docs
weight: 390
url: /es/java/com.aspose.words/imagecolormode/
---

**Inheritance:**
java.lang.Object
```
public class ImageColorMode
```

Especifica el modo de color para las imágenes generadas de las páginas del documento.

 **Examples:** 

Muestra cómo establecer un modo de color al renderizar documentos.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [BLACK_AND_WHITE](#BLACK-AND-WHITE) | Las páginas del documento se renderizarán como imágenes en blanco y negro. |
| [GRAYSCALE](#GRAYSCALE) | Las páginas del documento se renderizarán como imágenes en escala de grises. |
| [NONE](#NONE) | Las páginas del documento se renderizarán como imágenes en color. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String imageColorModeName)](#fromName-java.lang.String) |  |
| [getName(int imageColorMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int imageColorMode)](#toString-int) |  |
### BLACK_AND_WHITE {#BLACK-AND-WHITE}
```
public static int BLACK_AND_WHITE
```


Las páginas del documento se renderizarán como imágenes en blanco y negro.

### GRAYSCALE {#GRAYSCALE}
```
public static int GRAYSCALE
```


Las páginas del documento se renderizarán como imágenes en escala de grises.

### NONE {#NONE}
```
public static int NONE
```


Las páginas del documento se renderizarán como imágenes en color.

### length {#length}
```
public static int length
```


### fromName(String imageColorModeName) {#fromName-java.lang.String}
```
public static int fromName(String imageColorModeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| imageColorModeName | java.lang.String |  |

**Returns:**
int
### getName(int imageColorMode) {#getName-int}
```
public static String getName(int imageColorMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| imageColorMode | int |  |

**Returns:**
java.lang.String
