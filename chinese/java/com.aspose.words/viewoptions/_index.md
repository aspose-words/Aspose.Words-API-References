---
title: ViewOptions
second_title: Aspose.Words for Java API 参考
description: 提供各种选项来控制文档在 Microsoft Word 中的显示方式。
type: docs
weight: 601
url: /zh/java/com.aspose.words/viewoptions/
---

**遗产:**
java.lang.Object

**所有实现的接口:**
java.lang.Cloneable
```
public class ViewOptions implements Cloneable
```

提供各种选项来控制文档在 Microsoft Word 中的显示方式。

要了解更多信息，请访问**Work with Options and Appearance of Word Documents**文档文章。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getDisplayBackgroundShape()](#getDisplayBackgroundShape--) | 控制打印布局视图中背景形状的显示。 |
| [getDoNotDisplayPageBoundaries()](#getDoNotDisplayPageBoundaries--) | 关闭显示文本顶部和页面顶部边缘之间的空间。 |
| [getFormsDesign()](#getFormsDesign--) | 指定文档是否处于窗体设计模式。 |
| [getViewType()](#getViewType--) | 控制 Microsoft Word 中的查看模式。 |
| [getZoomPercent()](#getZoomPercent--) | 获取要查看文档的百分比（10 到 500 之间）。 |
| [getZoomType()](#getZoomType--) | 获取基于窗口大小的缩放值。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setDisplayBackgroundShape(boolean value)](#setDisplayBackgroundShape-boolean-) | 控制打印布局视图中背景形状的显示。 |
| [setDoNotDisplayPageBoundaries(boolean value)](#setDoNotDisplayPageBoundaries-boolean-) | 关闭显示文本顶部和页面顶部边缘之间的空间。 |
| [setFormsDesign(boolean value)](#setFormsDesign-boolean-) | 指定文档是否处于窗体设计模式。 |
| [setViewType(int value)](#setViewType-int-) | 控制 Microsoft Word 中的查看模式。 |
| [setZoomPercent(int value)](#setZoomPercent-int-) | 设置您要查看文档的百分比（10 到 500 之间）。 |
| [setZoomType(int value)](#setZoomType-int-) | 根据窗口大小设置缩放值。 |
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
### getDisplayBackgroundShape() {#getDisplayBackgroundShape--}
```
public boolean getDisplayBackgroundShape()
```


控制打印布局视图中背景形状的显示。

**退货:**
boolean - 对应的布尔值。
### getDoNotDisplayPageBoundaries() {#getDoNotDisplayPageBoundaries--}
```
public boolean getDoNotDisplayPageBoundaries()
```


关闭显示文本顶部和页面顶部边缘之间的空间。

**退货:**
boolean - 对应的布尔值。
### getFormsDesign() {#getFormsDesign--}
```
public boolean getFormsDesign()
```


指定文档是否处于窗体设计模式。

目前仅适用于 WordML 格式的文档。

**退货:**
boolean - 对应的布尔值。
### getViewType() {#getViewType--}
```
public int getViewType()
```


控制 Microsoft Word 中的查看模式。

虽然 Aspose.Words 能够读写这个选项，但它的用法是特定于应用程序的。例如 MS Word 2013 不遵守此选项的值。

**退货:**
int - 对应的 int 值。返回值是以下之一[ViewType](../../com.aspose.words/viewtype)常数。
### getZoomPercent() {#getZoomPercent--}
```
public int getZoomPercent()
```


获取要查看文档的百分比（10 到 500 之间）。

如果值为 0，则此属性使用 100，否则如果值小于 10 或大于 500，则此属性抛出。

虽然 Aspose.Words 能够读写这个选项，但它的用法是特定于应用程序的。例如 MS Word 2013 不遵守此选项的值。

**退货:**
int - 您希望查看文档的百分比（介于 10 和 500 之间）。
### getZoomType() {#getZoomType--}
```
public int getZoomType()
```


获取基于窗口大小的缩放值。

**退货:**
int - 基于窗口大小的缩放值。返回值是以下之一[ZoomType](../../com.aspose.words/zoomtype)常数。
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




### setDisplayBackgroundShape(boolean value) {#setDisplayBackgroundShape-boolean-}
```
public void setDisplayBackgroundShape(boolean value)
```


控制打印布局视图中背景形状的显示。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setDoNotDisplayPageBoundaries(boolean value) {#setDoNotDisplayPageBoundaries-boolean-}
```
public void setDoNotDisplayPageBoundaries(boolean value)
```


关闭显示文本顶部和页面顶部边缘之间的空间。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setFormsDesign(boolean value) {#setFormsDesign-boolean-}
```
public void setFormsDesign(boolean value)
```


指定文档是否处于窗体设计模式。

目前仅适用于 WordML 格式的文档。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setViewType(int value) {#setViewType-int-}
```
public void setViewType(int value)
```


控制 Microsoft Word 中的查看模式。

虽然 Aspose.Words 能够读写这个选项，但它的用法是特定于应用程序的。例如 MS Word 2013 不遵守此选项的值。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。该值必须是以下之一[ViewType](../../com.aspose.words/viewtype)常数。 |

### setZoomPercent(int value) {#setZoomPercent-int-}
```
public void setZoomPercent(int value)
```


设置您要查看文档的百分比（10 到 500 之间）。

如果值为 0，则此属性使用 100，否则如果值小于 10 或大于 500，则此属性抛出。

虽然 Aspose.Words 能够读写这个选项，但它的用法是特定于应用程序的。例如 MS Word 2013 不遵守此选项的值。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 您希望查看文档的百分比（10 到 500 之间）。 |

### setZoomType(int value) {#setZoomType-int-}
```
public void setZoomType(int value)
```


根据窗口大小设置缩放值。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 基于窗口大小的缩放值。该值必须是其中之一[ZoomType](../../com.aspose.words/zoomtype)常数。 |

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
