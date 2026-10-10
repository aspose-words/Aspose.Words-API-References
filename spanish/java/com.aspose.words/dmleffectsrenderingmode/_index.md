---
title: "DmlEffectsRenderingMode"
linktitle: "DmlEffectsRenderingMode"
second_title: "Aspose.Words para Java"
description: "Especifica cómo se renderizan los efectos DrawingML en formatos de página fija en Java."
type: docs
weight: 157
url: /es/java/com.aspose.words/dmleffectsrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class DmlEffectsRenderingMode
```

Especifica cómo se renderizan los efectos DrawingML en formatos de página fija.

 **Examples:** 

Muestra cómo configurar la calidad de renderizado de los efectos DrawingML en un documento al guardarlo en PDF.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [FINE](#FINE) | Los efectos DrawingML se renderizan en modo fino, lo que implica procesamiento avanzado. |
| [NONE](#NONE) | No se renderizan efectos DrawingML. |
| [SIMPLIFIED](#SIMPLIFIED) | El renderizado de los efectos DrawingML está simplificado. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String dmlEffectsRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int dmlEffectsRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int dmlEffectsRenderingMode)](#toString-int) |  |
### FINE {#FINE}
```
public static int FINE
```


Los efectos DrawingML se renderizan en modo fino, lo que implica procesamiento avanzado. En este modo, el renderizado de los efectos brinda mejores resultados pero a un mayor costo de rendimiento que el modo [SIMPLIFIED](../../com.aspose.words/dmleffectsrenderingmode/\\#SIMPLIFIED).

### NONE {#NONE}
```
public static int NONE
```


No se renderizan efectos DrawingML.

### SIMPLIFIED {#SIMPLIFIED}
```
public static int SIMPLIFIED
```


El renderizado de los efectos DrawingML está simplificado.

### length {#length}
```
public static int length
```


### fromName(String dmlEffectsRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String dmlEffectsRenderingModeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| dmlEffectsRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int dmlEffectsRenderingMode) {#getName-int}
```
public static String getName(int dmlEffectsRenderingMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| dmlEffectsRenderingMode | int |  |

**Returns:**
java.lang.String
