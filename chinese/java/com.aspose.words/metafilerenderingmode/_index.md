---
title: MetafileRenderingMode
second_title: Aspose.Words for Java API Reference
description: 指定 Aspose.Words 应如何呈现 WMF 和 EMF 元文件。
type: docs
weight: 396
url: /zh/java/com.aspose.words/metafilerenderingmode/
---

**遗产:**
java.lang.Object
```
public class MetafileRenderingMode
```

指定 Aspose.Words 应如何呈现 WMF 和 EMF 元文件。
## 字段

| 字段 | 描述 |
| --- | --- |
| [BITMAP](#BITMAP) | Aspose.Words 调用 GDI+ 将元文件呈现为位图，然后将位图保存到输出文档。 |
| [VECTOR](#VECTOR) | Aspose.Words 将元文件呈现为矢量图形。 |
| [VECTOR_WITH_FALLBACK](#VECTOR-WITH-FALLBACK) | Aspose.Words 尝试将元文件呈现为矢量图形。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String metafileRenderingModeName)](#fromName-java.lang.String-) |  |
| [get班级()](#get班级--) |  |
| [getName(int metafileRenderingMode)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int metafileRenderingMode)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### BITMAP {#BITMAP}
```
public static int BITMAP
```


Aspose.Words 调用 GDI+ 将元文件呈现为位图，然后将位图保存到输出文档。

### VECTOR {#VECTOR}
```
public static int VECTOR
```


Aspose.Words 将元文件呈现为矢量图形。

### VECTOR_WITH_FALLBACK {#VECTOR-WITH-FALLBACK}
```
public static int VECTOR_WITH_FALLBACK
```


Aspose.Words 尝试将元文件呈现为矢量图形。如果 Aspose.Words 无法正确地将某些元文件记录呈现为矢量图形，那么 Aspose.Words 会将此元文件呈现为位图。

### length {#length}
```
public static int length
```


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
### fromName(String metafileRenderingModeName) {#fromName-java.lang.String-}
```
public static int fromName(String metafileRenderingModeName)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| metafileRenderingModeName | java.lang.String |  |

**退货:**
整数
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getName(int metafileRenderingMode) {#getName-int-}
```
public static String getName(int metafileRenderingMode)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| metafileRenderingMode | int |  |

**退货:**
java.lang.String
### getValues() {#getValues--}
```
public static int[] getValues()
```




**退货:**
整数[]
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
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




**退货:**
java.lang.String
### toString(int metafileRenderingMode) {#toString-int-}
```
public static String toString(int metafileRenderingMode)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| metafileRenderingMode | int |  |

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
