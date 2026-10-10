---
title: "DmlEffectsRenderingMode"
linktitle: "DmlEffectsRenderingMode"
second_title: "Aspose.Words per Java"
description: "Specifica come gli effetti DrawingML vengono renderizzati nei formati di pagina fissi in Java."
type: docs
weight: 157
url: /it/java/com.aspose.words/dmleffectsrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class DmlEffectsRenderingMode
```

Specifica come vengono renderizzati gli effetti DrawingML nei formati di pagina fissi.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [FINE](#FINE) | Gli effetti DrawingML sono renderizzati in modalità fine, che comporta una elaborazione avanzata. |
| [NONE](#NONE) | Nessun effetto DrawingML viene renderizzato. |
| [SIMPLIFIED](#SIMPLIFIED) | Il rendering degli effetti DrawingML è semplificato. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String dmlEffectsRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int dmlEffectsRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int dmlEffectsRenderingMode)](#toString-int) |  |
### FINE {#FINE}
```
public static int FINE
```


Gli effetti DrawingML sono renderizzati in modalità fine, che comporta una elaborazione avanzata. In questa modalità il rendering degli effetti fornisce risultati migliori ma a un costo di prestazioni più elevato rispetto alla modalità [SIMPLIFIED](../../com.aspose.words/dmleffectsrenderingmode/\#SIMPLIFIED).

### NONE {#NONE}
```
public static int NONE
```


Nessun effetto DrawingML viene renderizzato.

### SIMPLIFIED {#SIMPLIFIED}
```
public static int SIMPLIFIED
```


Il rendering degli effetti DrawingML è semplificato.

### length {#length}
```
public static int length
```


### fromName(String dmlEffectsRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String dmlEffectsRenderingModeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dmlEffectsRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int dmlEffectsRenderingMode) {#getName-int}
```
public static String getName(int dmlEffectsRenderingMode)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dmlEffectsRenderingMode | int |  |

**Returns:**
java.lang.String
