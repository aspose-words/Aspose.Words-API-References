---
title: NumeralFormat
second_title: Aspose.Words for Java API Reference
description: 指示在呈现为固定页面格式时用于表示数字的符号集。
type: docs
weight: 410
url: /zh/java/com.aspose.words/numeralformat/
---

**遗产:**
java.lang.Object
```
public class NumeralFormat
```

指示在呈现为固定页面格式时用于表示数字的符号集。
## 字段

| 字段 | 描述 |
| --- | --- |
| [ARABIC_INDIC](#ARABIC-INDIC) | 阿拉伯语中使用的数字：\\u0660\\u0661\\u0662\\u0663\\u0664\\u0665\\u0666\\u0667\\u0668\\u0669。 |
| [CONTEXT](#CONTEXT) | 符号集由上下文（语言环境和 RTL 属性）决定。 |
| [EASTERN_ARABIC_INDIC](#EASTERN-ARABIC-INDIC) | 波斯语和乌尔都语中使用的数字：\\u06f0\\u06f1\\u06f2\\u06f3\\u06f4\\u06f5\\u06f6\\u06f7\\u06f8\\u06f9。 |
| [EUROPEAN](#EUROPEAN) | 欧洲数字：0123456789。 |
| [SYSTEM](#SYSTEM) | 不支持此选项。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String numeralFormatName)](#fromName-java.lang.String-) |  |
| [get班级()](#get班级--) |  |
| [getName(int numeralFormat)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int numeralFormat)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### ARABIC_INDIC {#ARABIC-INDIC}
```
public static int ARABIC_INDIC
```


阿拉伯语中使用的数字：\\u0660\\u0661\\u0662\\u0663\\u0664\\u0665\\u0666\\u0667\\u0668\\u0669。 Unicode 范围 U+0660 - u+0669。

### CONTEXT {#CONTEXT}
```
public static int CONTEXT
```


符号集由上下文（语言环境和 RTL 属性）决定。

### EASTERN_ARABIC_INDIC {#EASTERN-ARABIC-INDIC}
```
public static int EASTERN_ARABIC_INDIC
```


波斯语和乌尔都语中使用的数字：\\u06f0\\u06f1\\u06f2\\u06f3\\u06f4\\u06f5\\u06f6\\u06f7\\u06f8\\u06f9。 Unicode 范围 U+06F0 - u+06F9。

### EUROPEAN {#EUROPEAN}
```
public static int EUROPEAN
```


欧洲数字：0123456789。

### SYSTEM {#SYSTEM}
```
public static int SYSTEM
```


不支持此选项。符号集由区域设置决定。

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
### fromName(String numeralFormatName) {#fromName-java.lang.String-}
```
public static int fromName(String numeralFormatName)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| numeralFormatName | java.lang.String |  |

**退货:**
整数
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getName(int numeralFormat) {#getName-int-}
```
public static String getName(int numeralFormat)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| numeralFormat | int |  |

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
### toString(int numeralFormat) {#toString-int-}
```
public static String toString(int numeralFormat)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| numeralFormat | int |  |

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
