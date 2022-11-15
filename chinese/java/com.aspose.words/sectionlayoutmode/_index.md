---
title: SectionLayoutMode
second_title: Aspose.Words for Java API 参考
description: 指定允许定义文档网格行为的部分的布局模式。
type: docs
weight: 511
url: /zh/java/com.aspose.words/sectionlayoutmode/
---

**遗产：**
java.lang.Object
```
public class SectionLayoutMode
```

指定允许定义文档网格行为的部分的布局模式。
## 字段

| 场地 | 描述 |
| --- | --- |
| [DEFAULT](#DEFAULT) | 指定不应将文档网格应用于文档中相应部分的内容。 |
| [GRID](#GRID) | 指定相应的部分应将额外的行间距和字符间距添加到每一行和其中的字符，以保持每页的特定行数和每行的字符数。 |
| [LINE_GRID](#LINE-GRID) | 指定相应部分应为其中的每一行添加额外的行距，以保持每页的指定行数。 |
| [SNAP_TO_CHARS](#SNAP-TO-CHARS) | 指定相应的部分应将额外的行间距和字符间距添加到每一行和其中的字符，以保持每页的特定行数和每行的字符数。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String sectionLayoutModeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int sectionLayoutMode)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int sectionLayoutMode)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


指定不应将文档网格应用于文档中相应部分的内容。

### GRID {#GRID}
```
public static int GRID
```


指定相应的部分应将额外的行间距和字符间距添加到每一行和其中的字符，以保持每页的特定行数和每行的字符数。键入时字符不会自动与网格线对齐。

### LINE_GRID {#LINE-GRID}
```
public static int LINE_GRID
```


指定相应部分应为其中的每一行添加额外的行距，以保持每页的指定行数。

### SNAP_TO_CHARS {#SNAP-TO-CHARS}
```
public static int SNAP_TO_CHARS
```


指定相应的部分应将额外的行间距和字符间距添加到每一行和其中的字符，以保持每页的特定行数和每行的字符数。键入时字符将自动与网格线对齐。

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
### fromName(String sectionLayoutModeName) {#fromName-java.lang.String-}
```
public static int fromName(String sectionLayoutModeName)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| sectionLayoutModeName | java.lang.String |  |

**退货：**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getName(int sectionLayoutMode) {#getName-int-}
```
public static String getName(int sectionLayoutMode)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| sectionLayoutMode | int |  |

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
### toString(int sectionLayoutMode) {#toString-int-}
```
public static String toString(int sectionLayoutMode)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| sectionLayoutMode | int |  |

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
