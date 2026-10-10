---
title: "PdfZoomBehavior"
linktitle: "PdfZoomBehavior"
second_title: "Aspose.Words für Java"
description: "Gibt den Zoomtyp an, der auf ein PDF‑Dokument angewendet wird, wenn es in einem PDF‑Betrachter in Java geöffnet wird."
type: docs
weight: 544
url: /de/java/com.aspose.words/pdfzoombehavior/
---

**Inheritance:**
java.lang.Object
```
public class PdfZoomBehavior
```

Gibt den Zoomtyp an, der auf ein PDF‑Dokument angewendet wird, wenn es in einem PDF‑Betrachter geöffnet wird.

 **Examples:** 

Zeigt, wie man das Standard‑Zoomen festlegt, das ein Reader beim Öffnen eines gerenderten PDF‑Dokuments anwendet.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [FIT_BOX](#FIT-BOX) | Passt die Begrenzungsbox (Rechteck, das alle sichtbaren Elemente auf der Seite enthält). |
| [FIT_HEIGHT](#FIT-HEIGHT) | Passt die Höhe der Seite an. |
| [FIT_PAGE](#FIT-PAGE) | Zeigt die Seite so an, dass sie vollständig sichtbar ist. |
| [FIT_WIDTH](#FIT-WIDTH) | Passt die Breite der Seite an. |
| [NONE](#NONE) | Wie das Dokument angezeigt wird, bleibt dem PDF‑Betrachter überlassen. |
| [ZOOM_FACTOR](#ZOOM-FACTOR) | Zeigt die Seite mit dem angegebenen Zoom‑Faktor an. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String pdfZoomBehaviorName)](#fromName-java.lang.String) |  |
| [getName(int pdfZoomBehavior)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfZoomBehavior)](#toString-int) |  |
### FIT_BOX {#FIT-BOX}
```
public static int FIT_BOX
```


Passt die Begrenzungsbox (Rechteck, das alle sichtbaren Elemente auf der Seite enthält).

### FIT_HEIGHT {#FIT-HEIGHT}
```
public static int FIT_HEIGHT
```


Passt die Höhe der Seite an.

### FIT_PAGE {#FIT-PAGE}
```
public static int FIT_PAGE
```


Zeigt die Seite so an, dass sie vollständig sichtbar ist.

### FIT_WIDTH {#FIT-WIDTH}
```
public static int FIT_WIDTH
```


Passt die Breite der Seite an.

### NONE {#NONE}
```
public static int NONE
```


Wie das Dokument angezeigt wird, bleibt dem PDF‑Betrachter überlassen. Normalerweise passt der Betrachter das Dokument an die Seitenbreite an.

### ZOOM_FACTOR {#ZOOM-FACTOR}
```
public static int ZOOM_FACTOR
```


Zeigt die Seite mit dem angegebenen Zoom‑Faktor an.

### length {#length}
```
public static int length
```


### fromName(String pdfZoomBehaviorName) {#fromName-java.lang.String}
```
public static int fromName(String pdfZoomBehaviorName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pdfZoomBehaviorName | java.lang.String |  |

**Returns:**
int
### getName(int pdfZoomBehavior) {#getName-int}
```
public static String getName(int pdfZoomBehavior)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pdfZoomBehavior | int |  |

**Returns:**
java.lang.String
