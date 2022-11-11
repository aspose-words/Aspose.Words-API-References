---
title: ShapeRenderer
second_title: Aspose.Words for Java API Reference
description: 提供渲染个人或光栅或矢量图像或图形对象的方法。
type: docs
weight: 520
url: /zh/java/com.aspose.words/shaperenderer/
---

**遗产:**
java.lang.Object, [com.aspose.words.NodeRendererBase](../../com.aspose.words/noderendererbase)
```
public class ShapeRenderer extends NodeRendererBase
```

提供渲染个体的方法[Shape](../../com.aspose.words/shape)或者[GroupShape](../../com.aspose.words/groupshape)到光栅或矢量图像或到图形对象。

要了解更多信息，请访问**Working with Shapes**文档文章。
## 构造函数s

| 构造函数 | 描述 |
| --- | --- |
| [ShapeRenderer(ShapeBase shape)](#ShapeRenderer-com.aspose.words.ShapeBase-) | 初始化此类的新实例。 |
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBoundsInPixels(float scale, float dpi)](#getBoundsInPixels-float-float-) | 计算指定缩放因子和分辨率的形状边界（以像素为单位）。 |
| [getBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)](#getBoundsInPixels-float-float-float-) | 计算指定缩放因子和分辨率的形状边界（以像素为单位）。 |
| [getBoundsInPoints()](#getBoundsInPoints--) | 以点为单位获取形状的实际边界。 |
| [get班级()](#get班级--) |  |
| [getOpaqueBoundsInPixels(float scale, float dpi)](#getOpaqueBoundsInPixels-float-float-) | 为指定的缩放因子和分辨率计算形状的不透明边界（以像素为单位）。 |
| [getOpaqueBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)](#getOpaqueBoundsInPixels-float-float-float-) | 为指定的缩放因子和分辨率计算形状的不透明边界（以像素为单位）。 |
| [getOpaqueBoundsInPoints()](#getOpaqueBoundsInPoints--) | 以点为单位获取形状的不透明边界。 |
| [getSizeInPixels(float scale, float dpi)](#getSizeInPixels-float-float-) | 计算指定缩放因子和分辨率的形状大小（以像素为单位）。 |
| [getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)](#getSizeInPixels-float-float-float-) | 计算指定缩放因子和分辨率的形状大小（以像素为单位）。 |
| [getSizeInPoints()](#getSizeInPoints--) | 获取形状的实际大小（以磅为单位）。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [renderToScale(Graphics2D graphics, float x, float y, float scale)](#renderToScale-java.awt.Graphics2D-float-float-float-) | 将形状渲染为 java.awt.Graphics2D 对象到指定的比例。 |
| [renderToSize(Graphics2D graphics, float x, float y, float width, float height)](#renderToSize-java.awt.Graphics2D-float-float-float-float-) | 将形状渲染为 java.awt.Graphics2D 对象到指定大小。 |
| [save(OutputStream stream, ImageSaveOptions saveOptions)](#save-java.io.OutputStream-com.aspose.words.ImageSaveOptions-) |  |
| [save(String fileName, ImageSaveOptions saveOptions)](#save-java.lang.String-com.aspose.words.ImageSaveOptions-) | 渲染形状并保存到图像中。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### ShapeRenderer(ShapeBase shape) {#ShapeRenderer-com.aspose.words.ShapeBase-}
```
public ShapeRenderer(ShapeBase shape)
```


初始化此类的新实例。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| shape | [ShapeBase](../../com.aspose.words/shapebase) | 您要呈现的 DrawinML 形状对象。 |

### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货:**
布尔值
### getBoundsInPixels(float scale, float dpi) {#getBoundsInPixels-float-float-}
```
public Rectangle getBoundsInPixels(float scale, float dpi)
```


计算指定缩放因子和分辨率的形状边界（以像素为单位）。

该方法转换[getBoundsInPoints()](../../com.aspose.words/noderendererbase\#getBoundsInPoints--)以像素为单位的矩形。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| scale | float | 缩放系数（1.0 为 100%）。 |
| dpi | float | 从点转换为像素（每英寸点数）的分辨率（水平和垂直）。 |

**退货:**
java.awt.Rectangle - 形状的实际（在页面上呈现的）边界框，以像素为单位。
### getBoundsInPixels(float scale, float horizontalDpi, float verticalDpi) {#getBoundsInPixels-float-float-float-}
```
public Rectangle getBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)
```


计算指定缩放因子和分辨率的形状边界（以像素为单位）。

该方法转换[getBoundsInPoints()](../../com.aspose.words/noderendererbase\#getBoundsInPoints--)以像素为单位的矩形。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| scale | float | 缩放系数（1.0 为 100%）。 |
| horizontalDpi | float | 从点转换为像素（每英寸点数）的水平分辨率。 |
| verticalDpi | float | 从点转换为像素（每英寸点数）的垂直分辨率。 |

**退货:**
java.awt.Rectangle - 形状的实际（在页面上呈现的）边界框，以像素为单位。
### getBoundsInPoints() {#getBoundsInPoints--}
```
public Rectangle2D.Float getBoundsInPoints()
```


以点为单位获取形状的实际边界。

此属性返回形状的实际（在页面上呈现的）边界框。边界考虑了形状旋转（如果有的话）。

**退货:**
java.awt.geom.Rectangle2D.Float - 以点为单位的形状的实际边界。
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getOpaqueBoundsInPixels(float scale, float dpi) {#getOpaqueBoundsInPixels-float-float-}
```
public Rectangle getOpaqueBoundsInPixels(float scale, float dpi)
```


为指定的缩放因子和分辨率计算形状的不透明边界（以像素为单位）。

该方法转换[getOpaqueBoundsInPoints()](../../com.aspose.words/noderendererbase\#getOpaqueBoundsInPoints--)以像素为单位的矩形，当您想要创建位图以仅使用形状的不透明部分来渲染形状时，它很有用。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| scale | float | 缩放系数（1.0 为 100%）。 |
| dpi | float | 从点转换为像素（每英寸点数）的分辨率。 |

**退货:**
java.awt.Rectangle - 形状的不透明矩形，以像素为单位。
### getOpaqueBoundsInPixels(float scale, float horizontalDpi, float verticalDpi) {#getOpaqueBoundsInPixels-float-float-float-}
```
public Rectangle getOpaqueBoundsInPixels(float scale, float horizontalDpi, float verticalDpi)
```


为指定的缩放因子和分辨率计算形状的不透明边界（以像素为单位）。

该方法转换[getOpaqueBoundsInPoints()](../../com.aspose.words/noderendererbase\#getOpaqueBoundsInPoints--)以像素为单位的矩形，当您想要创建位图以仅使用形状的不透明部分来渲染形状时，它很有用。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| scale | float | 缩放系数（1.0 为 100%）。 |
| horizontalDpi | float | 从点转换为像素（每英寸点数）的水平分辨率。 |
| verticalDpi | float | 从点转换为像素（每英寸点数）的垂直分辨率。 |

**退货:**
java.awt.Rectangle - 形状的不透明矩形，以像素为单位。
### getOpaqueBoundsInPoints() {#getOpaqueBoundsInPoints--}
```
public Rectangle2D.Float getOpaqueBoundsInPoints()
```


以点为单位获取形状的不透明边界。

此属性返回形状的不透明（即忽略形状的透明部分）边界框。边界考虑了形状旋转。

**退货:**
java.awt.geom.Rectangle2D.Float - 形状的不透明边界，以点为单位。
### getSizeInPixels(float scale, float dpi) {#getSizeInPixels-float-float-}
```
public Dimension getSizeInPixels(float scale, float dpi)
```


计算指定缩放因子和分辨率的形状大小（以像素为单位）。

该方法转换[getSizeInPoints()](../../com.aspose.words/noderendererbase\#getSizeInPoints--)以像素为单位的大小，当您想要创建位图以将形状整齐地渲染到位图上时，它很有用。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| scale | float | 缩放系数（1.0 为 100%）。 |
| dpi | float | 从点转换为像素（每英寸点数）的分辨率（水平和垂直）。 |

**退货:**
java.awt.Dimension - 形状的大小（以像素为单位）。
### getSizeInPixels(float scale, float horizontalDpi, float verticalDpi) {#getSizeInPixels-float-float-float-}
```
public Dimension getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)
```


计算指定缩放因子和分辨率的形状大小（以像素为单位）。

该方法转换[getSizeInPoints()](../../com.aspose.words/noderendererbase\#getSizeInPoints--)以像素为单位的大小，当您想要创建位图以将形状整齐地渲染到位图上时，它很有用。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| scale | float | 缩放系数（1.0 为 100%）。 |
| horizontalDpi | float | 从点转换为像素（每英寸点数）的水平分辨率。 |
| verticalDpi | float | 从点转换为像素（每英寸点数）的垂直分辨率。 |

**退货:**
java.awt.Dimension - 形状的大小（以像素为单位）。
### getSizeInPoints() {#getSizeInPoints--}
```
public Point2D.Float getSizeInPoints()
```


获取形状的实际大小（以磅为单位）。

此属性返回形状的实际（在页面上呈现）边界框的大小。大小考虑了形状旋转（如果有）。

**退货:**
java.awt.geom.Point2D.Float - 形状的实际大小（以磅为单位）。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### renderToScale(Graphics2D graphics, float x, float y, float scale) {#renderToScale-java.awt.Graphics2D-float-float-float-}
```
public Point2D.Float renderToScale(Graphics2D graphics, float x, float y, float scale)
```


将形状渲染为 java.awt.Graphics2D 对象到指定的比例。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| graphics | java.awt.Graphics2D | 渲染到的对象。 |
| x | float | 渲染形状左上角的 X 坐标（以世界单位为单位）。 |
| y | float | 渲染形状左上角的 Y 坐标（以世界单位为单位）。 |
| scale | float | 渲染形状的比例（1.0 为 100%）。 |

**退货:**
java.awt.geom.Point2D.Float - 渲染形状的宽度和高度（以世界单位为单位）。
### renderToSize(Graphics2D graphics, float x, float y, float width, float height) {#renderToSize-java.awt.Graphics2D-float-float-float-float-}
```
public float renderToSize(Graphics2D graphics, float x, float y, float width, float height)
```


将形状渲染为 java.awt.Graphics2D 对象到指定大小。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| graphics | java.awt.Graphics2D | 渲染到的对象。 |
| x | float | 渲染形状左上角的 X 坐标（以世界单位为单位）。 |
| y | float | 渲染形状左上角的 Y 坐标（以世界单位为单位）。 |
| width | float | 渲染形状可以占据的最大宽度（以世界单位为单位）。 |
| height | float | 渲染形状可以占据的最大高度（以世界单位为单位）。 |

**退货:**
float - 为渲染形状自动计算的比例以适合指定大小。
### save(OutputStream stream, ImageSaveOptions saveOptions) {#save-java.io.OutputStream-com.aspose.words.ImageSaveOptions-}
```
public void save(OutputStream stream, ImageSaveOptions saveOptions)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| stream | java.io.OutputStream |  |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions) |  |

### save(String fileName, ImageSaveOptions saveOptions) {#save-java.lang.String-com.aspose.words.ImageSaveOptions-}
```
public void save(String fileName, ImageSaveOptions saveOptions)
```


渲染形状并保存到图像中。将形状渲染为图像并保存到文件中。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fileName | java.lang.String | 图像文件的名称。如果具有指定名称的文件已存在，则覆盖现有文件。 |
| saveOptions | [ImageSaveOptions](../../com.aspose.words/imagesaveoptions) | 指定控制如何渲染和保存形状的选项。可以为空。 |

### toString() {#toString--}
```
public String toString()
```




**退货:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
