---
title: "DataRow"
linktitle: "DataRow"
second_title: "Aspose.Words لـ Java"
description: "يمثل صفًا من البيانات في DataTable في Java."
type: docs
weight: 20
url: /ar/java/com.aspose.words.net.system.data/datarow/
---

**Inheritance:**
java.lang.Object
```
public class DataRow
```

يمثل صفًا من البيانات في [DataTable](../../com.aspose.words.net.system.data/datatable/).
## الطرق

| طريقة | الوصف |
| --- | --- |
| [delete()](#delete) | يحذف [DataRow](../../com.aspose.words.net.system.data/datarow/). |
| [get(System.Data.DataColumn column)](#get-com.aspose.words.net.System.Data.DataColumn) | يجلب البيانات المخزنة في [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) المحدد. |
| [get(int columnIndex)](#get-int) | يجلب البيانات المخزنة في العمود المحدد حسب الفهرس. |
| [get(String columnName)](#get-java.lang.String) | يجلب البيانات المخزنة في العمود المحدد حسب الاسم. |
| [getChildRows(System.Data.DataRelation relation)](#getChildRows-com.aspose.words.net.System.Data.DataRelation) | يجلب الصفوف الفرعية لهذا [DataRow](../../com.aspose.words.net.system.data/datarow/) باستخدام [DataRelation](../../com.aspose.words.net.system.data/datarelation/) المحدد. |
| [getItemArray()](#getItemArray) | يجلب جميع القيم لهذا الصف عبر مصفوفة. |
| [getKeyValues(System.Data.DataKey childKey)](#getKeyValues-com.aspose.words.net.System.Data.DataKey) |  |
| [getOriginalValue(String columnName)](#getOriginalValue-java.lang.String) |  |
| [getParentRow(System.Data.DataRelation relation)](#getParentRow-com.aspose.words.net.System.Data.DataRelation) | يجلب الصف الأب لـ [DataRow](../../com.aspose.words.net.system.data/datarow/) باستخدام [DataRelation](../../com.aspose.words.net.system.data/datarelation/) المحدد. |
| [getParentRows(System.Data.DataRelation relation)](#getParentRows-com.aspose.words.net.System.Data.DataRelation) | يجلب الصفوف الأب لـ [DataRow](../../com.aspose.words.net.system.data/datarow/) باستخدام [DataRelation](../../com.aspose.words.net.system.data/datarelation/) المحدد. |
| [getRowState()](#getRowState) | يجلب الحالة الحالية للصف فيما يتعلق بعلاقته بـ [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/). |
| [getTable()](#getTable) | يجلب [DataTable](../../com.aspose.words.net.system.data/datatable/) الذي يمتلك هذا الصف مخططًا. |
| [readFrom(ResultSet resultSet)](#readFrom-java.sql.ResultSet) | يقرأ القيم من java.sql.ResultSet |
| [remove(int index)](#remove-int) |  |
| [set(System.Data.DataColumn column, Object value)](#set-com.aspose.words.net.System.Data.DataColumn-java.lang.Object) | يضبط البيانات المخزنة في [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) المحدد. |
| [set(int columnIndex, Object value)](#set-int-java.lang.Object) | يضبط البيانات المخزنة في العمود المحدد حسب الفهرس. |
| [set(String columnName, Object value)](#set-java.lang.String-java.lang.Object) | يضبط البيانات المخزنة في العمود المحدد حسب الاسم. |
| [setItemArray(Object[] value)](#setItemArray-java.lang.Object) | يضبط جميع القيم لهذا الصف عبر مصفوفة. |
| [setOriginalValue(String columnName, Object data)](#setOriginalValue-java.lang.String-java.lang.Object) |  |
| [setRowState(int state)](#setRowState-int) |  |
| [toString()](#toString) |  |
### delete() {#delete}
```
public void delete()
```


يحذف [DataRow](../../com.aspose.words.net.system.data/datarow/).

### get(System.Data.DataColumn column) {#get-com.aspose.words.net.System.Data.DataColumn}
```
public Object get(System.Data.DataColumn column)
```


يجلب البيانات المخزنة في [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) يحتوي على البيانات. |

**Returns:**
java.lang.Object - كائن java.lang.Object يحتوي على البيانات.
### get(int columnIndex) {#get-int}
```
public Object get(int columnIndex)
```


يجلب البيانات المخزنة في العمود المحدد حسب الفهرس.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| columnIndex | int | الفهرس الصفري للعمود. |

**Returns:**
java.lang.Object - كائن java.lang.Object يحتوي على البيانات.
### get(String columnName) {#get-java.lang.String}
```
public Object get(String columnName)
```


يجلب البيانات المخزنة في العمود المحدد حسب الاسم.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| columnName | java.lang.String | اسم العمود. |

**Returns:**
java.lang.Object - كائن java.lang.Object يحتوي على البيانات.
### getChildRows(System.Data.DataRelation relation) {#getChildRows-com.aspose.words.net.System.Data.DataRelation}
```
public System.Data.DataRow[] getChildRows(System.Data.DataRelation relation)
```


يجلب الصفوف الفرعية لهذا [DataRow](../../com.aspose.words.net.system.data/datarow/) باستخدام [DataRelation](../../com.aspose.words.net.system.data/datarelation/) المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) للاستخدام. |

**Returns:**
com.aspose.words.net.System.Data.DataRow[] - مصفوفة من كائنات [DataRow](../../com.aspose.words.net.system.data/datarow/) أو مصفوفة بطول صفر.
### getItemArray() {#getItemArray}
```
public Object[] getItemArray()
```


يجلب جميع القيم لهذا الصف عبر مصفوفة.

**Returns:**
java.lang.Object[] - مصفوفة من نوع java.lang.Object.
### getKeyValues(System.Data.DataKey childKey) {#getKeyValues-com.aspose.words.net.System.Data.DataKey}
```
public Object[] getKeyValues(System.Data.DataKey childKey)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| childKey | [DataKey](../../com.aspose.words.net.system.data/datakey/) |  |

**Returns:**
java.lang.Object[]
### getOriginalValue(String columnName) {#getOriginalValue-java.lang.String}
```
public Object getOriginalValue(String columnName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| columnName | java.lang.String |  |

**Returns:**
java.lang.Object
### getParentRow(System.Data.DataRelation relation) {#getParentRow-com.aspose.words.net.System.Data.DataRelation}
```
public System.Data.DataRow getParentRow(System.Data.DataRelation relation)
```


يجلب الصف الأب لـ [DataRow](../../com.aspose.words.net.system.data/datarow/) باستخدام [DataRelation](../../com.aspose.words.net.system.data/datarelation/) المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) للاستخدام. |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - The parent [DataRow](../../com.aspose.words.net.system.data/datarow/) of the current row.
### getParentRows(System.Data.DataRelation relation) {#getParentRows-com.aspose.words.net.System.Data.DataRelation}
```
public System.Data.DataRow[] getParentRows(System.Data.DataRelation relation)
```


يجلب الصفوف الأب لـ [DataRow](../../com.aspose.words.net.system.data/datarow/) باستخدام [DataRelation](../../com.aspose.words.net.system.data/datarelation/) المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) للاستخدام. |

**Returns:**
com.aspose.words.net.System.Data.DataRow[] - مصفوفة من كائنات [DataRow](../../com.aspose.words.net.system.data/datarow/) أو مصفوفة بطول صفر.
### getRowState() {#getRowState}
```
public int getRowState()
```


يجلب الحالة الحالية للصف فيما يتعلق بعلاقته بـ [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/).

**Returns:**
int - أحد قيم [DataRowState](../../com.aspose.words.net.system.data/datarowstate/). القيمة المرجعة هي تركيبة بتية من ثوابت [DataRowState](../../com.aspose.words.net.system.data/datarowstate/).
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


يجلب [DataTable](../../com.aspose.words.net.system.data/datatable/) الذي يمتلك هذا الصف مخططًا.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The [DataTable](../../com.aspose.words.net.system.data/datatable/) to which this row belongs.
### readFrom(ResultSet resultSet) {#readFrom-java.sql.ResultSet}
```
public boolean readFrom(ResultSet resultSet)
```


يقرأ القيم من java.sql.ResultSet

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| resultSet | java.sql.ResultSet | مساحة التخزين للقراءة منها |

**Returns:**
boolean - true إذا لم تحدث أخطاء قراءة
### remove(int index) {#remove-int}
```
public void remove(int index)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفهرس | int |  |

### set(System.Data.DataColumn column, Object value) {#set-com.aspose.words.net.System.Data.DataColumn-java.lang.Object}
```
public void set(System.Data.DataColumn column, Object value)
```


يضبط البيانات المخزنة في [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) يحتوي على البيانات. |
| قيمة | java.lang.Object | كائن java.lang.Object يحتوي على البيانات. |

### set(int columnIndex, Object value) {#set-int-java.lang.Object}
```
public void set(int columnIndex, Object value)
```


يضبط البيانات المخزنة في العمود المحدد حسب الفهرس.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| columnIndex | int | الفهرس الصفري للعمود. |
| قيمة | java.lang.Object | كائن java.lang.Object يحتوي على البيانات. |

### set(String columnName, Object value) {#set-java.lang.String-java.lang.Object}
```
public void set(String columnName, Object value)
```


يضبط البيانات المخزنة في العمود المحدد حسب الاسم.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| columnName | java.lang.String | اسم العمود. |
| قيمة | java.lang.Object | كائن java.lang.Object يحتوي على البيانات. |

### setItemArray(Object[] value) {#setItemArray-java.lang.Object}
```
public void setItemArray(Object[] value)
```


يضبط جميع القيم لهذا الصف عبر مصفوفة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | java.lang.Object[] | مصفوفة من النوع java.lang.Object. |

### setOriginalValue(String columnName, Object data) {#setOriginalValue-java.lang.String-java.lang.Object}
```
public void setOriginalValue(String columnName, Object data)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| columnName | java.lang.String |  |
| بيانات | java.lang.Object |  |

### setRowState(int state) {#setRowState-int}
```
public void setRowState(int state)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الحالة | int |  |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
