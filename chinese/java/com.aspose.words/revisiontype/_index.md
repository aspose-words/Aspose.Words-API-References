---
title: RevisionType
second_title: Aspose.Words for Java API 参考
description: 指定在 中跟踪的更改类型。
type: docs
weight: 490
url: /zh/java/com.aspose.words/revisiontype/
---

**遗产:**
java.lang.Object
```
public class RevisionType
```

指定跟踪的更改类型[Revision](../../com.aspose.words/revision).
## 字段

| 场地 | 描述 |
| --- | --- |
| [DELETION](#DELETION) | 内容已从文档中删除。 |
| [FORMAT_CHANGE](#FORMAT-CHANGE) | 格式更改已应用于父节点。 |
| [INSERTION](#INSERTION) | 文档中插入了新内容。 |
| [MOVING](#MOVING) | 内容已在文档中移动。 |
| [STYLE_DEFINITION_CHANGE](#STYLE-DEFINITION-CHANGE) | 格式更改已应用于父样式。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String revisionTypeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int revisionType)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int revisionType)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### DELETION {#DELETION}
```
public static int DELETION
```


内容已从文档中删除。

### FORMAT_CHANGE {#FORMAT-CHANGE}
```
public static int FORMAT_CHANGE
```


格式更改已应用于父节点。

### INSERTION {#INSERTION}
```
public static int INSERTION
```


文档中插入了新内容。

### MOVING {#MOVING}
```
public static int MOVING
```


内容已在文档中移动。

### STYLE_DEFINITION_CHANGE {#STYLE-DEFINITION-CHANGE}
```
public static int STYLE_DEFINITION_CHANGE
```


格式更改已应用于父样式。

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
### fromName(String revisionTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String revisionTypeName)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| revisionTypeName | java.lang.String |  |

**退货:**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getName(int revisionType) {#getName-int-}
```
public static String getName(int revisionType)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| revisionType | int |  |

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
### toString(int revisionType) {#toString-int-}
```
public static String toString(int revisionType)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| revisionType | int |  |

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
