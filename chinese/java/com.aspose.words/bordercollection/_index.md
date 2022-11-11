---
title: BorderCollection
second_title: Aspose.Words for Java API Reference
description: 边框对象的集合。
type: docs
weight: 37
url: /zh/java/com.aspose.words/bordercollection/
---

**遗产:**
java.lang.Object

**所有实现的接口:**
java.lang.Iterable
```
public class BorderCollection implements Iterable
```

边框对象的集合。

要了解更多信息，请访问**Programming with Documents**文档文章。

不同的文档元素有不同的边界。例如，ParagraphFormat 具有底部、左侧、右侧和顶部边框。您可以为每个边框单独指定不同的格式，或者枚举所有边框并应用相同的格式。
## 方法

| 方法 | 描述 |
| --- | --- |
| [clearFormatting()](#clearFormatting--) | 移除对象的所有边框。 |
| [equals(BorderCollection brColl)](#equals-com.aspose.words.BorderCollection-) | 比较边框的集合。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | 按索引检索 Border 对象。 |
| [getBottom()](#getBottom--) | 获取底部边框。 |
| [getByBorder类型(int border类型)](#getByBorder类型-int-) |  |
| [get班级()](#get班级--) |  |
| [getColor()](#getColor--) | 获取边框颜色。 |
| [getCount()](#getCount--) | 获取集合中的边框数。 |
| [getDistanceFromText()](#getDistanceFromText--) | 以点为单位获取边框与文本的距离。 |
| [getHorizontal()](#getHorizontal--) | 获取在单元格或符合段落之间使用的水平边框。 |
| [getLeft()](#getLeft--) | 获取左边框。 |
| [getLineStyle()](#getLineStyle--) | 获取边框样式。 |
| [getLineWidth()](#getLineWidth--) | 以磅为单位获取边框宽度。 |
| [getRight()](#getRight--) | 获取正确的边框。 |
| [getShadow()](#getShadow--) | 获取一个值，该值指示边框是否有阴影。 |
| [getTop()](#getTop--) | 获取上边框。 |
| [getVertical()](#getVertical--) | 获取单元格之间使用的垂直边框。 |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | 返回一个可用于遍历集合中所有边框的枚举器对象。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setColor(Color value)](#setColor-java.awt.Color-) | 设置边框颜色。 |
| [setDistanceFromText(double value)](#setDistanceFromText-double-) | 以点为单位设置边框与文本的距离。 |
| [setLineStyle(int value)](#setLineStyle-int-) | 设置边框样式。 |
| [setLineWidth(double value)](#setLineWidth-double-) | 以磅为单位设置边框宽度。 |
| [setShadow(boolean value)](#setShadow-boolean-) | 设置一个值，指示边框是否有阴影。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clearFormatting() {#clearFormatting--}
```
public void clearFormatting()
```


移除对象的所有边框。

### equals(BorderCollection brColl) {#equals-com.aspose.words.BorderCollection-}
```
public boolean equals(BorderCollection brColl)
```


比较边框的集合。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| brColl | [BorderCollection](../../com.aspose.words/bordercollection) |  |

**退货:**
布尔值
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
### get(int index) {#get-int-}
```
public Border get(int index)
```


按索引检索 Border 对象。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 要检索的边界的从零开始的索引。 |

**退货:**
[Border](../../com.aspose.words/border) - 相应的[Border](../../com.aspose.words/border)价值。
### getBottom() {#getBottom--}
```
public Border getBottom()
```


获取底部边框。

**退货:**
[Border](../../com.aspose.words/border) - 底部边框。
### getByBorder类型(int border类型) {#getByBorder类型-int-}
```
public Border getByBorder类型(int border类型)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| border类型 | int |  |

**退货:**
[Border](../../com.aspose.words/border)
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getColor() {#getColor--}
```
public Color getColor()
```


获取边框颜色。

返回集合中第一个边框的颜色。

设置集合中所有边框的颜色，不包括对角线边框。

**退货:**
java.awt.Color - 边框颜色。
### getCount() {#getCount--}
```
public int getCount()
```


获取集合中的边框数。

**退货:**
int - 集合中的边框数。
### getDistanceFromText() {#getDistanceFromText--}
```
public double getDistanceFromText()
```


以点为单位获取边框与文本的距离。

获取第一个边框与文本的距离。

为集合中的所有边框设置与文本的距离，不包括对角线边框。

没有效果，表格单元格的边框将自动重置为零。

**退货:**
double - 边框与文本的距离（以磅为单位）。
### getHorizontal() {#getHorizontal--}
```
public Border getHorizontal()
```


获取在单元格或符合段落之间使用的水平边框。

**退货:**
[Border](../../com.aspose.words/border) - 在单元格或符合段落之间使用的水平边框。
### getLeft() {#getLeft--}
```
public Border getLeft()
```


获取左边框。

**退货:**
[Border](../../com.aspose.words/border) - 左边框。
### getLineStyle() {#getLineStyle--}
```
public int getLineStyle()
```


获取边框样式。

返回集合中第一个边框的样式。

设置集合中所有边框的样式，不包括对角线边框。

**退货:**
 int - 边框样式。返回值是以下之一[LineStyle](../../com.aspose.words/linestyle)常数。
### getLineWidth() {#getLineWidth--}
```
public double getLineWidth()
```


以磅为单位获取边框宽度。

返回集合中第一个边框的宽度。

设置集合中所有边框的宽度，不包括对角线边框。

**退货:**
double - 以磅为单位的边框宽度。
### getRight() {#getRight--}
```
public Border getRight()
```


获取正确的边框。

**退货:**
[Border](../../com.aspose.words/border) - 右边框。
### getShadow() {#getShadow--}
```
public boolean getShadow()
```


获取一个值，该值指示边框是否有阴影。

从集合中的第一个边框获取值。

设置集合中所有边框的值，不包括对角线边框。

**退货:**
boolean - 指示边框是否有阴影的值。
### getTop() {#getTop--}
```
public Border getTop()
```


获取上边框。

**退货:**
[Border](../../com.aspose.words/border) - 顶部边框。
### getVertical() {#getVertical--}
```
public Border getVertical()
```


获取单元格之间使用的垂直边框。

**退货:**
[Border](../../com.aspose.words/border) - 单元格之间使用的垂直边框。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### iterator() {#iterator--}
```
public Iterator iterator()
```


返回一个可用于遍历集合中所有边框的枚举器对象。

**退货:**
java.util.Iterator
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setColor(Color value) {#setColor-java.awt.Color-}
```
public void setColor(Color value)
```


设置边框颜色。

返回集合中第一个边框的颜色。

设置集合中所有边框的颜色，不包括对角线边框。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.Color | 边框颜色。 |

### setDistanceFromText(double value) {#setDistanceFromText-double-}
```
public void setDistanceFromText(double value)
```


以点为单位设置边框与文本的距离。

获取第一个边框与文本的距离。

为集合中的所有边框设置与文本的距离，不包括对角线边框。

没有效果，表格单元格的边框将自动重置为零。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 边框与文本的距离（以磅为单位）。 |

### setLineStyle(int value) {#setLineStyle-int-}
```
public void setLineStyle(int value)
```


设置边框样式。

返回集合中第一个边框的样式。

设置集合中所有边框的样式，不包括对角线边框。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 边框样式。该值必须是以下之一[LineStyle](../../com.aspose.words/linestyle)常数。 |

### setLineWidth(double value) {#setLineWidth-double-}
```
public void setLineWidth(double value)
```


以磅为单位设置边框宽度。

返回集合中第一个边框的宽度。

设置集合中所有边框的宽度，不包括对角线边框。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 以磅为单位的边框宽度。 |

### setShadow(boolean value) {#setShadow-boolean-}
```
public void setShadow(boolean value)
```


设置一个值，指示边框是否有阴影。

从集合中的第一个边框获取值。

设置集合中所有边框的值，不包括对角线边框。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 指示边框是否有阴影的值。 |

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
