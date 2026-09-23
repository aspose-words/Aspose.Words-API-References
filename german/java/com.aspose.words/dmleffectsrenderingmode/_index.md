---
title: "DmlEffectsRenderingMode"
linktitle: "DmlEffectsRenderingMode"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie DrawingML-Effekte in Java in feste Seitenformate gerendert werden."
type: docs
weight: 157
url: /de/java/com.aspose.words/dmleffectsrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class DmlEffectsRenderingMode
```

Gibt an, wie DrawingML‑Effekte in feste Seitenformate gerendert werden.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [FINE](#FINE) | DrawingML-Effekte werden im Feinkommodus gerendert, der eine erweiterte Verarbeitung beinhaltet. |
| [NONE](#NONE) | Keine DrawingML-Effekte werden gerendert. |
| [SIMPLIFIED](#SIMPLIFIED) | Das Rendern von DrawingML-Effekten ist vereinfacht. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String dmlEffectsRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int dmlEffectsRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int dmlEffectsRenderingMode)](#toString-int) |  |
### FINE {#FINE}
```
public static int FINE
```


DrawingML-Effekte werden im Feinkommodus gerendert, der eine erweiterte Verarbeitung beinhaltet. In diesem Modus liefert das Rendern von Effekten bessere Ergebnisse, jedoch zu höheren Leistungskosten als der [SIMPLIFIED](../../com.aspose.words/dmleffectsrenderingmode/\#SIMPLIFIED)-Modus.

### NONE {#NONE}
```
public static int NONE
```


Keine DrawingML-Effekte werden gerendert.

### SIMPLIFIED {#SIMPLIFIED}
```
public static int SIMPLIFIED
```


Das Rendern von DrawingML-Effekten ist vereinfacht.

### length {#length}
```
public static int length
```


### fromName(String dmlEffectsRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String dmlEffectsRenderingModeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dmlEffectsRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int dmlEffectsRenderingMode) {#getName-int}
```
public static String getName(int dmlEffectsRenderingMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dmlEffectsRenderingMode | int |  |

**Returns:**
java.lang.String
