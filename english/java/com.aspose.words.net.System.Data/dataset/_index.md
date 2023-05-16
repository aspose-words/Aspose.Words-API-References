---
title: DataSet
linktitle: DataSet
second_title: Aspose.Words for Java
description: Represents an in-memory cache of data in Java.
type: docs
weight: 24
url: /java/com.aspose.words.net.system.data/dataset/
---

**Inheritance:**
java.lang.Object
```
public class DataSet
```

Represents an in-memory cache of data.
## Constructors

| Constructor | Description |
| --- | --- |
| [DataSet()](#DataSet) | Initializes a new instance of the [DataSet](../../com.aspose.words.net.system.data/dataset/) class. |
| [DataSet(Connection connection)](#DataSet-java.sql.Connection) | Initializes a new instance of the DataSet class with data taken from Connection. |
| [DataSet(Connection connection, String schemaName)](#DataSet-java.sql.Connection-java.lang.String) | Initializes a new instance of the DataSet class with data taken from Connection. |
| [DataSet(String dataSetName)](#DataSet-java.lang.String) | Initializes a new instance of a [DataSet](../../com.aspose.words.net.system.data/dataset/) class with the given name. |
## Methods

| Method | Description |
| --- | --- |
| [IsSchemaWasRead()](#IsSchemaWasRead) |  |
| [clear()](#clear) | Clears the [DataSet](../../com.aspose.words.net.system.data/dataset/) of any data by removing all rows in all tables. |
| [close()](#close) |  |
| [getDataSetName()](#getDataSetName) | Gets the name of the current [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [getEnforceConstraints()](#getEnforceConstraints) | Gets a value indicating whether constraint rules are followed when attempting any update operation. |
| [getNamespace()](#getNamespace) | Gets the namespace of the [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [getRelations()](#getRelations) | Get the collection of relations that link tables and allow navigation from parent tables to child tables. |
| [getTables()](#getTables) | Gets the collection of tables contained in the [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [isLocaleSpecified()](#isLocaleSpecified) |  |
| [readXml(InputStream stream)](#readXml-java.io.InputStream) | Reads XML schema and data into the [DataSet](../../com.aspose.words.net.system.data/dataset/) using the specified java.io.InputStream. |
| [readXml(InputStream xmlStream, System.Data.XmlReadMode mode)](#readXml-java.io.InputStream-com.aspose.words.net.System.Data.XmlReadMode) | Reads XML schema and data into the DataSet using the specified java.io.InputStream and [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/). |
| [readXml(String fileName)](#readXml-java.lang.String) | Reads XML schema and data into the [DataSet](../../com.aspose.words.net.system.data/dataset/) using the specified file. |
| [readXml(String xmlPath, System.Data.XmlReadMode readMode)](#readXml-java.lang.String-com.aspose.words.net.System.Data.XmlReadMode) | Reads XML schema and data into the DataSet using the specified file and [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/). |
| [readXmlSchema(InputStream stream)](#readXmlSchema-java.io.InputStream) | Reads the XML schema from the specified java.io.InputStream into the [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [readXmlSchema(String fileName)](#readXmlSchema-java.lang.String) | Reads the XML schema from the specified file into the [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [reset()](#reset) | Resets the [DataSet](../../com.aspose.words.net.system.data/dataset/) to its original state. |
| [setDataSetName(String value)](#setDataSetName-java.lang.String) | Sets the name of the current [DataSet](../../com.aspose.words.net.system.data/dataset/). |
| [setEnforceConstraints(boolean value)](#setEnforceConstraints-boolean) | Sets a value indicating whether constraint rules are followed when attempting any update operation. |
| [setLocale(Locale locale)](#setLocale-java.util.Locale) | Sets the locale information used to compare strings within the table. |
### DataSet() {#DataSet}
```
public DataSet()
```


Initializes a new instance of the [DataSet](../../com.aspose.words.net.system.data/dataset/) class.

### DataSet(Connection connection) {#DataSet-java.sql.Connection}
```
public DataSet(Connection connection)
```


Initializes a new instance of the DataSet class with data taken from Connection. Tables, Relations, Constraints and Indexes will be copied into DataSet.

By default no schema name will be used.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| connection | java.sql.Connection | which contains DB data. |

### DataSet(Connection connection, String schemaName) {#DataSet-java.sql.Connection-java.lang.String}
```
public DataSet(Connection connection, String schemaName)
```


Initializes a new instance of the DataSet class with data taken from Connection. Tables, Relations, Constraints and Indexes will be copied into DataSet.

`DataSet dataSet = new DataSet(conn, "PUBLIC"); // HSQLDB`

or

`DataSet dataSet = new DataSet(conn); // MYSQL's default schema name.`

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| connection | java.sql.Connection | which contains DB data. |
| schemaName | java.lang.String | which contains the tables to be imported. |

### DataSet(String dataSetName) {#DataSet-java.lang.String}
```
public DataSet(String dataSetName)
```


Initializes a new instance of a [DataSet](../../com.aspose.words.net.system.data/dataset/) class with the given name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dataSetName | java.lang.String | The name of the [DataSet](../../com.aspose.words.net.system.data/dataset/). |

### IsSchemaWasRead() {#IsSchemaWasRead}
```
public boolean IsSchemaWasRead()
```




**Returns:**
boolean - true if schema was read
### clear() {#clear}
```
public void clear()
```


Clears the [DataSet](../../com.aspose.words.net.system.data/dataset/) of any data by removing all rows in all tables.

### close() {#close}
```
public void close()
```




### getDataSetName() {#getDataSetName}
```
public String getDataSetName()
```


Gets the name of the current [DataSet](../../com.aspose.words.net.system.data/dataset/).

**Returns:**
java.lang.String - The name of the [DataSet](../../com.aspose.words.net.system.data/dataset/).
### getEnforceConstraints() {#getEnforceConstraints}
```
public boolean getEnforceConstraints()
```


Gets a value indicating whether constraint rules are followed when attempting any update operation.

**Returns:**
boolean - true if rules are enforced; otherwise false. The default is true.
### getNamespace() {#getNamespace}
```
public String getNamespace()
```


Gets the namespace of the [DataSet](../../com.aspose.words.net.system.data/dataset/).

**Returns:**
java.lang.String - The namespace of the [DataSet](../../com.aspose.words.net.system.data/dataset/).
### getRelations() {#getRelations}
```
public System.Data.DataRelationCollection getRelations()
```


Get the collection of relations that link tables and allow navigation from parent tables to child tables.

**Returns:**
[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) - A [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) that contains a collection of [DataRelation](../../com.aspose.words.net.system.data/datarelation/) objects. An empty collection is returned if no [DataRelation](../../com.aspose.words.net.system.data/datarelation/) objects exist.
### getTables() {#getTables}
```
public System.Data.DataTableCollection getTables()
```


Gets the collection of tables contained in the [DataSet](../../com.aspose.words.net.system.data/dataset/).

**Returns:**
[DataTableCollection](../../com.aspose.words.net.system.data/datatablecollection/) - The [DataTableCollection](../../com.aspose.words.net.system.data/datatablecollection/) contained by this [DataSet](../../com.aspose.words.net.system.data/dataset/). An empty collection is returned if no [DataTable](../../com.aspose.words.net.system.data/datatable/) objects exist.
### isLocaleSpecified() {#isLocaleSpecified}
```
public boolean isLocaleSpecified()
```




**Returns:**
boolean - true if locale was set
### readXml(InputStream stream) {#readXml-java.io.InputStream}
```
public System.Data.XmlReadMode readXml(InputStream stream)
```


Reads XML schema and data into the [DataSet](../../com.aspose.words.net.system.data/dataset/) using the specified java.io.InputStream.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| stream | java.io.InputStream | An object that derives from java.io.InputStream. |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) - The [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) used to read the data. The returned value is one of [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) constants.
### readXml(InputStream xmlStream, System.Data.XmlReadMode mode) {#readXml-java.io.InputStream-com.aspose.words.net.System.Data.XmlReadMode}
```
public System.Data.XmlReadMode readXml(InputStream xmlStream, System.Data.XmlReadMode mode)
```


Reads XML schema and data into the DataSet using the specified java.io.InputStream and [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| xmlStream | java.io.InputStream | The Stream from which to read. |
| mode | [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) | One of the [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) values. |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) - The XmlReadMode used to read the data.
### readXml(String fileName) {#readXml-java.lang.String}
```
public System.Data.XmlReadMode readXml(String fileName)
```


Reads XML schema and data into the [DataSet](../../com.aspose.words.net.system.data/dataset/) using the specified file.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | The filename (including the path) from which to read. |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) - The XmlReadMode used to read the data. The returned value is one of [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) constants.
### readXml(String xmlPath, System.Data.XmlReadMode readMode) {#readXml-java.lang.String-com.aspose.words.net.System.Data.XmlReadMode}
```
public System.Data.XmlReadMode readXml(String xmlPath, System.Data.XmlReadMode readMode)
```


Reads XML schema and data into the DataSet using the specified file and [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| xmlPath | java.lang.String | the specified file |
| readMode | [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) | [XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) |

**Returns:**
[XmlReadMode](../../com.aspose.words.net.system.data/xmlreadmode/) - mode which was used while reading
### readXmlSchema(InputStream stream) {#readXmlSchema-java.io.InputStream}
```
public void readXmlSchema(InputStream stream)
```


Reads the XML schema from the specified java.io.InputStream into the [DataSet](../../com.aspose.words.net.system.data/dataset/).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| stream | java.io.InputStream | The java.io.InputStream from which to read. |

### readXmlSchema(String fileName) {#readXmlSchema-java.lang.String}
```
public void readXmlSchema(String fileName)
```


Reads the XML schema from the specified file into the [DataSet](../../com.aspose.words.net.system.data/dataset/).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| fileName | java.lang.String | The file name (including the path) from which to read. |

### reset() {#reset}
```
public void reset()
```


Resets the [DataSet](../../com.aspose.words.net.system.data/dataset/) to its original state. Subclasses should override [reset()](../../com.aspose.words.net.system.data/dataset/\#reset) to restore a [DataSet](../../com.aspose.words.net.system.data/dataset/) to its original state.

### setDataSetName(String value) {#setDataSetName-java.lang.String}
```
public void setDataSetName(String value)
```


Sets the name of the current [DataSet](../../com.aspose.words.net.system.data/dataset/).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of the [DataSet](../../com.aspose.words.net.system.data/dataset/). |

### setEnforceConstraints(boolean value) {#setEnforceConstraints-boolean}
```
public void setEnforceConstraints(boolean value)
```


Sets a value indicating whether constraint rules are followed when attempting any update operation.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | true if rules are enforced; otherwise false. The default is true. |

### setLocale(Locale locale) {#setLocale-java.util.Locale}
```
public void setLocale(Locale locale)
```


Sets the locale information used to compare strings within the table.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| locale | java.util.Locale | of this data set |

