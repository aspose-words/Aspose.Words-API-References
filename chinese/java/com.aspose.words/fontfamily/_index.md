---
title: FontFamily
second_title: Aspose.Words for Java API 参考
description: 表示字体系列。
type: docs
weight: 278
url: /zh/java/com.aspose.words/fontfamily/
---

**遗产：**
java.lang.Object
```
public class FontFamily
```

表示字体系列。

字体系列是一组具有共同笔画宽度和衬线特征的字体。
## 字段

| 场地 | 描述 |
| --- | --- |
| [AUTO](#AUTO) | 指定通用家族名称。 |
| [DECORATIVE](#DECORATIVE) | 指定新奇字体。 |
| [MODERN](#MODERN) | 指定带或不带衬线的等宽字体。 |
| [ROMAN](#ROMAN) | 指定带衬线的比例字体。 |
| [SCRIPT](#SCRIPT) | 指定一种设计为看起来像手写的字体；示例包括脚本和草书。 |
| [SWISS](#SWISS) | 指定不带衬线的比例字体。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String fontFamilyName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int fontFamily)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int fontFamily)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


指定通用家族名称。当有关字体的信息不存在或无关紧要时使用此名称。使用默认字体。

### DECORATIVE {#DECORATIVE}
```
public static int DECORATIVE
```


指定新奇字体。一个例子是古英语。

### MODERN {#MODERN}
```
public static int MODERN
```


指定带或不带衬线的等宽字体。等宽字体通常是现代的；示例包括 Pica、Elite 和 Courier New。

### ROMAN {#ROMAN}
```
public static int ROMAN
```


指定带衬线的比例字体。一个例子是Times New Roman。

### SCRIPT {#SCRIPT}
```
public static int SCRIPT
```


指定一种设计为看起来像手写的字体；示例包括脚本和草书。

### SWISS {#SWISS}
```
public static int SWISS
```


指定不带衬线的比例字体。一个例子是 Arial。

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
### fromName(String fontFamilyName) {#fromName-java.lang.String-}
```
public static int fromName(String fontFamilyName)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fontFamilyName | java.lang.String |  |

**退货：**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getName(int fontFamily) {#getName-int-}
```
public static String getName(int fontFamily)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fontFamily | int |  |

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
### toString(int fontFamily) {#toString-int-}
```
public static String toString(int fontFamily)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| fontFamily | int |  |

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
