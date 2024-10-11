---
title: GraphicsQualityOptions
linktitle: GraphicsQualityOptions
second_title: Aspose.Words for Java
description: Allows to specify additional java.awt.RenderingHints in Java.
type: docs
weight: 351
url: /java/com.aspose.words/graphicsqualityoptions/
---

**Inheritance:**
java.lang.Object
```
public class GraphicsQualityOptions
```

Allows to specify additional **java.awt.RenderingHints**.

To learn more, visit the [ Save a Document ][Save a Document] documentation article.

Gets current **java.awt.RenderingHints** to view or to add new hints. Overwrites current **java.awt.RenderingHints**.

 **Examples:** 

Shows how to set render quality options while converting documents to image formats.

```

 Document doc = new Document(getMyDir() + "Rendering.docx");

 GraphicsQualityOptions qualityOptions = new GraphicsQualityOptions();
 qualityOptions.getRenderingHints().put(RenderingHints.KEY_ANTIALIASING, RenderingHints.VALUE_ANTIALIAS_ON); // SmoothingMode
 qualityOptions.getRenderingHints().put(RenderingHints.KEY_TEXT_ANTIALIASING, RenderingHints.VALUE_TEXT_ANTIALIAS_ON); // TextRenderingHint
 qualityOptions.getRenderingHints().put(RenderingHints.KEY_COLOR_RENDERING, RenderingHints.VALUE_COLOR_RENDER_QUALITY); // CompositingMode
 qualityOptions.getRenderingHints().put(RenderingHints.KEY_RENDERING, RenderingHints.VALUE_RENDER_QUALITY); // CompositingQuality
 qualityOptions.getRenderingHints().put(RenderingHints.KEY_INTERPOLATION, RenderingHints.VALUE_INTERPOLATION_BILINEAR); // InterpolationMode
 qualityOptions.getRenderingHints().put(RenderingHints.KEY_FRACTIONALMETRICS, RenderingHints.VALUE_FRACTIONALMETRICS_ON); // StringFormat

 ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.JPEG);
 saveOptions.setGraphicsQualityOptions(qualityOptions);

 doc.save(getArtifactsDir() + "ImageSaveOptions.GraphicsQuality.jpg", saveOptions);
 
```


[Save a Document]: https://docs.aspose.com/words/java/save-a-document/
## Methods

| Method | Description |
| --- | --- |
| [getRenderingHints()](#getRenderingHints) |  |
| [getUseTileFlipMode()](#getUseTileFlipMode) | Gets a flag indicating whether WrapMode is TileFlipXY. |
| [setRenderingHints(RenderingHints renderingHints)](#setRenderingHints-java.awt.RenderingHints) |  |
| [setUseTileFlipMode(boolean value)](#setUseTileFlipMode-boolean) | Sets a flag indicating whether WrapMode is TileFlipXY. |
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

 **Remarks:** 

The WrapMode specifies how a texture or gradient is tiled when it is smaller than the area being filled.

By default uses WrapMode\#TILE.TILE (specifies tiling without flipping). This causes inaccurate rendering of the scaled image(with high resolution).

This property allows to switch WrapMode to WrapMode\#TILE\_FLIP\_XY.TILE\_FLIP\_XY (specifies that tiles are flipped horizontally as you move along a row and flipped vertically as you move along a column).

 **Examples:** 

Shows how to prevent the white line appears when rendering with a high resolution.

```

 Document doc = new Document(getMyDir() + "Shape high dpi.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShapeRenderer renderer = shape.getShapeRenderer();

 ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.PNG);
 {
     saveOptions.setResolution(500f); saveOptions.setGraphicsQualityOptions(new GraphicsQualityOptions()); { saveOptions.getGraphicsQualityOptions().setUseTileFlipMode(true); }
 }
 renderer.save(getArtifactsDir() + "ImageSaveOptions.UseTileFlipMode.png", saveOptions);
 
```

**Returns:**
boolean - A flag indicating whether WrapMode is TileFlipXY.
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

 **Remarks:** 

The WrapMode specifies how a texture or gradient is tiled when it is smaller than the area being filled.

By default uses WrapMode\#TILE.TILE (specifies tiling without flipping). This causes inaccurate rendering of the scaled image(with high resolution).

This property allows to switch WrapMode to WrapMode\#TILE\_FLIP\_XY.TILE\_FLIP\_XY (specifies that tiles are flipped horizontally as you move along a row and flipped vertically as you move along a column).

 **Examples:** 

Shows how to prevent the white line appears when rendering with a high resolution.

```

 Document doc = new Document(getMyDir() + "Shape high dpi.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ShapeRenderer renderer = shape.getShapeRenderer();

 ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.PNG);
 {
     saveOptions.setResolution(500f); saveOptions.setGraphicsQualityOptions(new GraphicsQualityOptions()); { saveOptions.getGraphicsQualityOptions().setUseTileFlipMode(true); }
 }
 renderer.save(getArtifactsDir() + "ImageSaveOptions.UseTileFlipMode.png", saveOptions);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether WrapMode is TileFlipXY. |

