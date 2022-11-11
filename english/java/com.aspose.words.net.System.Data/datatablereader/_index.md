---
title: DataTableReader
second_title: Aspose.Words for Java API Reference
description: The  obtains the contents of one or more  objects in the form of one or more read-only forward-only result sets.
type: docs
weight: 27
url: /java/com.aspose.words.net.system.data/datatablereader/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.net.System.Data.Common.DbDataReader](../../com.aspose.words.net.system.data.common/dbdatareader)
```
public class DataTableReader extends System.Data.Common.DbDataReader
```

The [DataTableReader](../../com.aspose.words.net.system.data/datatablereader) obtains the contents of one or more [DataTable](../../com.aspose.words.net.system.data/datatable) objects in the form of one or more read-only, forward-only result sets.
## Constructors

| Constructor | Description |
| --- | --- |
| [DataTableReader(System.Data.DataTable dataTable)](#DataTableReader-com.aspose.words.net.System.Data.DataTable-) | Initializes a new instance of the [DataTableReader](../../com.aspose.words.net.system.data/datatablereader) class by using data from the supplied [DataTable](../../com.aspose.words.net.system.data/datatable). |
| [DataTableReader(System.Data.DataTable[] dataTables)](#DataTableReader-com.aspose.words.net.System.Data.DataTable---) | Initializes a new instance of the [DataTableReader](../../com.aspose.words.net.system.data/datatablereader) class using the supplied array of [DataTable](../../com.aspose.words.net.system.data/datatable) objects. |
## Methods

| Method | Description |
| --- | --- |
| [close()](#close--) | Closes the current [DataTableReader](../../com.aspose.words.net.system.data/datatablereader). |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int ordinal)](#get-int-) | Gets the value of the specified column in its native format given the column ordinal. |
| [get(String name)](#get-java.lang.String-) | Gets the value of the specified column in its native format given the column name. |
| [getClass()](#getClass--) |  |
| [getDepth()](#getDepth--) | The depth of nesting for the current row of the [DataTableReader](../../com.aspose.words.net.system.data/datatablereader). |
| [getFieldCount()](#getFieldCount--) | Returns the number of columns in the current row. |
| [getFieldType(int ordinal)](#getFieldType-int-) | Gets the java.lang.Class that is the data type of the object. |
| [getName(int ordinal)](#getName-int-) | Gets the value of the specified column as a java.lang.String. |
| [getRecordsAffected()](#getRecordsAffected--) | Gets the number of rows inserted, changed, or deleted by execution of the SQL statement. |
| [getSchemaTable()](#getSchemaTable--) | Returns a [DataTable](../../com.aspose.words.net.system.data/datatable) that describes the column metadata of the [DataTableReader](../../com.aspose.words.net.system.data/datatablereader). |
| [getValue(int ordinal)](#getValue-int-) | Gets the value of the specified column in its native format. |
| [hasRows()](#hasRows--) | Gets a value that indicates whether the [DataTableReader](../../com.aspose.words.net.system.data/datatablereader) contains one or more rows. |
| [hashCode()](#hashCode--) |  |
| [isClosed()](#isClosed--) | Gets a value that indicates whether the [DataTableReader](../../com.aspose.words.net.system.data/datatablereader) is closed. |
| [iterator()](#iterator--) | Returns an enumerator that can be used to iterate through the item collection. |
| [nextResult()](#nextResult--) | Advances the [DataTableReader](../../com.aspose.words.net.system.data/datatablereader) to the next result set, if any. |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [read()](#read--) | Advances the [DataTableReader](../../com.aspose.words.net.system.data/datatablereader) to the next record. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### DataTableReader(System.Data.DataTable dataTable) {#DataTableReader-com.aspose.words.net.System.Data.DataTable-}
```
public DataTableReader(System.Data.DataTable dataTable)
```


Initializes a new instance of the [DataTableReader](../../com.aspose.words.net.system.data/datatablereader) class by using data from the supplied [DataTable](../../com.aspose.words.net.system.data/datatable).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable) | The [DataTable](../../com.aspose.words.net.system.data/datatable) from which the new [DataTableReader](../../com.aspose.words.net.system.data/datatablereader) obtains its result set. |

### DataTableReader(System.Data.DataTable[] dataTables) {#DataTableReader-com.aspose.words.net.System.Data.DataTable---}
```
public DataTableReader(System.Data.DataTable[] dataTables)
```


Initializes a new instance of the [DataTableReader](../../com.aspose.words.net.system.data/datatablereader) class using the supplied array of [DataTable](../../com.aspose.words.net.system.data/datatable) objects.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| dataTables | [DataTable\[\]](../../com.aspose.words.net.system.data/datatable) | The array of [DataTable](../../com.aspose.words.net.system.data/datatable) objects that supplies the results for the new [DataTableReader](../../com.aspose.words.net.system.data/datatablereader) object. |

### close() {#close--}
```
public void close()
```


Closes the current [DataTableReader](../../com.aspose.words.net.system.data/datatablereader).

### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### get(int ordinal) {#get-int-}
```
public Object get(int ordinal)
```


Gets the value of the specified column in its native format given the column ordinal.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ordinal | int | The zero-based column ordinal. |

**Returns:**
java.lang.Object - The value of the specified column in its native format.
### get(String name) {#get-java.lang.String-}
```
public Object get(String name)
```


Gets the value of the specified column in its native format given the column name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The name of the column. |

**Returns:**
java.lang.Object - The value of the specified column in its native format.
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getDepth() {#getDepth--}
```
public int getDepth()
```


The depth of nesting for the current row of the [DataTableReader](../../com.aspose.words.net.system.data/datatablereader).

**Returns:**
int - The depth of nesting for the current row; always zero.
### getFieldCount() {#getFieldCount--}
```
public int getFieldCount()
```


Returns the number of columns in the current row.

**Returns:**
int - When not positioned in a valid result set, 0; otherwise the number of columns in the current row.
### getFieldType(int ordinal) {#getFieldType-int-}
```
public Class getFieldType(int ordinal)
```


Gets the java.lang.Class that is the data type of the object.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ordinal | int | The zero-based column ordinal. |

**Returns:**
java.lang.Class - The java.lang.Class that is the data type of the object.
### getName(int ordinal) {#getName-int-}
```
public String getName(int ordinal)
```


Gets the value of the specified column as a java.lang.String.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ordinal | int | The zero-based column ordinal |

**Returns:**
java.lang.String - The name of the specified column.
### getRecordsAffected() {#getRecordsAffected--}
```
public int getRecordsAffected()
```


Gets the number of rows inserted, changed, or deleted by execution of the SQL statement.

**Returns:**
int - The [DataTableReader](../../com.aspose.words.net.system.data/datatablereader) does not support this property and always returns 0.
### getSchemaTable() {#getSchemaTable--}
```
public System.Data.DataTable getSchemaTable()
```


Returns a [DataTable](../../com.aspose.words.net.system.data/datatable) that describes the column metadata of the [DataTableReader](../../com.aspose.words.net.system.data/datatablereader).

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable) - A [DataTable](../../com.aspose.words.net.system.data/datatable) that describes the column metadata.
### getValue(int ordinal) {#getValue-int-}
```
public Object getValue(int ordinal)
```


Gets the value of the specified column in its native format.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| ordinal | int | The zero-based column ordinal |

**Returns:**
java.lang.Object - The value of the specified column. This method returns DBNull for null columns.
### hasRows() {#hasRows--}
```
public boolean hasRows()
```


Gets a value that indicates whether the [DataTableReader](../../com.aspose.words.net.system.data/datatablereader) contains one or more rows.

**Returns:**
boolean - true if the [DataTableReader](../../com.aspose.words.net.system.data/datatablereader) contains one or more rows; otherwise false.
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Returns:**
int
### isClosed() {#isClosed--}
```
public boolean isClosed()
```


Gets a value that indicates whether the [DataTableReader](../../com.aspose.words.net.system.data/datatablereader) is closed.

**Returns:**
boolean - Returns true if the [DataTableReader](../../com.aspose.words.net.system.data/datatablereader) is closed; otherwise, false.
### iterator() {#iterator--}
```
public Iterator iterator()
```


Returns an enumerator that can be used to iterate through the item collection.

**Returns:**
java.util.Iterator - An java.util.Iterator object that represents the item collection.
### nextResult() {#nextResult--}
```
public boolean nextResult()
```


Advances the [DataTableReader](../../com.aspose.words.net.system.data/datatablereader) to the next result set, if any.

**Returns:**
boolean - true if there was another result set; otherwise false.
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### read() {#read--}
```
public boolean read()
```


Advances the [DataTableReader](../../com.aspose.words.net.system.data/datatablereader) to the next record.

**Returns:**
boolean - true if there was another row to read; otherwise false.
### toString() {#toString--}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

