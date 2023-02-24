---
title: GraphicsQualityOptions
linktitle: GraphicsQualityOptions
second_title: Aspose.Words for Java API Reference
description: Allows to specify additional in Java.
type: docs
weight: 315
url: /java/com.aspose.words/graphicsqualityoptions/
---

**Inheritance:**
java.lang.Object
```
public class GraphicsQualityOptions
```

Allows to specify additional .

To learn more, visit the [ Save a Document ][Save a Document] documentation article.

Gets current  to view or to add new hints. Overwrites current .


[Save a Document]: https://docs.aspose.com/words/java/save-a-document/
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getRenderingHints()](#getRenderingHints) |  |
| [getUseTileFlipMode()](#getUseTileFlipMode) | Gets a flag indicating whether WrapMode is TileFlipXY. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setRenderingHints(RenderingHints renderingHints)](#setRenderingHints-java.awt.RenderingHints) |  |
| [setUseTileFlipMode(boolean value)](#setUseTileFlipMode-boolean) | Sets a flag indicating whether WrapMode is TileFlipXY. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getRenderingHints() {#getRenderingHints}
```
public RenderingHints getRenderingHints()
```




**Returns:**
java.awt.RenderingHints
### getUseTileFlipMode() {#getUseTileFlipMode}
```
public boolean getUseTileFlipMode()
```


Gets a flag indicating whether WrapMode is TileFlipXY.

The WrapMode specifies how a texture or gradient is tiled when it is smaller than the area being filled.

By default uses WrapMode\#TILE.TILE (specifies tiling without flipping). This causes inaccurate rendering of the scaled image(with high resolution).

This property allows to switch WrapMode to WrapMode\#TILE\_FLIP\_XY.TILE\_FLIP\_XY (specifies that tiles are flipped horizontally as you move along a row and flipped vertically as you move along a column).

**Returns:**
boolean - A flag indicating whether WrapMode is TileFlipXY.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### setRenderingHints(RenderingHints renderingHints) {#setRenderingHints-java.awt.RenderingHints}
```
public void setRenderingHints(RenderingHints renderingHints)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| renderingHints | java.awt.RenderingHints |  |

### setUseTileFlipMode(boolean value) {#setUseTileFlipMode-boolean}
```
public void setUseTileFlipMode(boolean value)
```


Sets a flag indicating whether WrapMode is TileFlipXY.

The WrapMode specifies how a texture or gradient is tiled when it is smaller than the area being filled.

By default uses WrapMode\#TILE.TILE (specifies tiling without flipping). This causes inaccurate rendering of the scaled image(with high resolution).

This property allows to switch WrapMode to WrapMode\#TILE\_FLIP\_XY.TILE\_FLIP\_XY (specifies that tiles are flipped horizontally as you move along a row and flipped vertically as you move along a column).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether WrapMode is TileFlipXY. |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

