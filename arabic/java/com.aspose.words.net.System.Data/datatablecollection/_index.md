---
title: "DataTableCollection"
linktitle: "DataTableCollection"
second_title: "Aspose.Words لـ Java"
description: "يمثل مجموعة الجداول الخاصة بـ DataSet في Java."
type: docs
weight: 26
url: /ar/java/com.aspose.words.net.system.data/datatablecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataTableCollection implements Iterable
```

يمثل مجموعة الجداول الخاصة بـ [DataSet](../../com.aspose.words.net.system.data/dataset/).
## الطرق

| طريقة | الوصف |
| --- | --- |
| [add(System.Data.DataTable table)](#add-com.aspose.words.net.System.Data.DataTable) | يضيف DataTable المحدد إلى المجموعة. |
| [add(String name)](#add-java.lang.String) | ينشئ كائن [DataTable](../../com.aspose.words.net.system.data/datatable/) باستخدام الاسم المحدد ويضيفه إلى المجموعة. |
| [contains(String name)](#contains-java.lang.String) | يحصل على قيمة تشير إلى ما إذا كان كائن [DataTable](../../com.aspose.words.net.system.data/datatable/) بالاسم المحدد موجودًا في المجموعة. |
| [get(int index)](#get-int) | يحصل على كائن [DataTable](../../com.aspose.words.net.system.data/datatable/) في الفهرس المحدد. |
| [get(String name)](#get-java.lang.String) | يحصل على كائن [DataTable](../../com.aspose.words.net.system.data/datatable/) بالاسم المحدد. |
| [get(String name, String tableNamespace)](#get-java.lang.String-java.lang.String) | يحصل على كائن [DataTable](../../com.aspose.words.net.system.data/datatable/) بالاسم المحدد في المجال المحدد. |
| [getCount()](#getCount) |  |
| [iterator()](#iterator) |  |
| [remove(String name)](#remove-java.lang.String) | يزيل كائن [DataTable](../../com.aspose.words.net.system.data/datatable/) بالاسم المحدد من المجموعة. |
### add(System.Data.DataTable table) {#add-com.aspose.words.net.System.Data.DataTable}
```
public void add(System.Data.DataTable table)
```


يضيف DataTable المحدد إلى المجموعة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable/) | كائن DataTable المراد إضافته. |

### add(String name) {#add-java.lang.String}
```
public System.Data.DataTable add(String name)
```


ينشئ كائن [DataTable](../../com.aspose.words.net.system.data/datatable/) باستخدام الاسم المحدد ويضيفه إلى المجموعة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| name | java.lang.String | الاسم الذي سيُعطى لـ [DataTable](../../com.aspose.words.net.system.data/datatable/) المُنشأ. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The newly created [DataTable](../../com.aspose.words.net.system.data/datatable/).
### contains(String name) {#contains-java.lang.String}
```
public boolean contains(String name)
```


يحصل على قيمة تشير إلى ما إذا كان كائن [DataTable](../../com.aspose.words.net.system.data/datatable/) بالاسم المحدد موجودًا في المجموعة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| name | java.lang.String | اسم الـ [DataTable](../../com.aspose.words.net.system.data/datatable/) المراد العثور عليه. |

**Returns:**
منطقي - true إذا كان الجدول المحدد موجودًا؛ وإلا false.
### get(int index) {#get-int}
```
public System.Data.DataTable get(int index)
```


يحصل على كائن [DataTable](../../com.aspose.words.net.system.data/datatable/) في الفهرس المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| index | int | الفهرس الصفري للـ [DataTable](../../com.aspose.words.net.system.data/datatable/) المراد العثور عليه. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/).
### get(String name) {#get-java.lang.String}
```
public System.Data.DataTable get(String name)
```


يحصل على كائن [DataTable](../../com.aspose.words.net.system.data/datatable/) بالاسم المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الاسم | java.lang.String | اسم الـ DataTable المراد العثور عليه. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) with the specified name; otherwise null if the [DataTable](../../com.aspose.words.net.system.data/datatable/) does not exist.
### get(String name, String tableNamespace) {#get-java.lang.String-java.lang.String}
```
public System.Data.DataTable get(String name, String tableNamespace)
```


يحصل على كائن [DataTable](../../com.aspose.words.net.system.data/datatable/) بالاسم المحدد في المجال المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الاسم | java.lang.String | اسم الـ DataTable المراد العثور عليه. |
| tableNamespace | java.lang.String | اسم مساحة أسماء الـ [DataTable](../../com.aspose.words.net.system.data/datatable/) التي سيتم البحث فيها. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) with the specified name; otherwise null if the [DataTable](../../com.aspose.words.net.system.data/datatable/) does not exist.
### getCount() {#getCount}
```
public int getCount()
```




**Returns:**
عدد صحيح - إجمالي عدد العناصر في هذه المجموعة.
### iterator() {#iterator}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator
### remove(String name) {#remove-java.lang.String}
```
public System.Data.DataTable remove(String name)
```


يزيل كائن [DataTable](../../com.aspose.words.net.system.data/datatable/) بالاسم المحدد من المجموعة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| name | java.lang.String | اسم كائن [DataTable](../../com.aspose.words.net.system.data/datatable/) المراد إزالته. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/)
