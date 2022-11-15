---
title: ReportingEngine
second_title: Aspose.Words for Java API 参考
description: 提供用数据填充模板文档的例程和一组控制这些例程的设置。
type: docs
weight: 478
url: /zh/java/com.aspose.words/reportingengine/
---

**遗产:**
java.lang.Object
```
public class ReportingEngine
```

提供用数据填充模板文档的例程和一组控制这些例程的设置。

要了解更多信息，请访问**LINQ Reporting Engine**文档文章。
## 构造函数

| 构造函数 | 描述 |
| --- | --- |
| [ReportingEngine()](#ReportingEngine--) | 初始化此类的新实例。 |
## 方法

| 方法 | 描述 |
| --- | --- |
| [buildReport(Document document, Object dataSource)](#buildReport-com.aspose.words.Document-java.lang.Object-) | 使用来自指定源的数据填充指定的模板文档，使其成为现成的报告。 |
| [buildReport(Document document, Object dataSource, String dataSourceName)](#buildReport-com.aspose.words.Document-java.lang.Object-java.lang.String-) | 使用来自指定源的数据填充指定的模板文档，使其成为现成的报告。 |
| [buildReport(Document document, Object[] dataSources, String[] dataSourceNames)](#buildReport-com.aspose.words.Document-java.lang.Object---java.lang.String---) | 使用来自指定源的数据填充指定的模板文档，使其成为现成的报告。 |
| [equals(Object obj)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getKnownTypes()](#getKnownTypes--) | 获取无序集（即 |
| [getOptions()](#getOptions--) | 获取一组控制此行为的标志[ReportingEngine](../../com.aspose.words/reportingengine)构建报告时的实例。 |
| [getUseReflectionOptimization()](#getUseReflectionOptimization--) | 获取一个值，该值指示通过反射 API 执行的自定义类型成员的调用是否使用动态类生成进行了优化。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setOptions(int value)](#setOptions-int-) | 设置一组控制此行为的标志[ReportingEngine](../../com.aspose.words/reportingengine)构建报告时的实例。 |
| [setUseReflectionOptimization(boolean value)](#setUseReflectionOptimization-boolean-) | 设置一个值，指示是否使用动态类生成优化通过反射 API 执行的自定义类型成员的调用。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### ReportingEngine() {#ReportingEngine--}
```
public ReportingEngine()
```


初始化此类的新实例。

### buildReport(Document document, Object dataSource) {#buildReport-com.aspose.words.Document-java.lang.Object-}
```
public boolean buildReport(Document document, Object dataSource)
```


使用来自指定源的数据填充指定的模板文档，使其成为现成的报告。

使用此重载，您可以在模板文档中引用数据源的成员，但不能引用数据源对象本身。你应该使用[buildReport(com.aspose.words.Document, java.lang.Object, java.lang.String)](../../com.aspose.words/reportingengine\#buildReport-com.aspose.words.Document--java.lang.Object--java.lang.String-)超载来实现这一点。

数据源对象可以是以下类型之一：

 *  [XmlDataSource](../../com.aspose.words/xmldatasource)
 *  [JsonDataSource](../../com.aspose.words/jsondatasource)
 *  [CsvDataSource](../../com.aspose.words/csvdatasource)
 *  [DataSet](../../com.aspose.words.net.system.data/dataset)
 *  [DataTable](../../com.aspose.words.net.system.data/datatable)
 *  [DataRow](../../com.aspose.words.net.system.data/datarow)
 *  [IDataReader](../../com.aspose.words.net.system.data/idatareader)
 *  [IDataRecord](../../com.aspose.words.net.system.data/idatarecord)
 *  [DataView](../../com.aspose.words.net.system.data/dataview)
 *  [DataRowView](../../com.aspose.words.net.system.data/datarowview)
 *  任何其他任意 Java 类型

有关如何在模板文档中使用不同类型的数据源的信息，请参阅模板语法参考 (https://docs.aspose.com/display/wordsjava/Template+Syntax)。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document) | 要填充数据的模板文档。 |
| dataSource | java.lang.Object | 数据源对象。 |

**退货:**
boolean - 指示模板文档解析是否成功的标志。返回的标志只有在[getOptions()](../../com.aspose.words/reportingengine\#getOptions--) / [setOptions(int)](../../com.aspose.words/reportingengine\#setOptions-int-)财产包括[ReportBuildOptions.INLINE\_ERROR\_MESSAGES](../../com.aspose.words/reportbuildoptions\#INLINE-ERROR-MESSAGES)选项。
### buildReport(Document document, Object dataSource, String dataSourceName) {#buildReport-com.aspose.words.Document-java.lang.Object-java.lang.String-}
```
public boolean buildReport(Document document, Object dataSource, String dataSourceName)
```


使用来自指定源的数据填充指定的模板文档，使其成为现成的报告。

使用此重载，您可以在模板中引用数据源的成员和数据源对象本身。如果您不打算引用数据源对象本身，则可以省略传递 null 的 dataSourceName 或使用[buildReport(com.aspose.words.Document, java.lang.Object)](../../com.aspose.words/reportingengine\#buildReport-com.aspose.words.Document--java.lang.Object-)超载。

数据源对象可以是以下类型之一：

 *  [XmlDataSource](../../com.aspose.words/xmldatasource)
 *  [JsonDataSource](../../com.aspose.words/jsondatasource)
 *  [CsvDataSource](../../com.aspose.words/csvdatasource)
 *  [DataSet](../../com.aspose.words.net.system.data/dataset)
 *  [DataTable](../../com.aspose.words.net.system.data/datatable)
 *  [DataRow](../../com.aspose.words.net.system.data/datarow)
 *  [IDataReader](../../com.aspose.words.net.system.data/idatareader)
 *  [IDataRecord](../../com.aspose.words.net.system.data/idatarecord)
 *  [DataView](../../com.aspose.words.net.system.data/dataview)
 *  [DataRowView](../../com.aspose.words.net.system.data/datarowview)
 *  任何其他任意 Java 类型

有关如何在模板文档中使用不同类型的数据源的信息，请参阅模板语法参考 (https://docs.aspose.com/display/wordsjava/Template+Syntax)。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document) | 要填充数据的模板文档。 |
| dataSource | java.lang.Object | 数据源对象。 |
| dataSourceName | java.lang.String | 引用模板中数据源对象的名称。 |

**退货:**
boolean - 指示模板文档解析是否成功的标志。返回的标志只有在[getOptions()](../../com.aspose.words/reportingengine\#getOptions--) / [setOptions(int)](../../com.aspose.words/reportingengine\#setOptions-int-)财产包括[ReportBuildOptions.INLINE\_ERROR\_MESSAGES](../../com.aspose.words/reportbuildoptions\#INLINE-ERROR-MESSAGES)选项。
### buildReport(Document document, Object[] dataSources, String[] dataSourceNames) {#buildReport-com.aspose.words.Document-java.lang.Object---java.lang.String---}
```
public boolean buildReport(Document document, Object[] dataSources, String[] dataSourceNames)
```


使用来自指定源的数据填充指定的模板文档，使其成为现成的报告。

使用此重载，您可以在模板中引用多个数据源对象及其成员。如果您要引用数据源的成员而不是数据源对象本身，则可以省略第一个数据源的名称（即为空字符串或 null）。其他数据源的名称必须指定且唯一。

如果要使用单个数据源，请考虑使用[buildReport(com.aspose.words.Document, java.lang.Object)](../../com.aspose.words/reportingengine\#buildReport-com.aspose.words.Document--java.lang.Object-)和[buildReport(com.aspose.words.Document, java.lang.Object, java.lang.String)](../../com.aspose.words/reportingengine\#buildReport-com.aspose.words.Document--java.lang.Object--java.lang.String-)而是重载。

数据源对象可以是以下类型之一：

 *  [XmlDataSource](../../com.aspose.words/xmldatasource)
 *  [JsonDataSource](../../com.aspose.words/jsondatasource)
 *  [CsvDataSource](../../com.aspose.words/csvdatasource)
 *  [DataSet](../../com.aspose.words.net.system.data/dataset)
 *  [DataTable](../../com.aspose.words.net.system.data/datatable)
 *  [DataRow](../../com.aspose.words.net.system.data/datarow)
 *  [IDataReader](../../com.aspose.words.net.system.data/idatareader)
 *  [IDataRecord](../../com.aspose.words.net.system.data/idatarecord)
 *  [DataView](../../com.aspose.words.net.system.data/dataview)
 *  [DataRowView](../../com.aspose.words.net.system.data/datarowview)
 *  任何其他任意 Java 类型

有关如何在模板文档中使用不同类型的数据源的信息，请参阅模板语法参考 (https://docs.aspose.com/display/wordsjava/Template+Syntax)。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document) | 要填充数据的模板文档。 |
| dataSources | java.lang.Object[] | 一组数据源对象。 |
| dataSourceNames | java.lang.String[] | 引用模板中数据源对象的名称数组。 |

**退货:**
boolean - 指示模板文档解析是否成功的标志。返回的标志只有在[getOptions()](../../com.aspose.words/reportingengine\#getOptions--) / [setOptions(int)](../../com.aspose.words/reportingengine\#setOptions-int-)财产包括[ReportBuildOptions.INLINE\_ERROR\_MESSAGES](../../com.aspose.words/reportbuildoptions\#INLINE-ERROR-MESSAGES)选项。
### equals(Object obj) {#equals-java.lang.Object-}
```
public boolean equals(Object obj)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| obj | java.lang.Object |  |

**退货:**
布尔值
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货:**
java.lang.Class<?>
### getKnownTypes() {#getKnownTypes--}
```
public KnownTypeSet getKnownTypes()
```


获取包含 java.lang.Class 对象的无序集（即唯一项的集合），这些对象的完全或部分限定名称可在此引擎实例处理的报告模板中使用，以调用相应类型的静态成员、执行类型转换等.

**退货:**
[KnownTypeSet](../../com.aspose.words/knowntypeset) - 一个无序集（即
### getOptions() {#getOptions--}
```
public int getOptions()
```


获取一组控制此行为的标志[ReportingEngine](../../com.aspose.words/reportingengine)构建报告时的实例。

**退货:**
int - 一组控制 this 行为的标志[ReportingEngine](../../com.aspose.words/reportingengine)构建报告时的实例。返回值是按位组合[ReportBuildOptions](../../com.aspose.words/reportbuildoptions)常数。
### getUseReflectionOptimization() {#getUseReflectionOptimization--}
```
public static boolean getUseReflectionOptimization()
```


获取一个值，该值指示通过反射 API 执行的自定义类型成员的调用是否使用动态类生成进行了优化。默认值是true。在某些情况下，最好禁用此优化。例如，如果您一直在处理小型数据项集合，那么动态类生成的开销可能比直接反射 API 调用的开销更明显。在 iOS 上运行且未使用反射优化时，该选项无效。

**退货:**
boolean - 一个值，指示通过反射 API 执行的自定义类型成员的调用是否使用动态类生成进行了优化。
### hashCode() {#hashCode--}
```
public int hashCode()
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




### setOptions(int value) {#setOptions-int-}
```
public void setOptions(int value)
```


设置一组控制此行为的标志[ReportingEngine](../../com.aspose.words/reportingengine)构建报告时的实例。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 一组控制此行为的标志[ReportingEngine](../../com.aspose.words/reportingengine)构建报告时的实例。该值必须是按位组合的[ReportBuildOptions](../../com.aspose.words/reportbuildoptions)常数。 |

### setUseReflectionOptimization(boolean value) {#setUseReflectionOptimization-boolean-}
```
public static void setUseReflectionOptimization(boolean value)
```


设置一个值，该值指示通过反射 API 执行的自定义类型成员的调用是否使用动态类生成进行了优化。默认值是true。在某些情况下，最好禁用此优化。例如，如果您一直在处理小型数据项集合，那么动态类生成的开销可能比直接反射 API 调用的开销更明显。该选项在 iOS 上运行且不使用反射优化时无效。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个值，指示是否使用动态类生成优化通过反射 API 执行的自定义类型成员的调用。 |

### toString() {#toString--}
```
public String toString()
```




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
