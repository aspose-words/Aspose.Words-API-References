---
title: PdfZoomBehavior
second_title: Aspose.Words for Java API Reference
description: Specifies the type of zoom applied to a PDF document when it is opened in a PDF viewer.
type: docs
weight: 463
url: /java/com.aspose.words/pdfzoombehavior/
---

**Inheritance:**
java.lang.Object
```
public class PdfZoomBehavior
```

Specifies the type of zoom applied to a PDF document when it is opened in a PDF viewer.
## Fields

| Field | Description |
| --- | --- |
| [NONE](#NONE) | How the document is displayed is left to the PDF viewer. |
| [ZOOM_FACTOR](#ZOOM-FACTOR) | Displays the page using the specified zoom factor. |
| [FIT_PAGE](#FIT-PAGE) | Displays the page so it visible entirely. |
| [FIT_WIDTH](#FIT-WIDTH) | Fits the width of the page. |
| [FIT_HEIGHT](#FIT-HEIGHT) | Fits the height of the page. |
| [FIT_BOX](#FIT-BOX) | Fits the bounding box (rectangle containing all visible elements on the page). |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int pdfZoomBehavior)](#getName-int-) |  |
| [toString(int pdfZoomBehavior)](#toString-int-) |  |
| [fromName(String pdfZoomBehaviorName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
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

### FIT_HEIGHT {#FIT-HEIGHT}
```
public static int FIT_HEIGHT
```


Fits the height of the page.

### FIT_BOX {#FIT-BOX}
```
public static int FIT_BOX
```


Fits the bounding box (rectangle containing all visible elements on the page).

### length {#length}
```
public static int length
```


### getName(int pdfZoomBehavior) {#getName-int-}
```
public static String getName(int pdfZoomBehavior)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfZoomBehavior | int |  |

**Returns:**
java.lang.String
### toString(int pdfZoomBehavior) {#toString-int-}
```
public static String toString(int pdfZoomBehavior)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfZoomBehavior | int |  |

**Returns:**
java.lang.String
### fromName(String pdfZoomBehaviorName) {#fromName-java.lang.String-}
```
public static int fromName(String pdfZoomBehaviorName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfZoomBehaviorName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
