---
title: "DataView"
linktitle: "DataView"
second_title: "Aspose.Words لـ Java"
description: "يمثل عرضًا مخصصًا قابلًا للربط بالبيانات من DataTable للفرز والتصفية والبحث والتحرير والتنقل في Java."
type: docs
weight: 28
url: /ar/java/com.aspose.words.net.system.data/dataview/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataView implements Iterable
```

يمثل عرضًا مخصصًا قابلًا للربط بالبيانات من [DataTable](../../com.aspose.words.net.system.data/datatable/) للفرز، والتصفية، والبحث، والتحرير، والتنقل.
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [DataView(System.Data.DataTable table)](#DataView-com.aspose.words.net.System.Data.DataTable) | ينشئ مثيلًا جديدًا من الفئة [DataView](../../com.aspose.words.net.system.data/dataview/) مع [DataTable](../../com.aspose.words.net.system.data/datatable/) المحدد. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [close()](#close) | يغلق [DataView](../../com.aspose.words.net.system.data/dataview/). |
| [get(int recordIndex)](#get-int) | يحصل على صف من البيانات من جدول محدد. |
| [getCount()](#getCount) | يحصل على عدد السجلات في [DataView](../../com.aspose.words.net.system.data/dataview/). |
| [getTable()](#getTable) | يحصل على مصدر [DataTable](../../com.aspose.words.net.system.data/datatable/). |
| [iterator()](#iterator) | يحصل على مُعدد لهذا [DataView](../../com.aspose.words.net.system.data/dataview/). |
### DataView(System.Data.DataTable table) {#DataView-com.aspose.words.net.System.Data.DataTable}
```
public DataView(System.Data.DataTable table)
```


ينشئ مثيلًا جديدًا من الفئة [DataView](../../com.aspose.words.net.system.data/dataview/) مع [DataTable](../../com.aspose.words.net.system.data/datatable/) المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable/) | [DataTable](../../com.aspose.words.net.system.data/datatable/) لإضافته إلى [DataView](../../com.aspose.words.net.system.data/dataview/). |

### close() {#close}
```
public void close()
```


يغلق [DataView](../../com.aspose.words.net.system.data/dataview/).

### get(int recordIndex) {#get-int}
```
public System.Data.DataRowView get(int recordIndex)
```


يحصل على صف من البيانات من جدول محدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| recordIndex | int | فهرس سجل في [DataTable](../../com.aspose.words.net.system.data/datatable/). |

**Returns:**
[DataRowView](../../com.aspose.words.net.system.data/datarowview/) - A [DataRowView](../../com.aspose.words.net.system.data/datarowview/) of the row that you want.
### getCount() {#getCount}
```
public int getCount()
```


يحصل على عدد السجلات في [DataView](../../com.aspose.words.net.system.data/dataview/).

**Returns:**
int - عدد السجلات في [DataView](../../com.aspose.words.net.system.data/dataview/).
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


يحصل على مصدر [DataTable](../../com.aspose.words.net.system.data/datatable/).

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that provides the data for this view.
### iterator() {#iterator}
```
public Iterator iterator()
```


يحصل على مُعدد لهذا [DataView](../../com.aspose.words.net.system.data/dataview/).

**Returns:**
java.util.Iterator - java.util.Iterator للتنقل عبر القائمة.
