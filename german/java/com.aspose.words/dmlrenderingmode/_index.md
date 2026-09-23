---
title: "DmlRenderingMode"
linktitle: "DmlRenderingMode"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie DrawingML‑Formen in feste Seitenformate in Java gerendert werden."
type: docs
weight: 158
url: /de/java/com.aspose.words/dmlrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class DmlRenderingMode
```

Gibt an, wie DrawingML‑Formen in feste Seitenformate gerendert werden.

 **Examples:** 

Zeigt, wie die Renderqualität von DrawingML‑Effekten in einem Dokument konfiguriert wird, wenn wir es als PDF speichern.

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

Zeigt, wie Ersatzformen beim Speichern als PDF gerendert werden.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [DRAWING_ML](#DRAWING-ML) | Aspose.Words ignoriert die Ersatzform von DrawingML und rendert DrawingML selbst. |
| [FALLBACK](#FALLBACK) | Wenn für DrawingML eine Ersatzform verfügbar ist, rendert Aspose.Words die Ersatzform anstelle von DrawingML. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String dmlRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int dmlRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int dmlRenderingMode)](#toString-int) |  |
### DRAWING_ML {#DRAWING-ML}
```
public static int DRAWING_ML
```


Aspose.Words ignoriert die Ersatzform von DrawingML und rendert DrawingML selbst. Dies ist der Standardmodus.

### FALLBACK {#FALLBACK}
```
public static int FALLBACK
```


Wenn für DrawingML eine Ersatzform verfügbar ist, rendert Aspose.Words die Ersatzform anstelle von DrawingML.

 **Remarks:** 

Bitte beachten Sie, dass nach dem Speichern eines Dokuments in ein festes Seitenformat mit dem Ersatz‑DML‑Rendermodus die DML‑Formen im AW‑Dokumentmodell dauerhaft durch ihre Ersatzgegenstücke ersetzt werden. Infolgedessen wird beim erneuten Speichern desselben Dokuments stets die Ersatzform verwendet, selbst wenn [DmlRenderingMode](../../com.aspose.words/dmlrenderingmode/) auf [DRAWING\_ML](../../com.aspose.words/dmlrenderingmode/\#DRAWING-ML) gesetzt ist.

### length {#length}
```
public static int length
```


### fromName(String dmlRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String dmlRenderingModeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dmlRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int dmlRenderingMode) {#getName-int}
```
public static String getName(int dmlRenderingMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dmlRenderingMode | int |  |

**Returns:**
java.lang.String
