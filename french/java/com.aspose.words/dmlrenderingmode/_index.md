---
title: "DmlRenderingMode"
linktitle: "DmlRenderingMode"
second_title: "Aspose.Words pour Java"
description: "Spécifie comment les formes DrawingML sont rendues aux formats de page fixes en Java."
type: docs
weight: 158
url: /fr/java/com.aspose.words/dmlrenderingmode/
---

**Inheritance:**
java.lang.Object
```
public class DmlRenderingMode
```

Spécifie comment les formes DrawingML sont rendues vers des formats de page fixes.

 **Examples:** 

Montre comment configurer la qualité de rendu des effets DrawingML dans un document lors de son enregistrement au format PDF.

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

Montre comment rendre les formes de secours lors de l'enregistrement au format PDF.

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
## Champs

| Champ | Description |
| --- | --- |
| [DRAWING_ML](#DRAWING-ML) | Aspose.Words ignore la forme de secours de DrawingML et rend le DrawingML lui‑même. |
| [FALLBACK](#FALLBACK) | Si une forme de secours est disponible pour DrawingML, Aspose.Words rend la forme de secours à la place du DrawingML. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String dmlRenderingModeName)](#fromName-java.lang.String) |  |
| [getName(int dmlRenderingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int dmlRenderingMode)](#toString-int) |  |
### DRAWING_ML {#DRAWING-ML}
```
public static int DRAWING_ML
```


Aspose.Words ignore la forme de secours de DrawingML et rend le DrawingML lui‑même. C’est le mode par défaut.

### FALLBACK {#FALLBACK}
```
public static int FALLBACK
```


Si une forme de secours est disponible pour DrawingML, Aspose.Words rend la forme de secours à la place du DrawingML.

 **Remarks:** 

Veuillez noter qu'après avoir enregistré un document au format de page fixe avec le mode de rendu DML de secours, les formes DML dans le modèle de document AW sont remplacées de façon permanente par leurs homologues de secours. En conséquence, enregistrer à nouveau le même document utilisera toujours les formes de secours, même si [DmlRenderingMode](../../com.aspose.words/dmlrenderingmode/) est défini sur [DRAWING\_ML](../../com.aspose.words/dmlrenderingmode/\#DRAWING-ML).

### length {#length}
```
public static int length
```


### fromName(String dmlRenderingModeName) {#fromName-java.lang.String}
```
public static int fromName(String dmlRenderingModeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| dmlRenderingModeName | java.lang.String |  |

**Returns:**
int
### getName(int dmlRenderingMode) {#getName-int}
```
public static String getName(int dmlRenderingMode)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| dmlRenderingMode | int |  |

**Returns:**
java.lang.String
