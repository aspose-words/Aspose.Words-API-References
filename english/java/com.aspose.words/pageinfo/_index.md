---
title: PageInfo
second_title: Aspose.Words for Java API 参考
description: 表示有关特定文档页面的信息。
type: docs
weight: 434
url: /zh/java/com.aspose.words/pageinfo/
---

**遗产:**
java.lang.Object
```
public class PageInfo
```

表示有关特定文档页面的信息。

要了解更多信息，请访问**Rendering**文档文章。

此对象返回的页面宽度和高度表示页面的“最终”大小，例如它们已经旋转到正确的方向。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get班级()](#get班级--) |  |
| [getHeightInPoints()](#getHeightInPoints--) | 获取页面的高度（以磅为单位）。 |
| [getLandscape()](#getLandscape--) | 如果在文档中为此页面指定的页面方向为横向，则返回 true。 |
| [getPaperSize()](#getPaperSize--) | 获取纸张大小作为枚举。 |
| [getPaperTray()](#getPaperTray--) | 获取文档中指定的此页面的纸盒（纸盒）。 |
| [getSizeInPixels(float scale, float dpi)](#getSizeInPixels-float-float-) | 计算指定缩放因子和分辨率的页面大小（以像素为单位）。 |
| [getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)](#getSizeInPixels-float-float-float-) | 计算指定缩放因子和分辨率的页面大小（以像素为单位）。 |
| [getSizeInPoints()](#getSizeInPoints--) | 以磅为单位获取页面大小。 |
| [getWidthInPoints()](#getWidthInPoints--) | 获取页面的宽度（以磅为单位）。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
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
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getHeightInPoints() {#getHeightInPoints--}
```
public float getHeightInPoints()
```


获取页面的高度（以磅为单位）。

**退货:**
float - 以磅为单位的页面高度。
### getLandscape() {#getLandscape--}
```
public boolean getLandscape()
```


如果在文档中为此页面指定的页面方向为横向，则返回 true。

**退货:**
boolean - 如果在文档中为此页面指定的页面方向为横向，则为真。
### getPaperSize() {#getPaperSize--}
```
public int getPaperSize()
```


获取纸张大小作为枚举。

**退货:**
 int - 作为枚举的纸张大小。返回值是以下之一[PaperSize](../../com.aspose.words/papersize)常数。
### getPaperTray() {#getPaperTray--}
```
public int getPaperTray()
```


获取文档中指定的此页面的纸盒（纸盒）。该值是特定于实现（打印机）的。

**退货:**
int - 文档中指定的此页面的纸盒（纸盒）。
### getSizeInPixels(float scale, float dpi) {#getSizeInPixels-float-float-}
```
public Dimension getSizeInPixels(float scale, float dpi)
```


计算指定缩放因子和分辨率的页面大小（以像素为单位）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| scale | float | 缩放系数（1.0 为 100%）。 |
| dpi | float | 从点转换为像素（每英寸点数）的分辨率（水平和垂直）。 |

**退货:**
java.awt.Dimension - 页面大小（以像素为单位）。
### getSizeInPixels(float scale, float horizontalDpi, float verticalDpi) {#getSizeInPixels-float-float-float-}
```
public Dimension getSizeInPixels(float scale, float horizontalDpi, float verticalDpi)
```


计算指定缩放因子和分辨率的页面大小（以像素为单位）。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| scale | float | 缩放系数（1.0 为 100%）。 |
| horizontalDpi | float | 从点转换为像素（每英寸点数）的水平分辨率。 |
| verticalDpi | float | 从点转换为像素（每英寸点数）的垂直分辨率。 |

**退货:**
java.awt.Dimension - 页面大小（以像素为单位）。
### getSizeInPoints() {#getSizeInPoints--}
```
public Point2D.Float getSizeInPoints()
```


以磅为单位获取页面大小。

**退货:**
java.awt.geom.Point2D.Float - 以磅为单位的页面大小。
### getWidthInPoints() {#getWidthInPoints--}
```
public float getWidthInPoints()
```


获取页面的宽度（以磅为单位）。

**退货:**
float - 以磅为单位的页面宽度。
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
