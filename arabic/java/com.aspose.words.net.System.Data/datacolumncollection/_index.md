---
title: "DataColumnCollection"
linktitle: "DataColumnCollection"
second_title: "Aspose.Words لـ Java"
description: "يمثل مجموعة من كائنات DataColumn الخاصة بـ DataTable في Java."
type: docs
weight: 15
url: /ar/java/com.aspose.words.net.system.data/datacolumncollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataColumnCollection implements Iterable
```

يمثل مجموعة من كائنات [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) الخاصة بـ [DataTable](../../com.aspose.words.net.system.data/datatable/).
## الطرق

| طريقة | الوصف |
| --- | --- |
| [add(System.Data.DataColumn column)](#add-com.aspose.words.net.System.Data.DataColumn) | ينشئ ويضيف كائن [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) المحدد إلى [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/). |
| [add(String columnName)](#add-java.lang.String) | ينشئ ويضيف كائن [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) يحمل الاسم المحدد إلى [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/). |
| [add(String columnName, Class type)](#add-java.lang.String-java.lang.Class) | ينشئ ويضيف كائن [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) يحمل الاسم والنوع المحددين إلى [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/). |
| [add(String columnName, Class type, int columnMapping, boolean allowAutoIncrement, boolean allowDBNull)](#add-java.lang.String-java.lang.Class-int-boolean-boolean) | ينشئ ويضيف كائن [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) بالاسم والنوع والقيم المحددة إلى مجموعة الأعمدة. |
| [clear()](#clear) | يمسح المجموعة من أي أعمدة. |
| [contains(String name)](#contains-java.lang.String) | يتحقق مما إذا كانت المجموعة تحتوي على عمود بالاسم المحدد. |
| [get(int index)](#get-int) | يحصل على [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) من المجموعة في الفهرس المحدد. |
| [get(String name)](#get-java.lang.String) | يحصل على [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) من المجموعة بالاسم المحدد. |
| [getCount()](#getCount) |  |
| [indexOf(System.Data.DataColumn column)](#indexOf-com.aspose.words.net.System.Data.DataColumn) | يحصل على فهرس العمود المحدد بالاسم. |
| [indexOf(String columnName)](#indexOf-java.lang.String) | يحصل على فهرس العمود الذي له الاسم المحدد (الاسم غير حساس لحالة الأحرف). |
| [iterator()](#iterator) |  |
| [remove(System.Data.DataColumn column)](#remove-com.aspose.words.net.System.Data.DataColumn) | يزيل الكائن [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) المحدد من المجموعة. |
| [remove(String name)](#remove-java.lang.String) | يزيل الكائن [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) الذي يحمل الاسم المحدد من المجموعة. |
### add(System.Data.DataColumn column) {#add-com.aspose.words.net.System.Data.DataColumn}
```
public void add(System.Data.DataColumn column)
```


ينشئ ويضيف كائن [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) المحدد إلى [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) المراد إضافته. |

### add(String columnName) {#add-java.lang.String}
```
public void add(String columnName)
```


ينشئ ويضيف كائن [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) يحمل الاسم المحدد إلى [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| columnName | java.lang.String | اسم العمود. |

### add(String columnName, Class type) {#add-java.lang.String-java.lang.Class}
```
public System.Data.DataColumn add(String columnName, Class type)
```


ينشئ ويضيف كائن [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) يحمل الاسم والنوع المحددين إلى [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| columnName | java.lang.String | [DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String) لاستخدامه عند إنشاء العمود. |
| type | java.lang.Class | [DataColumn.getDataType()](../../com.aspose.words.net.system.data/datacolumn/\#getDataType) / [DataColumn.setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\#setDataType-java.lang.Class) للعمود الجديد. |

**Returns:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn/) - The newly created [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).
### add(String columnName, Class type, int columnMapping, boolean allowAutoIncrement, boolean allowDBNull) {#add-java.lang.String-java.lang.Class-int-boolean-boolean}
```
public System.Data.DataColumn add(String columnName, Class type, int columnMapping, boolean allowAutoIncrement, boolean allowDBNull)
```


ينشئ ويضيف كائن [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) بالاسم والنوع والقيم المحددة إلى مجموعة الأعمدة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| columnName | java.lang.String | الاسم |
| نوع | java.lang.Class | نوع البيانات |
| تخطيط العمود | int | نوع تخطيط العمود |
| السماح بالزيادة التلقائية | boolean | هل يُسمح بالزيادة التلقائية |
| السماح بـ DBNull | boolean | هل يُسمح بقيمة DBNull |

**Returns:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn/) - created a [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) instance.
### clear() {#clear}
```
public void clear()
```


يمسح المجموعة من أي أعمدة.

### contains(String name) {#contains-java.lang.String}
```
public boolean contains(String name)
```


يتحقق مما إذا كانت المجموعة تحتوي على عمود بالاسم المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| name | java.lang.String | [DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String) للعمود المراد البحث عنه. |

**Returns:**
منطقي - true إذا كان هناك عمود بهذا الاسم؛ وإلا false.
### get(int index) {#get-int}
```
public System.Data.DataColumn get(int index)
```


يحصل على [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) من المجموعة في الفهرس المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفهرس | int | الفهرس الصفري للعمود المراد إرجاعه. |

**Returns:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn/) - The [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) at the specified index.
### get(String name) {#get-java.lang.String}
```
public System.Data.DataColumn get(String name)
```


يحصل على [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) من المجموعة بالاسم المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| name | java.lang.String | [DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String) للعمود المراد إرجاعه. |

**Returns:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn/) - The [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) in the collection with the specified [DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String); otherwise a null value if the [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) does not exist.
### getCount() {#getCount}
```
public int getCount()
```




**Returns:**
int - إجمالي عدد العناصر في مجموعة.
### indexOf(System.Data.DataColumn column) {#indexOf-com.aspose.words.net.System.Data.DataColumn}
```
public int indexOf(System.Data.DataColumn column)
```


يحصل على فهرس العمود المحدد بالاسم.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | اسم العمود المراد إرجاعه. |

**Returns:**
int - فهرس العمود المحدد بـ  column  إذا تم العثور عليه؛ وإلا -1.
### indexOf(String columnName) {#indexOf-java.lang.String}
```
public int indexOf(String columnName)
```


يحصل على فهرس العمود الذي له الاسم المحدد (الاسم غير حساس لحالة الأحرف).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| columnName | java.lang.String | اسم العمود المراد العثور عليه. |

**Returns:**
int - الفهرس الصفري للعمود الذي له الاسم المحدد، أو -1 إذا لم يكن العمود موجودًا في المجموعة.
### iterator() {#iterator}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator
### remove(System.Data.DataColumn column) {#remove-com.aspose.words.net.System.Data.DataColumn}
```
public void remove(System.Data.DataColumn column)
```


يزيل الكائن [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) المحدد من المجموعة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) المراد إزالته. |

### remove(String name) {#remove-java.lang.String}
```
public void remove(String name)
```


يزيل الكائن [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) الذي يحمل الاسم المحدد من المجموعة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الاسم | java.lang.String | اسم العمود المراد إزالته. |

