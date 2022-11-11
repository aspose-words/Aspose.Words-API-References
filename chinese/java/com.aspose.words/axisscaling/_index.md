---
title: AxisScaling
second_title: Aspose.Words for Java API Reference
description: 表示轴的缩放选项。
type: docs
weight: 22
url: /zh/java/com.aspose.words/axisscaling/
---

**遗产:**
java.lang.Object

**所有实现的接口:**
java.lang.Cloneable
```
public class AxisScaling implements Cloneable
```

表示轴的缩放选项。

要了解更多信息，请访问**Working with Charts**文档文章。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get班级()](#get班级--) |  |
| [getLogBase()](#getLogBase--) | 获取对数轴的对数底。 |
| [getMaximum()](#getMaximum--) | 获取轴的最大值。 |
| [getMinimum()](#getMinimum--) | 获取轴的最小值。 |
| [get类型()](#get类型--) | 获取轴的缩放类型。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setLogBase(double value)](#setLogBase-double-) | 设置对数轴的对数底。 |
| [setMaximum(AxisBound value)](#setMaximum-com.aspose.words.AxisBound-) | 设置轴的最大值。 |
| [setMinimum(AxisBound value)](#setMinimum-com.aspose.words.AxisBound-) | 设置轴的最小值。 |
| [set类型(int value)](#set类型-int-) | 设置轴的缩放类型。 |
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
### getLogBase() {#getLogBase--}
```
public double getLogBase()
```


获取对数轴的对数底。

MS Office 2016 新图表不支持该属性。

浮点值的有效范围大于等于 2 小于等于 1000。该属性只有在[get类型()](../../com.aspose.words/axisscaling\#get类型--) / [set类型(int)](../../com.aspose.words/axisscaling\#set类型-int-)被设定为[AxisScale类型.LOGARITHMIC](../../com.aspose.words/axisscaletype\#LOGARITHMIC).

设置此属性会设置[get类型()](../../com.aspose.words/axisscaling\#get类型--) / [set类型(int)](../../com.aspose.words/axisscaling\#set类型-int-)财产[AxisScale类型.LOGARITHMIC](../../com.aspose.words/axisscaletype\#LOGARITHMIC).

**退货:**
double - 对数轴的对数底。
### getMaximum() {#getMaximum--}
```
public AxisBound getMaximum()
```


获取轴的最大值。默认值为“自动”。

**退货:**
[AxisBound](../../com.aspose.words/axisbound) - 轴的最大值。
### getMinimum() {#getMinimum--}
```
public AxisBound getMinimum()
```


获取轴的最小值。默认值为“自动”。

**退货:**
[AxisBound](../../com.aspose.words/axisbound) - 轴的最小值。
### get类型() {#get类型--}
```
public int get类型()
```


获取轴的缩放类型。这[AxisScale类型.LINEAR](../../com.aspose.words/axisscaletype\#LINEAR)value 是 MS Office 2016 新图表中唯一允许的值。

**退货:**
int - 轴的缩放类型。返回值是以下之一[AxisScale类型](../../com.aspose.words/axisscaletype)常数。
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




### setLogBase(double value) {#setLogBase-double-}
```
public void setLogBase(double value)
```


设置对数轴的对数底。

MS Office 2016 新图表不支持该属性。

浮点值的有效范围大于等于 2 小于等于 1000。该属性只有在[get类型()](../../com.aspose.words/axisscaling\#get类型--) / [set类型(int)](../../com.aspose.words/axisscaling\#set类型-int-)被设定为[AxisScale类型.LOGARITHMIC](../../com.aspose.words/axisscaletype\#LOGARITHMIC).

设置此属性会设置[get类型()](../../com.aspose.words/axisscaling\#get类型--) / [set类型(int)](../../com.aspose.words/axisscaling\#set类型-int-)财产[AxisScale类型.LOGARITHMIC](../../com.aspose.words/axisscaletype\#LOGARITHMIC).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double | 对数轴的对数底。 |

### setMaximum(AxisBound value) {#setMaximum-com.aspose.words.AxisBound-}
```
public void setMaximum(AxisBound value)
```


设置轴的最大值。默认值为“自动”。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [AxisBound](../../com.aspose.words/axisbound) | 轴的最大值。 |

### setMinimum(AxisBound value) {#setMinimum-com.aspose.words.AxisBound-}
```
public void setMinimum(AxisBound value)
```


设置轴的最小值。默认值为“自动”。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [AxisBound](../../com.aspose.words/axisbound) | 轴的最小值。 |

### set类型(int value) {#set类型-int-}
```
public void set类型(int value)
```


设置轴的缩放类型。这[AxisScale类型.LINEAR](../../com.aspose.words/axisscaletype\#LINEAR)value 是 MS Office 2016 新图表中唯一允许的值。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 轴的缩放类型。该值必须是以下之一[AxisScale类型](../../com.aspose.words/axisscaletype)常数。 |

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
