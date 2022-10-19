---
title: PageInfo
second_title: Aspose.Words for Java API Reference
description: Represents information about a particular document page.
type: docs
weight: 434
url: /java/com.aspose.words/pageinfo/
---

**Inheritance:**
java.lang.Object
```
public class PageInfo
```

Represents information about a particular document page.

To learn more, visit the **Rendering** documentation article.

The page width and height returned by this object represent the "final" size of the page e.g. they are already rotated to the correct orientation.
## Methods

| Method | Description |
| --- | --- |
| [getSizeInPixels(float scale, float dpi)](#getSizeInPixels-float-float-) | Calculates the page size in pixels for a specified zoom factor and resolution. |
| [getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)](#getSizeInPixels-float-float-float-) | Calculates the page size in pixels for a specified zoom factor and resolution. |
| [getPaperSize()](#getPaperSize--) | Gets the paper size as enumeration. |
| [getWidthInPoints()](#getWidthInPoints--) | Gets the width of the page in points. |
| [getHeightInPoints()](#getHeightInPoints--) | Gets the height of the page in points. |
| [getSizeInPoints()](#getSizeInPoints--) | Gets the page size in points. |
| [getPaperTray()](#getPaperTray--) | Gets the paper tray (bin) for this page as specified in the document. |
| [getLandscape()](#getLandscape--) | Returns true if the page orientation specified in the document for this page is landscape. |
### getSizeInPixels(float scale, float dpi) {#getSizeInPixels-float-float-}
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
### getSizeInPixels(float scale, float horizontalDpi, float verticalDpi) {#getSizeInPixels-float-float-float-}
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
### getPaperSize() {#getPaperSize--}
```
public int getPaperSize()
```


Gets the paper size as enumeration.

**Returns:**
int - The paper size as enumeration. The returned value is one of [PaperSize](../../com.aspose.words/papersize) constants.
### getWidthInPoints() {#getWidthInPoints--}
```
public float getWidthInPoints()
```


Gets the width of the page in points.

**Returns:**
float - The width of the page in points.
### getHeightInPoints() {#getHeightInPoints--}
```
public float getHeightInPoints()
```


Gets the height of the page in points.

**Returns:**
float - The height of the page in points.
### getSizeInPoints() {#getSizeInPoints--}
```
public Point2D.Float getSizeInPoints()
```


Gets the page size in points.

**Returns:**
java.awt.geom.Point2D.Float - The page size in points.
### getPaperTray() {#getPaperTray--}
```
public int getPaperTray()
```


Gets the paper tray (bin) for this page as specified in the document. The value is implementation (printer) specific.

**Returns:**
int - The paper tray (bin) for this page as specified in the document.
### getLandscape() {#getLandscape--}
```
public boolean getLandscape()
```


Returns true if the page orientation specified in the document for this page is landscape.

**Returns:**
boolean - True if the page orientation specified in the document for this page is landscape.
