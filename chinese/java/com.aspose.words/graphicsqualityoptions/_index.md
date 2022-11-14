---
title: GraphicsQualityOptions
second_title: Aspose.Words for Java API 参考
description: 允许指定额外的 .
type: docs
weight: 313
url: /zh/java/com.aspose.words/graphicsqualityoptions/
---

**遗产:**
java.lang.Object
```
public class GraphicsQualityOptions
```

允许指定额外的 .

要了解更多信息，请访问**Save a Document**文档文章。

获取当前以查看或添加新提示。覆盖当前 .
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getRenderingHints()](#getRenderingHints--) |  |
| [getUseTileFlipMode()](#getUseTileFlipMode--) | 获取一个标志，该标志指示 WrapMode 是否为 TileFlipXY。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setRenderingHints(RenderingHints renderingHints)](#setRenderingHints-java.awt.RenderingHints-) |  |
| [setUseTileFlipMode(boolean value)](#setUseTileFlipMode-boolean-) | 设置一个标志，指示 WrapMode 是否为 TileFlipXY。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getRenderingHints() {#getRenderingHints--}
```
public RenderingHints getRenderingHints()
```




**退货:**
java.awt.RenderingHints
### getUseTileFlipMode() {#getUseTileFlipMode--}
```
public boolean getUseTileFlipMode()
```


获取一个标志，该标志指示 WrapMode 是否为 TileFlipXY。

WrapMode 指定当纹理或渐变小于要填充的区域时如何平铺。

默认使用 WrapMode\#TILE.TILE（指定不翻转的平铺）。这会导致缩放图像（具有高分辨率）的渲染不准确。

此属性允许将 WrapMode 切换为 WrapMode\＃瓦\_翻动\_XY.TILE\_翻动\_XY（指定平铺在您沿行移动时水平翻转，并在您沿列移动时垂直翻转）。

**退货:**
boolean - 指示 WrapMode 是否为 TileFlipXY 的标志。
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




### setRenderingHints(RenderingHints renderingHints) {#setRenderingHints-java.awt.RenderingHints-}
```
public void setRenderingHints(RenderingHints renderingHints)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| renderingHints | java.awt.RenderingHints |  |

### setUseTileFlipMode(boolean value) {#setUseTileFlipMode-boolean-}
```
public void setUseTileFlipMode(boolean value)
```


设置一个标志，指示 WrapMode 是否为 TileFlipXY。

WrapMode 指定当纹理或渐变小于要填充的区域时如何平铺。

默认使用 WrapMode\#TILE.TILE（指定不翻转的平铺）。这会导致缩放图像（具有高分辨率）的渲染不准确。

此属性允许将 WrapMode 切换为 WrapMode\＃瓦\_翻动\_XY.TILE\_翻动\_XY（指定平铺在您沿行移动时水平翻转，并在您沿列移动时垂直翻转）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 指示 WrapMode 是否为 TileFlipXY 的标志。 |

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
