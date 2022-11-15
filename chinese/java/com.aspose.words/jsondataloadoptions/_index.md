---
title: JsonDataLoadOptions
second_title: Aspose.Words for Java API 参考
description: 表示解析 JSON 数据的选项。
type: docs
weight: 353
url: /zh/java/com.aspose.words/jsondataloadoptions/
---

**遗产：**
java.lang.Object
```
public class JsonDataLoadOptions
```

表示解析 JSON 数据的选项。

要了解更多信息，请访问**LINQ Reporting Engine**文档文章。

此类的实例可以传递给的构造函数[JsonDataSource](../../com.aspose.words/jsondatasource).
## 构造器

| 构造函数 | 描述 |
| --- | --- |
| [JsonDataLoadOptions()](#JsonDataLoadOptions--) | 使用默认选项初始化此类的新实例。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getAlwaysGenerateRootObject()](#getAlwaysGenerateRootObject--) | 获取一个标志，该标志指示生成的数据源是否将始终包含 JSON 根元素的对象。 |
| [getClass()](#getClass--) |  |
| [getExactDateTimeParseFormat()](#getExactDateTimeParseFormat--) | 获取在加载 JSON 时解析 JSON 日期时间值的准确格式。 |
| [getExactDateTimeParseFormats()](#getExactDateTimeParseFormats--) | 获取在加载 JSON 时解析 JSON 日期时间值的准确格式。 |
| [getSimpleValueParseMode()](#getSimpleValueParseMode--) | 获取在加载 JSON 时解析 JSON 简单值（空值、布尔值、数字、整数和字符串）的模式。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setAlwaysGenerateRootObject(boolean value)](#setAlwaysGenerateRootObject-boolean-) | 设置一个标志，指示生成的数据源是否始终包含 JSON 根元素的对象。 |
| [setExactDateTimeParseFormat(String value)](#setExactDateTimeParseFormat-java.lang.String-) | 设置在加载 JSON 时解析 JSON 日期时间值的确切格式。 |
| [setExactDateTimeParseFormats(Iterable value)](#setExactDateTimeParseFormats-java.lang.Iterable-) | 设置加载 JSON 时解析 JSON 日期时间值的准确格式。 |
| [setSimpleValueParseMode(int value)](#setSimpleValueParseMode-int-) | 设置在加载 JSON 时解析 JSON 简单值（空值、布尔值、数字、整数和字符串）的模式。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### JsonDataLoadOptions() {#JsonDataLoadOptions--}
```
public JsonDataLoadOptions()
```


使用默认选项初始化此类的新实例。

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
### getAlwaysGenerateRootObject() {#getAlwaysGenerateRootObject--}
```
public boolean getAlwaysGenerateRootObject()
```


获取一个标志，该标志指示生成的数据源是否将始终包含 JSON 根元素的对象。如果 JSON 根元素包含单个复杂属性，则默认情况下不会创建此类对象。默认值为**false**.

**退货：**
boolean - 一个标志，指示生成的数据源是否将始终包含 JSON 根元素的对象。
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getExactDateTimeParseFormat() {#getExactDateTimeParseFormat--}
```
public String getExactDateTimeParseFormat()
```


获取在加载 JSON 时解析 JSON 日期时间值的准确格式。默认是**null**.

无论此属性的值如何，使用 Microsoft. JSON 日期时间格式（例如，“/Date(1224043200000)/”）编码的字符串始终被识别为日期时间值。该属性定义了以下列方式从字符串中解析日期时间值时要使用的其他格式：

 *  什么时候[getExactDateTimeParseFormat()](../../com.aspose.words/jsondataloadoptions\#getExactDateTimeParseFormat--) / [setExactDateTimeParseFormat(java.lang.String)](../../com.aspose.words/jsondataloadoptions\#setExactDateTimeParseFormat-java.lang.String-)是**null**, ISO-8601 格式和当前、美国英语和新西兰英语文化支持的所有日期时间格式在上述顺序中额外使用。
 *  什么时候[getExactDateTimeParseFormat()](../../com.aspose.words/jsondataloadoptions\#getExactDateTimeParseFormat--) / [setExactDateTimeParseFormat(java.lang.String)](../../com.aspose.words/jsondataloadoptions\#setExactDateTimeParseFormat-java.lang.String-)是一个非空字符串，它被用作利用当前文化的单个附加日期时间格式。
 *  什么时候[getExactDateTimeParseFormat()](../../com.aspose.words/jsondataloadoptions\#getExactDateTimeParseFormat--) / [setExactDateTimeParseFormat(java.lang.String)](../../com.aspose.words/jsondataloadoptions\#setExactDateTimeParseFormat-java.lang.String-)是空字符串，不使用其他日期时间格式。

**退货：**
java.lang.String - 加载 JSON 时解析 JSON 日期时间值的精确格式。
### getExactDateTimeParseFormats() {#getExactDateTimeParseFormats--}
```
public Iterable getExactDateTimeParseFormats()
```


获取在加载 JSON 时解析 JSON 日期时间值的准确格式。默认是**null**.

无论此属性的值如何，使用 Microsoft. JSON 日期时间格式（例如，“/Date(1224043200000)/”）编码的字符串始终被识别为日期时间值。该属性定义了以下列方式从字符串中解析日期时间值时要使用的其他格式：

 *  什么时候[getExactDateTimeParseFormats()](../../com.aspose.words/jsondataloadoptions\#getExactDateTimeParseFormats--) / [setExactDateTimeParseFormats(java.lang.Iterable)](../../com.aspose.words/jsondataloadoptions\#setExactDateTimeParseFormats-java.lang.Iterable-)是**null**, ISO-8601 格式和当前、美国英语和新西兰英语文化支持的所有日期时间格式在上述顺序中额外使用。
 *  什么时候[getExactDateTimeParseFormats()](../../com.aspose.words/jsondataloadoptions\#getExactDateTimeParseFormats--) / [setExactDateTimeParseFormats(java.lang.Iterable)](../../com.aspose.words/jsondataloadoptions\#setExactDateTimeParseFormats-java.lang.Iterable-)包含字符串，它们被用作利用当前文化的附加日期时间格式。
 *  什么时候[getExactDateTimeParseFormats()](../../com.aspose.words/jsondataloadoptions\#getExactDateTimeParseFormats--) / [setExactDateTimeParseFormats(java.lang.Iterable)](../../com.aspose.words/jsondataloadoptions\#setExactDateTimeParseFormats-java.lang.Iterable-)为空，则不使用其他日期时间格式。

**退货：**
java.lang.Iterable - 在加载 JSON 时解析 JSON 日期时间值的精确格式。
### getSimpleValueParseMode() {#getSimpleValueParseMode--}
```
public int getSimpleValueParseMode()
```


获取在加载 JSON 时解析 JSON 简单值（空值、布尔值、数字、整数和字符串）的模式。这种模式不会影响日期时间值的解析。默认是[JsonSimpleValueParseMode.LOOSE](../../com.aspose.words/jsonsimplevalueparsemode\#LOOSE).

**退货：**
int - 一种在加载 JSON 时解析 JSON 简单值（空值、布尔值、数字、整数和字符串）的模式。返回值是其中之一[JsonSimpleValueParseMode](../../com.aspose.words/jsonsimplevalueparsemode)常数。
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




### setAlwaysGenerateRootObject(boolean value) {#setAlwaysGenerateRootObject-boolean-}
```
public void setAlwaysGenerateRootObject(boolean value)
```


设置一个标志，指示生成的数据源是否始终包含 JSON 根元素的对象。如果 JSON 根元素包含单个复杂属性，则默认情况下不会创建此类对象。默认值为**false**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 指示生成的数据源是否始终包含 JSON 根元素的对象的标志。 |

### setExactDateTimeParseFormat(String value) {#setExactDateTimeParseFormat-java.lang.String-}
```
public void setExactDateTimeParseFormat(String value)
```


设置在加载 JSON 时解析 JSON 日期时间值的确切格式。默认是**null**.

无论此属性的值如何，使用 Microsoft. JSON 日期时间格式（例如，“/Date(1224043200000)/”）编码的字符串始终被识别为日期时间值。该属性定义了以下列方式从字符串中解析日期时间值时要使用的其他格式：

 *  什么时候[getExactDateTimeParseFormat()](../../com.aspose.words/jsondataloadoptions\#getExactDateTimeParseFormat--) / [setExactDateTimeParseFormat(java.lang.String)](../../com.aspose.words/jsondataloadoptions\#setExactDateTimeParseFormat-java.lang.String-)是**null**, ISO-8601 格式和当前、美国英语和新西兰英语文化支持的所有日期时间格式在上述顺序中额外使用。
 *  什么时候[getExactDateTimeParseFormat()](../../com.aspose.words/jsondataloadoptions\#getExactDateTimeParseFormat--) / [setExactDateTimeParseFormat(java.lang.String)](../../com.aspose.words/jsondataloadoptions\#setExactDateTimeParseFormat-java.lang.String-)是一个非空字符串，它被用作利用当前文化的单个附加日期时间格式。
 *  什么时候[getExactDateTimeParseFormat()](../../com.aspose.words/jsondataloadoptions\#getExactDateTimeParseFormat--) / [setExactDateTimeParseFormat(java.lang.String)](../../com.aspose.words/jsondataloadoptions\#setExactDateTimeParseFormat-java.lang.String-)是空字符串，不使用其他日期时间格式。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 加载 JSON 时解析 JSON 日期时间值的精确格式。 |

### setExactDateTimeParseFormats(Iterable value) {#setExactDateTimeParseFormats-java.lang.Iterable-}
```
public void setExactDateTimeParseFormats(Iterable value)
```


设置加载 JSON 时解析 JSON 日期时间值的准确格式。默认是**null**.

无论此属性的值如何，使用 Microsoft. JSON 日期时间格式（例如，“/Date(1224043200000)/”）编码的字符串始终被识别为日期时间值。该属性定义了以下列方式从字符串中解析日期时间值时要使用的其他格式：

 *  什么时候[getExactDateTimeParseFormats()](../../com.aspose.words/jsondataloadoptions\#getExactDateTimeParseFormats--) / [setExactDateTimeParseFormats(java.lang.Iterable)](../../com.aspose.words/jsondataloadoptions\#setExactDateTimeParseFormats-java.lang.Iterable-)是**null**, ISO-8601 格式和当前、美国英语和新西兰英语文化支持的所有日期时间格式在上述顺序中额外使用。
 *  什么时候[getExactDateTimeParseFormats()](../../com.aspose.words/jsondataloadoptions\#getExactDateTimeParseFormats--) / [setExactDateTimeParseFormats(java.lang.Iterable)](../../com.aspose.words/jsondataloadoptions\#setExactDateTimeParseFormats-java.lang.Iterable-)包含字符串，它们被用作利用当前文化的附加日期时间格式。
 *  什么时候[getExactDateTimeParseFormats()](../../com.aspose.words/jsondataloadoptions\#getExactDateTimeParseFormats--) / [setExactDateTimeParseFormats(java.lang.Iterable)](../../com.aspose.words/jsondataloadoptions\#setExactDateTimeParseFormats-java.lang.Iterable-)为空，则不使用其他日期时间格式。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.Iterable | 加载 JSON 时解析 JSON 日期时间值的精确格式。 |

### setSimpleValueParseMode(int value) {#setSimpleValueParseMode-int-}
```
public void setSimpleValueParseMode(int value)
```


设置在加载 JSON 时解析 JSON 简单值（空值、布尔值、数字、整数和字符串）的模式。这种模式不会影响日期时间值的解析。默认是[JsonSimpleValueParseMode.LOOSE](../../com.aspose.words/jsonsimplevalueparsemode\#LOOSE).

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 一种在加载 JSON 时解析 JSON 简单值（空值、布尔值、数字、整数和字符串）的模式。该值必须是其中之一[JsonSimpleValueParseMode](../../com.aspose.words/jsonsimplevalueparsemode)常数。 |

### toString() {#toString--}
```
public String toString()
```




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
