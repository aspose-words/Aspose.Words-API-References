---
title: JsonDataSource
second_title: Aspose.Words for Java API 参考
description: 提供对要在报告中使用的 JSON 文件或流的数据的访问。
type: docs
weight: 354
url: /zh/java/com.aspose.words/jsondatasource/
---

**遗产：**
java.lang.Object
```
public class JsonDataSource
```

提供对要在报告中使用的 JSON 文件或流的数据的访问。

要了解更多信息，请访问**LINQ Reporting Engine**文档文章。

要在生成报告时访问相应文件或流的数据，请将此类的实例作为数据源传递给其中一个[ReportingEngine](../../com.aspose.words/reportingengine)buildReport 重载。

在模板文档中，如果顶级 JSON 元素是数组，则[JsonDataSource](../../com.aspose.words/jsondatasource)实例的处理方式应与它是[DataTable](../../com.aspose.words.net.system.data/datatable)实例。如果顶级 JSON 元素是对象，则[JsonDataSource](../../com.aspose.words/jsondatasource)实例的处理方式应与它是[DataRow](../../com.aspose.words.net.system.data/datarow)实例。有关详细信息，请参阅模板语法参考 (https://docs.aspose.com/display/wordsjava/Template+Syntax)。

在模板文档中，您可以使用 JSON 元素的类型化值。为方便起见，引擎将一组 JSON 简单类型替换为以下类型：

 *  
 *  
 *  
 *  
 *  

引擎根据 JSON 表示自动识别额外类型的值。

要覆盖 JSON 数据加载的默认行为，初始化并传递一个[JsonDataLoadOptions](../../com.aspose.words/jsondataloadoptions)实例到此类的构造函数。
## 构造器

| 构造函数 | 描述 |
| --- | --- |
| [JsonDataSource(String jsonPath)](#JsonDataSource-java.lang.String-) | 使用用于解析 JSON 数据的默认选项，使用 JSON 文件中的数据创建新数据源。 |
| [JsonDataSource(InputStream jsonStream)](#JsonDataSource-java.io.InputStream-) | 初始化此类的新实例。 |
| [JsonDataSource(String jsonPath, JsonDataLoadOptions options)](#JsonDataSource-java.lang.String-com.aspose.words.JsonDataLoadOptions-) | 使用用于解析 JSON 数据的指定选项，使用来自 JSON 文件的数据创建新数据源。 |
| [JsonDataSource(InputStream jsonStream, JsonDataLoadOptions options)](#JsonDataSource-java.io.InputStream-com.aspose.words.JsonDataLoadOptions-) | 初始化此类的新实例。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### JsonDataSource(String jsonPath) {#JsonDataSource-java.lang.String-}
```
public JsonDataSource(String jsonPath)
```


使用用于解析 JSON 数据的默认选项，使用 JSON 文件中的数据创建新数据源。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| jsonPath | java.lang.String | 用作数据源的 JSON 文件的路径。 |

### JsonDataSource(InputStream jsonStream) {#JsonDataSource-java.io.InputStream-}
```
public JsonDataSource(InputStream jsonStream)
```


初始化此类的新实例。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| jsonStream | java.io.InputStream |  |

### JsonDataSource(String jsonPath, JsonDataLoadOptions options) {#JsonDataSource-java.lang.String-com.aspose.words.JsonDataLoadOptions-}
```
public JsonDataSource(String jsonPath, JsonDataLoadOptions options)
```


使用用于解析 JSON 数据的指定选项，使用来自 JSON 文件的数据创建新数据源。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| jsonPath | java.lang.String | 用作数据源的 JSON 文件的路径。 |
| options | [JsonDataLoadOptions](../../com.aspose.words/jsondataloadoptions) | 解析 JSON 数据的选项。 |

### JsonDataSource(InputStream jsonStream, JsonDataLoadOptions options) {#JsonDataSource-java.io.InputStream-com.aspose.words.JsonDataLoadOptions-}
```
public JsonDataSource(InputStream jsonStream, JsonDataLoadOptions options)
```


初始化此类的新实例。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| jsonStream | java.io.InputStream |  |
| options | [JsonDataLoadOptions](../../com.aspose.words/jsondataloadoptions) |  |

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
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
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
