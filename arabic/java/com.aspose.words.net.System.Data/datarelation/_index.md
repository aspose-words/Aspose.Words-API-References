---
title: "DataRelation"
linktitle: "DataRelation"
second_title: "Aspose.Words لـ Java"
description: "يمثل علاقة أب/ابن بين كائنين DataTable في Java."
type: docs
weight: 18
url: /ar/java/com.aspose.words.net.system.data/datarelation/
---

**Inheritance:**
java.lang.Object
```
public class DataRelation
```

يمثل علاقة أب/ابن بين كائنين [DataTable](../../com.aspose.words.net.system.data/datatable/).
## المنشئات

| المنشئ | الوصف |
| --- | --- |
| [DataRelation(String relationName, System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String) | ينشئ مثيلاً جديداً من الفئة [DataRelation](../../com.aspose.words.net.system.data/datarelation/) باستخدام الاسم المحدد، وجداول الأب والابن، ومصفوفات مطابقة من أعمدة الأب والابن. |
| [DataRelation(String relationName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns, boolean createConstraints)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn---boolean) | ينشئ مثيلاً جديداً من الفئة [DataRelation](../../com.aspose.words.net.system.data/datarelation/) باستخدام الاسم المحدد، ومصفوفات مطابقة من كائنات [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) للأب والابن، وقيمة تشير إلى ما إذا كان يجب إنشاء قيود. |
| [DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean) | ينشئ مثيلاً جديداً من الفئة [DataRelation](../../com.aspose.words.net.system.data/datarelation/) باستخدام الاسم المحدد، وكائنات [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) للأب والابن، وقيمة تشير إلى ما إذا كان يجب إنشاء قيود. |
| [DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | ينشئ مثيلاً جديداً من الفئة [DataRelation](../../com.aspose.words.net.system.data/datarelation/) باستخدام الاسم [DataRelation](../../com.aspose.words.net.system.data/datarelation/) المحدد، وكائنات [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) للأب والابن. |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) |  |
| [getChildColumnNames()](#getChildColumnNames) |  |
| [getChildColumns()](#getChildColumns) | يحصل على كائنات [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) للابن في هذه العلاقة. |
| [getChildKey()](#getChildKey) |  |
| [getChildKeyConstraint()](#getChildKeyConstraint) | يحصل على [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) للعلاقة. |
| [getChildTable()](#getChildTable) | يحصل على جدول الابن في هذه العلاقة. |
| [getChildTableName()](#getChildTableName) |  |
| [getDataSet()](#getDataSet) | يحصل على [DataSet](../../com.aspose.words.net.system.data/dataset/) الذي تنتمي إليه [DataRelation](../../com.aspose.words.net.system.data/datarelation/). |
| [getParentColumnNames()](#getParentColumnNames) |  |
| [getParentColumns()](#getParentColumns) | يحصل على مصفوفة من كائنات [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) التي تمثل أعمدة الأب لهذا [DataRelation](../../com.aspose.words.net.system.data/datarelation/). |
| [getParentKey()](#getParentKey) |  |
| [getParentKeyConstraint()](#getParentKeyConstraint) | يحصل على [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) الذي يضمن أن القيم في عمود الأب لـ [DataRelation](../../com.aspose.words.net.system.data/datarelation/) فريدة. |
| [getParentTable()](#getParentTable) | يحصل على [DataTable](../../com.aspose.words.net.system.data/datatable/) الأب لهذا [DataRelation](../../com.aspose.words.net.system.data/datarelation/). |
| [getParentTableName()](#getParentTableName) |  |
| [getRelationName()](#getRelationName) | يحصل على الاسم المستخدم لاسترجاع [DataRelation](../../com.aspose.words.net.system.data/datarelation/) من [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/). |
| [hashCode()](#hashCode) |  |
| [setChildKeyConstraint(System.Data.ForeignKeyConstraint childKeyConstraint)](#setChildKeyConstraint-com.aspose.words.net.System.Data.ForeignKeyConstraint) |  |
| [setNested(boolean value)](#setNested-boolean) | يضبط قيمة تشير إلى ما إذا كانت كائنات [DataRelation](../../com.aspose.words.net.system.data/datarelation/) متداخلة. |
| [setParentKeyConstraint(System.Data.UniqueConstraint parentKeyConstraint)](#setParentKeyConstraint-com.aspose.words.net.System.Data.UniqueConstraint) |  |
### DataRelation(String relationName, System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String}
```
public DataRelation(String relationName, System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)
```


ينشئ مثيلاً جديداً من الفئة [DataRelation](../../com.aspose.words.net.system.data/datarelation/) باستخدام الاسم المحدد، وجداول الأب والابن، ومصفوفات مطابقة من أعمدة الأب والابن.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| relationName | java.lang.String | اسم الـ DataRelation. إذا كان null أو سلسلة فارغة (""), سيتم إعطاء اسم افتراضي عند إضافة الكائن المُنشأ إلى DataRelationCollection. |
| parentTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | جدول الأب في العلاقة. |
| childTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | جدول الطفل في العلاقة. |
| parentColumnNames | java.lang.String[] | اسم DataColumn الأب في العلاقة. |
| childColumnNames | java.lang.String[] | DataColumn الطفل في العلاقة. |

### DataRelation(String relationName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns, boolean createConstraints) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn---boolean}
```
public DataRelation(String relationName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns, boolean createConstraints)
```


ينشئ مثيلاً جديداً من الفئة [DataRelation](../../com.aspose.words.net.system.data/datarelation/) باستخدام الاسم المحدد، ومصفوفات مطابقة من كائنات [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) للأب والابن، وقيمة تشير إلى ما إذا كان يجب إنشاء قيود.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| relationName | java.lang.String | اسم العلاقة. إذا كان null أو سلسلة فارغة (""), سيتم إعطاء اسم افتراضي عندما يُضاف الكائن المُنشأ إلى [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/). |
| parentColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | مصفوفة من كائنات [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) الأبوية. |
| childColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | مصفوفة من كائنات [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) التابعة. |
| createConstraints | boolean | قيمة تشير إلى ما إذا كان سيتم إنشاء القيود. true إذا تم إنشاء القيود. وإلا false. |

### DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean}
```
public DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)
```


ينشئ مثيلاً جديداً من الفئة [DataRelation](../../com.aspose.words.net.system.data/datarelation/) باستخدام الاسم المحدد، وكائنات [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) للأب والابن، وقيمة تشير إلى ما إذا كان يجب إنشاء قيود.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| relationName | java.lang.String | اسم العلاقة. إذا كان null أو سلسلة فارغة (""), سيتم إعطاء اسم افتراضي عندما يُضاف الكائن المُنشأ إلى [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/). |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | عمود البيانات الأب [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) في العلاقة. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | عمود البيانات الطفل [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) في العلاقة. |
| createConstraints | boolean | قيمة تشير إلى ما إذا تم إنشاء القيود. true إذا تم إنشاء القيود. وإلا false. |

### DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


ينشئ مثيلاً جديداً من الفئة [DataRelation](../../com.aspose.words.net.system.data/datarelation/) باستخدام الاسم [DataRelation](../../com.aspose.words.net.system.data/datarelation/) المحدد، وكائنات [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) للأب والابن.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| relationName | java.lang.String | اسم [DataRelation](../../com.aspose.words.net.system.data/datarelation/). إذا كان null أو سلسلة فارغة (""), سيتم إعطاء اسم افتراضي عندما يُضاف الكائن المُنشأ إلى [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/). |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | عمود البيانات الأب [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) في العلاقة. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | عمود البيانات الطفل [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) في العلاقة. |

### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getChildColumnNames() {#getChildColumnNames}
```
public String[] getChildColumnNames()
```




**Returns:**
java.lang.String[] - أسماء DataColumn الطفل لهذه العلاقة.
### getChildColumns() {#getChildColumns}
```
public System.Data.DataColumn[] getChildColumns()
```


يحصل على كائنات [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) للابن في هذه العلاقة.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - مصفوفة من كائنات [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).
### getChildKey() {#getChildKey}
```
public System.Data.DataKey getChildKey()
```




**Returns:**
[DataKey](../../com.aspose.words.net.system.data/datakey/)
### getChildKeyConstraint() {#getChildKeyConstraint}
```
public System.Data.ForeignKeyConstraint getChildKeyConstraint()
```


يحصل على [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) للعلاقة.

**Returns:**
[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) - A [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/).
### getChildTable() {#getChildTable}
```
public System.Data.DataTable getChildTable()
```


يحصل على جدول الابن في هذه العلاقة.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that is the child table of the relation.
### getChildTableName() {#getChildTableName}
```
public String getChildTableName()
```




**Returns:**
java.lang.String - اسم DataTable الطفل لهذا DataRelation.
### getDataSet() {#getDataSet}
```
public System.Data.DataSet getDataSet()
```


يحصل على [DataSet](../../com.aspose.words.net.system.data/dataset/) الذي تنتمي إليه [DataRelation](../../com.aspose.words.net.system.data/datarelation/).

**Returns:**
[DataSet](../../com.aspose.words.net.system.data/dataset/) - A [DataSet](../../com.aspose.words.net.system.data/dataset/) to which the [DataRelation](../../com.aspose.words.net.system.data/datarelation/) belongs.
### getParentColumnNames() {#getParentColumnNames}
```
public String[] getParentColumnNames()
```




**Returns:**
java.lang.String[] - أسماء DataColumn الأب لهذه العلاقة.
### getParentColumns() {#getParentColumns}
```
public System.Data.DataColumn[] getParentColumns()
```


يحصل على مصفوفة من كائنات [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) التي تمثل أعمدة الأب لهذا [DataRelation](../../com.aspose.words.net.system.data/datarelation/).

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - مصفوفة من كائنات [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) التي هي الأعمدة الأب لهذا [DataRelation](../../com.aspose.words.net.system.data/datarelation/).
### getParentKey() {#getParentKey}
```
public System.Data.DataKey getParentKey()
```




**Returns:**
[DataKey](../../com.aspose.words.net.system.data/datakey/)
### getParentKeyConstraint() {#getParentKeyConstraint}
```
public System.Data.UniqueConstraint getParentKeyConstraint()
```


يحصل على [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) الذي يضمن أن القيم في عمود الأب لـ [DataRelation](../../com.aspose.words.net.system.data/datarelation/) فريدة.

**Returns:**
[UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) - A [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) that makes sure that values in a parent column are unique.
### getParentTable() {#getParentTable}
```
public System.Data.DataTable getParentTable()
```


يحصل على [DataTable](../../com.aspose.words.net.system.data/datatable/) الأب لهذا [DataRelation](../../com.aspose.words.net.system.data/datarelation/).

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that is the parent table of this relation.
### getParentTableName() {#getParentTableName}
```
public String getParentTableName()
```




**Returns:**
java.lang.String - اسم DataTable الأب لهذا DataRelation.
### getRelationName() {#getRelationName}
```
public String getRelationName()
```


يحصل على الاسم المستخدم لاسترجاع [DataRelation](../../com.aspose.words.net.system.data/datarelation/) من [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/).

**Returns:**
java.lang.String - اسم [DataRelation](../../com.aspose.words.net.system.data/datarelation/).
### hashCode() {#hashCode}
```
public int hashCode()
```




**Returns:**
int
### setChildKeyConstraint(System.Data.ForeignKeyConstraint childKeyConstraint) {#setChildKeyConstraint-com.aspose.words.net.System.Data.ForeignKeyConstraint}
```
public void setChildKeyConstraint(System.Data.ForeignKeyConstraint childKeyConstraint)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| childKeyConstraint | [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) |  |

### setNested(boolean value) {#setNested-boolean}
```
public void setNested(boolean value)
```


يضبط قيمة تشير إلى ما إذا كانت كائنات [DataRelation](../../com.aspose.words.net.system.data/datarelation/) متداخلة.

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| value | boolean | true إذا كانت كائنات [DataRelation](../../com.aspose.words.net.system.data/datarelation/) متداخلة؛ وإلا false. |

### setParentKeyConstraint(System.Data.UniqueConstraint parentKeyConstraint) {#setParentKeyConstraint-com.aspose.words.net.System.Data.UniqueConstraint}
```
public void setParentKeyConstraint(System.Data.UniqueConstraint parentKeyConstraint)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| parentKeyConstraint | [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) |  |

