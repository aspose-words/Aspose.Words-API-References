---
title: DataRow
linktitle: DataRow
second_title: Aspose.Words for Java API Reference
description: Represents a row of data in a DataTable in Java.
type: docs
weight: 20
url: /java/com.aspose.words.net.system.data/datarow/
---

**Inheritance:**
java.lang.Object
```
public class DataRow
```

Represents a row of data in a [DataTable](../../com.aspose.words.net.system.data/datatable/).
## Methods

| Method | Description |
| --- | --- |
| [delete()](#delete) | Deletes the [DataRow](../../com.aspose.words.net.system.data/datarow/). |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [get(System.Data.DataColumn column)](#get-com.aspose.words.net.System.Data.DataColumn) | Gets the data stored in the specified [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
| [get(int columnIndex)](#get-int) | Gets the data stored in the column specified by index. |
| [get(String columnName)](#get-java.lang.String) | Gets the data stored in the column specified by name. |
| [getChildRows(System.Data.DataRelation relation)](#getChildRows-com.aspose.words.net.System.Data.DataRelation) | Gets the child rows of this [DataRow](../../com.aspose.words.net.system.data/datarow/) using the specified [DataRelation](../../com.aspose.words.net.system.data/datarelation/). |
| [getClass()](#getClass) |  |
| [getItemArray()](#getItemArray) | Gets all the values for this row through an array. |
| [getKeyValues(System.Data.DataKey childKey)](#getKeyValues-com.aspose.words.net.System.Data.DataKey) |  |
| [getOriginalValue(String columnName)](#getOriginalValue-java.lang.String) |  |
| [getParentRow(System.Data.DataRelation relation)](#getParentRow-com.aspose.words.net.System.Data.DataRelation) | Gets the parent row of a [DataRow](../../com.aspose.words.net.system.data/datarow/) using the specified [DataRelation](../../com.aspose.words.net.system.data/datarelation/). |
| [getParentRows(System.Data.DataRelation relation)](#getParentRows-com.aspose.words.net.System.Data.DataRelation) | Gets the parent rows of a [DataRow](../../com.aspose.words.net.system.data/datarow/) using the specified [DataRelation](../../com.aspose.words.net.system.data/datarelation/). |
| [getRowState()](#getRowState) | Gets the current state of the row with regard to its relationship to the [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/). |
| [getTable()](#getTable) | Gets the [DataTable](../../com.aspose.words.net.system.data/datatable/) for which this row has a schema. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [readFrom(ResultSet resultSet)](#readFrom-java.sql.ResultSet) | Reads values from the java.sql.ResultSet |
| [remove(int index)](#remove-int) |  |
| [set(System.Data.DataColumn column, Object value)](#set-com.aspose.words.net.System.Data.DataColumn-java.lang.Object) | Sets the data stored in the specified [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
| [set(int columnIndex, Object value)](#set-int-java.lang.Object) | Sets the data stored in the column specified by index. |
| [set(String columnName, Object value)](#set-java.lang.String-java.lang.Object) | Sets the data stored in the column specified by name. |
| [setItemArray(Object[] value)](#setItemArray-java.lang.Object) | Sets all the values for this row through an array. |
| [setOriginalValue(String columnName, Object data)](#setOriginalValue-java.lang.String-java.lang.Object) |  |
| [setRowState(int state)](#setRowState-int) |  |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### delete() {#delete}
```
public void delete()
```


Deletes the [DataRow](../../com.aspose.words.net.system.data/datarow/).

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
### get(System.Data.DataColumn column) {#get-com.aspose.words.net.System.Data.DataColumn}
```
public Object get(System.Data.DataColumn column)
```


Gets the data stored in the specified [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | A [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) that contains the data. |

**Returns:**
java.lang.Object - An java.lang.Object that contains the data.
### get(int columnIndex) {#get-int}
```
public Object get(int columnIndex)
```


Gets the data stored in the column specified by index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| columnIndex | int | The zero-based index of the column. |

**Returns:**
java.lang.Object - An java.lang.Object that contains the data.
### get(String columnName) {#get-java.lang.String}
```
public Object get(String columnName)
```


Gets the data stored in the column specified by name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| columnName | java.lang.String | The name of the column. |

**Returns:**
java.lang.Object - An java.lang.Object that contains the data.
### getChildRows(System.Data.DataRelation relation) {#getChildRows-com.aspose.words.net.System.Data.DataRelation}
```
public System.Data.DataRow[] getChildRows(System.Data.DataRelation relation)
```


Gets the child rows of this [DataRow](../../com.aspose.words.net.system.data/datarow/) using the specified [DataRelation](../../com.aspose.words.net.system.data/datarelation/).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | The [DataRelation](../../com.aspose.words.net.system.data/datarelation/) to use. |

**Returns:**
com.aspose.words.net.System.Data.DataRow[] - An array of [DataRow](../../com.aspose.words.net.system.data/datarow/) objects or an array of length zero.
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getItemArray() {#getItemArray}
```
public Object[] getItemArray()
```


Gets all the values for this row through an array.

**Returns:**
java.lang.Object[] - An array of type java.lang.Object.
### getKeyValues(System.Data.DataKey childKey) {#getKeyValues-com.aspose.words.net.System.Data.DataKey}
```
public Object[] getKeyValues(System.Data.DataKey childKey)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| childKey | [DataKey](../../com.aspose.words.net.system.data/datakey/) |  |

**Returns:**
java.lang.Object[]
### getOriginalValue(String columnName) {#getOriginalValue-java.lang.String}
```
public Object getOriginalValue(String columnName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| columnName | java.lang.String |  |

**Returns:**
java.lang.Object
### getParentRow(System.Data.DataRelation relation) {#getParentRow-com.aspose.words.net.System.Data.DataRelation}
```
public System.Data.DataRow getParentRow(System.Data.DataRelation relation)
```


Gets the parent row of a [DataRow](../../com.aspose.words.net.system.data/datarow/) using the specified [DataRelation](../../com.aspose.words.net.system.data/datarelation/).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | The [DataRelation](../../com.aspose.words.net.system.data/datarelation/) to use. |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - The parent [DataRow](../../com.aspose.words.net.system.data/datarow/) of the current row.
### getParentRows(System.Data.DataRelation relation) {#getParentRows-com.aspose.words.net.System.Data.DataRelation}
```
public System.Data.DataRow[] getParentRows(System.Data.DataRelation relation)
```


Gets the parent rows of a [DataRow](../../com.aspose.words.net.system.data/datarow/) using the specified [DataRelation](../../com.aspose.words.net.system.data/datarelation/).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | The [DataRelation](../../com.aspose.words.net.system.data/datarelation/) to use. |

**Returns:**
com.aspose.words.net.System.Data.DataRow[] - An array of [DataRow](../../com.aspose.words.net.system.data/datarow/) objects or an array of length zero.
### getRowState() {#getRowState}
```
public int getRowState()
```


Gets the current state of the row with regard to its relationship to the [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/).

**Returns:**
int - One of the [DataRowState](../../com.aspose.words.net.system.data/datarowstate/) values. The returned value is a bitwise combination of [DataRowState](../../com.aspose.words.net.system.data/datarowstate/) constants.
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


Gets the [DataTable](../../com.aspose.words.net.system.data/datatable/) for which this row has a schema.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The [DataTable](../../com.aspose.words.net.system.data/datatable/) to which this row belongs.
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




### readFrom(ResultSet resultSet) {#readFrom-java.sql.ResultSet}
```
public boolean readFrom(ResultSet resultSet)
```


Reads values from the java.sql.ResultSet

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| resultSet | java.sql.ResultSet | storage to read from |

**Returns:**
boolean - true if no read errors occurred
### remove(int index) {#remove-int}
```
public void remove(int index)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

### set(System.Data.DataColumn column, Object value) {#set-com.aspose.words.net.System.Data.DataColumn-java.lang.Object}
```
public void set(System.Data.DataColumn column, Object value)
```


Sets the data stored in the specified [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | A [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) that contains the data. |
| value | java.lang.Object | An java.lang.Object that contains the data. |

### set(int columnIndex, Object value) {#set-int-java.lang.Object}
```
public void set(int columnIndex, Object value)
```


Sets the data stored in the column specified by index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| columnIndex | int | The zero-based index of the column. |
| value | java.lang.Object | An java.lang.Object that contains the data. |

### set(String columnName, Object value) {#set-java.lang.String-java.lang.Object}
```
public void set(String columnName, Object value)
```


Sets the data stored in the column specified by name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| columnName | java.lang.String | The name of the column. |
| value | java.lang.Object | An java.lang.Object that contains the data. |

### setItemArray(Object[] value) {#setItemArray-java.lang.Object}
```
public void setItemArray(Object[] value)
```


Sets all the values for this row through an array.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.Object[] | An array of type java.lang.Object. |

### setOriginalValue(String columnName, Object data) {#setOriginalValue-java.lang.String-java.lang.Object}
```
public void setOriginalValue(String columnName, Object data)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| columnName | java.lang.String |  |
| data | java.lang.Object |  |

### setRowState(int state) {#setRowState-int}
```
public void setRowState(int state)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| state | int |  |

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

