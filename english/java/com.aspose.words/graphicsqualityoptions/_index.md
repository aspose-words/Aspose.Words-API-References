---
title: GraphicsQualityOptions
second_title: Aspose.Words for Java API Reference
description: Allows to specify additional .
type: docs
weight: 313
url: /java/com.aspose.words/graphicsqualityoptions/
---

**Inheritance:**
java.lang.Object
```
public class GraphicsQualityOptions
```

Allows to specify additional .

To learn more, visit the **Save a Document** documentation article.

Gets current  to view or to add new hints. Overwrites current .
## Methods

| Method | Description |
| --- | --- |
| [getRenderingHints()](#getRenderingHints--) |  |
| [setRenderingHints(RenderingHints renderingHints)](#setRenderingHints-java.awt.RenderingHints-) |  |
| [getUseTileFlipMode()](#getUseTileFlipMode--) | Gets a flag indicating whether WrapMode is TileFlipXY. |
| [setUseTileFlipMode(boolean value)](#setUseTileFlipMode-boolean-) | Sets a flag indicating whether WrapMode is TileFlipXY. |
### getRenderingHints() {#getRenderingHints--}
```
public RenderingHints getRenderingHints()
```




**Returns:**
java.awt.RenderingHints
### setRenderingHints(RenderingHints renderingHints) {#setRenderingHints-java.awt.RenderingHints-}
```
public void setRenderingHints(RenderingHints renderingHints)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| renderingHints | java.awt.RenderingHints |  |

### getUseTileFlipMode() {#getUseTileFlipMode--}
```
public boolean getUseTileFlipMode()
```


Gets a flag indicating whether WrapMode is TileFlipXY.

The WrapMode specifies how a texture or gradient is tiled when it is smaller than the area being filled.

By default uses WrapMode\#TILE.TILE (specifies tiling without flipping). This causes inaccurate rendering of the scaled image(with high resolution).

This property allows to switch WrapMode to WrapMode\#TILE\_FLIP\_XY.TILE\_FLIP\_XY (specifies that tiles are flipped horizontally as you move along a row and flipped vertically as you move along a column).

**Returns:**
boolean - A flag indicating whether WrapMode is TileFlipXY.
### setUseTileFlipMode(boolean value) {#setUseTileFlipMode-boolean-}
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

