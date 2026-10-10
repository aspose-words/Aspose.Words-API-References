---
title: "UniqueConstraint"
linktitle: "UniqueConstraint"
second_title: "Aspose.Words لـ Java"
description: "يمثل قيدًا على مجموعة من الأعمدة يجب أن تكون جميع القيم فيها فريدة في Java."
type: docs
weight: 32
url: /ar/java/com.aspose.words.net.system.data/uniqueconstraint/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.net.System.Data.Constraint](../../com.aspose.words.net.system.data/constraint/)
```
public class UniqueConstraint extends System.Data.Constraint
```

يمثل قيدًا على مجموعة من الأعمدة حيث يجب أن تكون جميع القيم فريدة
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [UniqueConstraint(String name, System.Data.DataColumn[] columns, boolean isPrimaryKey)](#UniqueConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---boolean) | يُنشئ مثالًا جديدًا من الفئة [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) بالاسم المحدد، ومصفوفة من كائنات [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) لتقييدها، وقيمة تحدد ما إذا كان القيد مفتاحًا أساسيًا. |
| [UniqueConstraint(System.Data.DataColumn[] columns, boolean isPrimaryKey)](#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn---boolean) | يُنشئ مثالًا جديدًا من الفئة [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) بمصفوفة من كائنات [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) لتقييدها، وقيمة تحدد ما إذا كان القيد مفتاحًا أساسيًا. |
| [UniqueConstraint(System.Data.DataColumn[] columns)](#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn) | يُنشئ مثالًا جديدًا من الفئة [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) بالمصفوفة المعطاة من كائنات [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
| [UniqueConstraint(System.Data.DataColumn column)](#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn) | يُنشئ مثالًا جديدًا من الفئة [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) بالـ [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) المحدد. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [equals(Object key2)](#equals-java.lang.Object) | يقارن هذا القيد بآخر لتحديد ما إذا كانا متطابقين. |
| [getColumns()](#getColumns) | يحصل على مصفوفة الأعمدة التي يؤثر عليها هذا القيد. |
| [getConstraintName()](#getConstraintName) | اسم القيد في [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/). |
| [getTable()](#getTable) | يحصل على الجدول الذي ينتمي إليه هذا القيد. |
| [hashCode()](#hashCode) |  |
| [isPrimaryKey()](#isPrimaryKey) | يحصل على قيمة تشير إلى ما إذا كان القيد على مفتاح أساسي أم لا. |
| [setConstraintName(String value)](#setConstraintName-java.lang.String) | اسم القيد في [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/). |
### UniqueConstraint(String name, System.Data.DataColumn[] columns, boolean isPrimaryKey) {#UniqueConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---boolean}
```
public UniqueConstraint(String name, System.Data.DataColumn[] columns, boolean isPrimaryKey)
```


يُنشئ مثالًا جديدًا من الفئة [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) بالاسم المحدد، ومصفوفة من كائنات [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) لتقييدها، وقيمة تحدد ما إذا كان القيد مفتاحًا أساسيًا.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| الاسم | java.lang.String | اسم القيد. |
| columns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | مصفوفة من كائنات [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) لتقييدها. |
| isPrimaryKey | boolean | true للإشارة إلى أن القيد هو مفتاح أساسي؛ وإلا false. |

### UniqueConstraint(System.Data.DataColumn[] columns, boolean isPrimaryKey) {#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn---boolean}
```
public UniqueConstraint(System.Data.DataColumn[] columns, boolean isPrimaryKey)
```


يُنشئ مثالًا جديدًا من الفئة [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) بمصفوفة من كائنات [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) لتقييدها، وقيمة تحدد ما إذا كان القيد مفتاحًا أساسيًا.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| columns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | مصفوفة من كائنات [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) لتقييدها. |
| isPrimaryKey | boolean | true للإشارة إلى أن القيد هو مفتاح أساسي؛ وإلا false. |

### UniqueConstraint(System.Data.DataColumn[] columns) {#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn}
```
public UniqueConstraint(System.Data.DataColumn[] columns)
```


يُنشئ مثالًا جديدًا من الفئة [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) بالمصفوفة المعطاة من كائنات [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| columns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | مصفوفة [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) لتقييدها. |

### UniqueConstraint(System.Data.DataColumn column) {#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn}
```
public UniqueConstraint(System.Data.DataColumn column)
```


يُنشئ مثالًا جديدًا من الفئة [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) بالـ [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | الـ [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) لتقييده. |

### equals(Object key2) {#equals-java.lang.Object}
```
public boolean equals(Object key2)
```


يقارن هذا القيد بآخر لتحديد ما إذا كانا متطابقين.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key2 | java.lang.Object | الكائن الذي يُقارن به هذا [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/). |

**Returns:**
boolean - true إذا كانت القيود متساوية؛ وإلا false.
### getColumns() {#getColumns}
```
public System.Data.DataColumn[] getColumns()
```


يحصل على مصفوفة الأعمدة التي يؤثر عليها هذا القيد.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - مصفوفة من كائنات [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).
### getConstraintName() {#getConstraintName}
```
public String getConstraintName()
```


اسم القيد في [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/).

**Returns:**
java.lang.String - اسم [Constraint](../../com.aspose.words.net.system.data/constraint/).
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


يحصل على الجدول الذي ينتمي إليه هذا القيد.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The [DataTable](../../com.aspose.words.net.system.data/datatable/) to which the constraint belongs.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### isPrimaryKey() {#isPrimaryKey}
```
public boolean isPrimaryKey()
```


يحصل على قيمة تشير إلى ما إذا كان القيد على مفتاح أساسي أم لا.

**Returns:**
boolean - true إذا كان القيد على المفتاح الأساسي؛ وإلا false.
### setConstraintName(String value) {#setConstraintName-java.lang.String}
```
public void setConstraintName(String value)
```


اسم القيد في [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | java.lang.String | اسم [Constraint](../../com.aspose.words.net.system.data/constraint/). |

