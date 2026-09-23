---
title: "PdfZoomBehavior"
linktitle: "PdfZoomBehavior"
second_title: "Aspose.Words per Java"
description: "Specifica il tipo di zoom applicato a un documento PDF quando viene aperto in un visualizzatore PDF in Java."
type: docs
weight: 544
url: /it/java/com.aspose.words/pdfzoombehavior/
---

**Inheritance:**
java.lang.Object
```
public class PdfZoomBehavior
```

Specifica il tipo di zoom applicato a un documento PDF quando viene aperto in un visualizzatore PDF.

 **Examples:** 

Mostra come impostare lo zoom predefinito che un lettore applica quando apre un documento PDF renderizzato.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [FIT_BOX](#FIT-BOX) | Adatta il riquadro di delimitazione (rettangolo che contiene tutti gli elementi visibili sulla pagina). |
| [FIT_HEIGHT](#FIT-HEIGHT) | Adatta l'altezza della pagina. |
| [FIT_PAGE](#FIT-PAGE) | Visualizza la pagina in modo che sia interamente visibile. |
| [FIT_WIDTH](#FIT-WIDTH) | Adatta la larghezza della pagina. |
| [NONE](#NONE) | Il modo in cui il documento viene visualizzato è lasciato al visualizzatore PDF. |
| [ZOOM_FACTOR](#ZOOM-FACTOR) | Visualizza la pagina usando il fattore di zoom specificato. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String pdfZoomBehaviorName)](#fromName-java.lang.String) |  |
| [getName(int pdfZoomBehavior)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfZoomBehavior)](#toString-int) |  |
### FIT_BOX {#FIT-BOX}
```
public static int FIT_BOX
```


Adatta il riquadro di delimitazione (rettangolo che contiene tutti gli elementi visibili sulla pagina).

### FIT_HEIGHT {#FIT-HEIGHT}
```
public static int FIT_HEIGHT
```


Adatta l'altezza della pagina.

### FIT_PAGE {#FIT-PAGE}
```
public static int FIT_PAGE
```


Visualizza la pagina in modo che sia interamente visibile.

### FIT_WIDTH {#FIT-WIDTH}
```
public static int FIT_WIDTH
```


Adatta la larghezza della pagina.

### NONE {#NONE}
```
public static int NONE
```


Il modo in cui il documento viene visualizzato è lasciato al visualizzatore PDF. Di solito il visualizzatore mostra il documento per adattarlo alla larghezza della pagina.

### ZOOM_FACTOR {#ZOOM-FACTOR}
```
public static int ZOOM_FACTOR
```


Visualizza la pagina usando il fattore di zoom specificato.

### length {#length}
```
public static int length
```


### fromName(String pdfZoomBehaviorName) {#fromName-java.lang.String}
```
public static int fromName(String pdfZoomBehaviorName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pdfZoomBehaviorName | java.lang.String |  |

**Returns:**
int
### getName(int pdfZoomBehavior) {#getName-int}
```
public static String getName(int pdfZoomBehavior)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pdfZoomBehavior | int |  |

**Returns:**
java.lang.String
