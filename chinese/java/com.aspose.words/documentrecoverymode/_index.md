---
title: "DocumentRecoveryMode"
linktitle: "DocumentRecoveryMode"
second_title: "Aspose.Words for Java"
description: "指定文档在 Java 中加载时遇到错误时可用的恢复选项。"
type: docs
weight: 171
url: /zh/java/com.aspose.words/documentrecoverymode/
---

**Inheritance:**
java.lang.Object
```
public class DocumentRecoveryMode
```

指定文档在加载时遇到错误时可用的恢复选项。

 **Examples:** 

展示如何在加载期间出现错误时尝试恢复文档。

```

 LoadOptions loadOptions = new LoadOptions();
 loadOptions.setRecoveryMode(DocumentRecoveryMode.TRY_RECOVER);

 Document doc = new Document(getMyDir() + "Corrupted footnotes.docx", loadOptions);
 
```
## 字段集合

| 字段 | 描述 |
| --- | --- |
| [NONE](#NONE) | 不尝试恢复。 |
| [TRY_RECOVER](#TRY-RECOVER) | 尝试在尽可能保留数据的情况下恢复文档。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [fromName(String documentRecoveryModeName)](#fromName-java.lang.String) |  |
| [getName(int documentRecoveryMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int documentRecoveryMode)](#toString-int) |  |
### NONE {#NONE}
```
public static int NONE
```


不尝试恢复。如果文档无效，加载将因错误而失败。

### TRY_RECOVER {#TRY-RECOVER}
```
public static int TRY_RECOVER
```


尝试在尽可能保留数据的情况下恢复文档。

### length {#length}
```
public static int length
```


### fromName(String documentRecoveryModeName) {#fromName-java.lang.String}
```
public static int fromName(String documentRecoveryModeName)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| documentRecoveryModeName | java.lang.String |  |

**Returns:**
int
### getName(int documentRecoveryMode) {#getName-int}
```
public static String getName(int documentRecoveryMode)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| documentRecoveryMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int documentRecoveryMode) {#toString-int}
```
public static String toString(int documentRecoveryMode)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| documentRecoveryMode | int |  |

**Returns:**
java.lang.String
