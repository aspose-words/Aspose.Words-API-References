---
title: DataTable
second_title: Aspose.Words for Java API Reference
description: Represents one table of in-memory data.
type: docs
weight: 25
url: /java/com.aspose.words.net.system.data/datatable/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
[com.aspose.words.net.System.Data.DataTableEventListener](../../com.aspose.words.net.system.data/datatableeventlistener)
```
public class DataTable implements System.Data.DataTableEventListener
```

Represents one table of in-memory data.
## Constructors

| Constructor | Description |
| --- | --- |
| [DataTable()](#DataTable) | Initializes a new instance of the [DataTable](../../com.aspose.words.net.system.data/datatable) class with no arguments. |
| [DataTable(String tableName)](#DataTable-java.lang.String) | Initializes a new instance of the [DataTable](../../com.aspose.words.net.system.data/datatable) class with the specified table name. |
| [DataTable(ResultSet resultSet)](#DataTable-java.sql.ResultSet) | Creates an object by wrapping the specified ResultSet. |
| [DataTable(ResultSet resultSet, String tableName)](#DataTable-java.sql.ResultSet-java.lang.String) | Creates an object by wrapping the specified ResultSet. |
## Methods

| Method | Description |
| --- | --- |
| [acceptChanges()](#acceptChanges) | Commits all the changes made to this table since the last time [acceptChanges()](../../com.aspose.words.net.system.data/datatable\#acceptChanges) was called. |
| [addEventListener(System.Data.DataTableEventListener listener)](#addEventListener-com.aspose.words.net.System.Data.DataTableEventListener) |  |
| [clearEventListneers()](#clearEventListneers) |  |
| [close()](#close) |  |
| [containsColumn(String columnName)](#containsColumn-java.lang.String) | Check whether the given column exists or not |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getChildRelations()](#getChildRelations) | Gets the collection of child relations for this [DataTable](../../com.aspose.words.net.system.data/datatable). |
| [getClass()](#getClass) |  |
| [getColumnName(int index)](#getColumnName-int) | Analog for .Net DataTable.Columns[i].ColumnName |
| [getColumns()](#getColumns) | Gets the collection of columns that belong to this table. |
| [getColumnsCount()](#getColumnsCount) |  |
| [getConstraints()](#getConstraints) | Gets the collection of constraints maintained by this table. |
| [getDataSet()](#getDataSet) | Gets the [DataSet](../../com.aspose.words.net.system.data/dataset) to which this table belongs. |
| [getEnforceConstraints()](#getEnforceConstraints) |  |
| [getNamespace()](#getNamespace) | Gets the namespace for the XML representation of the data stored in the [DataTable](../../com.aspose.words.net.system.data/datatable). |
| [getParentRelations()](#getParentRelations) | Gets the collection of parent relations for this [DataTable](../../com.aspose.words.net.system.data/datatable). |
| [getPrimaryKey()](#getPrimaryKey) | Gets an array of columns that function as primary keys for the data table. |
| [getResultSet()](#getResultSet) | Returns the underlying Java ResultSet object. |
| [getRows()](#getRows) | Gets the collection of rows that belong to this table. |
| [getTableName()](#getTableName) | Gets the name of the [DataTable](../../com.aspose.words.net.system.data/datatable). |
| [hashCode()](#hashCode) |  |
| [newRow()](#newRow) | Creates a new [DataRow](../../com.aspose.words.net.system.data/datarow) with the same schema as the table. |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [onDataColumnDeleted(System.Data.DataColumn column)](#onDataColumnDeleted-com.aspose.words.net.System.Data.DataColumn) |  |
| [onDataColumnInserted(System.Data.DataColumn column)](#onDataColumnInserted-com.aspose.words.net.System.Data.DataColumn) |  |
| [onDataRowChanged(System.Data.DataRow row)](#onDataRowChanged-com.aspose.words.net.System.Data.DataRow) |  |
| [onDataRowDeleted(System.Data.DataRow row)](#onDataRowDeleted-com.aspose.words.net.System.Data.DataRow) |  |
| [onDataRowInserted(System.Data.DataRow row)](#onDataRowInserted-com.aspose.words.net.System.Data.DataRow) |  |
| [refresh()](#refresh) | Reloads all the data from ResultSet if it is present. |
| [setEnforceConstraints(boolean enforceConstraints)](#setEnforceConstraints-boolean) |  |
| [setNamespace(String value)](#setNamespace-java.lang.String) | Sets the namespace for the XML representation of the data stored in the [DataTable](../../com.aspose.words.net.system.data/datatable). |
| [setPrimaryKey(System.Data.DataColumn[] value)](#setPrimaryKey-com.aspose.words.net.System.Data.DataColumn) | Sets an array of columns that function as primary keys for the data table. |
| [setTableName(String value)](#setTableName-java.lang.String) | Sets the name of the [DataTable](../../com.aspose.words.net.system.data/datatable). |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### DataTable() {#DataTable}
```
public DataTable()
```


Initializes a new instance of the [DataTable](../../com.aspose.words.net.system.data/datatable) class with no arguments.

### DataTable(String tableName) {#DataTable-java.lang.String}
```
public DataTable(String tableName)
```


Initializes a new instance of the [DataTable](../../com.aspose.words.net.system.data/datatable) class with the specified table name.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| tableName | java.lang.String | The name to give the table. If  tableName  is null or an empty string, a default name is given when added to the [DataTableCollection](../../com.aspose.words.net.system.data/datatablecollection). |

### DataTable(ResultSet resultSet) {#DataTable-java.sql.ResultSet}
```
public DataTable(ResultSet resultSet)
```


Creates an object by wrapping the specified ResultSet. Attempts to retrieve the table name from the metadata of the first column of the ResultSet.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| resultSet | java.sql.ResultSet | data set |

### DataTable(ResultSet resultSet, String tableName) {#DataTable-java.sql.ResultSet-java.lang.String}
```
public DataTable(ResultSet resultSet, String tableName)
```


Creates an object by wrapping the specified ResultSet.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| resultSet | java.sql.ResultSet | data set |
| tableName | java.lang.String | name of the table |

### acceptChanges() {#acceptChanges}
```
public void acceptChanges()
```


Commits all the changes made to this table since the last time [acceptChanges()](../../com.aspose.words.net.system.data/datatable\#acceptChanges) was called.

### addEventListener(System.Data.DataTableEventListener listener) {#addEventListener-com.aspose.words.net.System.Data.DataTableEventListener}
```
public synchronized void addEventListener(System.Data.DataTableEventListener listener)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| listener | [DataTableEventListener](../../com.aspose.words.net.system.data/datatableeventlistener) |  |

### clearEventListneers() {#clearEventListneers}
```
public synchronized void clearEventListneers()
```




### close() {#close}
```
public void close()
```




### containsColumn(String columnName) {#containsColumn-java.lang.String}
```
public boolean containsColumn(String columnName)
```


Check whether the given column exists or not

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| columnName | java.lang.String | name of the column |

**Returns:**
boolean - `true` is column can be found by the given `columnName`
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
### getChildRelations() {#getChildRelations}
```
public System.Data.DataRelationCollection getChildRelations()
```


Gets the collection of child relations for this [DataTable](../../com.aspose.words.net.system.data/datatable).

**Returns:**
[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection) - A [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection) that contains the child relations for the table. An empty collection is returned if no [DataRelation](../../com.aspose.words.net.system.data/datarelation) objects exist.
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getColumnName(int index) {#getColumnName-int}
```
public String getColumnName(int index)
```


Analog for .Net DataTable.Columns[i].ColumnName

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | \- column's index |

**Returns:**
java.lang.String - column's name by its index.
### getColumns() {#getColumns}
```
public System.Data.DataColumnCollection getColumns()
```


Gets the collection of columns that belong to this table.

**Returns:**
[DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection) - A [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection) that contains the collection of [DataColumn](../../com.aspose.words.net.system.data/datacolumn) objects for the table. An empty collection is returned if no [DataColumn](../../com.aspose.words.net.system.data/datacolumn) objects exist.
### getColumnsCount() {#getColumnsCount}
```
public int getColumnsCount()
```




**Returns:**
int - columns count
### getConstraints() {#getConstraints}
```
public System.Data.ConstraintCollection getConstraints()
```


Gets the collection of constraints maintained by this table.

**Returns:**
[ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection) - A [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection) that contains the collection of [Constraint](../../com.aspose.words.net.system.data/constraint) objects for the table. An empty collection is returned if no [Constraint](../../com.aspose.words.net.system.data/constraint) objects exist.
### getDataSet() {#getDataSet}
```
public System.Data.DataSet getDataSet()
```


Gets the [DataSet](../../com.aspose.words.net.system.data/dataset) to which this table belongs.

**Returns:**
[DataSet](../../com.aspose.words.net.system.data/dataset) - The [DataSet](../../com.aspose.words.net.system.data/dataset) to which this table belongs.
### getEnforceConstraints() {#getEnforceConstraints}
```
public boolean getEnforceConstraints()
```




**Returns:**
boolean - flag which indicates whether check constraint violation or not
### getNamespace() {#getNamespace}
```
public String getNamespace()
```


Gets the namespace for the XML representation of the data stored in the [DataTable](../../com.aspose.words.net.system.data/datatable).

**Returns:**
java.lang.String - The namespace of the [DataTable](../../com.aspose.words.net.system.data/datatable).
### getParentRelations() {#getParentRelations}
```
public System.Data.DataRelationCollection getParentRelations()
```


Gets the collection of parent relations for this [DataTable](../../com.aspose.words.net.system.data/datatable).

**Returns:**
[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection) - A [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection) that contains the parent relations for the table. An empty collection is returned if no [DataRelation](../../com.aspose.words.net.system.data/datarelation) objects exist.
### getPrimaryKey() {#getPrimaryKey}
```
public System.Data.DataColumn[] getPrimaryKey()
```


Gets an array of columns that function as primary keys for the data table.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - An array of [DataColumn](../../com.aspose.words.net.system.data/datacolumn) objects.
### getResultSet() {#getResultSet}
```
public ResultSet getResultSet()
```


Returns the underlying Java ResultSet object. Ideally we would like to work with DataTable in .Net manner. But some users and even some ours sample code are using this property.

**Returns:**
java.sql.ResultSet - the underlying java.sql.ResultSet
### getRows() {#getRows}
```
public System.Data.DataRowCollection getRows()
```


Gets the collection of rows that belong to this table.

**Returns:**
[DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection) - A [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection) that contains [DataRow](../../com.aspose.words.net.system.data/datarow) objects; otherwise a null value if no [DataRow](../../com.aspose.words.net.system.data/datarow) objects exist.
### getTableName() {#getTableName}
```
public String getTableName()
```


Gets the name of the [DataTable](../../com.aspose.words.net.system.data/datatable).

**Returns:**
java.lang.String - The name of the [DataTable](../../com.aspose.words.net.system.data/datatable).
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### newRow() {#newRow}
```
public System.Data.DataRow newRow()
```


Creates a new [DataRow](../../com.aspose.words.net.system.data/datarow) with the same schema as the table.

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow) - A [DataRow](../../com.aspose.words.net.system.data/datarow) with the same schema as the [DataTable](../../com.aspose.words.net.system.data/datatable).
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### onDataColumnDeleted(System.Data.DataColumn column) {#onDataColumnDeleted-com.aspose.words.net.System.Data.DataColumn}
```
public void onDataColumnDeleted(System.Data.DataColumn column)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) |  |

### onDataColumnInserted(System.Data.DataColumn column) {#onDataColumnInserted-com.aspose.words.net.System.Data.DataColumn}
```
public void onDataColumnInserted(System.Data.DataColumn column)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) |  |

### onDataRowChanged(System.Data.DataRow row) {#onDataRowChanged-com.aspose.words.net.System.Data.DataRow}
```
public void onDataRowChanged(System.Data.DataRow row)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow) |  |

### onDataRowDeleted(System.Data.DataRow row) {#onDataRowDeleted-com.aspose.words.net.System.Data.DataRow}
```
public void onDataRowDeleted(System.Data.DataRow row)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow) |  |

### onDataRowInserted(System.Data.DataRow row) {#onDataRowInserted-com.aspose.words.net.System.Data.DataRow}
```
public void onDataRowInserted(System.Data.DataRow row)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow) |  |

### refresh() {#refresh}
```
public void refresh()
```


Reloads all the data from ResultSet if it is present.

### setEnforceConstraints(boolean enforceConstraints) {#setEnforceConstraints-boolean}
```
public void setEnforceConstraints(boolean enforceConstraints)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| enforceConstraints | boolean | is the flag which indicates whether check constraint violation or not |

### setNamespace(String value) {#setNamespace-java.lang.String}
```
public void setNamespace(String value)
```


Sets the namespace for the XML representation of the data stored in the [DataTable](../../com.aspose.words.net.system.data/datatable).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The namespace of the [DataTable](../../com.aspose.words.net.system.data/datatable). |

### setPrimaryKey(System.Data.DataColumn[] value) {#setPrimaryKey-com.aspose.words.net.System.Data.DataColumn}
```
public void setPrimaryKey(System.Data.DataColumn[] value)
```


Sets an array of columns that function as primary keys for the data table.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn) | An array of [DataColumn](../../com.aspose.words.net.system.data/datacolumn) objects. |

### setTableName(String value) {#setTableName-java.lang.String}
```
public void setTableName(String value)
```


Sets the name of the [DataTable](../../com.aspose.words.net.system.data/datatable).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of the [DataTable](../../com.aspose.words.net.system.data/datatable). |

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

