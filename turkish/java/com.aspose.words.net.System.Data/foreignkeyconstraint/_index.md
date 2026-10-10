---
title: "ForeignKeyConstraint"
linktitle: "ForeignKeyConstraint"
second_title: "Aspose.Words Java için"
description: "Java'da bir değer veya satır silindiğinde veya güncellendiğinde, birincil anahtar/foreign key ilişkisi içindeki sütunlar kümesine uygulanan bir eylem kısıtlamasını temsil eder."
type: docs
weight: 29
url: /tr/java/com.aspose.words.net.system.data/foreignkeyconstraint/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.net.System.Data.Constraint](../../com.aspose.words.net.system.data/constraint/)
```
public class ForeignKeyConstraint extends System.Data.Constraint
```

Bir değer veya satır silindiğinde ya da güncellendiğinde birincil anahtar/foreign key ilişkisindeki sütunlar kümesine uygulanan bir eylem kısıtlamasını temsil eder.
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [ForeignKeyConstraint(String constraintName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns)](#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn) | Belirtilen ad ve ebeveyn ve çocuk [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnelerinin dizileri ile [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) sınıfının yeni bir örneğini başlatır. |
| [ForeignKeyConstraint(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#ForeignKeyConstraint-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | Belirtilen ebeveyn ve çocuk [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesneleri ile [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) sınıfının yeni bir örneğini başlatır. |
| [ForeignKeyConstraint(String constraintName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | Belirtilen ad, ebeveyn ve çocuk [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesneleri ile [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) sınıfının yeni bir örneğini başlatır. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [equals(Object key)](#equals-java.lang.Object) | Mevcut [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) nesnesinin belirtilen nesneyle aynı olup olmadığını gösteren bir değeri alır. |
| [getColumns()](#getColumns) | Bu kısıtlamanın çocuk sütunlarını alır. |
| [getConstraintName()](#getConstraintName) | [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/) içindeki bir kısıtlamanın adı. |
| [getDeleteRule()](#getDeleteRule) | Bir satır silindiğinde bu kısıtlama üzerinde gerçekleşen eylemi alır. |
| [getRelatedColumns()](#getRelatedColumns) | Bu kısıtlamanın ebeveyn sütunları. |
| [getRelatedTable()](#getRelatedTable) | Bu kısıtlamanın ebeveyn tablosunu alır. |
| [getTable()](#getTable) | Bu kısıtlamanın çocuk tablosunu alır. |
| [getUpdateRule()](#getUpdateRule) | Bir satır güncellendiğinde bu kısıtlama üzerinde gerçekleşen eylemi alır. |
| [hashCode()](#hashCode) |  |
| [setConstraintName(String value)](#setConstraintName-java.lang.String) | [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/) içindeki bir kısıtlamanın adı. |
### ForeignKeyConstraint(String constraintName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns) {#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn}
```
public ForeignKeyConstraint(String constraintName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns)
```


Belirtilen ad ve ebeveyn ve çocuk [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnelerinin dizileri ile [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) sınıfının yeni bir örneğini başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| constraintName | java.lang.String | [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) adını. Null veya boş dize ise, kısıtlamalar koleksiyonuna eklendiğinde varsayılan bir ad atanır. |
| parentColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Kısıtlamadaki ebeveyn [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) dizisi. |
| childColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Kısıtlamadaki çocuk [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) dizisi. |

### ForeignKeyConstraint(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#ForeignKeyConstraint-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public ForeignKeyConstraint(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


Belirtilen ebeveyn ve çocuk [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesneleri ile [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) sınıfının yeni bir örneğini başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Kısıtlamadaki ebeveyn [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Kısıtlamadaki çocuk [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |

### ForeignKeyConstraint(String constraintName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#ForeignKeyConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public ForeignKeyConstraint(String constraintName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


Belirtilen ad, ebeveyn ve çocuk [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesneleri ile [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) sınıfının yeni bir örneğini başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| constraintName | java.lang.String | Kısıtlamanın adı. |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Kısıtlamadaki ebeveyn [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Kısıtlamadaki çocuk [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |

### equals(Object key) {#equals-java.lang.Object}
```
public boolean equals(Object key)
```


Mevcut [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) nesnesinin belirtilen nesneyle aynı olup olmadığını gösteren bir değeri alır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key | java.lang.Object | Bu [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) nesnesinin karşılaştırıldığı nesne. Aynı sütunları kısıtladıkları sürece iki [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) eşittir. |

**Returns:**
boolean - nesneler aynıysa true; aksi takdirde false.
### getColumns() {#getColumns}
```
public System.Data.DataColumn[] getColumns()
```


Bu kısıtlamanın çocuk sütunlarını alır.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - Kısıtlamanın çocuk sütunları olan [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnelerinin dizisi.
### getConstraintName() {#getConstraintName}
```
public String getConstraintName()
```


[ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/) içindeki bir kısıtlamanın adı.

**Returns:**
java.lang.String - [Constraint](../../com.aspose.words.net.system.data/constraint/) adını.
### getDeleteRule() {#getDeleteRule}
```
public System.Data.Rule getDeleteRule()
```


Bir satır silindiğinde bu kısıtlama üzerinde gerçekleşen eylemi alır.

**Returns:**
[Rule](../../com.aspose.words.net.system.data/rule/) - One of the [Rule](../../com.aspose.words.net.system.data/rule/) values. The default is Cascade. The returned value is one of [Rule](../../com.aspose.words.net.system.data/rule/) constants.
### getRelatedColumns() {#getRelatedColumns}
```
public System.Data.DataColumn[] getRelatedColumns()
```


Bu kısıtlamanın ebeveyn sütunları.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - Kısıtlamanın ebeveyn sütunları olan [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnelerinin dizisi.
### getRelatedTable() {#getRelatedTable}
```
public System.Data.DataTable getRelatedTable()
```


Bu kısıtlamanın ebeveyn tablosunu alır.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The parent [DataTable](../../com.aspose.words.net.system.data/datatable/) of this constraint.
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


Bu kısıtlamanın çocuk tablosunu alır.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that is the child table in the constraint.
### getUpdateRule() {#getUpdateRule}
```
public System.Data.Rule getUpdateRule()
```


Bir satır güncellendiğinde bu kısıtlama üzerinde gerçekleşen eylemi alır.

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


[ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/) içindeki bir kısıtlamanın adı.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | java.lang.String | [Constraint](../../com.aspose.words.net.system.data/constraint/) adını. |

