---
title: TextFormFieldType
second_title: Aspose.Words for Java API 参考
description: 指定文本表单域的类型。
type: docs
weight: 565
url: /zh/java/com.aspose.words/textformfieldtype/
---

**遗产：**
java.lang.Object
```
public class TextFormFieldType
```

指定文本表单域的类型。
## 字段

| 场地 | 描述 |
| --- | --- |
| [CALCULATED](#CALCULATED) | 文本表单字段值是根据在[FormField.getTextInputDefault()](../../com.aspose.words/formfield\#getTextInputDefault--) / [FormField.setTextInputDefault(java.lang.String)](../../com.aspose.words/formfield\#setTextInputDefault-java.lang.String-)财产。 |
| [CURRENT_DATE](#CURRENT-DATE) | 文本表单字段值是字段更新时的当前日期。 |
| [CURRENT_TIME](#CURRENT-TIME) | 文本表单字段值是字段更新的当前时间。 |
| [DATE](#DATE) | 文本表单域只能包含一个有效的日期值。 |
| [NUMBER](#NUMBER) | 文本表单域只能包含数字。 |
| [REGULAR](#REGULAR) | 文本表单域可以包含任何文本。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String textFormFieldTypeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int textFormFieldType)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int textFormFieldType)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### CALCULATED {#CALCULATED}
```
public static int CALCULATED
```


文本表单字段值是根据在[FormField.getTextInputDefault()](../../com.aspose.words/formfield\#getTextInputDefault--) / [FormField.setTextInputDefault(java.lang.String)](../../com.aspose.words/formfield\#setTextInputDefault-java.lang.String-)财产。

### CURRENT_DATE {#CURRENT-DATE}
```
public static int CURRENT_DATE
```


文本表单字段值是字段更新时的当前日期。

### CURRENT_TIME {#CURRENT-TIME}
```
public static int CURRENT_TIME
```


文本表单字段值是字段更新的当前时间。

### DATE {#DATE}
```
public static int DATE
```


文本表单域只能包含一个有效的日期值。

### NUMBER {#NUMBER}
```
public static int NUMBER
```


文本表单域只能包含数字。

### REGULAR {#REGULAR}
```
public static int REGULAR
```


文本表单域可以包含任何文本。

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
### fromName(String textFormFieldTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String textFormFieldTypeName)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| textFormFieldTypeName | java.lang.String |  |

**退货：**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getName(int textFormFieldType) {#getName-int-}
```
public static String getName(int textFormFieldType)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| textFormFieldType | int |  |

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
### toString(int textFormFieldType) {#toString-int-}
```
public static String toString(int textFormFieldType)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| textFormFieldType | int |  |

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
