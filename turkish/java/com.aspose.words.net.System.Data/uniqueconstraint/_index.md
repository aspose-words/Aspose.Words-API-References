---
title: "UniqueConstraint"
linktitle: "UniqueConstraint"
second_title: "Aspose.Words Java için"
description: "Java'da tüm değerlerin benzersiz olması gereken bir sütun kümesi üzerindeki bir kısıtlamayı temsil eder."
type: docs
weight: 32
url: /tr/java/com.aspose.words.net.system.data/uniqueconstraint/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.net.System.Data.Constraint](../../com.aspose.words.net.system.data/constraint/)
```
public class UniqueConstraint extends System.Data.Constraint
```

Tüm değerlerin benzersiz olması gereken bir sütun kümesi üzerindeki kısıtlamayı temsil eder.
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [UniqueConstraint(String name, System.Data.DataColumn[] columns, boolean isPrimaryKey)](#UniqueConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---boolean) | Belirtilen ad, kısıtlanacak [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnelerinin bir dizisi ve kısıtlamanın bir birincil anahtar olup olmadığını belirten bir değer ile [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) sınıfının yeni bir örneğini başlatır. |
| [UniqueConstraint(System.Data.DataColumn[] columns, boolean isPrimaryKey)](#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn---boolean) | Kısıtlanacak [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnelerinin bir dizisi ve kısıtlamanın bir birincil anahtar olup olmadığını belirten bir değer ile [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) sınıfının yeni bir örneğini başlatır. |
| [UniqueConstraint(System.Data.DataColumn[] columns)](#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn) | Verilen [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnelerinin dizisi ile [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) sınıfının yeni bir örneğini başlatır. |
| [UniqueConstraint(System.Data.DataColumn column)](#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn) | Belirtilen [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) ile [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) sınıfının yeni bir örneğini başlatır. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [equals(Object key2)](#equals-java.lang.Object) | Bu kısıtlamayı ikinci bir kısıtlamayla karşılaştırarak ikisinin aynı olup olmadığını belirler. |
| [getColumns()](#getColumns) | Bu kısıtlamanın etkilediği sütunların dizisini alır. |
| [getConstraintName()](#getConstraintName) | [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/) içindeki bir kısıtlamanın adı. |
| [getTable()](#getTable) | Bu kısıtlamanın ait olduğu tabloyu alır. |
| [hashCode()](#hashCode) |  |
| [isPrimaryKey()](#isPrimaryKey) | Kısıtlamanın bir birincil anahtar üzerinde olup olmadığını gösteren bir değeri alır. |
| [setConstraintName(String value)](#setConstraintName-java.lang.String) | [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/) içindeki bir kısıtlamanın adı. |
### UniqueConstraint(String name, System.Data.DataColumn[] columns, boolean isPrimaryKey) {#UniqueConstraint-java.lang.String-com.aspose.words.net.System.Data.DataColumn---boolean}
```
public UniqueConstraint(String name, System.Data.DataColumn[] columns, boolean isPrimaryKey)
```


Belirtilen ad, kısıtlanacak [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnelerinin bir dizisi ve kısıtlamanın bir birincil anahtar olup olmadığını belirten bir değer ile [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) sınıfının yeni bir örneğini başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String | Kısıtlamanın adı. |
| columns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Kısıtlamak için bir [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesneleri dizisi. |
| isPrimaryKey | boolean | Kısıtlamanın bir birincil anahtar olduğunu göstermek için true; aksi takdirde false. |

### UniqueConstraint(System.Data.DataColumn[] columns, boolean isPrimaryKey) {#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn---boolean}
```
public UniqueConstraint(System.Data.DataColumn[] columns, boolean isPrimaryKey)
```


Kısıtlanacak [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnelerinin bir dizisi ve kısıtlamanın bir birincil anahtar olup olmadığını belirten bir değer ile [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) sınıfının yeni bir örneğini başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| columns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Kısıtlamak için bir [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesneleri dizisi. |
| isPrimaryKey | boolean | Kısıtlamanın bir birincil anahtar olduğunu göstermek için true; aksi takdirde false. |

### UniqueConstraint(System.Data.DataColumn[] columns) {#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn}
```
public UniqueConstraint(System.Data.DataColumn[] columns)
```


Verilen [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnelerinin dizisi ile [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) sınıfının yeni bir örneğini başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| columns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Kısıtlamak için [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnelerinin dizisi. |

### UniqueConstraint(System.Data.DataColumn column) {#UniqueConstraint-com.aspose.words.net.System.Data.DataColumn}
```
public UniqueConstraint(System.Data.DataColumn column)
```


Belirtilen [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) ile [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) sınıfının yeni bir örneğini başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Kısıtlamak için [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnesi. |

### equals(Object key2) {#equals-java.lang.Object}
```
public boolean equals(Object key2)
```


Bu kısıtlamayı ikinci bir kısıtlamayla karşılaştırarak ikisinin aynı olup olmadığını belirler.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| key2 | java.lang.Object | Bu [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) ile karşılaştırılan nesne. |

**Returns:**
boolean - kısıtlamalar eşitse true, aksi takdirde false.
### getColumns() {#getColumns}
```
public System.Data.DataColumn[] getColumns()
```


Bu kısıtlamanın etkilediği sütunların dizisini alır.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnelerinden oluşan bir dizi.
### getConstraintName() {#getConstraintName}
```
public String getConstraintName()
```


[ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/) içindeki bir kısıtlamanın adı.

**Returns:**
java.lang.String - [Constraint](../../com.aspose.words.net.system.data/constraint/) adını.
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


Bu kısıtlamanın ait olduğu tabloyu alır.

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


Kısıtlamanın bir birincil anahtar üzerinde olup olmadığını gösteren bir değeri alır.

**Returns:**
boolean - true, eğer kısıtlama bir birincil anahtar üzerindeyse; aksi takdirde, false.
### setConstraintName(String value) {#setConstraintName-java.lang.String}
```
public void setConstraintName(String value)
```


[ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/) içindeki bir kısıtlamanın adı.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | java.lang.String | [Constraint](../../com.aspose.words.net.system.data/constraint/) adını. |

