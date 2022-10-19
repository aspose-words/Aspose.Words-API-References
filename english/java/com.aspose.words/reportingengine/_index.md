---
title: ReportingEngine
second_title: Aspose.Words for Java API Reference
description: Provides routines to populate template documents with data and a set of settings to control these routines.
type: docs
weight: 478
url: /java/com.aspose.words/reportingengine/
---

**Inheritance:**
java.lang.Object
```
public class ReportingEngine
```

Provides routines to populate template documents with data and a set of settings to control these routines.

To learn more, visit the **LINQ Reporting Engine** documentation article.
## Constructors

| Constructor | Description |
| --- | --- |
| [ReportingEngine()](#ReportingEngine--) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [buildReport(Document document, Object dataSource)](#buildReport-com.aspose.words.Document-java.lang.Object-) | Populates the specified template document with data from the specified source making it a ready report. |
| [buildReport(Document document, Object dataSource, String dataSourceName)](#buildReport-com.aspose.words.Document-java.lang.Object-java.lang.String-) | Populates the specified template document with data from the specified source making it a ready report. |
| [buildReport(Document document, Object[] dataSources, String[] dataSourceNames)](#buildReport-com.aspose.words.Document-java.lang.Object---java.lang.String---) | Populates the specified template document with data from the specified sources making it a ready report. |
| [hashCode()](#hashCode--) |  |
| [equals(Object obj)](#equals-java.lang.Object-) |  |
| [getOptions()](#getOptions--) | Gets a set of flags controlling behavior of this [ReportingEngine](../../com.aspose.words/reportingengine) instance while building a report. |
| [setOptions(int value)](#setOptions-int-) | Sets a set of flags controlling behavior of this [ReportingEngine](../../com.aspose.words/reportingengine) instance while building a report. |
| [getKnownTypes()](#getKnownTypes--) | Gets an unordered set (i.e. |
| [getUseReflectionOptimization()](#getUseReflectionOptimization--) | Gets a value indicating whether invocations of custom type members performed via reflection API are optimized using dynamic class generation or not. |
| [setUseReflectionOptimization(boolean value)](#setUseReflectionOptimization-boolean-) | Sets a value indicating whether invocations of custom type members performed via reflection API are optimized using dynamic class generation or not. |
### ReportingEngine() {#ReportingEngine--}
```
public ReportingEngine()
```


Initializes a new instance of this class.

### buildReport(Document document, Object dataSource) {#buildReport-com.aspose.words.Document-java.lang.Object-}
```
public boolean buildReport(Document document, Object dataSource)
```


Populates the specified template document with data from the specified source making it a ready report.

Using this overload you can reference the data source's members in the template document, but you cannot reference the data source object itself. You should use the [buildReport(com.aspose.words.Document, java.lang.Object, java.lang.String)](../../com.aspose.words/reportingengine\#buildReport-com.aspose.words.Document--java.lang.Object--java.lang.String-) overload to achieve this.

A data source object can be of one of the following types:

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
 *  Any other arbitrary Java type

For information on how to work with data sources of different types in template documents, see template syntax reference(https://docs.aspose.com/display/wordsjava/Template+Syntax).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document) | A template document to be populated with data. |
| dataSource | java.lang.Object | A data source object. |

**Returns:**
boolean - A flag indicating whether parsing of the template document was successful. The returned flag makes sense only if a value of the [getOptions()](../../com.aspose.words/reportingengine\#getOptions--) / [setOptions(int)](../../com.aspose.words/reportingengine\#setOptions-int-) property includes the [ReportBuildOptions.INLINE\_ERROR\_MESSAGES](../../com.aspose.words/reportbuildoptions\#INLINE-ERROR-MESSAGES) option.
### buildReport(Document document, Object dataSource, String dataSourceName) {#buildReport-com.aspose.words.Document-java.lang.Object-java.lang.String-}
```
public boolean buildReport(Document document, Object dataSource, String dataSourceName)
```


Populates the specified template document with data from the specified source making it a ready report.

Using this overload you can reference the data source's members and the data source object itself in the template. If you are not going to reference the data source object itself, you can omit  dataSourceName  passing null or use the [buildReport(com.aspose.words.Document, java.lang.Object)](../../com.aspose.words/reportingengine\#buildReport-com.aspose.words.Document--java.lang.Object-) overload.

A data source object can be of one of the following types:

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
 *  Any other arbitrary Java type

For information on how to work with data sources of different types in template documents, see template syntax reference(https://docs.aspose.com/display/wordsjava/Template+Syntax).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document) | A template document to be populated with data. |
| dataSource | java.lang.Object | A data source object. |
| dataSourceName | java.lang.String | A name to reference the data source object in the template. |

**Returns:**
boolean - A flag indicating whether parsing of the template document was successful. The returned flag makes sense only if a value of the [getOptions()](../../com.aspose.words/reportingengine\#getOptions--) / [setOptions(int)](../../com.aspose.words/reportingengine\#setOptions-int-) property includes the [ReportBuildOptions.INLINE\_ERROR\_MESSAGES](../../com.aspose.words/reportbuildoptions\#INLINE-ERROR-MESSAGES) option.
### buildReport(Document document, Object[] dataSources, String[] dataSourceNames) {#buildReport-com.aspose.words.Document-java.lang.Object---java.lang.String---}
```
public boolean buildReport(Document document, Object[] dataSources, String[] dataSourceNames)
```


Populates the specified template document with data from the specified sources making it a ready report.

Using this overload you can reference multiple data source objects and their members in the template. The name of the first data source can be omitted (i.e. be an empty string or null) if you are going to reference the data source's members but not the data source object itself. Names of the other data sources must be specified and unique.

If you are going to use a single data source, consider using of [buildReport(com.aspose.words.Document, java.lang.Object)](../../com.aspose.words/reportingengine\#buildReport-com.aspose.words.Document--java.lang.Object-) and [buildReport(com.aspose.words.Document, java.lang.Object, java.lang.String)](../../com.aspose.words/reportingengine\#buildReport-com.aspose.words.Document--java.lang.Object--java.lang.String-) overloads instead.

A data source object can be of one of the following types:

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
 *  Any other arbitrary Java type

For information on how to work with data sources of different types in template documents, see template syntax reference(https://docs.aspose.com/display/wordsjava/Template+Syntax).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document) | A template document to be populated with data. |
| dataSources | java.lang.Object[] | An array of data source objects. |
| dataSourceNames | java.lang.String[] | An array of names to reference the data source objects within the template. |

**Returns:**
boolean - A flag indicating whether parsing of the template document was successful. The returned flag makes sense only if a value of the [getOptions()](../../com.aspose.words/reportingengine\#getOptions--) / [setOptions(int)](../../com.aspose.words/reportingengine\#setOptions-int-) property includes the [ReportBuildOptions.INLINE\_ERROR\_MESSAGES](../../com.aspose.words/reportbuildoptions\#INLINE-ERROR-MESSAGES) option.
### hashCode() {#hashCode--}
```
public int hashCode()
```




**Returns:**
int
### equals(Object obj) {#equals-java.lang.Object-}
```
public boolean equals(Object obj)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getOptions() {#getOptions--}
```
public int getOptions()
```


Gets a set of flags controlling behavior of this [ReportingEngine](../../com.aspose.words/reportingengine) instance while building a report.

**Returns:**
int - A set of flags controlling behavior of this [ReportingEngine](../../com.aspose.words/reportingengine) instance while building a report. The returned value is a bitwise combination of [ReportBuildOptions](../../com.aspose.words/reportbuildoptions) constants.
### setOptions(int value) {#setOptions-int-}
```
public void setOptions(int value)
```


Sets a set of flags controlling behavior of this [ReportingEngine](../../com.aspose.words/reportingengine) instance while building a report.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A set of flags controlling behavior of this [ReportingEngine](../../com.aspose.words/reportingengine) instance while building a report. The value must be a bitwise combination of [ReportBuildOptions](../../com.aspose.words/reportbuildoptions) constants. |

### getKnownTypes() {#getKnownTypes--}
```
public KnownTypeSet getKnownTypes()
```


Gets an unordered set (i.e. a collection of unique items) containing java.lang.Class objects which fully or partially qualified names can be used within report templates processed by this engine instance to invoke the corresponding types' static members, perform type casts, etc.

**Returns:**
[KnownTypeSet](../../com.aspose.words/knowntypeset) - An unordered set (i.e.
### getUseReflectionOptimization() {#getUseReflectionOptimization--}
```
public static boolean getUseReflectionOptimization()
```


Gets a value indicating whether invocations of custom type members performed via reflection API are optimized using dynamic class generation or not. The default value is true. There are some scenarios where it is preferrable to disable this optimization. For example, if you are dealing with small collections of data items all the time, then an overhead of dynamic class generation can be more noticeable than an overhead of direct reflection API calls. The option does not have effect when run on iOS and reflection optimization is not used.

**Returns:**
boolean - A value indicating whether invocations of custom type members performed via reflection API are optimized using dynamic class generation or not.
### setUseReflectionOptimization(boolean value) {#setUseReflectionOptimization-boolean-}
```
public static void setUseReflectionOptimization(boolean value)
```


Sets a value indicating whether invocations of custom type members performed via reflection API are optimized using dynamic class generation or not. The default value is true. There are some scenarios where it is preferrable to disable this optimization. For example, if you are dealing with small collections of data items all the time, then an overhead of dynamic class generation can be more noticeable than an overhead of direct reflection API calls. The option does not have effect when run on iOS and reflection optimization is not used.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether invocations of custom type members performed via reflection API are optimized using dynamic class generation or not. |
