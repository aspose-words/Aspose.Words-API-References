---
title: HtmlVersion
second_title: Aspose.Words for Java API 参考
description: 指示将文档保存为和格式时使用的 HTML 版本。
type: docs
weight: 332
url: /zh/java/com.aspose.words/htmlversion/
---

**遗产：**
java.lang.Object
```
public class HtmlVersion
```

表示将文档保存到时使用的 HTML 版本[SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML)和[SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML)格式。
## 字段

| 场地 | 描述 |
| --- | --- |
| [HTML_5](#HTML-5) | 按照 HTML 5 标准保存文档。 |
| [XHTML](#XHTML) | 按照 XHTML 1.0 Transitional 标准保存文档。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String htmlVersionName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int htmlVersion)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int htmlVersion)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### HTML_5 {#HTML-5}
```
public static int HTML_5
```


按照 HTML 5 标准保存文档。

### XHTML {#XHTML}
```
public static int XHTML
```


按照 XHTML 1.0 Transitional 标准保存文档。

Aspose.Words 旨在根据 XHTML 1.0 Transitional 标准输出 XHTML，但输出并不总是根据 DTD 进行验证。 Microsoft Word 文档中的某些结构很难或不可能映射到将根据 XHTML 模式进行验证的文档。例如，XHTML 不允许嵌套列表（UL 不能嵌套在另一个 UL 元素中），但在 Microsoft Word 文档中，多级列表经常出现。

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
### fromName(String htmlVersionName) {#fromName-java.lang.String-}
```
public static int fromName(String htmlVersionName)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| htmlVersionName | java.lang.String |  |

**退货：**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getName(int htmlVersion) {#getName-int-}
```
public static String getName(int htmlVersion)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| htmlVersion | int |  |

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
### toString(int htmlVersion) {#toString-int-}
```
public static String toString(int htmlVersion)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| htmlVersion | int |  |

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
