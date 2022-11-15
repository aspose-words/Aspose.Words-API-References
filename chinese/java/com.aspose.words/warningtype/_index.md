---
title: WarningType
second_title: Aspose.Words for Java API 参考
description: 指定在文档加载或保存期间由 Aspose.Words 发出的警告的类型。
type: docs
weight: 607
url: /zh/java/com.aspose.words/warningtype/
---

**遗产：**
java.lang.Object
```
public class WarningType
```

指定在文档加载或保存期间由 Aspose.Words 发出的警告的类型。
## 字段

| 场地 | 描述 |
| --- | --- |
| [DATA_LOSS](#DATA-LOSS) | 通用数据丢失，没有具体代码。 |
| [DATA_LOSS_CATEGORY](#DATA-LOSS-CATEGORY) | 加载后的文档树或保存后创建的文档中的某些文本/字符/图像或其他数据将丢失。 |
| [FONT_EMBEDDING](#FONT-EMBEDDING) | 文档保存期间嵌入字体信息丢失。 |
| [FONT_SUBSTITUTION](#FONT-SUBSTITUTION) | 字体已被替换。 |
| [HINT](#HINT) | 就潜在问题提出建议或建议改进。 |
| [MAJOR_FORMATTING_LOSS](#MAJOR-FORMATTING-LOSS) | 通用主要格式丢失，没有具体代码。 |
| [MAJOR_FORMATTING_LOSS_CATEGORY](#MAJOR-FORMATTING-LOSS-CATEGORY) | 与原始文档相比，生成的文档或其中的特定位置可能看起来有很大不同。 |
| [MINOR_FORMATTING_LOSS](#MINOR-FORMATTING-LOSS) | 一般轻微格式丢失，没有具体代码。 |
| [MINOR_FORMATTING_LOSS_CATEGORY](#MINOR-FORMATTING-LOSS-CATEGORY) | 与原始文档相比，生成的文档或其中的特定位置可能看起来有些不同。 |
| [UNEXPECTED_CONTENT](#UNEXPECTED-CONTENT) | 通用的意外内容，没有具体的代码。 |
| [UNEXPECTED_CONTENT_CATEGORY](#UNEXPECTED-CONTENT-CATEGORY) | 无法识别源文档中的某些内容（即 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String warningTypeName)](#fromName-java.lang.String-) |  |
| [fromNames(Set warningTypeNames)](#fromNames-java.util.Set-) |  |
| [getClass()](#getClass--) |  |
| [getName(int warningType)](#getName-int-) |  |
| [getNames(int warningType)](#getNames-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int warningType)](#toString-int-) |  |
| [toStringSet(int attr)](#toStringSet-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### DATA_LOSS {#DATA-LOSS}
```
public static int DATA_LOSS
```


通用数据丢失，没有具体代码。

### DATA_LOSS_CATEGORY {#DATA-LOSS-CATEGORY}
```
public static int DATA_LOSS_CATEGORY
```


加载后的文档树或保存后创建的文档中的某些文本/字符/图像或其他数据将丢失。

### FONT_EMBEDDING {#FONT-EMBEDDING}
```
public static int FONT_EMBEDDING
```


文档保存期间嵌入字体信息丢失。

### FONT_SUBSTITUTION {#FONT-SUBSTITUTION}
```
public static int FONT_SUBSTITUTION
```


字体已被替换。

### HINT {#HINT}
```
public static int HINT
```


就潜在问题提出建议或建议改进。

### MAJOR_FORMATTING_LOSS {#MAJOR-FORMATTING-LOSS}
```
public static int MAJOR_FORMATTING_LOSS
```


通用主要格式丢失，没有具体代码。

### MAJOR_FORMATTING_LOSS_CATEGORY {#MAJOR-FORMATTING-LOSS-CATEGORY}
```
public static int MAJOR_FORMATTING_LOSS_CATEGORY
```


与原始文档相比，生成的文档或其中的特定位置可能看起来有很大不同。

### MINOR_FORMATTING_LOSS {#MINOR-FORMATTING-LOSS}
```
public static int MINOR_FORMATTING_LOSS
```


一般轻微格式丢失，没有具体代码。

### MINOR_FORMATTING_LOSS_CATEGORY {#MINOR-FORMATTING-LOSS-CATEGORY}
```
public static int MINOR_FORMATTING_LOSS_CATEGORY
```


与原始文档相比，生成的文档或其中的特定位置可能看起来有些不同。

### UNEXPECTED_CONTENT {#UNEXPECTED-CONTENT}
```
public static int UNEXPECTED_CONTENT
```


通用的意外内容，没有具体的代码。

### UNEXPECTED_CONTENT_CATEGORY {#UNEXPECTED-CONTENT-CATEGORY}
```
public static int UNEXPECTED_CONTENT_CATEGORY
```


无法识别源文档中的某些内容（即不受支持），这可能会也可能不会导致问题或导致数据/格式丢失。

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
### fromName(String warningTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String warningTypeName)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| warningTypeName | java.lang.String |  |

**退货：**
整数
### fromNames(Set warningTypeNames) {#fromNames-java.util.Set-}
```
public static int fromNames(Set warningTypeNames)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| warningTypeNames | java.util.Set |  |

**退货：**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getName(int warningType) {#getName-int-}
```
public static String getName(int warningType)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| warningType | int |  |

**退货：**
java.lang.字符串
### getNames(int warningType) {#getNames-int-}
```
public static Set getNames(int warningType)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| warningType | int |  |

**退货：**
java.util.Set
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
### toString(int warningType) {#toString-int-}
```
public static String toString(int warningType)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| warningType | int |  |

**退货：**
java.lang.字符串
### toStringSet(int attr) {#toStringSet-int-}
```
public static String toStringSet(int attr)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| attr | int |  |

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
