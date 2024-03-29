---
title: JsonSimpleValueParseMode
second_title: Aspose.Words for Java API 参考
description: 指定在加载 JSON 时解析 JSON 简单值空布尔数字整数和字符串的模式。
type: docs
weight: 355
url: /zh/java/com.aspose.words/jsonsimplevalueparsemode/
---

**遗产：**
java.lang.Object
```
public class JsonSimpleValueParseMode
```

指定在加载 JSON 时解析 JSON 简单值（空值、布尔值、数字、整数和字符串）的模式。这种模式不会影响日期时间值的解析。
## 字段

| 场地 | 描述 |
| --- | --- |
| [LOOSE](#LOOSE) | 指定在解析其字符串表示时确定 JSON 简单值类型的模式。 |
| [STRICT](#STRICT) | 指定从 JSON 表示法本身确定 JSON 简单值类型的模式。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String jsonSimpleValueParseModeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int jsonSimpleValueParseMode)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int jsonSimpleValueParseMode)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### LOOSE {#LOOSE}
```
public static int LOOSE
```


指定在解析其字符串表示时确定 JSON 简单值类型的模式。例如，JSON 片段中的“道具”类型“\ { 道具：“123”\}' 在此模式下被确定为整数。

### STRICT {#STRICT}
```
public static int STRICT
```


指定从 JSON 表示法本身确定 JSON 简单值类型的模式。例如，JSON 片段中的“道具”类型“\ { 道具：“123”\}' 在此模式下被确定为字符串。

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
### fromName(String jsonSimpleValueParseModeName) {#fromName-java.lang.String-}
```
public static int fromName(String jsonSimpleValueParseModeName)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| jsonSimpleValueParseModeName | java.lang.String |  |

**退货：**
整数
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getName(int jsonSimpleValueParseMode) {#getName-int-}
```
public static String getName(int jsonSimpleValueParseMode)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| jsonSimpleValueParseMode | int |  |

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
### toString(int jsonSimpleValueParseMode) {#toString-int-}
```
public static String toString(int jsonSimpleValueParseMode)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| jsonSimpleValueParseMode | int |  |

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
