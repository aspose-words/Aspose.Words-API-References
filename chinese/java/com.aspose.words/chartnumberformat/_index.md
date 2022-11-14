---
title: ChartNumberFormat
second_title: Aspose.Words for Java API 参考
description: 表示父元素的数字格式。
type: docs
weight: 67
url: /zh/java/com.aspose.words/chartnumberformat/
---

**遗产:**
java.lang.Object
```
public class ChartNumberFormat
```

表示父元素的数字格式。

要了解更多信息，请访问**Working with Charts**文档文章。
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getFormatCode()](#getFormatCode--) | 获取应用于数据标签的格式代码。 |
| [hashCode()](#hashCode--) |  |
| [isLinkedToSource()](#isLinkedToSource--) | 指定格式代码是否链接到源单元格。 |
| [isLinkedToSource(boolean value)](#isLinkedToSource-boolean-) | 指定格式代码是否链接到源单元格。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setFormatCode(String value)](#setFormatCode-java.lang.String-) | 设置应用于数据标签的格式代码。 |
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
### getFormatCode() {#getFormatCode--}
```
public String getFormatCode()
```


获取应用于数据标签的格式代码。数字格式用于更改值在数据标签中的显示方式，并且可以以一些非常有创意的方式使用。数字格式示例：

数字 - ”\#,\#\#0.00"

货币 - ”\\"$\\"\#,\#\#0.00"

时间 - ”[$-x-systime]h:mm:ss AM/PM"

日期 - “d/mm/yyyy”

百分比 - “0.00%”

分数 - ”\＃？/？

科学 - “0.00E+00”

文本 - ”@”

会计-》\_-\\"$\\"\ *\#,\#\#0.00\_-;-\\"$\\"\ *\#,\#\#0.00\_-;\_-\\"$\\"\ *\\"-\\”？？\_-;\_-@\_-”

自定义颜色 - ”[红色的]-\#,\#\#0.0"

**退货:**
java.lang.String - 应用于数据标签的格式代码。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### isLinkedToSource() {#isLinkedToSource--}
```
public boolean isLinkedToSource()
```


指定格式代码是否链接到源单元格。默认为真。如果格式代码链接到源，NumberFormat 将被重置为一般。

**退货:**
boolean - 对应的布尔值。
### isLinkedToSource(boolean value) {#isLinkedToSource-boolean-}
```
public void isLinkedToSource(boolean value)
```


指定格式代码是否链接到源单元格。默认为真。如果格式代码链接到源，NumberFormat 将被重置为一般。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setFormatCode(String value) {#setFormatCode-java.lang.String-}
```
public void setFormatCode(String value)
```


设置应用于数据标签的格式代码。数字格式用于更改值在数据标签中的显示方式，并且可以以一些非常有创意的方式使用。数字格式示例：

数字 - ”\#,\#\#0.00"

货币 - ”\\"$\\"\#,\#\#0.00"

时间 - ”[$-x-systime]h:mm:ss AM/PM"

日期 - “d/mm/yyyy”

百分比 - “0.00%”

分数 - ”\＃？/？

科学 - “0.00E+00”

文本 - ”@”

会计-》\_-\\"$\\"\ *\#,\#\#0.00\_-;-\\"$\\"\ *\#,\#\#0.00\_-;\_-\\"$\\"\ *\\"-\\”？？\_-;\_-@\_-”

自定义颜色 - ”[红色的]-\#,\#\#0.0"

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 应用于数据标签的格式代码。 |

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
