---
title: "DataTable"
linktitle: "DataTable"
second_title: "Aspose.Words لـ Java"
description: "يمثل جدولًا واحدًا من البيانات في الذاكرة في جافا."
type: docs
weight: 25
url: /ar/java/com.aspose.words.net.system.data/datatable/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
[com.aspose.words.net.System.Data.DataTableEventListener](../../com.aspose.words.net.system.data/datatableeventlistener/)
```
public class DataTable implements System.Data.DataTableEventListener
```

يمثل جدولًا واحدًا من البيانات في الذاكرة
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [DataTable()](#DataTable) | ينشئ نسخة جديدة من فئة [DataTable](../../com.aspose.words.net.system.data/datatable/) دون أي معاملات. |
| [DataTable(String tableName)](#DataTable-java.lang.String) | ينشئ نسخة جديدة من فئة [DataTable](../../com.aspose.words.net.system.data/datatable/) بالاسم المحدد للجدول. |
| [DataTable(ResultSet resultSet)](#DataTable-java.sql.ResultSet) | ينشئ كائنًا عن طريق تغليف ResultSet المحدد. |
| [DataTable(ResultSet resultSet, String tableName)](#DataTable-java.sql.ResultSet-java.lang.String) | ينشئ كائنًا عن طريق تغليف ResultSet المحدد. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [acceptChanges()](#acceptChanges) | يطبق جميع التغييرات التي أُجريت على هذا الجدول منذ آخر مرة تم فيها استدعاء [acceptChanges()](../../com.aspose.words.net.system.data/datatable/\#acceptChanges). |
| [addEventListener(System.Data.DataTableEventListener listener)](#addEventListener-com.aspose.words.net.System.Data.DataTableEventListener) |  |
| [clearEventListneers()](#clearEventListneers) |  |
| [close()](#close) |  |
| [containsColumn(String columnName)](#containsColumn-java.lang.String) | تحقق مما إذا كان العمود المحدد موجودًا أم لا |
| [getChildRelations()](#getChildRelations) | يحصل على مجموعة العلاقات الفرعية لهذا [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [getColumnName(int index)](#getColumnName-int) | تمثيل مماثل لـ .Net DataTable.Columns[i].ColumnName |
| [getColumns()](#getColumns) | يحصل على مجموعة الأعمدة التي تنتمي إلى هذا الجدول. |
| [getColumnsCount()](#getColumnsCount) |  |
| [getConstraints()](#getConstraints) | يحصل على مجموعة القيود التي يحافظ عليها هذا الجدول. |
| [getDataSet()](#getDataSet) | يحصل على الـ [DataSet](../../com.aspose.words.net.system.data/dataset/) الذي ينتمي إليه هذا الجدول. |
| [getEnforceConstraints()](#getEnforceConstraints) |  |
| [getNamespace()](#getNamespace) | يحصل على مساحة الاسم لتمثيل XML للبيانات المخزنة في الـ [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [getParentRelations()](#getParentRelations) | يحصل على مجموعة العلاقات الأم لهذا [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [getPrimaryKey()](#getPrimaryKey) | يحصل على مصفوفة من الأعمدة التي تعمل كمفاتيح أساسية لجدول البيانات. |
| [getResultSet()](#getResultSet) | يرجع كائن Java ResultSet الأساسي. |
| [getRows()](#getRows) | يحصل على مجموعة الصفوف التي تنتمي إلى هذا الجدول. |
| [getTableName()](#getTableName) | يحصل على اسم الـ [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [newRow()](#newRow) | ينشئ [DataRow](../../com.aspose.words.net.system.data/datarow/) جديدًا بنفس المخطط كالجدول. |
| [onDataColumnDeleted(System.Data.DataColumn column)](#onDataColumnDeleted-com.aspose.words.net.System.Data.DataColumn) |  |
| [onDataColumnInserted(System.Data.DataColumn column)](#onDataColumnInserted-com.aspose.words.net.System.Data.DataColumn) |  |
| [onDataRowChanged(System.Data.DataRow row)](#onDataRowChanged-com.aspose.words.net.System.Data.DataRow) |  |
| [onDataRowDeleted(System.Data.DataRow row)](#onDataRowDeleted-com.aspose.words.net.System.Data.DataRow) |  |
| [onDataRowInserted(System.Data.DataRow row)](#onDataRowInserted-com.aspose.words.net.System.Data.DataRow) |  |
| [refresh()](#refresh) | يعيد تحميل جميع البيانات من ResultSet إذا كان موجودًا. |
| [setEnforceConstraints(boolean enforceConstraints)](#setEnforceConstraints-boolean) |  |
| [setNamespace(String value)](#setNamespace-java.lang.String) | يضبط مساحة الاسم لتمثيل XML للبيانات المخزنة في الـ [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [setPrimaryKey(System.Data.DataColumn[] value)](#setPrimaryKey-com.aspose.words.net.System.Data.DataColumn) | يضبط مصفوفة من الأعمدة التي تعمل كمفاتيح أساسية لجدول البيانات. |
| [setTableName(String value)](#setTableName-java.lang.String) | يضبط اسم الـ [DataTable](../../com.aspose.words.net.system.data/datatable/). |
### DataTable() {#DataTable}
```
public DataTable()
```


ينشئ نسخة جديدة من فئة [DataTable](../../com.aspose.words.net.system.data/datatable/) دون أي معاملات.

### DataTable(String tableName) {#DataTable-java.lang.String}
```
public DataTable(String tableName)
```


ينشئ نسخة جديدة من فئة [DataTable](../../com.aspose.words.net.system.data/datatable/) بالاسم المحدد للجدول.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| tableName | java.lang.String | الاسم الذي سيُعطى للجدول. إذا كان  tableName  فارغًا (null) أو سلسلةً فارغة، يتم إعطاء اسم افتراضي عند إضافته إلى الـ [DataTableCollection](../../com.aspose.words.net.system.data/datatablecollection/). |

### DataTable(ResultSet resultSet) {#DataTable-java.sql.ResultSet}
```
public DataTable(ResultSet resultSet)
```


ينشئ كائنًا عن طريق تغليف الـ ResultSet المحدد. يحاول استرجاع اسم الجدول من بيانات التعريف للعمود الأول في الـ ResultSet.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| resultSet | java.sql.ResultSet | مجموعة بيانات |

### DataTable(ResultSet resultSet, String tableName) {#DataTable-java.sql.ResultSet-java.lang.String}
```
public DataTable(ResultSet resultSet, String tableName)
```


ينشئ كائنًا عن طريق تغليف ResultSet المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| resultSet | java.sql.ResultSet | مجموعة بيانات |
| tableName | java.lang.String | اسم الجدول |

### acceptChanges() {#acceptChanges}
```
public void acceptChanges()
```


يطبق جميع التغييرات التي أُجريت على هذا الجدول منذ آخر مرة تم فيها استدعاء [acceptChanges()](../../com.aspose.words.net.system.data/datatable/\#acceptChanges).

### addEventListener(System.Data.DataTableEventListener listener) {#addEventListener-com.aspose.words.net.System.Data.DataTableEventListener}
```
public synchronized void addEventListener(System.Data.DataTableEventListener listener)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| listener | [DataTableEventListener](../../com.aspose.words.net.system.data/datatableeventlistener/) |  |

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


تحقق مما إذا كان العمود المحدد موجودًا أم لا

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| columnName | java.lang.String | اسم العمود |

**Returns:**
منطقي - `true` يعني يمكن العثور على العمود بواسطة `columnName` المعطى
### getChildRelations() {#getChildRelations}
```
public System.Data.DataRelationCollection getChildRelations()
```


يحصل على مجموعة العلاقات الفرعية لهذا [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Returns:**
[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) - A [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) that contains the child relations for the table. An empty collection is returned if no [DataRelation](../../com.aspose.words.net.system.data/datarelation/) objects exist.
### getColumnName(int index) {#getColumnName-int}
```
public String getColumnName(int index)
```


تمثيل مماثل لـ .Net DataTable.Columns[i].ColumnName

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفهرس | int | \- فهرس العمود |

**Returns:**
java.lang.String - اسم العمود وفقًا لفهرسه.
### getColumns() {#getColumns}
```
public System.Data.DataColumnCollection getColumns()
```


يحصل على مجموعة الأعمدة التي تنتمي إلى هذا الجدول.

**Returns:**
[DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) - A [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) that contains the collection of [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) objects for the table. An empty collection is returned if no [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) objects exist.
### getColumnsCount() {#getColumnsCount}
```
public int getColumnsCount()
```




**Returns:**
int - عدد الأعمدة
### getConstraints() {#getConstraints}
```
public System.Data.ConstraintCollection getConstraints()
```


يحصل على مجموعة القيود التي يحافظ عليها هذا الجدول.

**Returns:**
[ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/) - A [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/) that contains the collection of [Constraint](../../com.aspose.words.net.system.data/constraint/) objects for the table. An empty collection is returned if no [Constraint](../../com.aspose.words.net.system.data/constraint/) objects exist.
### getDataSet() {#getDataSet}
```
public System.Data.DataSet getDataSet()
```


يحصل على الـ [DataSet](../../com.aspose.words.net.system.data/dataset/) الذي ينتمي إليه هذا الجدول.

**Returns:**
[DataSet](../../com.aspose.words.net.system.data/dataset/) - The [DataSet](../../com.aspose.words.net.system.data/dataset/) to which this table belongs.
### getEnforceConstraints() {#getEnforceConstraints}
```
public boolean getEnforceConstraints()
```




**Returns:**
boolean - علامة تشير إلى ما إذا كان هناك انتهاك لقيود الفحص أم لا
### getNamespace() {#getNamespace}
```
public String getNamespace()
```


يحصل على مساحة الاسم لتمثيل XML للبيانات المخزنة في الـ [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Returns:**
java.lang.String - مساحة الاسم الخاصة بـ [DataTable](../../com.aspose.words.net.system.data/datatable/).
### getParentRelations() {#getParentRelations}
```
public System.Data.DataRelationCollection getParentRelations()
```


يحصل على مجموعة العلاقات الأم لهذا [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Returns:**
[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) - A [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) that contains the parent relations for the table. An empty collection is returned if no [DataRelation](../../com.aspose.words.net.system.data/datarelation/) objects exist.
### getPrimaryKey() {#getPrimaryKey}
```
public System.Data.DataColumn[] getPrimaryKey()
```


يحصل على مصفوفة من الأعمدة التي تعمل كمفاتيح أساسية لجدول البيانات.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - مصفوفة من كائنات [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).
### getResultSet() {#getResultSet}
```
public ResultSet getResultSet()
```


يرجع كائن Java ResultSet الأساسي. نود في المثالية العمل مع DataTable بطريقة .Net. لكن بعض المستخدمين وحتى بعض أكوادنا النموذجية يستخدمون هذه الخاصية.

**Returns:**
java.sql.ResultSet - الـ java.sql.ResultSet الأساسي
### getRows() {#getRows}
```
public System.Data.DataRowCollection getRows()
```


يحصل على مجموعة الصفوف التي تنتمي إلى هذا الجدول.

**Returns:**
[DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/) - A [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/) that contains [DataRow](../../com.aspose.words.net.system.data/datarow/) objects; otherwise a null value if no [DataRow](../../com.aspose.words.net.system.data/datarow/) objects exist.
### getTableName() {#getTableName}
```
public String getTableName()
```


يحصل على اسم الـ [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Returns:**
java.lang.String - اسم الـ [DataTable](../../com.aspose.words.net.system.data/datatable/).
### newRow() {#newRow}
```
public System.Data.DataRow newRow()
```


ينشئ [DataRow](../../com.aspose.words.net.system.data/datarow/) جديدًا بنفس المخطط كالجدول.

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - A [DataRow](../../com.aspose.words.net.system.data/datarow/) with the same schema as the [DataTable](../../com.aspose.words.net.system.data/datatable/).
### onDataColumnDeleted(System.Data.DataColumn column) {#onDataColumnDeleted-com.aspose.words.net.System.Data.DataColumn}
```
public void onDataColumnDeleted(System.Data.DataColumn column)
```


تحديث المستمع عند حذف DataColumn

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) |  |

### onDataColumnInserted(System.Data.DataColumn column) {#onDataColumnInserted-com.aspose.words.net.System.Data.DataColumn}
```
public void onDataColumnInserted(System.Data.DataColumn column)
```


تحديث المستمع عند إدراج DataColumn

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) |  |

### onDataRowChanged(System.Data.DataRow row) {#onDataRowChanged-com.aspose.words.net.System.Data.DataRow}
```
public void onDataRowChanged(System.Data.DataRow row)
```


تحديث المستمع عند تعديل DataRow

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

### onDataRowDeleted(System.Data.DataRow row) {#onDataRowDeleted-com.aspose.words.net.System.Data.DataRow}
```
public void onDataRowDeleted(System.Data.DataRow row)
```


تحديث المستمع عند حذف DataRow

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

### onDataRowInserted(System.Data.DataRow row) {#onDataRowInserted-com.aspose.words.net.System.Data.DataRow}
```
public void onDataRowInserted(System.Data.DataRow row)
```


تحديث المستمع عند إدراج DataRow

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

### refresh() {#refresh}
```
public void refresh()
```


يعيد تحميل جميع البيانات من ResultSet إذا كان موجودًا.

### setEnforceConstraints(boolean enforceConstraints) {#setEnforceConstraints-boolean}
```
public void setEnforceConstraints(boolean enforceConstraints)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| enforceConstraints | boolean | هي العلامة التي تشير إلى ما إذا كان هناك انتهاك لقيود الفحص أم لا |

### setNamespace(String value) {#setNamespace-java.lang.String}
```
public void setNamespace(String value)
```


يضبط مساحة الاسم لتمثيل XML للبيانات المخزنة في الـ [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | java.lang.String | مساحة الاسم الخاصة بـ [DataTable](../../com.aspose.words.net.system.data/datatable/). |

### setPrimaryKey(System.Data.DataColumn[] value) {#setPrimaryKey-com.aspose.words.net.System.Data.DataColumn}
```
public void setPrimaryKey(System.Data.DataColumn[] value)
```


يضبط مصفوفة من الأعمدة التي تعمل كمفاتيح أساسية لجدول البيانات.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | مصفوفة من كائنات [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |

### setTableName(String value) {#setTableName-java.lang.String}
```
public void setTableName(String value)
```


يضبط اسم الـ [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | java.lang.String | اسم الـ [DataTable](../../com.aspose.words.net.system.data/datatable/). |

