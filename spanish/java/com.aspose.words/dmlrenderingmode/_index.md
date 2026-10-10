---
title: "DmlRenderingMode"
linktitle: "DmlRenderingMode"
second_title: "Aspose.Words para Java"
description: "Especifica cómo se renderizan las formas DrawingML a formatos de página fija en Java."
type: docs
weight: 158
url: /es/java/com.aspose.words/dmlrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class DmlRenderingMode
```

Especifica cómo se renderizan las formas DrawingML en formatos de página fija.

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

Muestra cómo renderizar formas de reserva al guardar en PDF.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [DRAWING_ML](#DRAWING-ML) | Aspose.Words ignora la forma de reserva de DrawingML y renderiza DrawingML directamente. |
| [FALLBACK](#FALLBACK) | Si hay una forma de reserva disponible para DrawingML, Aspose.Words renderiza la forma de reserva en lugar de DrawingML. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String dmlRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int dmlRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int dmlRenderingMode)](#toString-int) |  |
### DRAWING_ML {#DRAWING-ML}
```
public static int DRAWING_ML
```


Aspose.Words ignora la forma de reserva de DrawingML y renderiza DrawingML directamente. Este es el modo predeterminado.

### FALLBACK {#FALLBACK}
```
public static int FALLBACK
```


Si hay una forma de reserva disponible para DrawingML, Aspose.Words renderiza la forma de reserva en lugar de DrawingML.

 **Remarks:** 

Tenga en cuenta que después de guardar un documento en un formato de página fija con el modo de renderizado DML de reserva, las formas DML en el modelo de documento AW se reemplazan permanentemente por sus contrapartes de reserva. Como resultado, al guardar el mismo documento nuevamente siempre se usarán las formas de reserva, incluso si [DmlRenderingMode](../../com.aspose.words/dmlrenderingmode/) está configurado a [DRAWING\_ML](../../com.aspose.words/dmlrenderingmode/\#DRAWING-ML).

### length {#length}
```
public static int length
```


### fromName(String dmlRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String dmlRenderingModeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| dmlRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int dmlRenderingMode) {#getName-int}
```
public static String getName(int dmlRenderingMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| dmlRenderingMode | int |  |

**Returns:**
java.lang.String
