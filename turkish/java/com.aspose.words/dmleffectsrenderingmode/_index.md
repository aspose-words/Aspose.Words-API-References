---
title: "DmlEffectsRenderingMode"
linktitle: "DmlEffectsRenderingMode"
second_title: "Aspose.Words Java için"
description: "Java'da DrawingML efektlerinin sabit sayfa formatlarına nasıl render edildiğini belirtir."
type: docs
weight: 157
url: /tr/java/com.aspose.words/dmleffectsrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class DmlEffectsRenderingMode
```

DrawingML efektlerinin sabit sayfa formatlarına nasıl işleneceğini belirtir.

 **Examples:** 

Bir belgeyi PDF olarak kaydederken DrawingML efektlerinin render kalitesini nasıl yapılandıracağımızı gösterir.

```

 Document doc = new Document(getMyDir() + "DrawingML shape effects.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.None" to discard all DrawingML effects.
 // Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.Simplified"
 // to render a simplified version of DrawingML effects.
 // Set the "DmlEffectsRenderingMode" property to "DmlEffectsRenderingMode.Fine" to
 // render DrawingML effects with more accuracy and also with more processing cost.
 options.setDmlEffectsRenderingMode(effectsRenderingMode);

 Assert.assertEquals(DmlRenderingMode.DRAWING_ML, options.getDmlRenderingMode());

 doc.save(getArtifactsDir() + "PdfSaveOptions.DrawingMLEffects.pdf", options);
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [FINE](#FINE) | DrawingML efektleri, gelişmiş işleme dahil olan ince modda render edilir. |
| [NONE](#NONE) | Hiçbir DrawingML efekti render edilmez. |
| [SIMPLIFIED](#SIMPLIFIED) | DrawingML efektlerinin render edilmesi basitleştirilir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String dmlEffectsRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int dmlEffectsRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int dmlEffectsRenderingMode)](#toString-int) |  |
### FINE {#FINE}
```
public static int FINE
```


DrawingML efektleri, gelişmiş işleme dahil olan ince modda render edilir. Bu modda efektlerin render edilmesi, [SIMPLIFIED](../../com.aspose.words/dmleffectsrenderingmode/\#SIMPLIFIED) moduna göre daha iyi sonuçlar verir ancak daha yüksek bir performans maliyeti gerektirir.

### NONE {#NONE}
```
public static int NONE
```


Hiçbir DrawingML efekti render edilmez.

### SIMPLIFIED {#SIMPLIFIED}
```
public static int SIMPLIFIED
```


DrawingML efektlerinin render edilmesi basitleştirilir.

### length {#length}
```
public static int length
```


### fromName(String dmlEffectsRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String dmlEffectsRenderingModeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| dmlEffectsRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int dmlEffectsRenderingMode) {#getName-int}
```
public static String getName(int dmlEffectsRenderingMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| dmlEffectsRenderingMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int dmlEffectsRenderingMode) {#toString-int}
```
public static String toString(int dmlEffectsRenderingMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| dmlEffectsRenderingMode | int |  |

**Returns:**
java.lang.String
