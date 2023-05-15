---
title: DataColumnCollection
linktitle: DataColumnCollection
second_title: Aspose.Words for Java
description: Represents a collection of DataColumn objects for a DataTable in Java.
type: docs
weight: 15
url: /java/com.aspose.words.net.system.data/datacolumncollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataColumnCollection implements Iterable
```

Represents a collection of [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) objects for a [DataTable](../../com.aspose.words.net.system.data/datatable/).
## Methods

| Method | Description |
| --- | --- |
| [add(System.Data.DataColumn column)](#add-com.aspose.words.net.System.Data.DataColumn) | Creates and adds the specified [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) object to the [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/). |
| [add(String columnName)](#add-java.lang.String) | Creates and adds a [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) object that has the specified name to the [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/). |
| [add(String columnName, Class type)](#add-java.lang.String-java.lang.Class) | Creates and adds a [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) object that has the specified name and type to the [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/). |
| [add(String columnName, Class type, int columnMapping, boolean allowAutoIncrement, boolean allowDBNull)](#add-java.lang.String-java.lang.Class-int-boolean-boolean) | Creates and adds a [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) with the specified name, type and specific values to the columns collection. |
| [clear()](#clear) | Clears the collection of any columns. |
| [contains(String name)](#contains-java.lang.String) | Checks whether the collection contains a column with the specified name. |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [get(int index)](#get-int) | Gets the [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) from the collection at the specified index. |
| [get(String name)](#get-java.lang.String) | Gets the [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) from the collection with the specified name. |
| [getClass()](#getClass) |  |
| [getCount()](#getCount) |  |
| [hashCode()](#hashCode) |  |
| [indexOf(System.Data.DataColumn column)](#indexOf-com.aspose.words.net.System.Data.DataColumn) | Gets the index of a column specified by name. |
| [indexOf(String columnName)](#indexOf-java.lang.String) | Gets the index of the column with the specific name (the name is not case sensitive). |
| [iterator()](#iterator) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [remove(System.Data.DataColumn column)](#remove-com.aspose.words.net.System.Data.DataColumn) | Removes the specified [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) object from the collection. |
| [remove(String name)](#remove-java.lang.String) | Removes the [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) object that has the specified name from the collection. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### add(System.Data.DataColumn column) {#add-com.aspose.words.net.System.Data.DataColumn}
```
public void add(System.Data.DataColumn column)
```


Creates and adds the specified [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) object to the [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | The [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) to add. |

### add(String columnName) {#add-java.lang.String}
```
public void add(String columnName)
```


Creates and adds a [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) object that has the specified name to the [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| columnName | java.lang.String | The name of the column. |

### add(String columnName, Class type) {#add-java.lang.String-java.lang.Class}
```
public System.Data.DataColumn add(String columnName, Class type)
```


Creates and adds a [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) object that has the specified name and type to the [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| columnName | java.lang.String | The [DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String) to use when you create the column. |
| type | java.lang.Class | The [DataColumn.getDataType()](../../com.aspose.words.net.system.data/datacolumn/\#getDataType) / [DataColumn.setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\#setDataType-java.lang.Class) of the new column. |

**Returns:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn/) - The newly created [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).
### add(String columnName, Class type, int columnMapping, boolean allowAutoIncrement, boolean allowDBNull) {#add-java.lang.String-java.lang.Class-int-boolean-boolean}
```
public System.Data.DataColumn add(String columnName, Class type, int columnMapping, boolean allowAutoIncrement, boolean allowDBNull)
```


Creates and adds a [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) with the specified name, type and specific values to the columns collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| columnName | java.lang.String | name |
| type | java.lang.Class | data type |
| columnMapping | int | column mapping type |
| allowAutoIncrement | boolean | is auto increment allowed |
| allowDBNull | boolean | is DBNull value allowed |

**Returns:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn/) - created a [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) instance.
### clear() {#clear}
```
public void clear()
```


Clears the collection of any columns.

### contains(String name) {#contains-java.lang.String}
```
public boolean contains(String name)
```


Checks whether the collection contains a column with the specified name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The [DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String) of the column to look for. |

**Returns:**
boolean - true if a column exists with this name; otherwise, false.
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
### get(int index) {#get-int}
```
public System.Data.DataColumn get(int index)
```


Gets the [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) from the collection at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero-based index of the column to return. |

**Returns:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn/) - The [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) at the specified index.
### get(String name) {#get-java.lang.String}
```
public System.Data.DataColumn get(String name)
```


Gets the [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) from the collection with the specified name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The [DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String) of the column to return. |

**Returns:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn/) - The [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) in the collection with the specified [DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String); otherwise a null value if the [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) does not exist.
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getCount() {#getCount}
```
public int getCount()
```




**Returns:**
int - the total number of elements in a collection.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### indexOf(System.Data.DataColumn column) {#indexOf-com.aspose.words.net.System.Data.DataColumn}
```
public int indexOf(System.Data.DataColumn column)
```


Gets the index of a column specified by name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | The name of the column to return. |

**Returns:**
int - The index of the column specified by  column  if it is found; otherwise, -1.
### indexOf(String columnName) {#indexOf-java.lang.String}
```
public int indexOf(String columnName)
```


Gets the index of the column with the specific name (the name is not case sensitive).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| columnName | java.lang.String | The name of the column to find. |

**Returns:**
int - The zero-based index of the column with the specified name, or -1 if the column does not exist in the collection.
### iterator() {#iterator}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### remove(System.Data.DataColumn column) {#remove-com.aspose.words.net.System.Data.DataColumn}
```
public void remove(System.Data.DataColumn column)
```


Removes the specified [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) object from the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | The [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) to remove. |

### remove(String name) {#remove-java.lang.String}
```
public void remove(String name)
```


Removes the [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) object that has the specified name from the collection.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| name | java.lang.String | The name of the column to remove. |

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

