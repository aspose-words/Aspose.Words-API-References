---
title: DocumentSecurity
second_title: Aspose.Words for Java API 参考
description: 用作 / 属性的值。
type: docs
weight: 130
url: /zh/java/com.aspose.words/documentsecurity/
---

**遗产：**
java.lang.Object
```
public class DocumentSecurity
```

用作值[BuiltInDocumentProperties.getSecurity()](../../com.aspose.words/builtindocumentproperties\#getSecurity--) / [BuiltInDocumentProperties.setSecurity(int)](../../com.aspose.words/builtindocumentproperties\#setSecurity-int-)财产。将文档的安全级别指定为数值。
## 字段

| 场地 | 描述 |
| --- | --- |
| [NONE](#NONE) | 该属性没有指定安全状态。 |
| [PASSWORD_PROTECTED](#PASSWORD-PROTECTED) | 该文档受密码保护。 |
| [READ_ONLY_ENFORCED](#READ-ONLY-ENFORCED) | 始终以只读方式打开的文档。 |
| [READ_ONLY_EXCEPT_ANNOTATIONS](#READ-ONLY-EXCEPT-ANNOTATIONS) | 文档始终以只读方式打开，注释除外。 |
| [READ_ONLY_RECOMMENDED](#READ-ONLY-RECOMMENDED) | 如果可能，要以只读方式打开的文档，但可以覆盖该设置。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String documentSecurityName)](#fromName-java.lang.String-) |  |
| [fromNames(Set documentSecurityNames)](#fromNames-java.util.Set-) |  |
| [getClass()](#getClass--) |  |
| [getName(int documentSecurity)](#getName-int-) |  |
| [getNames(int documentSecurity)](#getNames-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int documentSecurity)](#toString-int-) |  |
| [toStringSet(int attr)](#toStringSet-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### NONE {#NONE}
```
public static int NONE
```


该属性没有指定安全状态。

### PASSWORD_PROTECTED {#PASSWORD-PROTECTED}
```
public static int PASSWORD_PROTECTED
```


该文档受密码保护。 （到目前为止，从未在文档中看到过注释）。

### READ_ONLY_ENFORCED {#READ-ONLY-ENFORCED}
```
public static int READ_ONLY_ENFORCED
```


始终以只读方式打开的文档。

### READ_ONLY_EXCEPT_ANNOTATIONS {#READ-ONLY-EXCEPT-ANNOTATIONS}
```
public static int READ_ONLY_EXCEPT_ANNOTATIONS
```


文档始终以只读方式打开，注释除外。

### READ_ONLY_RECOMMENDED {#READ-ONLY-RECOMMENDED}
```
public static int READ_ONLY_RECOMMENDED
```


如果可能，要以只读方式打开的文档，但可以覆盖该设置。

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
### fromName(String documentSecurityName) {#fromName-java.lang.String-}
```
public static int fromName(String documentSecurityName)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| documentSecurityName | java.lang.String |  |

**退货：**
整数
### fromNames(Set documentSecurityNames) {#fromNames-java.util.Set-}
```
public static int fromNames(Set documentSecurityNames)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| documentSecurityNames | java.util.Set |  |

**退货：**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getName(int documentSecurity) {#getName-int-}
```
public static String getName(int documentSecurity)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| documentSecurity | int |  |

**退货：**
java.lang.字符串
### getNames(int documentSecurity) {#getNames-int-}
```
public static Set getNames(int documentSecurity)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| documentSecurity | int |  |

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
### toString(int documentSecurity) {#toString-int-}
```
public static String toString(int documentSecurity)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| documentSecurity | int |  |

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
