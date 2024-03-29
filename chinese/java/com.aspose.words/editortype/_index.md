---
title: EditorType
second_title: Aspose.Words for Java API 参考
description: 指定一组可能的别名或编辑组，这些别名或编辑组可用作别名以确定是否允许当前用户编辑由文档中的可编辑范围定义的单个范围。
type: docs
weight: 140
url: /zh/java/com.aspose.words/editortype/
---

**遗产：**
java.lang.Object
```
public class EditorType
```

指定一组可能的别名（或编辑组），这些别名可用作别名以确定是否允许当前用户编辑由文档中的可编辑范围定义的单个范围。
## 字段

| 场地 | 描述 |
| --- | --- |
| [ADMINISTRATORS](#ADMINISTRATORS) | 指定当启用文档保护时，与 Administrators 组关联的用户应被允许使用此编辑类型编辑可编辑范围。 |
| [CONTRIBUTORS](#CONTRIBUTORS) | 指定当启用文档保护时，应允许与贡献者组关联的用户使用此编辑类型编辑可编辑范围。 |
| [CURRENT](#CURRENT) | 指定当启用文档保护时，应允许与当前组关联的用户使用此编辑类型编辑可编辑范围。 |
| [DEFAULT](#DEFAULT) | 如同[UNSPECIFIED](../../com.aspose.words/editortype\#UNSPECIFIED). |
| [EDITORS](#EDITORS) | 指定当启用文档保护时，应允许与 Editors 组关联的用户使用此编辑类型编辑可编辑范围。 |
| [EVERYONE](#EVERYONE) | 指定在启用文档保护时，应允许所有打开文档的用户使用此编辑类型编辑可编辑范围。 |
| [NONE](#NONE) | 指定在启用文档保护时，不允许打开文档的任何用户使用此编辑类型编辑可编辑范围。 |
| [OWNERS](#OWNERS) | 指定当启用文档保护时，应允许与所有者组关联的用户使用此编辑类型编辑可编辑范围。 |
| [UNSPECIFIED](#UNSPECIFIED) | 表示未指定编辑器类型。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String editorTypeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int editorType)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int editorType)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### ADMINISTRATORS {#ADMINISTRATORS}
```
public static int ADMINISTRATORS
```


指定当启用文档保护时，与 Administrators 组关联的用户应被允许使用此编辑类型编辑可编辑范围。

### CONTRIBUTORS {#CONTRIBUTORS}
```
public static int CONTRIBUTORS
```


指定当启用文档保护时，应允许与贡献者组关联的用户使用此编辑类型编辑可编辑范围。

### CURRENT {#CURRENT}
```
public static int CURRENT
```


指定当启用文档保护时，应允许与当前组关联的用户使用此编辑类型编辑可编辑范围。

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


如同[UNSPECIFIED](../../com.aspose.words/editortype\#UNSPECIFIED).

### EDITORS {#EDITORS}
```
public static int EDITORS
```


指定当启用文档保护时，应允许与 Editors 组关联的用户使用此编辑类型编辑可编辑范围。

### EVERYONE {#EVERYONE}
```
public static int EVERYONE
```


指定在启用文档保护时，应允许所有打开文档的用户使用此编辑类型编辑可编辑范围。

### NONE {#NONE}
```
public static int NONE
```


指定在启用文档保护时，不允许打开文档的任何用户使用此编辑类型编辑可编辑范围。

### OWNERS {#OWNERS}
```
public static int OWNERS
```


指定当启用文档保护时，应允许与所有者组关联的用户使用此编辑类型编辑可编辑范围。

### UNSPECIFIED {#UNSPECIFIED}
```
public static int UNSPECIFIED
```


表示未指定编辑器类型。

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
### fromName(String editorTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String editorTypeName)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| editorTypeName | java.lang.String |  |

**退货：**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getName(int editorType) {#getName-int-}
```
public static String getName(int editorType)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| editorType | int |  |

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
### toString(int editorType) {#toString-int-}
```
public static String toString(int editorType)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| editorType | int |  |

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
