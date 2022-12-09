---
title: NodeRendererBase
second_title: Aspose.Words for Java API Reference
description: Base class for  and .
type: docs
weight: 410
url: /java/com.aspose.words/noderendererbase/
---

**Inheritance:**
java.lang.Object
```
public abstract class NodeRendererBase
```

Base class for [ShapeRenderer](../../com.aspose.words/shaperenderer) and [OfficeMathRenderer](../../com.aspose.words/officemathrenderer).

To learn more, visit the [ Working with Shapes ][Working with Shapes] documentation article.


[Working with Shapes]: https://docs.aspose.com/words/java/working-with-shapes/
## Constructors

| Constructor | Description |
| --- | --- |
| [NodeRendererBase()](#NodeRendererBase) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getBoundsInPixels(float scale, float dpi)](#getBoundsInPixels-float-float) | Calculates the bounds of the shape in pixels for a specified zoom factor and resolution. |
| [getBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)](#getBoundsInPixels-float-float-float) | Calculates the bounds of the shape in pixels for a specified zoom factor and resolution. |
| [getBoundsInPoints()](#getBoundsInPoints) | Gets the actual bounds of the shape in points. |
| [getClass()](#getClass) |  |
| [getOpaqueBoundsInPixels(float scale, float dpi)](#getOpaqueBoundsInPixels-float-float) | Calculates the opaque bounds of the shape in pixels for a specified zoom factor and resolution. |
| [getOpaqueBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)](#getOpaqueBoundsInPixels-float-float-float) | Calculates the opaque bounds of the shape in pixels for a specified zoom factor and resolution. |
| [getOpaqueBoundsInPoints()](#getOpaqueBoundsInPoints) | Gets the opaque bounds of the shape in points. |
| [getSizeInPixels(float scale, float dpi)](#getSizeInPixels-float-float) | Calculates the size of the shape in pixels for a specified zoom factor and resolution. |
| [getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)](#getSizeInPixels-float-float-float) | Calculates the size of the shape in pixels for a specified zoom factor and resolution. |
| [getSizeInPoints()](#getSizeInPoints) | Gets the actual size of the shape in points. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [renderToScale(Graphics2D graphics, float x, float y, float scale)](#renderToScale-java.awt.Graphics2D-float-float-float) | Renders the shape into a java.awt.Graphics2D object to a specified scale. |
| [renderToSize(Graphics2D graphics, float x, float y, float width, float height)](#renderToSize-java.awt.Graphics2D-float-float-float-float) | Renders the shape into a java.awt.Graphics2D object to a specified size. |
| [save(OutputStream stream, ImageSaveOptions saveOptions)](#save-java.io.OutputStream-com.aspose.words.ImageSaveOptions) |  |
| [save(String fileName, ImageSaveOptions saveOptions)](#save-java.lang.String-com.aspose.words.ImageSaveOptions) | Renders the shape and saves into an image. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### NodeRendererBase() {#NodeRendererBase}
```
public NodeRendererBase()
```


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
### getBoundsInPixels(float scale, float dpi) {#getBoundsInPixels-float-float}
```
public Rectangle getBoundsInPixels(float scale, float dpi)
```


Calculates the bounds of the shape in pixels for a specified zoom factor and resolution.

This method converts [getBoundsInPoints()](../../com.aspose.words/noderendererbase\#getBoundsInPoints) into rectangle in pixels.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| scale | float | The zoom factor (1.0 is 100%). |
| dpi | float | The resolution (horizontal and vertical) to convert from points to pixels (dots per inch). |

**Returns:**
java.awt.Rectangle - The actual (as rendered on the page) bounding box of the shape in pixels.
### getBoundsInPixels(float scale, float horizontalDpi, float verticalDpi) {#getBoundsInPixels-float-float-float}
```
public Rectangle getBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)
```


Calculates the bounds of the shape in pixels for a specified zoom factor and resolution.

This method converts [getBoundsInPoints()](../../com.aspose.words/noderendererbase\#getBoundsInPoints) into rectangle in pixels.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| scale | float | The zoom factor (1.0 is 100%). |
| horizontalDpi | float | The horizontal resolution to convert from points to pixels (dots per inch). |
| verticalDpi | float | The vertical resolution to convert from points to pixels (dots per inch). |

**Returns:**
java.awt.Rectangle - The actual (as rendered on the page) bounding box of the shape in pixels.
### getBoundsInPoints() {#getBoundsInPoints}
```
public Rectangle2D.Float getBoundsInPoints()
```


Gets the actual bounds of the shape in points.

This property returns the actual (as rendered on the page) bounding box of the shape. The bounds takes into account shape rotation (if any).

**Returns:**
java.awt.geom.Rectangle2D.Float - The actual bounds of the shape in points.
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getOpaqueBoundsInPixels(float scale, float dpi) {#getOpaqueBoundsInPixels-float-float}
```
public Rectangle getOpaqueBoundsInPixels(float scale, float dpi)
```


Calculates the opaque bounds of the shape in pixels for a specified zoom factor and resolution.

This method converts [getOpaqueBoundsInPoints()](../../com.aspose.words/noderendererbase\#getOpaqueBoundsInPoints) into rectangle in pixels and it is useful when you want to create a bitmap for rendering the shape with only opaque part of the shape.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| scale | float | The zoom factor (1.0 is 100%). |
| dpi | float | The resolution to convert from points to pixels (dots per inch). |

**Returns:**
java.awt.Rectangle - The opaque rectangle of the shape in pixels.
### getOpaqueBoundsInPixels(float scale, float horizontalDpi, float verticalDpi) {#getOpaqueBoundsInPixels-float-float-float}
```
public Rectangle getOpaqueBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)
```


Calculates the opaque bounds of the shape in pixels for a specified zoom factor and resolution.

This method converts [getOpaqueBoundsInPoints()](../../com.aspose.words/noderendererbase\#getOpaqueBoundsInPoints) into rectangle in pixels and it is useful when you want to create a bitmap for rendering the shape with only opaque part of the shape.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| scale | float | The zoom factor (1.0 is 100%). |
| horizontalDpi | float | The horizontal resolution to convert from points to pixels (dots per inch). |
| verticalDpi | float | The vertical resolution to convert from points to pixels (dots per inch). |

**Returns:**
java.awt.Rectangle - The opaque rectangle of the shape in pixels.
### getOpaqueBoundsInPoints() {#getOpaqueBoundsInPoints}
```
public Rectangle2D.Float getOpaqueBoundsInPoints()
```


Gets the opaque bounds of the shape in points.

This property returns the opaque (i.e. transparent parts of the shape are ignored) bounding box of the shape. The bounds takes the shape rotation into account.

**Returns:**
java.awt.geom.Rectangle2D.Float - The opaque bounds of the shape in points.
### getSizeInPixels(float scale, float dpi) {#getSizeInPixels-float-float}
```
public Dimension getSizeInPixels(float scale, float dpi)
```


Calculates the size of the shape in pixels for a specified zoom factor and resolution.

This method converts [getSizeInPoints()](../../com.aspose.words/noderendererbase\#getSizeInPoints) into size in pixels and it is useful when you want to create a bitmap for rendering the shape neatly onto the bitmap.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| scale | float | The zoom factor (1.0 is 100%). |
| dpi | float | The resolution (horizontal and vertical) to convert from points to pixels (dots per inch). |

**Returns:**
java.awt.Dimension - The size of the shape in pixels.
### getSizeInPixels(float scale, float horizontalDpi, float verticalDpi) {#getSizeInPixels-float-float-float}
```
public Dimension getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)
```


Calculates the size of the shape in pixels for a specified zoom factor and resolution.

This method converts [getSizeInPoints()](../../com.aspose.words/noderendererbase\#getSizeInPoints) into size in pixels and it is useful when you want to create a bitmap for rendering the shape neatly onto the bitmap.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| scale | float | The zoom factor (1.0 is 100%). |
| horizontalDpi | float | The horizontal resolution to convert from points to pixels (dots per inch). |
| verticalDpi | float | The vertical resolution to convert from points to pixels (dots per inch). |

**Returns:**
java.awt.Dimension - The size of the shape in pixels.
### getSizeInPoints() {#getSizeInPoints}
```
public Point2D.Float getSizeInPoints()
```


Gets the actual size of the shape in points.

This property returns the size of the actual (as rendered on the page) bounding box of the shape. The size takes into account shape rotation (if any).

**Returns:**
java.awt.geom.Point2D.Float - The actual size of the shape in points.
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




### renderToScale(Graphics2D graphics, float x, float y, float scale) {#renderToScale-java.awt.Graphics2D-float-float-float}
```
public Point2D.Float renderToScale(Graphics2D graphics, float x, float y, float scale)
```


Renders the shape into a java.awt.Graphics2D object to a specified scale.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| graphics | java.awt.Graphics2D | The object where to render to. |
| x | float | The X coordinate (in world units) of the top left corner of the rendered shape. |
| y | float | The Y coordinate (in world units) of the top left corner of the rendered shape. |
| scale | float | The scale for rendering the shape (1.0 is 100%). |

**Returns:**
java.awt.geom.Point2D.Float - The width and height (in world units) of the rendered shape.
### renderToSize(Graphics2D graphics, float x, float y, float width, float height) {#renderToSize-java.awt.Graphics2D-float-float-float-float}
```
public float renderToSize(Graphics2D graphics, float x, float y, float width, float height)
```


Renders the shape into a java.awt.Graphics2D object to a specified size.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| graphics | java.awt.Graphics2D | The object where to render to. |
| x | float | The X coordinate (in world units) of the top left corner of the rendered shape. |
| y | float | The Y coordinate (in world units) of the top left corner of the rendered shape. |
| width | float | The maximum width (in world units) that can be occupied by the rendered shape. |
| height | float | The maximum height (in world units) that can be occupied by the rendered shape. |

**Returns:**
float - The scale that was automatically calculated for the rendered shape to fit the specified size.
### save(OutputStream stream, ImageSaveOptions saveOptions) {#save-java.io.OutputStream-com.aspose.words.ImageSaveOptions}
```
public void save(OutputStream stream, ImageSaveOptions saveOptions)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| stream | java.io.OutputStream |  |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions) |  |

### save(String fileName, ImageSaveOptions saveOptions) {#save-java.lang.String-com.aspose.words.ImageSaveOptions}
```
public void save(String fileName, ImageSaveOptions saveOptions)
```


Renders the shape and saves into an image.  Renders the shape into an image and saves into a file.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | The name for the image file. If a file with the specified name already exists, the existing file is overwritten. |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions) | Specifies the options that control how the shape is rendered and saved. Can be  null . |

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

