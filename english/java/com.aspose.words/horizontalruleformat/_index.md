---
title: HorizontalRuleFormat
second_title: Aspose.Words for Java API 参考
description: 表示水平规则格式。
type: docs
weight: 322
url: /zh/java/com.aspose.words/horizontalruleformat/
---

**遗产:**
java.lang.Object
```
public class HorizontalRuleFormat
```

表示水平规则格式。

要了解更多信息，请访问**Working with Shapes**文档文章。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAlignment()](#getAlignment--) | 获取水平线的对齐方式。 |
| [get班级()](#get班级--) |  |
| [getColor()](#getColor--) | 获取填充水平线的画笔颜色。 |
| [getHeight()](#getHeight--) | 获取水平线的高度。 |
| [getNoShade()](#getNoShade--) | 表示存在水平线的 3D 阴影。 |
| [getWidthPercent()](#getWidthPercent--) | 获取以窗口宽度百分比表示的指定水平线的长度。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setAlignment(int value)](#setAlignment-int-) | 设置水平线的对齐方式。 |
| [setColor(Color value)](#setColor-java.awt.Color-) | 设置填充水平线的画笔颜色。 |
| [setHeight(double value)](#setHeight-double-) | 设置水平线的高度。 |
| [setNoShade(boolean value)](#setNoShade-boolean-) | 表示存在水平线的 3D 阴影。 |
| [setWidthPercent(double value)](#setWidthPercent-double-) | 设置指定水平线的长度，以窗口宽度的百分比表示。 |
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
### getAlignment() {#getAlignment--}
```
public int getAlignment()
```


获取水平线的对齐方式。

默认值为[HorizontalRuleAlignment.LEFT](../../com.aspose.words/horizontalrulealignment\#LEFT).

**退货:**
 int - 水平线的对齐方式。返回值是以下之一[HorizontalRuleAlignment](../../com.aspose.words/horizontalrulealignment)常数。
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


获取填充水平线的画笔颜色。

这是一个快捷方式[Fill.getColor()](../../com.aspose.words/fill\#getColor--) / [Fill.setColor(java.awt.Color)](../../com.aspose.words/fill\#setColor-java.awt.Color-)财产。

默认值为 。

**退货:**
java.awt.Color - 填充水平线的画笔颜色。
### getHeight() {#getHeight--}
```
public double getHeight()
```


获取水平线的高度。

这是一个快捷方式[ShapeBase.getHeight()](../../com.aspose.words/shapebase\#getHeight--) / [ShapeBase.setHeight(double)](../../com.aspose.words/shapebase\#setHeight-double-)财产。

有效值\\u200b\\u200brange 从 0 到 1584（含）。

默认值为 1.5。

**退货:**
double - 水平线的高度。
### getNoShade() {#getNoShade--}
```
public boolean getNoShade()
```


表示存在水平线的 3D 阴影。如果为 true，则水平规则不使用 3D 阴影并使用纯色。

默认值为假。

**退货:**
boolean - 对应的布尔值。
### getWidthPercent() {#getWidthPercent--}
```
public double getWidthPercent()
```


获取以窗口宽度百分比表示的指定水平线的长度。

有效值\\u200b\\u200b 范围从 1 到 100（含）。

默认值为 100。

**退货:**
double - 指定水平线的长度，以窗口宽度的百分比表示。
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




### setAlignment(int value) {#setAlignment-int-}
```
public void setAlignment(int value)
```


设置水平线的对齐方式。

默认值为[HorizontalRuleAlignment.LEFT](../../com.aspose.words/horizontalrulealignment\#LEFT).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 水平线的对齐方式。该值必须是以下之一[HorizontalRuleAlignment](../../com.aspose.words/horizontalrulealignment)常数。 |

### setColor(Color value) {#setColor-java.awt.Color-}
```
public void setColor(Color value)
```


设置填充水平线的画笔颜色。

这是一个快捷方式[Fill.getColor()](../../com.aspose.words/fill\#getColor--) / [Fill.setColor(java.awt.Color)](../../com.aspose.words/fill\#setColor-java.awt.Color-)财产。

默认值为 。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.awt.Color | 填充水平线的画笔颜色。 |

### setHeight(double value) {#setHeight-double-}
```
public void setHeight(double value)
```


设置水平线的高度。

这是一个快捷方式[ShapeBase.getHeight()](../../com.aspose.words/shapebase\#getHeight--) / [ShapeBase.setHeight(double)](../../com.aspose.words/shapebase\#setHeight-double-)财产。

有效值\\u200b\\u200brange 从 0 到 1584（含）。

默认值为 1.5。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 水平尺的高度。 |

### setNoShade(boolean value) {#setNoShade-boolean-}
```
public void setNoShade(boolean value)
```


表示存在水平线的 3D 阴影。如果为 true，则水平规则不使用 3D 阴影并使用纯色。

默认值为假。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setWidthPercent(double value) {#setWidthPercent-double-}
```
public void setWidthPercent(double value)
```


设置指定水平线的长度，以窗口宽度的百分比表示。

有效值\\u200b\\u200b 范围从 1 到 100（含）。

默认值为 100。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 以窗口宽度百分比表示的指定水平线的长度。 |

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
