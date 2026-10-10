---
title: "ColorMode"
linktitle: "ColorMode"
second_title: "Aspose.Words Java için"
description: "Java'da renklerin nasıl işleneceğini belirtir."
type: docs
weight: 105
url: /tr/java/com.aspose.words/colormode/
---

**Inheritance:**
java.lang.Object
```
public class ColorMode
```

Renklerin nasıl işlendiğini belirtir.

 **Examples:** 

Kaydetme seçenekleri özelliğiyle görüntü renginin nasıl değiştirileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 // Set the "ColorMode" property to "Grayscale" to render all images from the document in black and white.
 // The size of the output document may be larger with this setting.
 // Set the "ColorMode" property to "Normal" to render all images in color.
 PdfSaveOptions pdfSaveOptions = new PdfSaveOptions();
 {
     pdfSaveOptions.setColorMode(colorMode);
 }

 doc.save(getArtifactsDir() + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [GRAYSCALE](#GRAYSCALE) | Beyazdan siyaha kadar bir dizi gri tonunda renklerle işleme. |
| [NORMAL](#NORMAL) | Değiştirilmemiş renklerle işleme. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String colorModeName)](#fromName-java.lang.String) |  |
| [getName(int colorMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int colorMode)](#toString-int) |  |
### GRAYSCALE {#GRAYSCALE}
```
public static int GRAYSCALE
```


Beyazdan siyaha kadar bir dizi gri tonunda renklerle işleme.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Değiştirilmemiş renklerle işleme.

### length {#length}
```
public static int length
```


### fromName(String colorModeName) {#fromName-java.lang.String}
```
public static int fromName(String colorModeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| colorModeName | java.lang.String |  |

**Returns:**
int
### getName(int colorMode) {#getName-int}
```
public static String getName(int colorMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| colorMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int colorMode) {#toString-int}
```
public static String toString(int colorMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| colorMode | int |  |

**Returns:**
java.lang.String
