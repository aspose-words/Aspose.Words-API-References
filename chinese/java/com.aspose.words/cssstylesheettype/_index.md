---
title: CssStyleSheetType
second_title: Aspose.Words for Java API 参考
description: 指定如何将 CSS 层叠样式表样式导出为 HTML。
type: docs
weight: 97
url: /zh/java/com.aspose.words/cssstylesheettype/
---

**遗产：**
java.lang.Object
```
public class CssStyleSheetType
```

指定如何将 CSS（层叠样式表）样式导出到 HTML。
## 字段

| 场地 | 描述 |
| --- | --- |
| [EMBEDDED](#EMBEDDED) | CSS 样式与嵌入在 HTML 文件中的样式表中的内容分开编写。 |
| [EXTERNAL](#EXTERNAL) | CSS 样式与外部文件中样式表的内容分开编写。 |
| [INLINE](#INLINE) |  CSS 样式是内联编写的（作为**style**每个元素的属性）。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String cssStyleSheetTypeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int cssStyleSheetType)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int cssStyleSheetType)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### EMBEDDED {#EMBEDDED}
```
public static int EMBEDDED
```


CSS 样式与嵌入在 HTML 文件中的样式表中的内容分开编写。

### EXTERNAL {#EXTERNAL}
```
public static int EXTERNAL
```


CSS 样式与外部文件中样式表的内容分开编写。 HTML 文件链接样式表。

### INLINE {#INLINE}
```
public static int INLINE
```


 CSS 样式是内联编写的（作为**style**每个元素的属性）。

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
### fromName(String cssStyleSheetTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String cssStyleSheetTypeName)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| cssStyleSheetTypeName | java.lang.String |  |

**退货：**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getName(int cssStyleSheetType) {#getName-int-}
```
public static String getName(int cssStyleSheetType)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| cssStyleSheetType | int |  |

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
### toString(int cssStyleSheetType) {#toString-int-}
```
public static String toString(int cssStyleSheetType)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| cssStyleSheetType | int |  |

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
