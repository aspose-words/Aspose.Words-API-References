---
title: "DataRelation"
linktitle: "DataRelation"
second_title: "Aspose.Words Java için"
description: "Java'da iki DataTable nesnesi arasındaki ebeveyn/çocuk ilişkiyi temsil eder."
type: docs
weight: 18
url: /tr/java/com.aspose.words.net.system.data/datarelation/
---

**Inheritance:**
java.lang.Object
```
public class DataRelation
```

İki [DataTable](../../com.aspose.words.net.system.data/datatable/) nesnesi arasındaki ebeveyn/çocuk ilişkiyi temsil eder.
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [DataRelation(String relationName, System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String) | Belirtilen ad, ebeveyn ve çocuk tabloları, eşleşen ebeveyn ve çocuk sütun dizileri kullanılarak yeni bir [DataRelation](../../com.aspose.words.net.system.data/datarelation/) sınıfı örneği başlatır. |
| [DataRelation(String relationName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns, boolean createConstraints)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn---boolean) | Belirtilen ad, eşleşen ebeveyn ve çocuk [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesneleri dizileri ve kısıtlamaların oluşturulup oluşturulmayacağını gösteren değer kullanılarak yeni bir [DataRelation](../../com.aspose.words.net.system.data/datarelation/) sınıfı örneği başlatır. |
| [DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean) | Belirtilen ad, ebeveyn ve çocuk [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesneleri ve kısıtlamaların oluşturulup oluşturulmayacağını gösteren bir değer kullanılarak yeni bir [DataRelation](../../com.aspose.words.net.system.data/datarelation/) sınıfı örneği başlatır. |
| [DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | Belirtilen [DataRelation](../../com.aspose.words.net.system.data/datarelation/) adı, ebeveyn ve çocuk [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesneleri kullanılarak yeni bir [DataRelation](../../com.aspose.words.net.system.data/datarelation/) sınıfı örneği başlatır. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) |  |
| [getChildColumnNames()](#getChildColumnNames) |  |
| [getChildColumns()](#getChildColumns) | Bu ilişkinin çocuk [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnelerini alır. |
| [getChildKey()](#getChildKey) |  |
| [getChildKeyConstraint()](#getChildKeyConstraint) | İlişki için [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) öğesini alır. |
| [getChildTable()](#getChildTable) | Bu ilişkinin çocuk tablosunu alır. |
| [getChildTableName()](#getChildTableName) |  |
| [getDataSet()](#getDataSet) | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) ait olduğu [DataSet](../../com.aspose.words.net.system.data/dataset/) öğesini alır. |
| [getParentColumnNames()](#getParentColumnNames) |  |
| [getParentColumns()](#getParentColumns) | Bu [DataRelation](../../com.aspose.words.net.system.data/datarelation/) için ebeveyn sütunları olan [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnelerinin bir dizisini alır. |
| [getParentKey()](#getParentKey) |  |
| [getParentKeyConstraint()](#getParentKeyConstraint) | Bir [DataRelation](../../com.aspose.words.net.system.data/datarelation/) ebeveyn sütunundaki değerlerin benzersiz olmasını garantileyen [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) öğesini alır. |
| [getParentTable()](#getParentTable) | Bu [DataRelation](../../com.aspose.words.net.system.data/datarelation/) için ebeveyn [DataTable](../../com.aspose.words.net.system.data/datatable/) öğesini alır. |
| [getParentTableName()](#getParentTableName) |  |
| [getRelationName()](#getRelationName) | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) öğesini [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) üzerinden almak için kullanılan adı alır. |
| [hashCode()](#hashCode) |  |
| [setChildKeyConstraint(System.Data.ForeignKeyConstraint childKeyConstraint)](#setChildKeyConstraint-com.aspose.words.net.System.Data.ForeignKeyConstraint) |  |
| [setNested(boolean value)](#setNested-boolean) | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) nesnelerinin iç içe olup olmadığını belirten bir değer ayarlar. |
| [setParentKeyConstraint(System.Data.UniqueConstraint parentKeyConstraint)](#setParentKeyConstraint-com.aspose.words.net.System.Data.UniqueConstraint) |  |
### DataRelation(String relationName, System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String}
```
public DataRelation(String relationName, System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)
```


Belirtilen ad, ebeveyn ve çocuk tabloları, eşleşen ebeveyn ve çocuk sütun dizileri kullanılarak yeni bir [DataRelation](../../com.aspose.words.net.system.data/datarelation/) sınıfı örneği başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| relationName | java.lang.String | DataRelation'ın adı. Null veya boş bir dize (""), oluşturulan nesne DataRelationCollection'a eklendiğinde varsayılan bir ad verilir. |
| parentTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | İlişkideki ebeveyn tablo. |
| childTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | İlişkideki alt tablo. |
| parentColumnNames | java.lang.String[] | İlişkideki üst DataColumn'un adı. |
| childColumnNames | java.lang.String[] | İlişkideki alt DataColumn'lar. |

### DataRelation(String relationName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns, boolean createConstraints) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn---com.aspose.words.net.System.Data.DataColumn---boolean}
```
public DataRelation(String relationName, System.Data.DataColumn[] parentColumns, System.Data.DataColumn[] childColumns, boolean createConstraints)
```


Belirtilen ad, eşleşen ebeveyn ve çocuk [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesneleri dizileri ve kısıtlamaların oluşturulup oluşturulmayacağını gösteren değer kullanılarak yeni bir [DataRelation](../../com.aspose.words.net.system.data/datarelation/) sınıfı örneği başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| relationName | java.lang.String | İlişkinin adı. Null veya boş bir dize (\"\"), oluşturulan nesne [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) e eklendiğinde varsayılan bir ad atanır. |
| parentColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Üst [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnelerinin bir dizisi. |
| childColumns | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | Alt [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnelerinin bir dizisi. |
| createConstraints | boolean | Kısıtlamaların oluşturulup oluşturulmayacağını gösteren bir değer. Kısıtlamalar oluşturulmuşsa true, aksi takdirde false. |

### DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean}
```
public DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)
```


Belirtilen ad, ebeveyn ve çocuk [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesneleri ve kısıtlamaların oluşturulup oluşturulmayacağını gösteren bir değer kullanılarak yeni bir [DataRelation](../../com.aspose.words.net.system.data/datarelation/) sınıfı örneği başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| relationName | java.lang.String | İlişkinin adı. Null veya boş bir dize (\"\"), oluşturulan nesne [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) e eklendiğinde varsayılan bir ad atanır. |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | İlişkideki üst [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | İlişkideki alt [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
| createConstraints | boolean | Kısıtlamaların oluşturulup oluşturulmadığını gösteren bir değer. Kısıtlamalar oluşturulmuşsa true, aksi takdirde false. |

### DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#DataRelation-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public DataRelation(String relationName, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


Belirtilen [DataRelation](../../com.aspose.words.net.system.data/datarelation/) adı, ebeveyn ve çocuk [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesneleri kullanılarak yeni bir [DataRelation](../../com.aspose.words.net.system.data/datarelation/) sınıfı örneği başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| relationName | java.lang.String | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) adını. Null veya boş bir dize (\"\"), oluşturulan nesne [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) e eklendiğinde varsayılan bir ad atanır. |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | İlişkideki üst [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | İlişkideki alt [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |

### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### getChildColumnNames() {#getChildColumnNames}
```
public String[] getChildColumnNames()
```




**Returns:**
java.lang.String[] - bu ilişkinin alt DataColumn adları.
### getChildColumns() {#getChildColumns}
```
public System.Data.DataColumn[] getChildColumns()
```


Bu ilişkinin çocuk [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnelerini alır.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnelerinden oluşan bir dizi.
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


İlişki için [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) öğesini alır.

**Returns:**
[ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) - A [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/).
### getChildTable() {#getChildTable}
```
public System.Data.DataTable getChildTable()
```


Bu ilişkinin çocuk tablosunu alır.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that is the child table of the relation.
### getChildTableName() {#getChildTableName}
```
public String getChildTableName()
```




**Returns:**
java.lang.String - bu DataRelation'ın alt DataTable adını.
### getDataSet() {#getDataSet}
```
public System.Data.DataSet getDataSet()
```


[DataRelation](../../com.aspose.words.net.system.data/datarelation/) ait olduğu [DataSet](../../com.aspose.words.net.system.data/dataset/) öğesini alır.

**Returns:**
[DataSet](../../com.aspose.words.net.system.data/dataset/) - A [DataSet](../../com.aspose.words.net.system.data/dataset/) to which the [DataRelation](../../com.aspose.words.net.system.data/datarelation/) belongs.
### getParentColumnNames() {#getParentColumnNames}
```
public String[] getParentColumnNames()
```




**Returns:**
java.lang.String[] - bu ilişkinin üst DataColumn adları.
### getParentColumns() {#getParentColumns}
```
public System.Data.DataColumn[] getParentColumns()
```


Bu [DataRelation](../../com.aspose.words.net.system.data/datarelation/) için ebeveyn sütunları olan [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnelerinin bir dizisini alır.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - Bu [DataRelation](../../com.aspose.words.net.system.data/datarelation/) 'ın üst sütunları olan [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnelerinin bir dizisi.
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


Bir [DataRelation](../../com.aspose.words.net.system.data/datarelation/) ebeveyn sütunundaki değerlerin benzersiz olmasını garantileyen [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) öğesini alır.

**Returns:**
[UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) - A [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) that makes sure that values in a parent column are unique.
### getParentTable() {#getParentTable}
```
public System.Data.DataTable getParentTable()
```


Bu [DataRelation](../../com.aspose.words.net.system.data/datarelation/) için ebeveyn [DataTable](../../com.aspose.words.net.system.data/datatable/) öğesini alır.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that is the parent table of this relation.
### getParentTableName() {#getParentTableName}
```
public String getParentTableName()
```




**Returns:**
java.lang.String - bu DataRelation'ın üst DataTable adını.
### getRelationName() {#getRelationName}
```
public String getRelationName()
```


[DataRelation](../../com.aspose.words.net.system.data/datarelation/) öğesini [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) üzerinden almak için kullanılan adı alır.

**Returns:**
java.lang.String - bir [DataRelation](../../com.aspose.words.net.system.data/datarelation/) adını.
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| childKeyConstraint | [ForeignKeyConstraint](../../com.aspose.words.net.system.data/foreignkeyconstraint/) |  |

### setNested(boolean value) {#setNested-boolean}
```
public void setNested(boolean value)
```


[DataRelation](../../com.aspose.words.net.system.data/datarelation/) nesnelerinin iç içe olup olmadığını belirten bir değer ayarlar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | boolean | true, eğer [DataRelation](../../com.aspose.words.net.system.data/datarelation/) nesneleri iç içe ise; aksi takdirde false. |

### setParentKeyConstraint(System.Data.UniqueConstraint parentKeyConstraint) {#setParentKeyConstraint-com.aspose.words.net.System.Data.UniqueConstraint}
```
public void setParentKeyConstraint(System.Data.UniqueConstraint parentKeyConstraint)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| parentKeyConstraint | [UniqueConstraint](../../com.aspose.words.net.system.data/uniqueconstraint/) |  |

