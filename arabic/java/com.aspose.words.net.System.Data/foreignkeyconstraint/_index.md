---
title: "ForeignKeyConstraint"
linktitle: "ForeignKeyConstraint"
second_title: "Aspose.Words لـ Java"
description: "يمثل تقييدًا للإجراء يتم تطبيقه على مجموعة من الأعمدة في علاقة المفتاح الأساسي/المفتاح الخارجي عندما يتم حذف قيمة أو صف أو تحديثه في Java."
type: docs
weight: 29
url: /ar/java/com.aspose.words.net.system.data/foreignkeyconstraint/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.net.System.Data.Constraint](../../com.aspose.words.net.system.data/constraint/)
```
public class ForeignKeyConstraint extends System.Data.Constraint
```

يمثل تقييدًا للإجراء يُفرض على مجموعة من الأعمدة في علاقة المفتاح الأساسي/المفتاح الأجنبي عندما يتم حذف قيمة أو صف أو تحديثه
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [ForeignKeyConstraint(String constraintName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns)](#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn) | ينشئ مثيلًا جديدًا من الفئة [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) بالاسم المحدد، ومصفوفات من أعمدة الأصل والابن [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
| [ForeignKeyConstraint(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#ForeignKeyConstraint-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | ينشئ مثيلًا جديدًا من الفئة [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) بالأعمدة الأصلية والابنة المحددة [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
| [ForeignKeyConstraint(String constraintName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | ينشئ مثيلًا جديدًا من الفئة [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) بالاسم المحدد، والأعمدة الأصلية والابنة [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [equals(Object key)](#equals-java.lang.Object) | يحصل على قيمة تشير إلى ما إذا كان [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) الحالي مطابقًا للكائن المحدد. |
| [getColumns()](#getColumns) | يحصل على الأعمدة الابنة لهذا القيد. |
| [getConstraintName()](#getConstraintName) | اسم القيد في [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/). |
| [getDeleteRule()](#getDeleteRule) | يحصل على الإجراء الذي يحدث عبر هذا القيد عندما يتم حذف صف. |
| [getRelatedColumns()](#getRelatedColumns) | الأعمدة الأصلية لهذا القيد. |
| [getRelatedTable()](#getRelatedTable) | يحصل على جدول الأصل لهذا القيد. |
| [getTable()](#getTable) | يحصل على جدول الابن لهذا القيد. |
| [getUpdateRule()](#getUpdateRule) | يحصل على الإجراء الذي يحدث عبر هذا القيد عندما يتم تحديث صف. |
| [hashCode()](#hashCode) |  |
| [setConstraintName(String value)](#setConstraintName-java.lang.String) | اسم القيد في [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/). |
### ForeignKeyConstraint(String constraintName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns) {#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn}
```
public ForeignKeyConstraint(String constraintName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns)
```


ينشئ مثيلًا جديدًا من الفئة [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) بالاسم المحدد، ومصفوفات من أعمدة الأصل والابن [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| constraintName | java.lang.String | اسم [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/). إذا كان null أو سلسلة فارغة، سيتم إعطاء اسم افتراضي عند إضافته إلى مجموعة القيود. |
| parentColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | مصفوفة من الأعمدة الأصلية [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) في القيد. |
| childColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | مصفوفة من الأعمدة الابنة [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) في القيد. |

### ForeignKeyConstraint(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#ForeignKeyConstraint-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public ForeignKeyConstraint(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


ينشئ مثيلًا جديدًا من الفئة [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) بالأعمدة الأصلية والابنة المحددة [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | العمود الأصلي [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) في القيد. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | العمود الابن [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) في القيد. |

### ForeignKeyConstraint(String constraintName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public ForeignKeyConstraint(String constraintName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


ينشئ مثيلًا جديدًا من الفئة [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) بالاسم المحدد، والأعمدة الأصلية والابنة [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| constraintName | java.lang.String | اسم القيد. |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | العمود الأصلي [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) في القيد. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | العمود الابن [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) في القيد. |

### equals(Object key) {#equals-java.lang.Object}
```
public boolean equals(Object key)
```


يحصل على قيمة تشير إلى ما إذا كان [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) الحالي مطابقًا للكائن المحدد.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| key | java.lang.Object | الكائن الذي يتم مقارنة هذا [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) معه. يعتبر [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/)ان متساويين إذا كانا يقيدان نفس الأعمدة. |

**Returns:**
منطقي - true إذا كان الكائنان متطابقان؛ وإلا false.
### getColumns() {#getColumns}
```
public System.Data.DataColumn[] getColumns()
```


يحصل على الأعمدة الابنة لهذا القيد.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - مصفوفة من كائنات [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) التي تمثل الأعمدة الابنة للقيد.
### getConstraintName() {#getConstraintName}
```
public String getConstraintName()
```


اسم القيد في [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/).

**Returns:**
java.lang.String - اسم [Constraint](../../com.aspose.words.net.system.data/constraint/).
### getDeleteRule() {#getDeleteRule}
```
public System.Data.Rule getDeleteRule()
```


يحصل على الإجراء الذي يحدث عبر هذا القيد عندما يتم حذف صف.

**Returns:**
[Rule](../../com.aspose.words.net.system.data/rule/) - One of the [Rule](../../com.aspose.words.net.system.data/rule/) values. The default is Cascade. The returned value is one of [Rule](../../com.aspose.words.net.system.data/rule/) constants.
### getRelatedColumns() {#getRelatedColumns}
```
public System.Data.DataColumn[] getRelatedColumns()
```


الأعمدة الأصلية لهذا القيد.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - مصفوفة من كائنات [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) التي تمثل الأعمدة الأصلية للقيد.
### getRelatedTable() {#getRelatedTable}
```
public System.Data.DataTable getRelatedTable()
```


يحصل على جدول الأصل لهذا القيد.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The parent [DataTable](../../com.aspose.words.net.system.data/datatable/) of this constraint.
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


يحصل على جدول الابن لهذا القيد.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that is the child table in the constraint.
### getUpdateRule() {#getUpdateRule}
```
public System.Data.Rule getUpdateRule()
```


يحصل على الإجراء الذي يحدث عبر هذا القيد عندما يتم تحديث صف.

**Returns:**
[Rule](../../com.aspose.words.net.system.data/rule/) - One of the [Rule](../../com.aspose.words.net.system.data/rule/) values. The default is Cascade. The returned value is one of [Rule](../../com.aspose.words.net.system.data/rule/) constants.
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### setConstraintName(String value) {#setConstraintName-java.lang.String}
```
public void setConstraintName(String value)
```


اسم القيد في [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/).

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | java.lang.String | اسم [Constraint](../../com.aspose.words.net.system.data/constraint/). |

