---
title: TabStop
second_title: Aspose.Words for Java API 参考
description: 表示单个自定义制表位。
type: docs
weight: 546
url: /zh/java/com.aspose.words/tabstop/
---

**遗产：**
java.lang.Object

**所有已实现的接口：**
java.lang.Cloneable
```
public class TabStop implements Cloneable
```

表示单个自定义制表位。这**TabStop**对象是[TabStopCollection](../../com.aspose.words/tabstopcollection)收藏。

要了解更多信息，请访问**Aspose.Words Document Object Model (DOM)**文档文章。

通常，制表位指定制表位存在的位置。但是因为制表位可以从父样式继承，所以子对象可能需要明确定义在给定位置没有制表位。要清除给定位置的继承制表位，请创建一个**TabStop**对象和集合[getAlignment()](../../com.aspose.words/tabstop\#getAlignment--) / [setAlignment(int)](../../com.aspose.words/tabstop\#setAlignment-int-)到 TabAlignment.Clear 。

有关详细信息，请参阅[TabStopCollection](../../com.aspose.words/tabstopcollection).
## 构造器

| 构造函数 | 描述 |
| --- | --- |
| [TabStop(double position)](#TabStop-double-) | 初始化此类的新实例。 |
| [TabStop(double position, int alignment, int leader)](#TabStop-double-int-int-) | 初始化此类的新实例。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(TabStop rhs)](#equals-com.aspose.words.TabStop-) | 与指定的 TabStop 进行比较。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAlignment()](#getAlignment--) | 获取此制表位处的文本对齐方式。 |
| [getClass()](#getClass--) |  |
| [getLeader()](#getLeader--) | 获取制表符下显示的引导线类型。 |
| [getPosition()](#getPosition--) | 获取制表位的位置（以磅为单位）。 |
| [hashCode()](#hashCode--) |  |
| [isClear()](#isClear--) | 如果此制表位清除此位置的任何现有制表位，则返回 true。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setAlignment(int value)](#setAlignment-int-) | 设置此制表位处的文本对齐方式。 |
| [setLeader(int value)](#setLeader-int-) | 设置制表符下显示的引线类型。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### TabStop(double position) {#TabStop-double-}
```
public TabStop(double position)
```


初始化此类的新实例。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| position | double |  |

### TabStop(double position, int alignment, int leader) {#TabStop-double-int-int-}
```
public TabStop(double position, int alignment, int leader)
```


初始化此类的新实例。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| position | double |  |
| alignment | int |  |
| leader | int |  |

### equals(TabStop rhs) {#equals-com.aspose.words.TabStop-}
```
public boolean equals(TabStop rhs)
```


与指定的 TabStop 进行比较。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| rhs | [TabStop](../../com.aspose.words/tabstop) |  |

**退货：**
布尔值
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货：**
布尔值
### getAlignment() {#getAlignment--}
```
public int getAlignment()
```


获取此制表位处的文本对齐方式。

**退货：**
int - 此制表位处的文本对齐方式。返回值是其中之一[TabAlignment](../../com.aspose.words/tabalignment)常数。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getLeader() {#getLeader--}
```
public int getLeader()
```


获取制表符下显示的引导线类型。

**退货：**
int - 制表符下显示的引导线类型。返回值是其中之一[TabLeader](../../com.aspose.words/tableader)常数。
### getPosition() {#getPosition--}
```
public double getPosition()
```


获取制表位的位置（以磅为单位）。

**退货：**
double - 制表位的位置，以磅为单位。
### hashCode() {#hashCode--}
```
public int hashCode()
```




**退货：**
整数
### isClear() {#isClear--}
```
public boolean isClear()
```


如果此制表位清除此位置的任何现有制表位，则返回 true。

**退货：**
boolean - 如果此制表位清除此位置的任何现有制表位，则为真。
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


设置此制表位处的文本对齐方式。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 此制表位处的文本对齐方式。该值必须是其中之一[TabAlignment](../../com.aspose.words/tabalignment)常数。 |

### setLeader(int value) {#setLeader-int-}
```
public void setLeader(int value)
```


设置制表符下显示的引线类型。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 制表符下方显示的引线类型。该值必须是其中之一[TabLeader](../../com.aspose.words/tableader)常数。 |

### toString() {#toString--}
```
public String toString()
```




**退货：**
java.lang.字符串
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
