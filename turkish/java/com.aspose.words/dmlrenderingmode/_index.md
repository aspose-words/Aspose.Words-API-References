---
title: "DmlRenderingMode"
linktitle: "DmlRenderingMode"
second_title: "Aspose.Words Java için"
description: "Java'da DrawingML şekillerinin sabit sayfa formatlarına nasıl render edildiğini belirtir."
type: docs
weight: 158
url: /tr/java/com.aspose.words/dmlrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class DmlRenderingMode
```

DrawingML şekillerinin sabit sayfa formatlarına nasıl işleneceğini belirtir.

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

PDF olarak kaydederken yedek (fallback) şekillerin nasıl render edileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "DrawingML shape fallbacks.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "DmlRenderingMode" property to "DmlRenderingMode.Fallback"
 // to substitute DML shapes with their fallback shapes.
 // Set the "DmlRenderingMode" property to "DmlRenderingMode.DrawingML"
 // to render the DML shapes themselves.
 options.setDmlRenderingMode(dmlRenderingMode);

 doc.save(getArtifactsDir() + "PdfSaveOptions.DrawingMLFallback.pdf", options);
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [DRAWING_ML](#DRAWING-ML) | Aspose.Words, DrawingML'in yedek şekillerini yok sayar ve DrawingML'i kendisi render eder. |
| [FALLBACK](#FALLBACK) | DrawingML için yedek şekil mevcutsa, Aspose.Words DrawingML yerine yedek şekli render eder. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String dmlRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int dmlRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int dmlRenderingMode)](#toString-int) |  |
### DRAWING_ML {#DRAWING-ML}
```
public static int DRAWING_ML
```


Aspose.Words, DrawingML'in yedek şekillerini yok sayar ve DrawingML'i kendisi render eder. Bu varsayılan moddur.

### FALLBACK {#FALLBACK}
```
public static int FALLBACK
```


DrawingML için yedek şekil mevcutsa, Aspose.Words DrawingML yerine yedek şekli render eder.

 **Remarks:** 

Lütfen unutmayın ki, bir belgeyi yedek DML render moduyla sabit sayfa formatına kaydettikten sonra, AW belge modelindeki DML şekilleri kalıcı olarak yedek karşılıklarıyla değiştirilir. Sonuç olarak, aynı belgeyi tekrar kaydetmek her zaman yedek şekilleri kullanacaktır, hatta [DmlRenderingMode](../../com.aspose.words/dmlrenderingmode/) [DRAWING\_ML](../../com.aspose.words/dmlrenderingmode/\#DRAWING-ML) olarak ayarlı olsa bile.

### length {#length}
```
public static int length
```


### fromName(String dmlRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String dmlRenderingModeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| dmlRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int dmlRenderingMode) {#getName-int}
```
public static String getName(int dmlRenderingMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| dmlRenderingMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int dmlRenderingMode) {#toString-int}
```
public static String toString(int dmlRenderingMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| dmlRenderingMode | int |  |

**Returns:**
java.lang.String
