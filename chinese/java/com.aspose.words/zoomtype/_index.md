---
title: ZoomType
second_title: Aspose.Words for Java API 参考
description: 文档在 Microsoft Word 屏幕上显示的大小的可能值。
type: docs
weight: 631
url: /zh/java/com.aspose.words/zoomtype/
---

**遗产：**
java.lang.Object
```
public class ZoomType
```

文档在 Microsoft Word 屏幕上显示的大小的可能值。
## 字段

| 场地 | 描述 |
| --- | --- |
| [CUSTOM](#CUSTOM) | 缩放百分比是明确设置的。 |
| [FULL_PAGE](#FULL-PAGE) | 缩放百分比会自动重新计算以适应一整页。 |
| [NONE](#NONE) | 指示使用显式缩放百分比。 |
| [PAGE_WIDTH](#PAGE-WIDTH) | 缩放百分比会自动重新计算以适应页面宽度。 |
| [TEXT_FIT](#TEXT-FIT) | 缩放百分比会自动重新计算以适合文本。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String zoomTypeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int zoomType)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int zoomType)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


缩放百分比是明确设置的。当控件大小更改时，它不会自动重新计算。

### FULL_PAGE {#FULL-PAGE}
```
public static int FULL_PAGE
```


缩放百分比会自动重新计算以适应一整页。

### NONE {#NONE}
```
public static int NONE
```


指示使用显式缩放百分比。如同[CUSTOM](../../com.aspose.words/zoomtype\#CUSTOM).

### PAGE_WIDTH {#PAGE-WIDTH}
```
public static int PAGE_WIDTH
```


缩放百分比会自动重新计算以适应页面宽度。

### TEXT_FIT {#TEXT-FIT}
```
public static int TEXT_FIT
```


缩放百分比会自动重新计算以适合文本。

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
### fromName(String zoomTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String zoomTypeName)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| zoomTypeName | java.lang.String |  |

**退货：**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getName(int zoomType) {#getName-int-}
```
public static String getName(int zoomType)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| zoomType | int |  |

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
### toString(int zoomType) {#toString-int-}
```
public static String toString(int zoomType)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| zoomType | int |  |

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
