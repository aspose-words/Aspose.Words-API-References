---
title: "ImagePixelFormat"
linktitle: "ImagePixelFormat"
second_title: "Aspose.Words per Java"
description: "Specifica il formato pixel per le immagini generate delle pagine del documento in Java."
type: docs
weight: 393
url: /it/java/com.aspose.words/imagepixelformat/
---

**Inheritance:**
java.lang.Object
```
public class ImagePixelFormat
```

Specifica il formato pixel per le immagini generate delle pagine del documento.

 **Examples:** 

Mostra come selezionare un tasso di bit per pixel con cui renderizzare un documento in un'immagine.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.getParagraphFormat().setStyle(doc.getStyles().get("Heading 1"));
 builder.writeln("Hello world!");
 builder.insertImage(getImageDir() + "Logo.jpg");

 Assert.assertTrue(new File(getImageDir() + "Logo.jpg").length() < 21000);

 // When we save the document as an image, we can pass a SaveOptions object to
 // select a pixel format for the image that the saving operation will generate.
 // Various bit per pixel rates will affect the quality and file size of the generated image.
 ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.PNG);
 imageSaveOptions.setPixelFormat(imagePixelFormat);

 // We can clone ImageSaveOptions instances.
 Assert.assertNotEquals(imageSaveOptions, imageSaveOptions.deepClone());

 doc.save(getArtifactsDir() + "ImageSaveOptions.PixelFormat.png", imageSaveOptions);
 
```
## Campi

| Campo | Descrizione |
| --- | --- |
| [FORMAT_16_BPP_ARGB_1555](#FORMAT-16-BPP-ARGB-1555) | 16 bit per pixel, ARGB. |
| [FORMAT_16_BPP_RGB_555](#FORMAT-16-BPP-RGB-555) | 16 bit per pixel, RGB. |
| [FORMAT_16_BPP_RGB_565](#FORMAT-16-BPP-RGB-565) | 16 bit per pixel, RGB. |
| [FORMAT_1_BPP_INDEXED](#FORMAT-1-BPP-INDEXED) | 1 bit per pixel, Indicizzato. |
| [FORMAT_24_BPP_RGB](#FORMAT-24-BPP-RGB) | 24 bit per pixel, RGB. |
| [FORMAT_32_BPP_ARGB](#FORMAT-32-BPP-ARGB) | 32 bit per pixel, ARGB. |
| [FORMAT_32_BPP_P_ARGB](#FORMAT-32-BPP-P-ARGB) | 32 bit per pixel, ARGB, alfa premoltiplicata. |
| [FORMAT_32_BPP_RGB](#FORMAT-32-BPP-RGB) | 32 bit per pixel, RGB. |
| [FORMAT_48_BPP_RGB](#FORMAT-48-BPP-RGB) | 48 bit per pixel, RGB. |
| [FORMAT_64_BPP_ARGB](#FORMAT-64-BPP-ARGB) | 64 bit per pixel, ARGB. |
| [FORMAT_64_BPP_P_ARGB](#FORMAT-64-BPP-P-ARGB) | 64 bit per pixel, ARGB, alfa premoltiplicata. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String imagePixelFormatName)](#fromName-java.lang.String) |  |
| [getName(int imagePixelFormat)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int imagePixelFormat)](#toString-int) |  |
### FORMAT_16_BPP_ARGB_1555 {#FORMAT-16-BPP-ARGB-1555}
```
public static int FORMAT_16_BPP_ARGB_1555
```


16 bit per pixel, ARGB.

### FORMAT_16_BPP_RGB_555 {#FORMAT-16-BPP-RGB-555}
```
public static int FORMAT_16_BPP_RGB_555
```


16 bit per pixel, RGB.

### FORMAT_16_BPP_RGB_565 {#FORMAT-16-BPP-RGB-565}
```
public static int FORMAT_16_BPP_RGB_565
```


16 bit per pixel, RGB.

### FORMAT_1_BPP_INDEXED {#FORMAT-1-BPP-INDEXED}
```
public static int FORMAT_1_BPP_INDEXED
```


1 bit per pixel, Indicizzato.

### FORMAT_24_BPP_RGB {#FORMAT-24-BPP-RGB}
```
public static int FORMAT_24_BPP_RGB
```


24 bit per pixel, RGB.

### FORMAT_32_BPP_ARGB {#FORMAT-32-BPP-ARGB}
```
public static int FORMAT_32_BPP_ARGB
```


32 bit per pixel, ARGB.

### FORMAT_32_BPP_P_ARGB {#FORMAT-32-BPP-P-ARGB}
```
public static int FORMAT_32_BPP_P_ARGB
```


32 bit per pixel, ARGB, alfa premoltiplicata.

### FORMAT_32_BPP_RGB {#FORMAT-32-BPP-RGB}
```
public static int FORMAT_32_BPP_RGB
```


32 bit per pixel, RGB.

### FORMAT_48_BPP_RGB {#FORMAT-48-BPP-RGB}
```
public static int FORMAT_48_BPP_RGB
```


48 bit per pixel, RGB.

### FORMAT_64_BPP_ARGB {#FORMAT-64-BPP-ARGB}
```
public static int FORMAT_64_BPP_ARGB
```


64 bit per pixel, ARGB.

### FORMAT_64_BPP_P_ARGB {#FORMAT-64-BPP-P-ARGB}
```
public static int FORMAT_64_BPP_P_ARGB
```


64 bit per pixel, ARGB, alfa premoltiplicata.

### length {#length}
```
public static int length
```


### fromName(String imagePixelFormatName) {#fromName-java.lang.String}
```
public static int fromName(String imagePixelFormatName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| imagePixelFormatName | java.lang.String |  |

**Returns:**
int
### getName(int imagePixelFormat) {#getName-int}
```
public static String getName(int imagePixelFormat)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| imagePixelFormat | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int imagePixelFormat) {#toString-int}
```
public static String toString(int imagePixelFormat)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| imagePixelFormat | int |  |

**Returns:**
java.lang.String
