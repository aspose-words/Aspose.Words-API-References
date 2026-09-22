---
title: "ConstraintCollection"
linktitle: "ConstraintCollection"
second_title: "Aspose.Words لـ Java"
description: "يمثل مجموعة من القيود لجدول البيانات DataTable في Java."
type: docs
weight: 11
url: /ar/java/com.aspose.words.net.system.data/constraintcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ConstraintCollection implements Iterable
```

يمثل مجموعة من القيود لــ [DataTable](../../com.aspose.words.net.system.data/datatable/).
## الطرق

| طريقة | الوصف |
| --- | --- |
| [add(System.Data.Constraint constraint)](#add-com.aspose.words.net.System.Data.Constraint) | يضيف الكائن [Constraint](../../com.aspose.words.net.system.data/constraint/) المحدد إلى المجموعة. |
| [contains(System.Data.Constraint cc)](#contains-com.aspose.words.net.System.Data.Constraint) | يشير إلى ما إذا كان كائن Constraint المحدد بالاسم موجودًا في المجموعة. |
| [get(int index)](#get-int) | يحصل على [Constraint](../../com.aspose.words.net.system.data/constraint/) من المجموعة عند الفهرس المحدد. |
| [get(String name)](#get-java.lang.String) | يحصل على [Constraint](../../com.aspose.words.net.system.data/constraint/) من المجموعة بالاسم المحدد. |
| [getCount()](#getCount) | يحصل على العدد الإجمالي للعناصر في مجموعة. |
| [iterator()](#iterator) |  |
| [remove(System.Data.Constraint constraint)](#remove-com.aspose.words.net.System.Data.Constraint) | يزيل [Constraint](../../com.aspose.words.net.system.data/constraint/) المحدد من المجموعة. |
### add(System.Data.Constraint constraint) {#add-com.aspose.words.net.System.Data.Constraint}
```
public void add(System.Data.Constraint constraint)
```


يضيف الكائن [Constraint](../../com.aspose.words.net.system.data/constraint/) المحدد إلى المجموعة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| constraint | [Constraint](../../com.aspose.words.net.system.data/constraint/) | الـ Constraint للإضافة. |

### contains(System.Data.Constraint cc) {#contains-com.aspose.words.net.System.Data.Constraint}
```
public boolean contains(System.Data.Constraint cc)
```


يشير إلى ما إذا كان كائن Constraint المحدد بالاسم موجودًا في المجموعة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| cc | [Constraint](../../com.aspose.words.net.system.data/constraint/) | الـ Constraint للإزالة. |

**Returns:**
boolean - true إذا كانت المجموعة تحتوي على القيد المحدد؛ وإلا false.
### get(int index) {#get-int}
```
public System.Data.Constraint get(int index)
```


يحصل على [Constraint](../../com.aspose.words.net.system.data/constraint/) من المجموعة عند الفهرس المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الفهرس | int | الفهرس الخاص بالقيد لإرجاعه. |

**Returns:**
[Constraint](../../com.aspose.words.net.system.data/constraint/) - The [Constraint](../../com.aspose.words.net.system.data/constraint/) at the specified index.
### get(String name) {#get-java.lang.String}
```
public System.Data.Constraint get(String name)
```


يحصل على [Constraint](../../com.aspose.words.net.system.data/constraint/) من المجموعة بالاسم المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| name | java.lang.String | الـ [Constraint.getConstraintName()](../../com.aspose.words.net.system.data/constraint/\#getConstraintName) / [Constraint.setConstraintName(java.lang.String)](../../com.aspose.words.net.system.data/constraint/\#setConstraintName-java.lang.String) للقيد لإرجاعه. |

**Returns:**
[Constraint](../../com.aspose.words.net.system.data/constraint/) - The [Constraint](../../com.aspose.words.net.system.data/constraint/) with the specified name; otherwise a null value if the [Constraint](../../com.aspose.words.net.system.data/constraint/) does not exist.
### getCount() {#getCount}
```
public int getCount()
```


يحصل على العدد الإجمالي للعناصر في مجموعة.

**Returns:**
int - العدد الإجمالي للعناصر في مجموعة.
### iterator() {#iterator}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator
### remove(System.Data.Constraint constraint) {#remove-com.aspose.words.net.System.Data.Constraint}
```
public void remove(System.Data.Constraint constraint)
```


يزيل [Constraint](../../com.aspose.words.net.system.data/constraint/) المحدد من المجموعة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| constraint | [Constraint](../../com.aspose.words.net.system.data/constraint/) | الـ [Constraint](../../com.aspose.words.net.system.data/constraint/) للإزالة. |

