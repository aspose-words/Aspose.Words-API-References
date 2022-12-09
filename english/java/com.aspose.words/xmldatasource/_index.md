---
title: XmlDataSource
second_title: Aspose.Words for Java API Reference
description: Provides access to data of an XML file or stream to be used within a report.
type: docs
weight: 631
url: /java/com.aspose.words/xmldatasource/
---

**Inheritance:**
java.lang.Object
```
public class XmlDataSource
```

Provides access to data of an XML file or stream to be used within a report.

To learn more, visit the [ LINQ Reporting Engine ][LINQ Reporting Engine] documentation article.

To access data of the corresponding file or stream while generating a report, pass an instance of this class as a data source to one of [ReportingEngine](../../com.aspose.words/reportingengine). buildReport overloads.

In template documents, if a top-level XML element contains only a list of elements of the same type, an [XmlDataSource](../../com.aspose.words/xmldatasource) instance should be treated in the same way as if it was a [DataTable](../../com.aspose.words.net.system.data/datatable) instance. Otherwise, an [XmlDataSource](../../com.aspose.words/xmldatasource) instance should be treated in the same way as if it was a [DataRow](../../com.aspose.words.net.system.data/datarow) instance. For more information, see template syntax reference(https://docs.aspose.com/display/wordsjava/Template+Syntax).

When XML Schema Definition is passed to a constructor of this class, data types of values of simple XML elements and attributes are determined according to the schema. So in template documents, you can work with typed values rather than just strings.

When XML Schema Definition is not passed to a constructor of this class, data types of values of simple XML elements and attributes are determined automatically upon their string representations. So in template documents, you can work with typed values in this case as well. The engine is capable to automatically recognize values of the following types:

 *  
 *  
 *  
 *  
 *  

Note that for automatic recognition of data types to work, string representations of values of simple XML elements and attributes should be formed using invariant culture settings.

To override default behavior of XML data loading, initialize and pass a [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions) instance to a constructor of this class.


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Constructors

| Constructor | Description |
| --- | --- |
| [XmlDataSource(String xmlPath)](#XmlDataSource-java.lang.String) | Creates a new data source with data from an XML file using default options for XML data loading. |
| [XmlDataSource(InputStream xmlStream)](#XmlDataSource-java.io.InputStream) | Initializes a new instance of this class. |
| [XmlDataSource(String xmlPath, String xmlSchemaPath)](#XmlDataSource-java.lang.String-java.lang.String) | Creates a new data source with data from an XML file using an XML Schema Definition file. |
| [XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream)](#XmlDataSource-java.io.InputStream-java.io.InputStream) | Initializes a new instance of this class. |
| [XmlDataSource(String xmlPath, XmlDataLoadOptions options)](#XmlDataSource-java.lang.String-com.aspose.words.XmlDataLoadOptions) | Creates a new data source with data from an XML file using the specified options for XML data loading. |
| [XmlDataSource(InputStream xmlStream, XmlDataLoadOptions options)](#XmlDataSource-java.io.InputStream-com.aspose.words.XmlDataLoadOptions) | Initializes a new instance of this class. |
| [XmlDataSource(String xmlPath, String xmlSchemaPath, XmlDataLoadOptions options)](#XmlDataSource-java.lang.String-java.lang.String-com.aspose.words.XmlDataLoadOptions) | Creates a new data source with data from an XML file using an XML Schema Definition file. |
| [XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream, XmlDataLoadOptions options)](#XmlDataSource-java.io.InputStream-java.io.InputStream-com.aspose.words.XmlDataLoadOptions) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### XmlDataSource(String xmlPath) {#XmlDataSource-java.lang.String}
```
public XmlDataSource(String xmlPath)
```


Creates a new data source with data from an XML file using default options for XML data loading.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| xmlPath | java.lang.String | The path to the XML file to be used as the data source. |

### XmlDataSource(InputStream xmlStream) {#XmlDataSource-java.io.InputStream}
```
public XmlDataSource(InputStream xmlStream)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |

### XmlDataSource(String xmlPath, String xmlSchemaPath) {#XmlDataSource-java.lang.String-java.lang.String}
```
public XmlDataSource(String xmlPath, String xmlSchemaPath)
```


Creates a new data source with data from an XML file using an XML Schema Definition file. Default options are used for XML data loading.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| xmlPath | java.lang.String | The path to the XML file to be used as the data source. |
| xmlSchemaPath | java.lang.String | The path to the XML Schema Definition file that provides schema for the XML file. |

### XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream) {#XmlDataSource-java.io.InputStream-java.io.InputStream}
```
public XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |
| xmlSchemaStream | java.io.InputStream |  |

### XmlDataSource(String xmlPath, XmlDataLoadOptions options) {#XmlDataSource-java.lang.String-com.aspose.words.XmlDataLoadOptions}
```
public XmlDataSource(String xmlPath, XmlDataLoadOptions options)
```


Creates a new data source with data from an XML file using the specified options for XML data loading.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| xmlPath | java.lang.String | The path to the XML file to be used as the data source. |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions) | Options for XML data loading. |

### XmlDataSource(InputStream xmlStream, XmlDataLoadOptions options) {#XmlDataSource-java.io.InputStream-com.aspose.words.XmlDataLoadOptions}
```
public XmlDataSource(InputStream xmlStream, XmlDataLoadOptions options)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions) |  |

### XmlDataSource(String xmlPath, String xmlSchemaPath, XmlDataLoadOptions options) {#XmlDataSource-java.lang.String-java.lang.String-com.aspose.words.XmlDataLoadOptions}
```
public XmlDataSource(String xmlPath, String xmlSchemaPath, XmlDataLoadOptions options)
```


Creates a new data source with data from an XML file using an XML Schema Definition file. The specified options are used for XML data loading.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| xmlPath | java.lang.String | The path to the XML file to be used as the data source. |
| xmlSchemaPath | java.lang.String | The path to the XML Schema Definition file that provides schema for the XML file. |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions) | Options for XML data loading. |

### XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream, XmlDataLoadOptions options) {#XmlDataSource-java.io.InputStream-java.io.InputStream-com.aspose.words.XmlDataLoadOptions}
```
public XmlDataSource(InputStream xmlStream, InputStream xmlSchemaStream, XmlDataLoadOptions options)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| xmlStream | java.io.InputStream |  |
| xmlSchemaStream | java.io.InputStream |  |
| options | [XmlDataLoadOptions](../../com.aspose.words/xmldataloadoptions) |  |

### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

