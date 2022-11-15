---
title: HtmlElementSizeOutputMode
second_title: Aspose.Words for Java API 参考
description: 指定 Aspose.Words 如何将元素宽度和高度导出到 HTML MHTML 和 EPUB。
type: docs
weight: 324
url: /zh/java/com.aspose.words/htmlelementsizeoutputmode/
---

**遗产：**
java.lang.Object
```
public class HtmlElementSizeOutputMode
```

指定 Aspose.Words 如何将元素宽度和高度导出到 HTML、MHTML 和 EPUB。
## 字段

| 场地 | 描述 |
| --- | --- |
| [ALL](#ALL) | 导出文档中指定的所有元素大小，包括绝对单位和相对单位。 |
| [NONE](#NONE) | 不导出元素大小。 |
| [RELATIVE_ONLY](#RELATIVE-ONLY) | 只有在文档中以相对单位指定元素大小时，才会导出元素大小。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String htmlElementSizeOutputModeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int htmlElementSizeOutputMode)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int htmlElementSizeOutputMode)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### ALL {#ALL}
```
public static int ALL
```


导出文档中指定的所有元素大小，包括绝对单位和相对单位。

### NONE {#NONE}
```
public static int NONE
```


不导出元素大小。视觉代理会根据元素之间的关系自动构建布局。

### RELATIVE_ONLY {#RELATIVE-ONLY}
```
public static int RELATIVE_ONLY
```


只有在文档中以相对单位指定元素大小时，才会导出元素大小。在此模式下不导出固定尺寸。视觉代理将计算缺失的尺寸以使文档布局更自然。

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
### fromName(String htmlElementSizeOutputModeName) {#fromName-java.lang.String-}
```
public static int fromName(String htmlElementSizeOutputModeName)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| htmlElementSizeOutputModeName | java.lang.String |  |

**退货：**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getName(int htmlElementSizeOutputMode) {#getName-int-}
```
public static String getName(int htmlElementSizeOutputMode)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| htmlElementSizeOutputMode | int |  |

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
### toString(int htmlElementSizeOutputMode) {#toString-int-}
```
public static String toString(int htmlElementSizeOutputMode)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| htmlElementSizeOutputMode | int |  |

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
