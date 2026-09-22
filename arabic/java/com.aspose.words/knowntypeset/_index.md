---
title: "KnownTypeSet"
linktitle: "KnownTypeSet"
second_title: "Aspose.Words لـ Java"
description: "يمثل مجموعة غير مرتبة، أي في Java."
type: docs
weight: 412
url: /ar/java/com.aspose.words/knowntypeset/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class KnownTypeSet implements Iterable
```

يمثل مجموعة غير مرتبة (أي مجموعة من العناصر الفريدة) تحتوي على كائنات java.lang.Class التي يمكن استخدام أسمائها المؤهلة بالكامل أو جزئياً داخل قوالب التقارير لاستدعاء الأعضاء الثابتة للأنواع المقابلة، وإجراء تحويلات النوع، إلخ.

للتعرف على المزيد، زر مقالة توثيق [ LINQ Reporting Engine ][LINQ Reporting Engine].


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## الطرق

| طريقة | الوصف |
| --- | --- |
| [add(Class type)](#add-java.lang.Class) | يضيف كائن java.lang.Class المحدد إلى المجموعة. |
| [clear()](#clear) | يزيل جميع العناصر من المجموعة. |
| [getCount()](#getCount) | يحصل على عدد العناصر في المجموعة. |
| [iterator()](#iterator) | يرجع كائن java.util.Iterator للتنقل عبر عناصر المجموعة. |
| [remove(Class type)](#remove-java.lang.Class) | يزيل كائن java.lang.Class المحدد من المجموعة. |
### add(Class type) {#add-java.lang.Class}
```
public void add(Class type)
```


يضيف كائن java.lang.Class المحدد إلى المجموعة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| نوع | java.lang.Class | كائن java.lang.Class للإضافة. |

### clear() {#clear}
```
public void clear()
```


يزيل جميع العناصر من المجموعة.

### getCount() {#getCount}
```
public int getCount()
```


يحصل على عدد العناصر في المجموعة.

**Returns:**
int - عدد العناصر في المجموعة.
### iterator() {#iterator}
```
public Iterator iterator()
```


يرجع كائن java.util.Iterator للتنقل عبر عناصر المجموعة.

**Returns:**
java.util.Iterator - كائن java.util.Iterator للتنقل عبر عناصر المجموعة.
### remove(Class type) {#remove-java.lang.Class}
```
public void remove(Class type)
```


يزيل كائن java.lang.Class المحدد من المجموعة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| نوع | java.lang.Class | كائن java.lang.Class للإزالة. |

