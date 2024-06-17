---
title: ReportingEngine
linktitle: ReportingEngine
second_title: Aspose.Words for Java
description: Provides routines to populate template documents with data and a set of settings to control these routines in Java.
type: docs
weight: 524
url: /java/com.aspose.words/reportingengine/
---

**Inheritance:**
java.lang.Object
```
public class ReportingEngine
```

Provides routines to populate template documents with data and a set of settings to control these routines.

To learn more, visit the [ LINQ Reporting Engine ][LINQ Reporting Engine] documentation article.


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Constructors

| Constructor | Description |
| --- | --- |
| [ReportingEngine()](#ReportingEngine) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [buildReport(Document document, Object dataSource)](#buildReport-com.aspose.words.Document-java.lang.Object) | Populates the specified template document with data from the specified source making it a ready report. |
| [buildReport(Document document, Object dataSource, String dataSourceName)](#buildReport-com.aspose.words.Document-java.lang.Object-java.lang.String) | Populates the specified template document with data from the specified source making it a ready report. |
| [buildReport(Document document, Object[] dataSources, String[] dataSourceNames)](#buildReport-com.aspose.words.Document-java.lang.Object---java.lang.String) | Populates the specified template document with data from the specified sources making it a ready report. |
| [equals(Object obj)](#equals-java.lang.Object) | Determines whether the specified object is equal in value to the current object. |
| [getKnownTypes()](#getKnownTypes) | Gets an unordered set (i.e. |
| [getMissingMemberMessage()](#getMissingMemberMessage) | Gets a string value printed instead of a template expression that represents a plain reference to a missing member of an object. |
| [getOptions()](#getOptions) | Gets a set of flags controlling behavior of this [ReportingEngine](../../com.aspose.words/reportingengine/) instance while building a report. |
| [getRestrictedTypes()](#getRestrictedTypes) | Returns types, which members as well as which derived types' members should be inaccessible by the engine through template syntax. |
| [getUseReflectionOptimization()](#getUseReflectionOptimization) | Gets a value indicating whether invocations of custom type members performed via reflection API are optimized using dynamic class generation or not. |
| [hashCode()](#hashCode) |  |
| [setMissingMemberMessage(String value)](#setMissingMemberMessage-java.lang.String) | Sets a string value printed instead of a template expression that represents a plain reference to a missing member of an object. |
| [setOptions(int value)](#setOptions-int) | Sets a set of flags controlling behavior of this [ReportingEngine](../../com.aspose.words/reportingengine/) instance while building a report. |
| [setRestrictedTypes(Class[] types)](#setRestrictedTypes-java.lang.Class...) | Specifies types, which members as well as which derived types' members should be inaccessible by the engine through template syntax. |
| [setUseReflectionOptimization(boolean value)](#setUseReflectionOptimization-boolean) | Sets a value indicating whether invocations of custom type members performed via reflection API are optimized using dynamic class generation or not. |
### ReportingEngine() {#ReportingEngine}
```
public ReportingEngine()
```


Initializes a new instance of this class.

### buildReport(Document document, Object dataSource) {#buildReport-com.aspose.words.Document-java.lang.Object}
```
public boolean buildReport(Document document, Object dataSource)
```


Populates the specified template document with data from the specified source making it a ready report.

 **Remarks:** 

Using this overload you can reference the data source's members in the template document, but you cannot reference the data source object itself. You should use the [buildReport(com.aspose.words.Document, java.lang.Object, java.lang.String)](../../com.aspose.words/reportingengine/\#buildReport-com.aspose.words.Document--java.lang.Object--java.lang.String) overload to achieve this.

A data source object can be of one of the following types:

 *  [XmlDataSource](../../com.aspose.words/xmldatasource/)
 *  [JsonDataSource](../../com.aspose.words/jsondatasource/)
 *  [CsvDataSource](../../com.aspose.words/csvdatasource/)
 *  [DataSet](../../com.aspose.words.net.system.data/dataset/)
 *  [DataTable](../../com.aspose.words.net.system.data/datatable/)
 *  [DataRow](../../com.aspose.words.net.system.data/datarow/)
 *  [IDataReader](../../com.aspose.words.net.system.data/idatareader/)
 *  [IDataRecord](../../com.aspose.words.net.system.data/idatarecord/)
 *  [DataView](../../com.aspose.words.net.system.data/dataview/)
 *  [DataRowView](../../com.aspose.words.net.system.data/datarowview/)
 *  Any other arbitrary Java type

For information on how to work with data sources of different types in template documents, see template syntax reference(https://docs.aspose.com/display/wordsjava/Template+Syntax).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document/) | A template document to be populated with data. |
| dataSource | java.lang.Object | A data source object. |

**Returns:**
boolean - A flag indicating whether parsing of the template document was successful. The returned flag makes sense only if a value of the [getOptions()](../../com.aspose.words/reportingengine/\#getOptions) / [setOptions(int)](../../com.aspose.words/reportingengine/\#setOptions-int) property includes the [ReportBuildOptions.INLINE\_ERROR\_MESSAGES](../../com.aspose.words/reportbuildoptions/\#INLINE-ERROR-MESSAGES) option.
### buildReport(Document document, Object dataSource, String dataSourceName) {#buildReport-com.aspose.words.Document-java.lang.Object-java.lang.String}
```
public boolean buildReport(Document document, Object dataSource, String dataSourceName)
```


Populates the specified template document with data from the specified source making it a ready report.

 **Remarks:** 

Using this overload you can reference the data source's members and the data source object itself in the template. If you are not going to reference the data source object itself, you can omit  dataSourceName  passing  null  or use the [buildReport(com.aspose.words.Document, java.lang.Object)](../../com.aspose.words/reportingengine/\#buildReport-com.aspose.words.Document--java.lang.Object) overload.

A data source object can be of one of the following types:

 *  [XmlDataSource](../../com.aspose.words/xmldatasource/)
 *  [JsonDataSource](../../com.aspose.words/jsondatasource/)
 *  [CsvDataSource](../../com.aspose.words/csvdatasource/)
 *  [DataSet](../../com.aspose.words.net.system.data/dataset/)
 *  [DataTable](../../com.aspose.words.net.system.data/datatable/)
 *  [DataRow](../../com.aspose.words.net.system.data/datarow/)
 *  [IDataReader](../../com.aspose.words.net.system.data/idatareader/)
 *  [IDataRecord](../../com.aspose.words.net.system.data/idatarecord/)
 *  [DataView](../../com.aspose.words.net.system.data/dataview/)
 *  [DataRowView](../../com.aspose.words.net.system.data/datarowview/)
 *  Any other arbitrary Java type

For information on how to work with data sources of different types in template documents, see template syntax reference(https://docs.aspose.com/display/wordsjava/Template+Syntax).

 **Examples:** 

Shows how to remove paragraphs selectively.

```

 // Template contains tags with an exclamation mark. For such tags, empty paragraphs will be removed.
 Document doc = new Document(getMyDir() + "Reporting engine template - Selective remove paragraphs.docx");

 ReportingEngine engine = new ReportingEngine();
 engine.buildReport(doc, false, "value");

 doc.save(getArtifactsDir() + "ReportingEngine.SelectiveDeletionOfParagraphs.docx");
 
```

Shows how to allow missing members.

```

 DocumentBuilder builder = new DocumentBuilder();
 builder.writeln("<<[missingObject.First().id]>>");
 builder.writeln("<><<[id]>><>");

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS); }
 engine.setMissingMemberMessage("Missed");
 engine.buildReport(builder.getDocument(), new DataSet(), "");
 
```

Shows how to display values as dollar text.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 builder.writeln("<<[ds.getValue1()]:dollarText>>\r<<[ds.getValue2()]:dollarText>>");

 NumericTestClass testData = new NumericTestBuilder().withValues(1234, 5621718.589).build();

 ReportingEngine report = new ReportingEngine();
 report.getKnownTypes().add(NumericTestClass.class);
 report.buildReport(doc, testData, "ds");

 doc.save(getArtifactsDir() + "ReportingEngine.DollarTextFormat.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document/) | A template document to be populated with data. |
| dataSource | java.lang.Object | A data source object. |
| dataSourceName | java.lang.String | A name to reference the data source object in the template. |

**Returns:**
boolean - A flag indicating whether parsing of the template document was successful. The returned flag makes sense only if a value of the [getOptions()](../../com.aspose.words/reportingengine/\#getOptions) / [setOptions(int)](../../com.aspose.words/reportingengine/\#setOptions-int) property includes the [ReportBuildOptions.INLINE\_ERROR\_MESSAGES](../../com.aspose.words/reportbuildoptions/\#INLINE-ERROR-MESSAGES) option.
### buildReport(Document document, Object[] dataSources, String[] dataSourceNames) {#buildReport-com.aspose.words.Document-java.lang.Object---java.lang.String}
```
public boolean buildReport(Document document, Object[] dataSources, String[] dataSourceNames)
```


Populates the specified template document with data from the specified sources making it a ready report.

 **Remarks:** 

Using this overload you can reference multiple data source objects and their members in the template. The name of the first data source can be omitted (i.e. be an empty string or  null ) if you are going to reference the data source's members but not the data source object itself. Names of the other data sources must be specified and unique.

If you are going to use a single data source, consider using of [buildReport(com.aspose.words.Document, java.lang.Object)](../../com.aspose.words/reportingengine/\#buildReport-com.aspose.words.Document--java.lang.Object) and [buildReport(com.aspose.words.Document, java.lang.Object, java.lang.String)](../../com.aspose.words/reportingengine/\#buildReport-com.aspose.words.Document--java.lang.Object--java.lang.String) overloads instead.

A data source object can be of one of the following types:

 *  [XmlDataSource](../../com.aspose.words/xmldatasource/)
 *  [JsonDataSource](../../com.aspose.words/jsondatasource/)
 *  [CsvDataSource](../../com.aspose.words/csvdatasource/)
 *  [DataSet](../../com.aspose.words.net.system.data/dataset/)
 *  [DataTable](../../com.aspose.words.net.system.data/datatable/)
 *  [DataRow](../../com.aspose.words.net.system.data/datarow/)
 *  [IDataReader](../../com.aspose.words.net.system.data/idatareader/)
 *  [IDataRecord](../../com.aspose.words.net.system.data/idatarecord/)
 *  [DataView](../../com.aspose.words.net.system.data/dataview/)
 *  [DataRowView](../../com.aspose.words.net.system.data/datarowview/)
 *  Any other arbitrary Java type

For information on how to work with data sources of different types in template documents, see template syntax reference(https://docs.aspose.com/display/wordsjava/Template+Syntax).

 **Examples:** 

Shows how to work with charts from word 2016.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - Word 2016 Charts (Java).docx");

 ReportingEngine engine = new ReportingEngine();
 engine.buildReport(doc, new Object[] { Common.getShares(), Common.getShareQuotes() },
         new String[] { "shares", "quotes" });

 doc.save(getArtifactsDir() + "ReportingEngine.Word2016Charts.docx");
 
```

Shows how to keep inserted numbering as is.

```

 // By default, numbered lists from a template document are continued when their identifiers match those from a document being inserted.
 // With "-sourceNumbering" numbering should be separated and kept as is.
 Document template = DocumentHelper.createSimpleDocument("<>" + System.lineSeparator() + "<>");

 DocumentTestClass doc = new DocumentTestBuilder()
         .withDocument(new Document(getMyDir() + "List item.docx")).build();

 ReportingEngine engine = new ReportingEngine(); { engine.setOptions(ReportBuildOptions.REMOVE_EMPTY_PARAGRAPHS); }
 engine.buildReport(template, new Object[] { doc }, new String[] { "src" });

 template.save(getArtifactsDir() + "ReportingEngine.SourseListNumbering.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| document | [Document](../../com.aspose.words/document/) | A template document to be populated with data. |
| dataSources | java.lang.Object[] | An array of data source objects. |
| dataSourceNames | java.lang.String[] | An array of names to reference the data source objects within the template. |

**Returns:**
boolean - A flag indicating whether parsing of the template document was successful. The returned flag makes sense only if a value of the [getOptions()](../../com.aspose.words/reportingengine/\#getOptions) / [setOptions(int)](../../com.aspose.words/reportingengine/\#setOptions-int) property includes the [ReportBuildOptions.INLINE\_ERROR\_MESSAGES](../../com.aspose.words/reportbuildoptions/\#INLINE-ERROR-MESSAGES) option.
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Determines whether the specified object is equal in value to the current object.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getKnownTypes() {#getKnownTypes}
```
public KnownTypeSet getKnownTypes()
```


Gets an unordered set (i.e. a collection of unique items) containing java.lang.Class objects which fully or partially qualified names can be used within report templates processed by this engine instance to invoke the corresponding types' static members, perform type casts, etc.

**Returns:**
[KnownTypeSet](../../com.aspose.words/knowntypeset/) - An unordered set (i.e.
### getMissingMemberMessage() {#getMissingMemberMessage}
```
public String getMissingMemberMessage()
```


Gets a string value printed instead of a template expression that represents a plain reference to a missing member of an object. The default value is an empty string.

 **Remarks:** 

The property should be used in conjunction with the [ReportBuildOptions.ALLOW\_MISSING\_MEMBERS](../../com.aspose.words/reportbuildoptions/\#ALLOW-MISSING-MEMBERS) option. Otherwise, an exception is thrown when a missing member of an object is encountered.

The property affects only printing of a template expression representing a plain reference to a missing object member. For example, printing of a binary operator, one of which operands references a missing object member, is not affected.

The value of this property cannot be set to null.

**Returns:**
java.lang.String - A string value printed instead of a template expression that represents a plain reference to a missing member of an object.
### getOptions() {#getOptions}
```
public int getOptions()
```


Gets a set of flags controlling behavior of this [ReportingEngine](../../com.aspose.words/reportingengine/) instance while building a report.

 **Examples:** 

Shows how to set options for Reporting Engine

```

 Document doc = new Document(getMyDir() + "Reporting engine template - Fields (Java).docx");

 // Note that enabling of the option makes the engine to update fields while building a report,
 // so there is no need to update fields separately after that.
 ReportingEngine engine = new ReportingEngine();
 engine.setOptions(ReportBuildOptions.UPDATE_FIELDS_SYNTAX_AWARE);
 engine.buildReport(doc, new String[] { "First topic", "Second topic", "Third topic" }, "topics");

 doc.save(getArtifactsDir() + "ReportingEngine.UpdateFieldsSyntaxAware.docx");
 
```

**Returns:**
int - A set of flags controlling behavior of this [ReportingEngine](../../com.aspose.words/reportingengine/) instance while building a report. The returned value is a bitwise combination of [ReportBuildOptions](../../com.aspose.words/reportbuildoptions/) constants.
### getRestrictedTypes() {#getRestrictedTypes}
```
public static Class[] getRestrictedTypes()
```


Returns types, which members as well as which derived types' members should be inaccessible by the engine through template syntax.

 **Remarks:** 

The returned array contains items previously set using [setRestrictedTypes(java.lang.Class[])](../../com.aspose.words/reportingengine/\#setRestrictedTypes-java.lang.Class).

Changing items of the returned array has no effect on restricted types. To change restricted types, use [setRestrictedTypes(java.lang.Class[])](../../com.aspose.words/reportingengine/\#setRestrictedTypes-java.lang.Class) instead.

**Returns:**
java.lang.Class[] - Types, which members as well as which derived types' members should be inaccessible by the engine through template syntax.
### getUseReflectionOptimization() {#getUseReflectionOptimization}
```
public static boolean getUseReflectionOptimization()
```


Gets a value indicating whether invocations of custom type members performed via reflection API are optimized using dynamic class generation or not. The default value is  true .

 **Remarks:** 

There are some scenarios where it is preferrable to disable this optimization. For example, if you are dealing with small collections of data items all the time, then an overhead of dynamic class generation can be more noticeable than an overhead of direct reflection API calls. The option does not have effect when run on iOS and reflection optimization is not used.

**Returns:**
boolean - A value indicating whether invocations of custom type members performed via reflection API are optimized using dynamic class generation or not.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### setMissingMemberMessage(String value) {#setMissingMemberMessage-java.lang.String}
```
public void setMissingMemberMessage(String value)
```


Sets a string value printed instead of a template expression that represents a plain reference to a missing member of an object. The default value is an empty string.

 **Remarks:** 

The property should be used in conjunction with the [ReportBuildOptions.ALLOW\_MISSING\_MEMBERS](../../com.aspose.words/reportbuildoptions/\#ALLOW-MISSING-MEMBERS) option. Otherwise, an exception is thrown when a missing member of an object is encountered.

The property affects only printing of a template expression representing a plain reference to a missing object member. For example, printing of a binary operator, one of which operands references a missing object member, is not affected.

The value of this property cannot be set to null.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | A string value printed instead of a template expression that represents a plain reference to a missing member of an object. |

### setOptions(int value) {#setOptions-int}
```
public void setOptions(int value)
```


Sets a set of flags controlling behavior of this [ReportingEngine](../../com.aspose.words/reportingengine/) instance while building a report.

 **Examples:** 

Shows how to set options for Reporting Engine

```

 Document doc = new Document(getMyDir() + "Reporting engine template - Fields (Java).docx");

 // Note that enabling of the option makes the engine to update fields while building a report,
 // so there is no need to update fields separately after that.
 ReportingEngine engine = new ReportingEngine();
 engine.setOptions(ReportBuildOptions.UPDATE_FIELDS_SYNTAX_AWARE);
 engine.buildReport(doc, new String[] { "First topic", "Second topic", "Third topic" }, "topics");

 doc.save(getArtifactsDir() + "ReportingEngine.UpdateFieldsSyntaxAware.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | A set of flags controlling behavior of this [ReportingEngine](../../com.aspose.words/reportingengine/) instance while building a report. The value must be a bitwise combination of [ReportBuildOptions](../../com.aspose.words/reportbuildoptions/) constants. |

### setRestrictedTypes(Class[] types) {#setRestrictedTypes-java.lang.Class...}
```
public static void setRestrictedTypes(Class[] types)
```


Specifies types, which members as well as which derived types' members should be inaccessible by the engine through template syntax.

 **Remarks:** 

Restricted types should be set before the very first building of a report. After  BuildReportbuildReport  is invoked, restricted types cannot be modified and an exception is thrown on attempt to do this. The best place to set restricted types is application startup.

Note that a big amount of restricted types may affect performance, so it is better to restrict only those types, access to which members is really sensitive.

Throws java.lang.IllegalArgumentException in the following cases:

\-  types  is null.

\- One of  types  items is  null .

\- One of  types  items represents an invisible type, i.e. a non-public type or a public nested type which has a non-public outer type.

\- One of  types  items represents an array type.

\-  types  contain duplicate entries.

 **Examples:** 

Shows how to deny access to members of types considered insecure.

```

 Document doc =
         DocumentHelper.createSimpleDocument(
                 "<><<[typeVar]>>");

 // Note, that you can't set restricted types during or after building a report.
 ReportingEngine.setRestrictedTypes(Class.class);
 // We set "AllowMissingMembers" option to avoid exceptions during building a report.
 ReportingEngine engine = new ReportingEngine();
 engine.setOptions(ReportBuildOptions.ALLOW_MISSING_MEMBERS);
 engine.buildReport(doc, new Object());

 // We get an empty string because we can't access the GetType() method.
 Assert.assertEquals(doc.getText().trim(), "");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| types | java.lang.Class[] | Types to be restricted. |

### setUseReflectionOptimization(boolean value) {#setUseReflectionOptimization-boolean}
```
public static void setUseReflectionOptimization(boolean value)
```


Sets a value indicating whether invocations of custom type members performed via reflection API are optimized using dynamic class generation or not. The default value is  true .

 **Remarks:** 

There are some scenarios where it is preferrable to disable this optimization. For example, if you are dealing with small collections of data items all the time, then an overhead of dynamic class generation can be more noticeable than an overhead of direct reflection API calls. The option does not have effect when run on iOS and reflection optimization is not used.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether invocations of custom type members performed via reflection API are optimized using dynamic class generation or not. |

