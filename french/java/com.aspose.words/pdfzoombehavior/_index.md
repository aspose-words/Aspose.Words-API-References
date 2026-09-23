---
title: "PdfZoomBehavior"
linktitle: "PdfZoomBehavior"
second_title: "Aspose.Words pour Java"
description: "Spécifie le type de zoom appliqué à un document PDF lorsqu'il est ouvert dans un visualiseur PDF en Java."
type: docs
weight: 544
url: /fr/java/com.aspose.words/pdfzoombehavior/
---

**Inheritance:**
java.lang.Object
```
public class PdfZoomBehavior
```

Spécifie le type de zoom appliqué à un document PDF lorsqu'il est ouvert dans un visualiseur PDF.

 **Examples:** 

Montre comment définir le zoom par défaut qu'un lecteur applique lors de l'ouverture d'un document PDF rendu.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);
 builder.writeln("Hello world!");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 // Set the "ZoomBehavior" property to "PdfZoomBehavior.ZoomFactor" to get a PDF reader to
 // apply a percentage-based zoom factor when we open the document with it.
 // Set the "ZoomFactor" property to "25" to give the zoom factor a value of 25%.
 PdfSaveOptions options = new PdfSaveOptions();
 {
     options.setZoomBehavior(PdfZoomBehavior.ZOOM_FACTOR);
     options.setZoomFactor(25);
 }

 // When we open this document using a reader such as Adobe Acrobat, we will see the document scaled at 1/4 of its actual size.
 doc.save(getArtifactsDir() + "PdfSaveOptions.ZoomBehaviour.pdf", options);
 
```
## Champs

| Champ | Description |
| --- | --- |
| [FIT_BOX](#FIT-BOX) | Ajuste la boîte englobante (rectangle contenant tous les éléments visibles sur la page). |
| [FIT_HEIGHT](#FIT-HEIGHT) | Ajuste la hauteur de la page. |
| [FIT_PAGE](#FIT-PAGE) | Affiche la page de manière à ce qu'elle soit entièrement visible. |
| [FIT_WIDTH](#FIT-WIDTH) | Ajuste la largeur de la page. |
| [NONE](#NONE) | La façon dont le document est affiché est laissée au visualiseur PDF. |
| [ZOOM_FACTOR](#ZOOM-FACTOR) | Affiche la page en utilisant le facteur de zoom spécifié. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String pdfZoomBehaviorName)](#fromName-java.lang.String) |  |
| [getName(int pdfZoomBehavior)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfZoomBehavior)](#toString-int) |  |
### FIT_BOX {#FIT-BOX}
```
public static int FIT_BOX
```


Ajuste la boîte englobante (rectangle contenant tous les éléments visibles sur la page).

### FIT_HEIGHT {#FIT-HEIGHT}
```
public static int FIT_HEIGHT
```


Ajuste la hauteur de la page.

### FIT_PAGE {#FIT-PAGE}
```
public static int FIT_PAGE
```


Affiche la page de manière à ce qu'elle soit entièrement visible.

### FIT_WIDTH {#FIT-WIDTH}
```
public static int FIT_WIDTH
```


Ajuste la largeur de la page.

### NONE {#NONE}
```
public static int NONE
```


La façon dont le document est affiché est laissée au visualiseur PDF. Généralement, le visualiseur affiche le document pour ajuster la largeur de la page.

### ZOOM_FACTOR {#ZOOM-FACTOR}
```
public static int ZOOM_FACTOR
```


Affiche la page en utilisant le facteur de zoom spécifié.

### length {#length}
```
public static int length
```


### fromName(String pdfZoomBehaviorName) {#fromName-java.lang.String}
```
public static int fromName(String pdfZoomBehaviorName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| pdfZoomBehaviorName | java.lang.String |  |

**Returns:**
int
### getName(int pdfZoomBehavior) {#getName-int}
```
public static String getName(int pdfZoomBehavior)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| pdfZoomBehavior | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pdfZoomBehavior) {#toString-int}
```
public static String toString(int pdfZoomBehavior)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| pdfZoomBehavior | int |  |

**Returns:**
java.lang.String
