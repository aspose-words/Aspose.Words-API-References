---
title: MarkupLevel
second_title: Aspose.Words for Java API 参考
description: 指定文档树中可以出现特定内容的级别。
type: docs
weight: 390
url: /zh/java/com.aspose.words/markuplevel/
---

**遗产：**
java.lang.Object
```
public class MarkupLevel
```

指定文档树中特定的级别[StructuredDocumentTag](../../com.aspose.words/structureddocumenttag)可能发生。
## 字段

| 场地 | 描述 |
| --- | --- |
| [BLOCK](#BLOCK) | 该元素出现在块级别（例如 |
| [CELL](#CELL) | 该元素出现在一行中的单元格中。 |
| [INLINE](#INLINE) | 该元素出现在行内级别（例如 |
| [ROW](#ROW) | 该元素出现在表中的行之间。 |
| [UNKNOWN](#UNKNOWN) | 指定未知或无效值。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String markupLevelName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int markupLevel)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int markupLevel)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### BLOCK {#BLOCK}
```
public static int BLOCK
```


该元素出现在块级别（例如在表格和段落之间）。

### CELL {#CELL}
```
public static int CELL
```


该元素出现在一行中的单元格中。

### INLINE {#INLINE}
```
public static int INLINE
```


该元素出现在行内级别（例如，在文本运行中）。

### ROW {#ROW}
```
public static int ROW
```


该元素出现在表中的行之间。

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


指定未知或无效值。

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
### fromName(String markupLevelName) {#fromName-java.lang.String-}
```
public static int fromName(String markupLevelName)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| markupLevelName | java.lang.String |  |

**退货：**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getName(int markupLevel) {#getName-int-}
```
public static String getName(int markupLevel)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| markupLevel | int |  |

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
### toString(int markupLevel) {#toString-int-}
```
public static String toString(int markupLevel)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| markupLevel | int |  |

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
