---
title: CompressionLevel
second_title: Aspose.Words for Java API 参考
description: OOXML 文件的压缩级别。
type: docs
weight: 88
url: /zh/java/com.aspose.words/compressionlevel/
---

**遗产:**
java.lang.Object
```
public class CompressionLevel
```

OOXML 文件的压缩级别。

（DOCX 和 DOTX 文件在内部是一个 ZIP 存档，此属性控制存档的压缩级别。

请注意，FlatOpc 文件不是 ZIP 存档，因此，此属性不会影响 FlatOpc 文件。）
## 字段

| 字段 | 描述 |
| --- | --- |
| [FAST](#FAST) | 快速压缩级别。 |
| [MAXIMUM](#MAXIMUM) | 最大压缩级别。 |
| [NORMAL](#NORMAL) | 正常压缩级别。 |
| [SUPER_FAST](#SUPER-FAST) | 超快速压缩级别。 |
| [length](#length) |  |
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String compressionLevelName)](#fromName-java.lang.String-) |  |
| [get班级()](#get班级--) |  |
| [getName(int compressionLevel)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int compressionLevel)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### FAST {#FAST}
```
public static int FAST
```


快速压缩级别。

### MAXIMUM {#MAXIMUM}
```
public static int MAXIMUM
```


最大压缩级别。

### NORMAL {#NORMAL}
```
public static int NORMAL
```


正常压缩级别。 Aspose.Words 使用的默认压缩级别。

### SUPER_FAST {#SUPER-FAST}
```
public static int SUPER_FAST
```


超快速压缩级别。 Microsoft Word 使用此压缩级别。

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
### fromName(String compressionLevelName) {#fromName-java.lang.String-}
```
public static int fromName(String compressionLevelName)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| compressionLevelName | java.lang.String |  |

**退货:**
整数
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getName(int compressionLevel) {#getName-int-}
```
public static String getName(int compressionLevel)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| compressionLevel | int |  |

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
### toString(int compressionLevel) {#toString-int-}
```
public static String toString(int compressionLevel)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| compressionLevel | int |  |

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
