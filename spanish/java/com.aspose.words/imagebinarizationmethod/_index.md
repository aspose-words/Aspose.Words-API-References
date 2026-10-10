---
title: "ImageBinarizationMethod"
linktitle: "ImageBinarizationMethod"
second_title: "Aspose.Words para Java"
description: "Especifica el método utilizado para binarizar la imagen en Java."
type: docs
weight: 389
url: /es/java/com.aspose.words/imagebinarizationmethod/
---

**Inheritance:**
java.lang.Object
```
public class ImageBinarizationMethod
```

Especifica el método utilizado para binarizar la imagen.

 **Examples:** 

Muestra cómo establecer el umbral de error de binarización TIFF al usar el método Floyd‑Steinberg para renderizar una imagen TIFF.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [FLOYD_STEINBERG_DITHERING](#FLOYD-STEINBERG-DITHERING) | Especifica el tramado usando el método de difusión de error Floyd‑Steinberg. |
| [THRESHOLD](#THRESHOLD) | Especifica el método de umbral. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String imageBinarizationMethodName)](#fromName-java.lang.String) |  |
| [getName(int imageBinarizationMethod)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int imageBinarizationMethod)](#toString-int) |  |
### FLOYD_STEINBERG_DITHERING {#FLOYD-STEINBERG-DITHERING}
```
public static int FLOYD_STEINBERG_DITHERING
```


Especifica el tramado usando el método de difusión de error Floyd‑Steinberg.

### THRESHOLD {#THRESHOLD}
```
public static int THRESHOLD
```


Especifica el método de umbral.

### length {#length}
```
public static int length
```


### fromName(String imageBinarizationMethodName) {#fromName-java.lang.String}
```
public static int fromName(String imageBinarizationMethodName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| imageBinarizationMethodName | java.lang.String |  |

**Returns:**
int
### getName(int imageBinarizationMethod) {#getName-int}
```
public static String getName(int imageBinarizationMethod)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| imageBinarizationMethod | int |  |

**Returns:**
java.lang.String
