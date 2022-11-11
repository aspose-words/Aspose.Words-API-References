---
title: PreferredWidth
second_title: Aspose.Words for Java API Reference
description: 表示一个值及其度量单位，用于指定表格或单元格的首选宽度。
type: docs
weight: 466
url: /zh/java/com.aspose.words/preferredwidth/
---

**遗产:**
java.lang.Object
```
public class PreferredWidth
```

表示一个值及其度量单位，用于指定表格或单元格的首选宽度。

要了解更多信息，请访问**Working with Tables**文档文章。

首选宽度可以指定为百分比、点数或特殊的“无/自动”值。

这个类的实例是不可变的。
## 字段

| 字段 | 描述 |
| --- | --- |
| [AUTO](#AUTO) | 返回一个表示“未指定首选宽度”值的实例。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(PreferredWidth other)](#equals-com.aspose.words.PreferredWidth-) | 确定指定的 PreferredWidth 值是否等于当前 PreferredWidth。 |
| [equals(Object obj)](#equals-java.lang.Object-) | 确定指定对象的值是否与当前对象相等。 |
| [fromPercent(double percent)](#fromPercent-double-) | 一种创建方法，它返回一个新实例，该实例表示以百分比指定的首选宽度。 |
| [fromPoints(double points)](#fromPoints-double-) | 一种创建方法，它返回一个新实例，该实例表示使用多个点指定的首选宽度。 |
| [get班级()](#get班级--) |  |
| [get类型()](#get类型--) | 获取用于此首选宽度值的度量单位。 |
| [getValue()](#getValue--) | 获取首选宽度值。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) | 返回显示此对象值的用户友好字符串。 |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### AUTO {#AUTO}
```
public static PreferredWidth AUTO
```


返回一个表示“未指定首选宽度”值的实例。

### equals(PreferredWidth other) {#equals-com.aspose.words.PreferredWidth-}
```
public boolean equals(PreferredWidth other)
```


确定指定的 PreferredWidth 值是否等于当前 PreferredWidth。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| other | [PreferredWidth](../../com.aspose.words/preferredwidth) |  |

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
### fromPercent(double percent) {#fromPercent-double-}
```
public static PreferredWidth fromPercent(double percent)
```


一种创建方法，它返回一个新实例，该实例表示以百分比指定的首选宽度。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| percent | double | 该值必须介于 0 到 100 之间。 |

**退货:**
[PreferredWidth](../../com.aspose.words/preferredwidth)
### fromPoints(double points) {#fromPoints-double-}
```
public static PreferredWidth fromPoints(double points)
```


一种创建方法，它返回一个新实例，该实例表示使用多个点指定的首选宽度。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| points | double | 该值必须介于 0 到 22 英寸（22\* 72 分）。 |

**退货:**
[PreferredWidth](../../com.aspose.words/preferredwidth)
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### get类型() {#get类型--}
```
public int get类型()
```


获取用于此首选宽度值的度量单位。

**退货:**
 int - 用于此首选宽度值的度量单位。返回值是以下之一[PreferredWidth类型](../../com.aspose.words/preferredwidthtype)常数。
### getValue() {#getValue--}
```
public double getValue()
```


获取首选宽度值。计量单位在[get类型()](../../com.aspose.words/preferredwidth\#get类型--)财产。

**退货:**
double - 首选宽度值。
### hashCode() {#hashCode--}
```
public int hashCode()
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
