---
title: BuildingBlockType
second_title: Aspose.Words for Java API 参考
description: 指定构建基块类型。
type: docs
weight: 45
url: /zh/java/com.aspose.words/buildingblocktype/
---

**遗产：**
java.lang.Object
```
public class BuildingBlockType
```

指定构建基块类型。该类型可能会影响构建基块在 Microsoft Word 中的可见性和行为。

对应于**ST\_DocPartType**输入 OOXML。
## 字段

| 场地 | 描述 |
| --- | --- |
| [ALL](#ALL) | 构建块与所有类型相关联。 |
| [AUTOMATICALLY_REPLACE_NAME_WITH_CONTENT](#AUTOMATICALLY-REPLACE-NAME-WITH-CONTENT) | 允许将构建块的名称输入应用程序时自动插入到文档中。 |
| [AUTO_CORRECT](#AUTO-CORRECT) | 构建块与拼写和语法工具相关联。 |
| [AUTO_TEXT](#AUTO-TEXT) | 构建基块是一个自动图文集词条。 |
| [DEFAULT](#DEFAULT) | 另存为[NONE](../../com.aspose.words/buildingblocktype\#NONE). |
| [FORM_FIELD_HELP_TEXT](#FORM-FIELD-HELP-TEXT) | 构建块是一个表单字段帮助文本。 |
| [NONE](#NONE) | 没有为构建块指定类型信息。 |
| [NORMAL](#NORMAL) | 积木是正常的（即 |
| [STRUCTURED_DOCUMENT_TAG_PLACEHOLDER_TEXT](#STRUCTURED-DOCUMENT-TAG-PLACEHOLDER-TEXT) | 构建块是结构化的文档标签占位符文本。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String buildingBlockTypeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int buildingBlockType)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int buildingBlockType)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### ALL {#ALL}
```
public static int ALL
```


构建块与所有类型相关联。

### AUTOMATICALLY_REPLACE_NAME_WITH_CONTENT {#AUTOMATICALLY-REPLACE-NAME-WITH-CONTENT}
```
public static int AUTOMATICALLY_REPLACE_NAME_WITH_CONTENT
```


允许将构建块的名称输入应用程序时自动插入到文档中。

### AUTO_CORRECT {#AUTO-CORRECT}
```
public static int AUTO_CORRECT
```


构建块与拼写和语法工具相关联。

### AUTO_TEXT {#AUTO-TEXT}
```
public static int AUTO_TEXT
```


构建基块是一个自动图文集词条。

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


另存为[NONE](../../com.aspose.words/buildingblocktype\#NONE).

### FORM_FIELD_HELP_TEXT {#FORM-FIELD-HELP-TEXT}
```
public static int FORM_FIELD_HELP_TEXT
```


构建块是一个表单字段帮助文本。

### NONE {#NONE}
```
public static int NONE
```


没有为构建块指定类型信息。

### NORMAL {#NORMAL}
```
public static int NORMAL
```


构建块是一个正常的（即常规的）词汇表文档条目。

### STRUCTURED_DOCUMENT_TAG_PLACEHOLDER_TEXT {#STRUCTURED-DOCUMENT-TAG-PLACEHOLDER-TEXT}
```
public static int STRUCTURED_DOCUMENT_TAG_PLACEHOLDER_TEXT
```


构建块是结构化的文档标签占位符文本。

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
### fromName(String buildingBlockTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String buildingBlockTypeName)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| buildingBlockTypeName | java.lang.String |  |

**退货：**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getName(int buildingBlockType) {#getName-int-}
```
public static String getName(int buildingBlockType)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| buildingBlockType | int |  |

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
### toString(int buildingBlockType) {#toString-int-}
```
public static String toString(int buildingBlockType)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| buildingBlockType | int |  |

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
