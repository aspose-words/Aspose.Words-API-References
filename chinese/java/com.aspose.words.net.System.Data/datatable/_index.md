---
title: DataTable
second_title: Aspose.Words for Java API 参考
description:表示一个内存数据表。
type: docs
weight: 25
url: /zh/java/com.aspose.words.net.system.data/datatable/
---

**遗产:**
java.lang.Object

**All Implemented 界面s:**
[com.aspose.words.net.System.Data.DataTableEventListener](../../com.aspose.words.net.system.data/datatableeventlistener)
```
public class DataTable implements System.Data.DataTableEventListener
```

表示一个内存数据表。
## 构造函数s

| 构造函数 | 描述 |
| --- | --- |
| [DataTable()](#DataTable--) | 初始化一个新的实例[DataTable](../../com.aspose.words.net.system.data/datatable)没有参数的类。 |
| [DataTable(String tableName)](#DataTable-java.lang.String-) | 初始化一个新的实例[DataTable](../../com.aspose.words.net.system.data/datatable)具有指定表名的类。 |
| [DataTable(ResultSet resultSet)](#DataTable-java.sql.ResultSet-) | 通过包装指定的 ResultSet 创建一个对象。 |
| [DataTable(ResultSet resultSet, String tableName)](#DataTable-java.sql.ResultSet-java.lang.String-) | 通过包装指定的 ResultSet 创建一个对象。 |
## 方法s

| 方法 | 描述 |
| --- | --- |
| [acceptChanges()](#acceptChanges--) | 提交自上次以来对该表所做的所有更改[acceptChanges()](../../com.aspose.words.net.system.data/datatable\#acceptChanges--)被称为。 |
| [addEventListener(System.Data.DataTableEventListener listener)](#addEventListener-com.aspose.words.net.System.Data.DataTableEventListener-) |  |
| [clearEventListneers()](#clearEventListneers--) |  |
| [close()](#close--) |  |
| [containsColumn(String columnName)](#containsColumn-java.lang.String-) | 检查给定列是否存在 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getChildRelations()](#getChildRelations--) | 获取此子关系的集合[DataTable](../../com.aspose.words.net.system.data/datatable). |
| [get班级()](#get班级--) |  |
| [getColumnName(int index)](#getColumnName-int-) | .Net DataTable.Columns 的模拟[i].ColumnName |
| [getColumns()](#getColumns--) | 获取属于此表的列的集合。 |
| [getColumnsCount()](#getColumnsCount--) |  |
| [getConstraints()](#getConstraints--) | 获取此表维护的约束集合。 |
| [getDataSet()](#getDataSet--) | 获取[DataSet](../../com.aspose.words.net.system.data/dataset)此表所属的。 |
| [getEnforceConstraints()](#getEnforceConstraints--) |  |
| [getNamespace()](#getNamespace--) | 获取存储在[DataTable](../../com.aspose.words.net.system.data/datatable). |
| [getParentRelations()](#getParentRelations--) | 获取此父关系的集合[DataTable](../../com.aspose.words.net.system.data/datatable). |
| [getPrimaryKey()](#getPrimaryKey--) | 获取用作数据表主键的列数组。 |
| [getResultSet()](#getResultSet--) | 返回底层 Java ResultSet 对象。 |
| [getRows()](#getRows--) | 获取属于此表的行的集合。 |
| [getTableName()](#getTableName--) | 获取名称[DataTable](../../com.aspose.words.net.system.data/datatable). |
| [hashCode()](#hashCode--) |  |
| [newRow()](#newRow--) | 创建一个新的[DataRow](../../com.aspose.words.net.system.data/datarow)具有与表相同的架构。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [onDataColumnDeleted(System.Data.DataColumn column)](#onDataColumnDeleted-com.aspose.words.net.System.Data.DataColumn-) |  |
| [onDataColumnInserted(System.Data.DataColumn column)](#onDataColumnInserted-com.aspose.words.net.System.Data.DataColumn-) |  |
| [onDataRowChanged(System.Data.DataRow row)](#onDataRowChanged-com.aspose.words.net.System.Data.DataRow-) |  |
| [onDataRowDeleted(System.Data.DataRow row)](#onDataRowDeleted-com.aspose.words.net.System.Data.DataRow-) |  |
| [onDataRowInserted(System.Data.DataRow row)](#onDataRowInserted-com.aspose.words.net.System.Data.DataRow-) |  |
| [refresh()](#refresh--) | 如果存在，则从 ResultSet 重新加载所有数据。 |
| [setEnforceConstraints(boolean enforceConstraints)](#setEnforceConstraints-boolean-) |  |
| [setNamespace(String value)](#setNamespace-java.lang.String-) | 为存储在[DataTable](../../com.aspose.words.net.system.data/datatable). |
| [setPrimaryKey(System.Data.DataColumn[] value)](#setPrimaryKey-com.aspose.words.net.System.Data.DataColumn---) | 设置用作数据表主键的列数组。 |
| [setTableName(String value)](#setTableName-java.lang.String-) | 设置名称[DataTable](../../com.aspose.words.net.system.data/datatable). |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### DataTable() {#DataTable--}
```
public DataTable()
```


初始化一个新的实例[DataTable](../../com.aspose.words.net.system.data/datatable)没有参数的类。

### DataTable(String tableName) {#DataTable-java.lang.String-}
```
public DataTable(String tableName)
```


初始化一个新的实例[DataTable](../../com.aspose.words.net.system.data/datatable)具有指定表名的类。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| tableName | java.lang.String | 表的名称。如果 tableName 为 null 或空字符串，则添加到[DataTableCollection](../../com.aspose.words.net.system.data/datatablecollection). |

### DataTable(ResultSet resultSet) {#DataTable-java.sql.ResultSet-}
```
public DataTable(ResultSet resultSet)
```


通过包装指定的 ResultSet 创建一个对象。尝试从 ResultSet 第一列的元数据中检索表名。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| resultSet | java.sql.ResultSet | 数据集 |

### DataTable(ResultSet resultSet, String tableName) {#DataTable-java.sql.ResultSet-java.lang.String-}
```
public DataTable(ResultSet resultSet, String tableName)
```


通过包装指定的 ResultSet 创建一个对象。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| resultSet | java.sql.ResultSet | 数据集 |
| tableName | java.lang.String | 表名 |

### acceptChanges() {#acceptChanges--}
```
public void acceptChanges()
```


提交自上次以来对该表所做的所有更改[acceptChanges()](../../com.aspose.words.net.system.data/datatable\#acceptChanges--)被称为。

### addEventListener(System.Data.DataTableEventListener listener) {#addEventListener-com.aspose.words.net.System.Data.DataTableEventListener-}
```
public synchronized void addEventListener(System.Data.DataTableEventListener listener)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| listener | [DataTableEventListener](../../com.aspose.words.net.system.data/datatableeventlistener) |  |

### clearEventListneers() {#clearEventListneers--}
```
public synchronized void clearEventListneers()
```




### close() {#close--}
```
public void close()
```




### containsColumn(String columnName) {#containsColumn-java.lang.String-}
```
public boolean containsColumn(String columnName)
```


检查给定列是否存在

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| columnName | java.lang.String | 列名 |

**退货:**
布尔值 -`true`is 列可以通过给定找到`columnName`
### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货:**
布尔值
### getChildRelations() {#getChildRelations--}
```
public System.Data.DataRelationCollection getChildRelations()
```


获取此子关系的集合[DataTable](../../com.aspose.words.net.system.data/datatable).

**退货:**
[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection) - 一个[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection)包含表的子关系。如果没有，则返回一个空集合[DataRelation](../../com.aspose.words.net.system.data/datarelation)对象存在。
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getColumnName(int index) {#getColumnName-int-}
```
public String getColumnName(int index)
```


.Net DataTable.Columns 的模拟[i].ColumnName

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | \列的索引 |

**退货:**
java.lang.String - 列的索引名称。
### getColumns() {#getColumns--}
```
public System.Data.DataColumnCollection getColumns()
```


获取属于此表的列的集合。

**退货:**
[DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection) - 一个[DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection)包含的集合[DataColumn](../../com.aspose.words.net.system.data/datacolumn)表的对象。如果没有，则返回一个空集合[DataColumn](../../com.aspose.words.net.system.data/datacolumn)对象存在。
### getColumnsCount() {#getColumnsCount--}
```
public int getColumnsCount()
```




**退货:**
int - 列数
### getConstraints() {#getConstraints--}
```
public System.Data.ConstraintCollection getConstraints()
```


获取此表维护的约束集合。

**退货:**
[ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection) - 一个[ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection)包含的集合[Constraint](../../com.aspose.words.net.system.data/constraint)表的对象。如果没有，则返回一个空集合[Constraint](../../com.aspose.words.net.system.data/constraint)对象存在。
### getDataSet() {#getDataSet--}
```
public System.Data.DataSet getDataSet()
```


获取[DataSet](../../com.aspose.words.net.system.data/dataset)此表所属的。

**退货:**
[DataSet](../../com.aspose.words.net.system.data/dataset) - 这[DataSet](../../com.aspose.words.net.system.data/dataset)此表所属的。
### getEnforceConstraints() {#getEnforceConstraints--}
```
public boolean getEnforceConstraints()
```




**退货:**
boolean - 指示是否违反检查约束的标志
### getNamespace() {#getNamespace--}
```
public String getNamespace()
```


获取存储在[DataTable](../../com.aspose.words.net.system.data/datatable).

**退货:**
 java.lang.String - 的命名空间[DataTable](../../com.aspose.words.net.system.data/datatable).
### getParentRelations() {#getParentRelations--}
```
public System.Data.DataRelationCollection getParentRelations()
```


获取此父关系的集合[DataTable](../../com.aspose.words.net.system.data/datatable).

**退货:**
[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection) - 一个[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection)包含表的父关系。如果没有，则返回一个空集合[DataRelation](../../com.aspose.words.net.system.data/datarelation)对象存在。
### getPrimaryKey() {#getPrimaryKey--}
```
public System.Data.DataColumn[] getPrimaryKey()
```


获取用作数据表主键的列数组。

**退货:**
com.aspose.words.net.System.Data.DataColumn[ ] - 一个数组[DataColumn](../../com.aspose.words.net.system.data/datacolumn)对象。
### getResultSet() {#getResultSet--}
```
public ResultSet getResultSet()
```


返回底层 Java ResultSet 对象。理想情况下，我们希望以 .Net 方式使用 DataTable。但是一些用户，甚至我们的一些示例代码正在使用这个属性。

**退货:**
java.sql.ResultSet - 底层 java.sql.ResultSet
### getRows() {#getRows--}
```
public System.Data.DataRowCollection getRows()
```


获取属于此表的行的集合。

**退货:**
[DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection) - 一个[DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection)包含[DataRow](../../com.aspose.words.net.system.data/datarow)物体；如果没有，则为空值[DataRow](../../com.aspose.words.net.system.data/datarow)对象存在。
### getTableName() {#getTableName--}
```
public String getTableName()
```


获取名称[DataTable](../../com.aspose.words.net.system.data/datatable).

**退货:**
java.lang.String - 的名称[DataTable](../../com.aspose.words.net.system.data/datatable).
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### newRow() {#newRow--}
```
public System.Data.DataRow newRow()
```


创建一个新的[DataRow](../../com.aspose.words.net.system.data/datarow)具有与表相同的架构。

**退货:**
[DataRow](../../com.aspose.words.net.system.data/datarow) - 一个[DataRow](../../com.aspose.words.net.system.data/datarow)具有与[DataTable](../../com.aspose.words.net.system.data/datatable).
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### onDataColumnDeleted(System.Data.DataColumn column) {#onDataColumnDeleted-com.aspose.words.net.System.Data.DataColumn-}
```
public void onDataColumnDeleted(System.Data.DataColumn column)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) |  |

### onDataColumnInserted(System.Data.DataColumn column) {#onDataColumnInserted-com.aspose.words.net.System.Data.DataColumn-}
```
public void onDataColumnInserted(System.Data.DataColumn column)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn) |  |

### onDataRowChanged(System.Data.DataRow row) {#onDataRowChanged-com.aspose.words.net.System.Data.DataRow-}
```
public void onDataRowChanged(System.Data.DataRow row)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow) |  |

### onDataRowDeleted(System.Data.DataRow row) {#onDataRowDeleted-com.aspose.words.net.System.Data.DataRow-}
```
public void onDataRowDeleted(System.Data.DataRow row)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow) |  |

### onDataRowInserted(System.Data.DataRow row) {#onDataRowInserted-com.aspose.words.net.System.Data.DataRow-}
```
public void onDataRowInserted(System.Data.DataRow row)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow) |  |

### refresh() {#refresh--}
```
public void refresh()
```


如果存在，则从 ResultSet 重新加载所有数据。

### setEnforceConstraints(boolean enforceConstraints) {#setEnforceConstraints-boolean-}
```
public void setEnforceConstraints(boolean enforceConstraints)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| enforceConstraints | boolean | 是指示是否违反检查约束的标志 |

### setNamespace(String value) {#setNamespace-java.lang.String-}
```
public void setNamespace(String value)
```


为存储在[DataTable](../../com.aspose.words.net.system.data/datatable).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 的命名空间[DataTable](../../com.aspose.words.net.system.data/datatable). |

### setPrimaryKey(System.Data.DataColumn[] value) {#setPrimaryKey-com.aspose.words.net.System.Data.DataColumn---}
```
public void setPrimaryKey(System.Data.DataColumn[] value)
```


设置用作数据表主键的列数组。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn) | 一个数组[DataColumn](../../com.aspose.words.net.system.data/datacolumn)对象。 |

### setTableName(String value) {#setTableName-java.lang.String-}
```
public void setTableName(String value)
```


设置名称[DataTable](../../com.aspose.words.net.system.data/datatable).

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 的名称[DataTable](../../com.aspose.words.net.system.data/datatable). |

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
