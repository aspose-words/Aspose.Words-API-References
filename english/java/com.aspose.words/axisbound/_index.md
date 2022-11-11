---
title: AxisBound
second_title: Aspose.Words for Java API 参考
description: 表示轴值的最小或最大界限。
type: docs
weight: 16
url: /zh/java/com.aspose.words/axisbound/
---

**遗产:**
java.lang.Object
```
public class AxisBound
```

表示轴值的最小或最大界限。

要了解更多信息，请访问**Working with Charts**文档文章。

Bound 可以指定为数字、日期时间或特殊的“自动”值。

这个类的实例是不可变的。
## 构造函数s

| 构造函数 | 描述 |
| --- | --- |
| [AxisBound()](#AxisBound--) | 创建一个新实例，指示轴边界应由文字处理应用程序自动确定。 |
| [AxisBound(double value)](#AxisBound-double-) | 创建一个以数字表示的轴边界。 |
| [AxisBound(Date datetime)](#AxisBound-java.util.Date-) | 创建表示为日期时间值的轴边界。 |
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object-) | 确定指定对象的值是否与当前对象相等。 |
| [get班级()](#get班级--) |  |
| [getValue()](#getValue--) | 返回轴边界的数值。 |
| [getValueAsDate()](#getValueAsDate--) | 返回表示为日期时间的轴边界值。 |
| [hashCode()](#hashCode--) |  |
| [isAuto()](#isAuto--) | 返回一个标志，指示应自动确定轴边界。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) | 返回显示此对象值的用户友好字符串。 |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### AxisBound() {#AxisBound--}
```
public AxisBound()
```


创建一个新实例，指示轴边界应由文字处理应用程序自动确定。

### AxisBound(double value) {#AxisBound-double-}
```
public AxisBound(double value)
```


创建一个以数字表示的轴边界。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | double |  |

### AxisBound(Date datetime) {#AxisBound-java.util.Date-}
```
public AxisBound(Date datetime)
```


创建表示为日期时间值的轴边界。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| datetime | java.util.Date |  |

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
### getValue() {#getValue--}
```
public double getValue()
```


返回轴边界的数值。

**退货:**
double - 轴边界的数值。
### getValueAsDate() {#getValueAsDate--}
```
public Date getValueAsDate()
```


返回表示为日期时间的轴边界值。

**退货:**
java.util.Date - 表示为日期时间的轴边界值。
### hashCode() {#hashCode--}
```
public int hashCode()
```




**退货:**
整数
### isAuto() {#isAuto--}
```
public boolean isAuto()
```


返回一个标志，指示应自动确定轴边界。

**退货:**
boolean - 一个标志，表示应该自动确定轴边界。
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


返回显示此对象值的用户友好字符串。

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
