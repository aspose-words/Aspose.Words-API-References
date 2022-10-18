---
title: DataRow
second_title: Aspose.Words for Java API Reference
description: Represents a row of data in a .
type: docs
weight: 20
url: /java/com.aspose.words.net.system.data/datarow/
---

**Inheritance:**
java.lang.Object
```
public class DataRow
```

Represents a row of data in a [DataTable](../../com.aspose.words.net.system.data/datatable).
## Methods

| Method | Description |
| --- | --- |
| [readFrom(ResultSet resultSet)](#readFrom-java.sql.ResultSet-) | Reads values from the java.sql.ResultSet |
| [get(int columnIndex)](#get-int-) | Gets the data stored in the column specified by index. |
| [get(String columnName)](#get-java.lang.String-) | Gets the data stored in the column specified by name. |
| [get(System.Data.DataColumn column)](#get-com.aspose.words.net.System.Data.DataColumn-) | Gets the data stored in the specified [DataColumn](../../com.aspose.words.net.system.data/datacolumn). |
| [getTable()](#getTable--) | Gets the [DataTable](../../com.aspose.words.net.system.data/datatable) for which this row has a schema. |
| [getChildRows(System.Data.DataRelation relation)](#getChildRows-com.aspose.words.net.System.Data.DataRelation-) | Gets the child rows of this [DataRow](../../com.aspose.words.net.system.data/datarow) using the specified [DataRelation](../../com.aspose.words.net.system.data/datarelation). |
| [getParentRow(System.Data.DataRelation relation)](#getParentRow-com.aspose.words.net.System.Data.DataRelation-) | Gets the parent row of a [DataRow](../../com.aspose.words.net.system.data/datarow) using the specified [DataRelation](../../com.aspose.words.net.system.data/datarelation). |
| [getParentRows(System.Data.DataRelation relation)](#getParentRows-com.aspose.words.net.System.Data.DataRelation-) | Gets the parent rows of a [DataRow](../../com.aspose.words.net.system.data/datarow) using the specified [DataRelation](../../com.aspose.words.net.system.data/datarelation). |
| [set(int value, Object columnIndex)](#set-int-java.lang.Object-) | Sets the data stored in the column specified by index. |
| [set(String value, Object columnName)](#set-java.lang.String-java.lang.Object-) | Sets the data stored in the column specified by name. |
| [set(System.Data.DataColumn value, Object column)](#set-com.aspose.words.net.System.Data.DataColumn-java.lang.Object-) | Sets the data stored in the specified [DataColumn](../../com.aspose.words.net.system.data/datacolumn). |
| [getRowState()](#getRowState--) | Gets the current state of the row with regard to its relationship to the [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection). |
| [setRowState(int state)](#setRowState-int-) |  |
| [delete()](#delete--) | Deletes the [DataRow](../../com.aspose.words.net.system.data/datarow). |
| [setOriginalValue(String columnName, Object data)](#setOriginalValue-java.lang.String-java.lang.Object-) |  |
| [getOriginalValue(String columnName)](#getOriginalValue-java.lang.String-) |  |
| [getItemArray()](#getItemArray--) | Gets all the values for this row through an array. |
| [setItemArray(Object[] value)](#setItemArray-java.lang.Object---) | Sets all the values for this row through an array. |
| [getKeyValues(System.Data.DataKey childKey)](#getKeyValues-com.aspose.words.net.System.Data.DataKey-) |  |
| [remove(int index)](#remove-int-) |  |
| [toString()](#toString--) |  |
### readFrom(ResultSet resultSet) {#readFrom-java.sql.ResultSet-}
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
### get(int columnIndex) {#get-int-}
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
### get(String columnName) {#get-java.lang.String-}
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
### get(System.Data.DataColumn column) {#get-com.aspose.words.net.System.Data.DataColumn-}
```
public Object get(System.Data.DataColumn column)
```


Gets the data stored in the specified [DataColumn](../../com.aspose.words.net.system.data/datacolumn).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | A [DataColumn](../../com.aspose.words.net.system.data/datacolumn) that contains the data. |

**Returns:**
java.lang.Object - An java.lang.Object that contains the data.
### getTable() {#getTable--}
```
public System.Data.DataTable getTable()
```


Gets the [DataTable](../../com.aspose.words.net.system.data/datatable) for which this row has a schema.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable) - The [DataTable](../../com.aspose.words.net.system.data/datatable) to which this row belongs.
### getChildRows(System.Data.DataRelation relation) {#getChildRows-com.aspose.words.net.System.Data.DataRelation-}
```
public System.Data.DataRow[] getChildRows(System.Data.DataRelation relation)
```


Gets the child rows of this [DataRow](../../com.aspose.words.net.system.data/datarow) using the specified [DataRelation](../../com.aspose.words.net.system.data/datarelation).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation) | The [DataRelation](../../com.aspose.words.net.system.data/datarelation) to use. |

**Returns:**
com.aspose.words.net.System.Data.DataRow[] - An array of [DataRow](../../com.aspose.words.net.system.data/datarow) objects or an array of length zero.
### getParentRow(System.Data.DataRelation relation) {#getParentRow-com.aspose.words.net.System.Data.DataRelation-}
```
public System.Data.DataRow getParentRow(System.Data.DataRelation relation)
```


Gets the parent row of a [DataRow](../../com.aspose.words.net.system.data/datarow) using the specified [DataRelation](../../com.aspose.words.net.system.data/datarelation).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation) | The [DataRelation](../../com.aspose.words.net.system.data/datarelation) to use. |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow) - The parent [DataRow](../../com.aspose.words.net.system.data/datarow) of the current row.
### getParentRows(System.Data.DataRelation relation) {#getParentRows-com.aspose.words.net.System.Data.DataRelation-}
```
public System.Data.DataRow[] getParentRows(System.Data.DataRelation relation)
```


Gets the parent rows of a [DataRow](../../com.aspose.words.net.system.data/datarow) using the specified [DataRelation](../../com.aspose.words.net.system.data/datarelation).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation) | The [DataRelation](../../com.aspose.words.net.system.data/datarelation) to use. |

**Returns:**
com.aspose.words.net.System.Data.DataRow[] - An array of [DataRow](../../com.aspose.words.net.system.data/datarow) objects or an array of length zero.
### set(int value, Object columnIndex) {#set-int-java.lang.Object-}
```
public void set(int value, Object columnIndex)
```


Sets the data stored in the column specified by index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | An java.lang.Object that contains the data. |
| columnIndex | java.lang.Object | The zero-based index of the column. |

### set(String value, Object columnName) {#set-java.lang.String-java.lang.Object-}
```
public void set(String value, Object columnName)
```


Sets the data stored in the column specified by name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | An java.lang.Object that contains the data. |
| columnName | java.lang.Object | The name of the column. |

### set(System.Data.DataColumn value, Object column) {#set-com.aspose.words.net.System.Data.DataColumn-java.lang.Object-}
```
public void set(System.Data.DataColumn value, Object column)
```


Sets the data stored in the specified [DataColumn](../../com.aspose.words.net.system.data/datacolumn).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) | An java.lang.Object that contains the data. |
| column | java.lang.Object | A [DataColumn](../../com.aspose.words.net.system.data/datacolumn) that contains the data. |

### getRowState() {#getRowState--}
```
public int getRowState()
```


Gets the current state of the row with regard to its relationship to the [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection).

**Returns:**
int - One of the [DataRowState](../../com.aspose.words.net.system.data/datarowstate) values. The returned value is a bitwise combination of [DataRowState](../../com.aspose.words.net.system.data/datarowstate) constants.
### setRowState(int state) {#setRowState-int-}
```
public void setRowState(int state)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| state | int |  |

### delete() {#delete--}
```
public void delete()
```


Deletes the [DataRow](../../com.aspose.words.net.system.data/datarow).

### setOriginalValue(String columnName, Object data) {#setOriginalValue-java.lang.String-java.lang.Object-}
```
public void setOriginalValue(String columnName, Object data)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| columnName | java.lang.String |  |
| data | java.lang.Object |  |

### getOriginalValue(String columnName) {#getOriginalValue-java.lang.String-}
```
public Object getOriginalValue(String columnName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| columnName | java.lang.String |  |

**Returns:**
java.lang.Object
### getItemArray() {#getItemArray--}
```
public Object[] getItemArray()
```


Gets all the values for this row through an array.

**Returns:**
java.lang.Object[] - An array of type java.lang.Object.
### setItemArray(Object[] value) {#setItemArray-java.lang.Object---}
```
public void setItemArray(Object[] value)
```


Sets all the values for this row through an array.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.Object[] | An array of type java.lang.Object. |

### getKeyValues(System.Data.DataKey childKey) {#getKeyValues-com.aspose.words.net.System.Data.DataKey-}
```
public Object[] getKeyValues(System.Data.DataKey childKey)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| childKey | [DataKey](../../com.aspose.words.net.system.data/datakey) |  |

**Returns:**
java.lang.Object[]
### remove(int index) {#remove-int-}
```
public void remove(int index)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

### toString() {#toString--}
```
public String toString()
```




**Returns:**
java.lang.String
