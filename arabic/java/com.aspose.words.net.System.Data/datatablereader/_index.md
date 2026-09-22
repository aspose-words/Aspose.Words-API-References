---
title: "DataTableReader"
linktitle: "DataTableReader"
second_title: "Aspose.Words لـ Java"
description: "DataTableReader يحصل على محتويات كائن أو أكثر من DataTable في شكل مجموعة نتائج واحدة أو أكثر للقراءة فقط وتقدم للأمام في Java."
type: docs
weight: 27
url: /ar/java/com.aspose.words.net.system.data/datatablereader/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.net.System.Data.Common.DbDataReader](../../com.aspose.words.net.system.data.common/dbdatareader/)
```
public class DataTableReader extends System.Data.Common.DbDataReader
```

[DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) يحصل على محتويات كائن أو أكثر من [DataTable](../../com.aspose.words.net.system.data/datatable/) في شكل مجموعة نتائج واحدة أو أكثر للقراءة فقط وتقدم للأمام.
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [DataTableReader(System.Data.DataTable dataTable)](#DataTableReader-com.aspose.words.net.System.Data.DataTable) | يُنشئ مثيلاً جديداً من الفئة [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) باستخدام البيانات من [DataTable](../../com.aspose.words.net.system.data/datatable/) المزوَّدة. |
| [DataTableReader(System.Data.DataTable[] dataTables)](#DataTableReader-com.aspose.words.net.System.Data.DataTable) | يُنشئ مثيلًا جديدًا من الفئة [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) باستخدام المصفوفة المقدمة من كائنات [DataTable](../../com.aspose.words.net.system.data/datatable/). |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [close()](#close) | يغلق [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) الحالي. |
| [get(int ordinal)](#get-int) | يحصل على قيمة العمود المحدد بتنسيقه الأصلي بناءً على ترتيب العمود. |
| [get(String name)](#get-java.lang.String) | يحصل على قيمة العمود المحدد بتنسيقه الأصلي بناءً على اسم العمود. |
| [getDepth()](#getDepth) | عمق التعشيش للصف الحالي في [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/). |
| [getFieldCount()](#getFieldCount) | يعيد عدد الأعمدة في الصف الحالي. |
| [getFieldType(int ordinal)](#getFieldType-int) | يحصل على الـ java.lang.Class الذي يمثل نوع البيانات للكائن. |
| [getName(int ordinal)](#getName-int) | يحصل على قيمة العمود المحدد كـ java.lang.String. |
| [getRecordsAffected()](#getRecordsAffected) | يحصل على عدد الصفوف التي تم إدراجها أو تعديلها أو حذفها نتيجة تنفيذ جملة SQL. |
| [getSchemaTable()](#getSchemaTable) | يعيد [DataTable](../../com.aspose.words.net.system.data/datatable/) الذي يصف بيانات تعريف الأعمدة لـ [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/). |
| [getValue(int ordinal)](#getValue-int) | يحصل على قيمة العمود المحدد بتنسيقه الأصلي. |
| [hasRows()](#hasRows) | يحصل على قيمة تشير إلى ما إذا كان [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) يحتوي على صف واحد أو أكثر. |
| [isClosed()](#isClosed) | يحصل على قيمة تشير إلى ما إذا كان [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) مغلقًا. |
| [iterator()](#iterator) | يعيد عدادًا يمكن استخدامه للتنقل عبر مجموعة العناصر. |
| [nextResult()](#nextResult) | يتقدم [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) إلى مجموعة النتائج التالية، إن وجدت. |
| [read()](#read) | يتقدم [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) إلى السجل التالي. |
### DataTableReader(System.Data.DataTable dataTable) {#DataTableReader-com.aspose.words.net.System.Data.DataTable}
```
public DataTableReader(System.Data.DataTable dataTable)
```


يُنشئ مثيلاً جديداً من الفئة [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) باستخدام البيانات من [DataTable](../../com.aspose.words.net.system.data/datatable/) المزوَّدة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | الـ [DataTable](../../com.aspose.words.net.system.data/datatable/) الذي يحصل منه [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) الجديد على مجموعة النتائج الخاصة به. |

### DataTableReader(System.Data.DataTable[] dataTables) {#DataTableReader-com.aspose.words.net.System.Data.DataTable}
```
public DataTableReader(System.Data.DataTable[] dataTables)
```


يُنشئ مثيلًا جديدًا من الفئة [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) باستخدام المصفوفة المقدمة من كائنات [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| dataTables | [DataTable\[\]](../../com.aspose.words.net.system.data/datatable/) | المصفوفة من كائنات [DataTable](../../com.aspose.words.net.system.data/datatable/) التي تزود النتائج لكائن [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) الجديد. |

### close() {#close}
```
public void close()
```


يغلق [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) الحالي.

### get(int ordinal) {#get-int}
```
public Object get(int ordinal)
```


يحصل على قيمة العمود المحدد بتنسيقه الأصلي بناءً على ترتيب العمود.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الترتيب | int | ترتيب العمود القائم على الصفر. |

**Returns:**
java.lang.Object - قيمة العمود المحدد بتنسيقه الأصلي.
### get(String name) {#get-java.lang.String}
```
public Object get(String name)
```


يحصل على قيمة العمود المحدد بتنسيقه الأصلي بناءً على اسم العمود.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الاسم | java.lang.String | اسم العمود. |

**Returns:**
java.lang.Object - قيمة العمود المحدد بتنسيقه الأصلي.
### getDepth() {#getDepth}
```
public int getDepth()
```


عمق التعشيش للصف الحالي في [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/).

**Returns:**
int - عمق التعشيش للصف الحالي؛ دائمًا صفر.
### getFieldCount() {#getFieldCount}
```
public int getFieldCount()
```


يعيد عدد الأعمدة في الصف الحالي.

**Returns:**
int - عندما لا يكون الموقع في مجموعة نتائج صالحة، 0؛ وإلا عدد الأعمدة في الصف الحالي.
### getFieldType(int ordinal) {#getFieldType-int}
```
public Class getFieldType(int ordinal)
```


يحصل على الـ java.lang.Class الذي يمثل نوع البيانات للكائن.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الترتيب | int | ترتيب العمود القائم على الصفر. |

**Returns:**
java.lang.Class - الـ java.lang.Class الذي يمثل نوع البيانات للكائن.
### getName(int ordinal) {#getName-int}
```
public String getName(int ordinal)
```


يحصل على قيمة العمود المحدد كـ java.lang.String.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الترتيب | int | ترتيب العمود القائم على الصفر |

**Returns:**
java.lang.String - اسم العمود المحدد.
### getRecordsAffected() {#getRecordsAffected}
```
public int getRecordsAffected()
```


يحصل على عدد الصفوف التي تم إدراجها أو تعديلها أو حذفها نتيجة تنفيذ جملة SQL.

**Returns:**
int - الـ [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) لا يدعم هذه الخاصية ويعيد دائمًا 0.
### getSchemaTable() {#getSchemaTable}
```
public System.Data.DataTable getSchemaTable()
```


يعيد [DataTable](../../com.aspose.words.net.system.data/datatable/) الذي يصف بيانات تعريف الأعمدة لـ [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/).

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that describes the column metadata.
### getValue(int ordinal) {#getValue-int}
```
public Object getValue(int ordinal)
```


يحصل على قيمة العمود المحدد بتنسيقه الأصلي.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الترتيب | int | ترتيب العمود القائم على الصفر |

**Returns:**
java.lang.Object - قيمة العمود المحدد. تُعيد هذه الطريقة DBNull للأعمدة الفارغة.
### hasRows() {#hasRows}
```
public boolean hasRows()
```


يحصل على قيمة تشير إلى ما إذا كان [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) يحتوي على صف واحد أو أكثر.

**Returns:**
boolean - true إذا كان الـ [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) يحتوي على صف واحد أو أكثر؛ وإلا false.
### isClosed() {#isClosed}
```
public boolean isClosed()
```


يحصل على قيمة تشير إلى ما إذا كان [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) مغلقًا.

**Returns:**
boolean - تُعيد true إذا كان الـ [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) مغلقًا؛ وإلا false.
### iterator() {#iterator}
```
public Iterator iterator()
```


يعيد عدادًا يمكن استخدامه للتنقل عبر مجموعة العناصر.

**Returns:**
java.util.Iterator - كائن java.util.Iterator يمثل مجموعة العناصر.
### nextResult() {#nextResult}
```
public boolean nextResult()
```


يتقدم [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) إلى مجموعة النتائج التالية، إن وجدت.

**Returns:**
boolean - true إذا كان هناك مجموعة نتائج أخرى؛ وإلا false.
### read() {#read}
```
public boolean read()
```


يتقدم [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) إلى السجل التالي.

**Returns:**
boolean - true إذا كان هناك صف آخر للقراءة؛ وإلا false.
