---
title: Border
second_title: Aspose.Words for Java API 参考
description:表示对象的边框。
type: docs
weight: 36
url: /zh/java/com.aspose.words/border/
---

**遗产:**
java.lang.Object, [com.aspose.words.InternableComplexAttr](../../com.aspose.words/internablecomplexattr)

**All Implemented 界面s:**
java.lang.Cloneable
```
public class Border extends InternableComplexAttr implements Cloneable
```

表示对象的边框。

要了解更多信息，请访问**Programming with Documents**文档文章。

边框可以应用于各种文档元素，包括段落、段落内的文本行或表格单元格。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [clearFormatting()](#clearFormatting--) | 将边框属性重置为默认值。 |
| [equals(Border rhs)](#equals-com.aspose.words.Border-) | 确定指定边框的值是否与当前边框相等。 |
| [equals(Object obj)](#equals-java.lang.Object-) | 确定指定对象的值是否与当前对象相等。 |
| [get班级()](#get班级--) |  |
| [getColor()](#getColor--) | 获取边框颜色。 |
| [getDistanceFromText()](#getDistanceFromText--) | 获取边框与文本或页面边缘的距离（以磅为单位）。 |
| [getLineStyle()](#getLineStyle--) | 获取边框样式。 |
| [getLineWidth()](#getLineWidth--) | 以磅为单位获取边框宽度。 |
| [getShadow()](#getShadow--) | 获取一个值，该值指示边框是否有阴影。 |
| [hashCode()](#hashCode--) |  |
| [isInheritedComplexAttr()](#isInheritedComplexAttr--) |  |
| [isVisible()](#isVisible--) | 如果 LineStyle 不是 LineStyle.None，则返回 true。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setColor(Color value)](#setColor-java.awt.Color-) | 设置边框颜色。 |
| [setDistanceFromText(double value)](#setDistanceFromText-double-) | 以点为单位设置边框与文本或页面边缘的距离。 |
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


将边框属性重置为默认值。当边框属性重置为默认值时，边框是不可见的。

### equals(Border rhs) {#equals-com.aspose.words.Border-}
```
public boolean equals(Border rhs)
```


确定指定边框的值是否与当前边框相等。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| rhs | [Border](../../com.aspose.words/border) |  |

**退货:**
布尔值
### equals(Object obj) {#equals-java.lang.Object-}
```
public boolean equals(Object obj)
```


确定指定对象的值是否与当前对象相等。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| obj | java.lang.Object |  |

**退货:**
布尔值
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

**退货:**
java.awt.Color - 边框颜色。
### getDistanceFromText() {#getDistanceFromText--}
```
public double getDistanceFromText()
```


获取边框与文本或页面边缘的距离（以磅为单位）。没有效果，表格单元格的边框将自动重置为零。

**退货:**
double - 边框与文本或页面边缘的距离（以磅为单位）。
### getLineStyle() {#getLineStyle--}
```
public int getLineStyle()
```


获取边框样式。

如果将线型设置为无，则线宽会自动更改为零。

**退货:**
 int - 边框样式。返回值是以下之一[LineStyle](../../com.aspose.words/linestyle)常数。
### getLineWidth() {#getLineWidth--}
```
public double getLineWidth()
```


以磅为单位获取边框宽度。

线型为无时，如果设置线宽大于零，线型自动变为单线。

**退货:**
double - 以磅为单位的边框宽度。
### getShadow() {#getShadow--}
```
public boolean getShadow()
```


获取一个值，该值指示边框是否有阴影。

在 Microsoft Word 中，要使边框具有阴影，所有四个边（左、上、右和下）的边框都应具有相同的类型、宽度、颜色，并且都应将 Shadow 属性设置为 true。

**退货:**
boolean - 指示边框是否有阴影的值。
### hashCode() {#hashCode--}
```
public int hashCode()
```




**退货:**
整数
### isInheritedComplexAttr() {#isInheritedComplexAttr--}
```
public boolean isInheritedComplexAttr()
```




**退货:**
布尔值
### isVisible() {#isVisible--}
```
public boolean isVisible()
```


如果 LineStyle 不是 LineStyle.None，则返回 true。

**退货:**
boolean - 如果 LineStyle 不是 LineStyle.None，则为真。
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

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.Color | 边框颜色。 |

### setDistanceFromText(double value) {#setDistanceFromText-double-}
```
public void setDistanceFromText(double value)
```


以点为单位设置边框与文本或页面边缘的距离。没有效果，表格单元格的边框将自动重置为零。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 边框与文本或页面边缘的距离（以磅为单位）。 |

### setLineStyle(int value) {#setLineStyle-int-}
```
public void setLineStyle(int value)
```


设置边框样式。

如果将线型设置为无，则线宽会自动更改为零。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 边框样式。该值必须是以下之一[LineStyle](../../com.aspose.words/linestyle)常数。 |

### setLineWidth(double value) {#setLineWidth-double-}
```
public void setLineWidth(double value)
```


以磅为单位设置边框宽度。

线型为无时，如果设置线宽大于零，线型自动变为单线。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 以磅为单位的边框宽度。 |

### setShadow(boolean value) {#setShadow-boolean-}
```
public void setShadow(boolean value)
```


设置一个值，指示边框是否有阴影。

在 Microsoft Word 中，要使边框具有阴影，所有四个边（左、上、右和下）的边框都应具有相同的类型、宽度、颜色，并且都应将 Shadow 属性设置为 true。

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
