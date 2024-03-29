---
title: PreferredWidthType
second_title: Aspose.Words for Java API 参考
description: 指定表格或单元格的首选宽度的测量单位。
type: docs
weight: 467
url: /zh/java/com.aspose.words/preferredwidthtype/
---

**遗产：**
java.lang.Object
```
public class PreferredWidthType
```

指定表格或单元格的首选宽度的测量单位。
## 字段

| 场地 | 描述 |
| --- | --- |
| [AUTO](#AUTO) | 未指定首选宽度。 |
| [PERCENT](#PERCENT) | 使用指定的百分比测量当前项目宽度。 |
| [POINTS](#POINTS) | 使用指定数量的点（1/72 英寸）测量当前项目宽度。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String preferredWidthTypeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int preferredWidthType)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int preferredWidthType)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


未指定首选宽度。表格或单元格的实际宽度要么使用显式宽度指定，要么在显示表格时由表格布局算法自动确定，具体取决于表格自动调整设置。

### PERCENT {#PERCENT}
```
public static int PERCENT
```


使用指定的百分比测量当前项目宽度。

### POINTS {#POINTS}
```
public static int POINTS
```


使用指定数量的点（1/72 英寸）测量当前项目宽度。

### length {#length}
```
public static int length
```


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
### fromName(String preferredWidthTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String preferredWidthTypeName)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| preferredWidthTypeName | java.lang.String |  |

**退货：**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getName(int preferredWidthType) {#getName-int-}
```
public static String getName(int preferredWidthType)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| preferredWidthType | int |  |

**退货：**
java.lang.字符串
### getValues() {#getValues--}
```
public static int[] getValues()
```




**退货：**
整数[]
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货：**
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




**退货：**
java.lang.字符串
### toString(int preferredWidthType) {#toString-int-}
```
public static String toString(int preferredWidthType)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| preferredWidthType | int |  |

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
