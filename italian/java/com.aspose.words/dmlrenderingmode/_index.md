---
title: "DmlRenderingMode"
linktitle: "DmlRenderingMode"
second_title: "Aspose.Words per Java"
description: "Specifica come le forme DrawingML vengono renderizzate nei formati di pagina fissi in Java."
type: docs
weight: 158
url: /it/java/com.aspose.words/dmlrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class DmlRenderingMode
```

Specifica come vengono renderizzate le forme DrawingML nei formati di pagina fissi.

 **Examples:** 

Mostra come configurare la qualità di rendering degli effetti DrawingML in un documento quando lo salviamo in PDF.

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

Mostra come renderizzare le forme di fallback durante il salvataggio in PDF.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [DRAWING_ML](#DRAWING-ML) | Aspose.Words ignora la forma di fallback di DrawingML e renderizza direttamente DrawingML. |
| [FALLBACK](#FALLBACK) | Se è disponibile una forma di fallback per DrawingML, Aspose.Words renderizza la forma di fallback invece di DrawingML. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String dmlRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int dmlRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int dmlRenderingMode)](#toString-int) |  |
### DRAWING_ML {#DRAWING-ML}
```
public static int DRAWING_ML
```


Aspose.Words ignora la forma di fallback di DrawingML e renderizza direttamente DrawingML. Questa è la modalità predefinita.

### FALLBACK {#FALLBACK}
```
public static int FALLBACK
```


Se è disponibile una forma di fallback per DrawingML, Aspose.Words renderizza la forma di fallback invece di DrawingML.

 **Remarks:** 

Si noti che dopo aver salvato un documento in un formato di pagina fisso con la modalità di rendering DML di fallback, le forme DML nel modello di documento AW vengono sostituite permanentemente con le loro controparti di fallback. Di conseguenza, salvare nuovamente lo stesso documento utilizzerà sempre le forme di fallback, anche se [DmlRenderingMode](../../com.aspose.words/dmlrenderingmode/) è impostato su [DRAWING\_ML](../../com.aspose.words/dmlrenderingmode/\#DRAWING-ML).

### length {#length}
```
public static int length
```


### fromName(String dmlRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String dmlRenderingModeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dmlRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int dmlRenderingMode) {#getName-int}
```
public static String getName(int dmlRenderingMode)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dmlRenderingMode | int |  |

**Returns:**
java.lang.String
