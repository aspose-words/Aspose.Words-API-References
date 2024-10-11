---
title: PageInfo
linktitle: PageInfo
second_title: Aspose.Words for Java
description: Represents information about a particular document page in Java.
type: docs
weight: 484
url: /java/com.aspose.words/pageinfo/
---

**Inheritance:**
java.lang.Object
```
public class PageInfo
```

Represents information about a particular document page.

To learn more, visit the [ Rendering ][Rendering] documentation article.

 **Remarks:** 

The page width and height returned by this object represent the "final" size of the page e.g. they are already rotated to the correct orientation.


[Rendering]: https://docs.aspose.com/words/java/rendering/
## Methods

| Method | Description |
| --- | --- |
| [getColored()](#getColored) | Returns  true  if the page contains colored content. |
| [getHeightInPoints()](#getHeightInPoints) | Gets the height of the page in points. |
| [getLandscape()](#getLandscape) | Returns  true  if the page orientation specified in the document for this page is landscape. |
| [getPaperSize()](#getPaperSize) | Gets the paper size as enumeration. |
| [getPaperTray()](#getPaperTray) | Gets the paper tray (bin) for this page as specified in the document. |
| [getSizeInPixels(float scale, float dpi)](#getSizeInPixels-float-float) | Calculates the page size in pixels for a specified zoom factor and resolution. |
| [getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)](#getSizeInPixels-float-float-float) | Calculates the page size in pixels for a specified zoom factor and resolution. |
| [getSizeInPoints()](#getSizeInPoints) | Gets the page size in points. |
| [getWidthInPoints()](#getWidthInPoints) | Gets the width of the page in points. |
### getColored() {#getColored}
```
public boolean getColored()
```


Returns  true  if the page contains colored content.

 **Examples:** 

Shows how to check whether the page is in color or not.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 // Check that the first page of the document is not colored.
 Assert.assertFalse(doc.getPageInfo(0).getColored());
 
```

**Returns:**
boolean -  true  if the page contains colored content.
### getHeightInPoints() {#getHeightInPoints}
```
public float getHeightInPoints()
```


Gets the height of the page in points.

**Returns:**
float - The height of the page in points.
### getLandscape() {#getLandscape}
```
public boolean getLandscape()
```


Returns  true  if the page orientation specified in the document for this page is landscape.

**Returns:**
boolean -  true  if the page orientation specified in the document for this page is landscape.
### getPaperSize() {#getPaperSize}
```
public int getPaperSize()
```


Gets the paper size as enumeration.

**Returns:**
int - The paper size as enumeration. The returned value is one of [PaperSize](../../com.aspose.words/papersize/) constants.
### getPaperTray() {#getPaperTray}
```
public int getPaperTray()
```


Gets the paper tray (bin) for this page as specified in the document. The value is implementation (printer) specific.

**Returns:**
int - The paper tray (bin) for this page as specified in the document.
### getSizeInPixels(float scale, float dpi) {#getSizeInPixels-float-float}
```
public Dimension getSizeInPixels(float scale, float dpi)
```


Calculates the page size in pixels for a specified zoom factor and resolution.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| scale | float | The zoom factor (1.0 is 100%). |
| dpi | float | The resolution (horizontal and vertical) to convert from points to pixels (dots per inch). |

**Returns:**
java.awt.Dimension - The size of the page in pixels.
### getSizeInPixels(float scale, float horizontalDpi, float verticalDpi) {#getSizeInPixels-float-float-float}
```
public Dimension getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)
```


Calculates the page size in pixels for a specified zoom factor and resolution.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| scale | float | The zoom factor (1.0 is 100%). |
| horizontalDpi | float | The horizontal resolution to convert from points to pixels (dots per inch). |
| verticalDpi | float | The vertical resolution to convert from points to pixels (dots per inch). |

**Returns:**
java.awt.Dimension - The size of the page in pixels.
### getSizeInPoints() {#getSizeInPoints}
```
public Point2D.Float getSizeInPoints()
```


Gets the page size in points.

**Returns:**
java.awt.geom.Point2D.Float - The page size in points.
### getWidthInPoints() {#getWidthInPoints}
```
public float getWidthInPoints()
```


Gets the width of the page in points.

**Returns:**
float - The width of the page in points.
