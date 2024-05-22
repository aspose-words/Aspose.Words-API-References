---
title: PdfZoomBehavior
linktitle: PdfZoomBehavior
second_title: Aspose.Words for Java
description: Specifies the type of zoom applied to a PDF document when it is opened in a PDF viewer in Java.
type: docs
weight: 502
url: /java/com.aspose.words/pdfzoombehavior/
---

**Inheritance:**
java.lang.Object
```
public class PdfZoomBehavior
```

Specifies the type of zoom applied to a PDF document when it is opened in a PDF viewer.

 **Examples:** 

Shows how to set the default zooming that a reader applies when opening a rendered PDF document.

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
## Fields

| Field | Description |
| --- | --- |
| [FIT_BOX](#FIT-BOX) | Fits the bounding box (rectangle containing all visible elements on the page). |
| [FIT_HEIGHT](#FIT-HEIGHT) | Fits the height of the page. |
| [FIT_PAGE](#FIT-PAGE) | Displays the page so it visible entirely. |
| [FIT_WIDTH](#FIT-WIDTH) | Fits the width of the page. |
| [NONE](#NONE) | How the document is displayed is left to the PDF viewer. |
| [ZOOM_FACTOR](#ZOOM-FACTOR) | Displays the page using the specified zoom factor. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String pdfZoomBehaviorName)](#fromName-java.lang.String) |  |
| [getName(int pdfZoomBehavior)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfZoomBehavior)](#toString-int) |  |
### FIT_BOX {#FIT-BOX}
```
public static int FIT_BOX
```


Fits the bounding box (rectangle containing all visible elements on the page).

### FIT_HEIGHT {#FIT-HEIGHT}
```
public static int FIT_HEIGHT
```


Fits the height of the page.

### FIT_PAGE {#FIT-PAGE}
```
public static int FIT_PAGE
```


Displays the page so it visible entirely.

### FIT_WIDTH {#FIT-WIDTH}
```
public static int FIT_WIDTH
```


Fits the width of the page.

### NONE {#NONE}
```
public static int NONE
```


How the document is displayed is left to the PDF viewer. Usually the viewer displays the document to fit page width.

### ZOOM_FACTOR {#ZOOM-FACTOR}
```
public static int ZOOM_FACTOR
```


Displays the page using the specified zoom factor.

### length {#length}
```
public static int length
```


### fromName(String pdfZoomBehaviorName) {#fromName-java.lang.String}
```
public static int fromName(String pdfZoomBehaviorName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfZoomBehaviorName | java.lang.String |  |

**Returns:**
int
### getName(int pdfZoomBehavior) {#getName-int}
```
public static String getName(int pdfZoomBehavior)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| pdfZoomBehavior | int |  |

**Returns:**
java.lang.String
