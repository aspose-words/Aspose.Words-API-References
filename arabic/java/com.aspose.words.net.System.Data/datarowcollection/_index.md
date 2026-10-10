---
title: "DataRowCollection"
linktitle: "DataRowCollection"
second_title: "Aspose.Words لـ Java"
description: "يمثل مجموعة من الصفوف لجدول DataTable في Java."
type: docs
weight: 21
url: /ar/java/com.aspose.words.net.system.data/datarowcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataRowCollection implements Iterable
```

يمثل مجموعة من الصفوف لــ [DataTable](../../com.aspose.words.net.system.data/datatable/).
## الطرق

| طريقة | الوصف |
| --- | --- |
| [add(System.Data.DataRow row)](#add-com.aspose.words.net.System.Data.DataRow) | يضيف الـ [DataRow](../../com.aspose.words.net.system.data/datarow/) المحدد إلى كائن [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/). |
| [add(Object[] values)](#add-java.lang.Object...) | ينشئ صفًا باستخدام القيم المحددة ويضيفه إلى [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/). |
| [clear()](#clear) | يمسح المجموعة من جميع الصفوف. |
| [find(Object[] keys)](#find-java.lang.Object) | يحصل على الصف الذي يحتوي على قيم المفتاح الأساسي المحددة. |
| [find(String primaryKeyValue)](#find-java.lang.String) | يحصل على الصف المحدد بواسطة قيمة المفتاح الأساسي. |
| [get(int index)](#get-int) | يحصل على الصف عند الفهرس المحدد. |
| [get(Object[] values)](#get-java.lang.Object) | يحصل على الصف الذي يحتوي على القيم المحددة. |
| [getCount()](#getCount) | يحصل على العدد الإجمالي لكائنات [DataRow](../../com.aspose.words.net.system.data/datarow/) في هذه المجموعة. |
| [insertAt(System.Data.DataRow row, int pos)](#insertAt-com.aspose.words.net.System.Data.DataRow-int) | يدرج صفًا جديدًا في المجموعة عند الموقع المحدد. |
| [iterator()](#iterator) | يحصل على java.util.Iterator لهذه المجموعة. |
| [removeAt(int index)](#removeAt-int) | يزيل الصف عند الفهرس المحدد من المجموعة. |
### add(System.Data.DataRow row) {#add-com.aspose.words.net.System.Data.DataRow}
```
public void add(System.Data.DataRow row)
```


يضيف الـ [DataRow](../../com.aspose.words.net.system.data/datarow/) المحدد إلى كائن [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) | الـ [DataRow](../../com.aspose.words.net.system.data/datarow/) المراد إضافته. |

### add(Object[] values) {#add-java.lang.Object...}
```
public void add(Object[] values)
```


ينشئ صفًا باستخدام القيم المحددة ويضيفه إلى [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| القيم | java.lang.Object[] | المصفوفة التي تحتوي على القيم المستخدمة لإنشاء الصف الجديد. |

### clear() {#clear}
```
public void clear()
```


يمسح المجموعة من جميع الصفوف.

### find(Object[] keys) {#find-java.lang.Object}
```
public System.Data.DataRow find(Object[] keys)
```


يحصل على الصف الذي يحتوي على قيم المفتاح الأساسي المحددة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| المفاتيح | java.lang.Object[] | مصفوفة من قيم المفتاح الأساسي للبحث. نوع المصفوفة هو Object. |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - A [DataRow](../../com.aspose.words.net.system.data/datarow/) object that contains the primary key values specified; otherwise a null value if the primary key value does not exist in the [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/).
### find(String primaryKeyValue) {#find-java.lang.String}
```
public System.Data.DataRow find(String primaryKeyValue)
```


يحصل على الصف المحدد بواسطة قيمة المفتاح الأساسي.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| primaryKeyValue | java.lang.String | قيمة المفتاح الأساسي لـ DataRow للعثور عليها. |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - A DataRow that contains the primary key value specified; otherwise a null value if the primary key value does not exist in the DataRowCollection.
### get(int index) {#get-int}
```
public System.Data.DataRow get(int index)
```


يحصل على الصف عند الفهرس المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفهرس | int | الفهرس الصفري للصف لإرجاعه. |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - The specified [DataRow](../../com.aspose.words.net.system.data/datarow/).
### get(Object[] values) {#get-java.lang.Object}
```
public System.Data.DataRow get(Object[] values)
```


يحصل على الصف الذي يحتوي على القيم المحددة. إذا كانت أعمدة المفتاح الأساسي موجودة فسيتم استخدام الفهرس. إذا لم يكن هناك فهرس فسيتم استخدام مسح خطي بسيط. كن حذرًا مع ذلك لأنه قد يستغرق وقتًا كبيرًا.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| القيم | java.lang.Object[] | بيانات الصف |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - found row or `null`
### getCount() {#getCount}
```
public int getCount()
```


يحصل على العدد الإجمالي لكائنات [DataRow](../../com.aspose.words.net.system.data/datarow/) في هذه المجموعة.

**Returns:**
int - إجمالي عدد كائنات [DataRow](../../com.aspose.words.net.system.data/datarow/) في هذه المجموعة.
### insertAt(System.Data.DataRow row, int pos) {#insertAt-com.aspose.words.net.System.Data.DataRow-int}
```
public void insertAt(System.Data.DataRow row, int pos)
```


يدرج صفًا جديدًا في المجموعة عند الموقع المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) | الـ [DataRow](../../com.aspose.words.net.system.data/datarow/) المراد إضافته. |
| pos | int | الموقع (الصفري) في المجموعة حيث تريد إضافة DataRow. |

### iterator() {#iterator}
```
public Iterator iterator()
```


يحصل على java.util.Iterator لهذه المجموعة.

**Returns:**
java.util.Iterator - java.util.Iterator لهذه المجموعة.
### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


يزيل الصف عند الفهرس المحدد من المجموعة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفهرس | int | فهرس الصف لإزالته. |

