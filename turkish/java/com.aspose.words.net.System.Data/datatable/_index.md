---
title: "DataTable"
linktitle: "DataTable"
second_title: "Aspose.Words Java için"
description: "Java'da bellek içi verinin bir tablosunu temsil eder."
type: docs
weight: 25
url: /tr/java/com.aspose.words.net.system.data/datatable/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
[com.aspose.words.net.System.Data.DataTableEventListener](../../com.aspose.words.net.system.data/datatableeventlistener/)
```
public class DataTable implements System.Data.DataTableEventListener
```

Bellek içi verinin bir tablosunu temsil eder.
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [DataTable()](#DataTable) | Argüman olmadan [DataTable](../../com.aspose.words.net.system.data/datatable/) sınıfının yeni bir örneğini başlatır. |
| [DataTable(String tableName)](#DataTable-java.lang.String) | Belirtilen tablo adıyla [DataTable](../../com.aspose.words.net.system.data/datatable/) sınıfının yeni bir örneğini başlatır. |
| [DataTable(ResultSet resultSet)](#DataTable-java.sql.ResultSet) | Belirtilen ResultSet'i sarmalayarak bir nesne oluşturur. |
| [DataTable(ResultSet resultSet, String tableName)](#DataTable-java.sql.ResultSet-java.lang.String) | Belirtilen ResultSet'i sarmalayarak bir nesne oluşturur. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [acceptChanges()](#acceptChanges) | Son kez [acceptChanges()](../../com.aspose.words.net.system.data/datatable/\#acceptChanges) çağrıldığından bu tabloya yapılan tüm değişiklikleri kaydeder. |
| [addEventListener(System.Data.DataTableEventListener listener)](#addEventListener-com.aspose.words.net.System.Data.DataTableEventListener) |  |
| [clearEventListneers()](#clearEventListneers) |  |
| [close()](#close) |  |
| [containsColumn(String columnName)](#containsColumn-java.lang.String) | Verilen sütunun mevcut olup olmadığını kontrol edin |
| [getChildRelations()](#getChildRelations) | Bu [DataTable](../../com.aspose.words.net.system.data/datatable/) için alt ilişkilerin koleksiyonunu alır. |
| [getColumnName(int index)](#getColumnName-int) | .Net DataTable.Columns[i].ColumnName için analog. |
| [getColumns()](#getColumns) | Bu tabloya ait sütunların koleksiyonunu alır. |
| [getColumnsCount()](#getColumnsCount) |  |
| [getConstraints()](#getConstraints) | Bu tablo tarafından tutulan kısıtlamaların koleksiyonunu alır. |
| [getDataSet()](#getDataSet) | Bu tabloya ait [DataSet](../../com.aspose.words.net.system.data/dataset/) alır. |
| [getEnforceConstraints()](#getEnforceConstraints) |  |
| [getNamespace()](#getNamespace) | [DataTable](../../com.aspose.words.net.system.data/datatable/) içinde depolanan verinin XML temsilinin ad alanını alır. |
| [getParentRelations()](#getParentRelations) | Bu [DataTable](../../com.aspose.words.net.system.data/datatable/) için üst ilişkilerin koleksiyonunu alır. |
| [getPrimaryKey()](#getPrimaryKey) | Veri tablosu için birincil anahtar olarak işlev gören sütunların bir dizisini alır. |
| [getResultSet()](#getResultSet) | Altta yatan Java ResultSet nesnesini döndürür. |
| [getRows()](#getRows) | Bu tabloya ait satırların koleksiyonunu alır. |
| [getTableName()](#getTableName) | [DataTable](../../com.aspose.words.net.system.data/datatable/) adını alır. |
| [newRow()](#newRow) | Tabloyla aynı şemaya sahip yeni bir [DataRow](../../com.aspose.words.net.system.data/datarow/) oluşturur. |
| [onDataColumnDeleted(System.Data.DataColumn column)](#onDataColumnDeleted-com.aspose.words.net.System.Data.DataColumn) |  |
| [onDataColumnInserted(System.Data.DataColumn column)](#onDataColumnInserted-com.aspose.words.net.System.Data.DataColumn) |  |
| [onDataRowChanged(System.Data.DataRow row)](#onDataRowChanged-com.aspose.words.net.System.Data.DataRow) |  |
| [onDataRowDeleted(System.Data.DataRow row)](#onDataRowDeleted-com.aspose.words.net.System.Data.DataRow) |  |
| [onDataRowInserted(System.Data.DataRow row)](#onDataRowInserted-com.aspose.words.net.System.Data.DataRow) |  |
| [refresh()](#refresh) | ResultSet mevcutsa tüm verileri yeniden yükler. |
| [setEnforceConstraints(boolean enforceConstraints)](#setEnforceConstraints-boolean) |  |
| [setNamespace(String value)](#setNamespace-java.lang.String) | [DataTable](../../com.aspose.words.net.system.data/datatable/) içinde depolanan verinin XML temsilinin ad alanını ayarlar. |
| [setPrimaryKey(System.Data.DataColumn[] value)](#setPrimaryKey-com.aspose.words.net.System.Data.DataColumn) | Veri tablosu için birincil anahtar olarak işlev gören sütunların bir dizisini ayarlar. |
| [setTableName(String value)](#setTableName-java.lang.String) | [DataTable](../../com.aspose.words.net.system.data/datatable/) adını ayarlar. |
### DataTable() {#DataTable}
```
public DataTable()
```


Argüman olmadan [DataTable](../../com.aspose.words.net.system.data/datatable/) sınıfının yeni bir örneğini başlatır.

### DataTable(String tableName) {#DataTable-java.lang.String}
```
public DataTable(String tableName)
```


Belirtilen tablo adıyla [DataTable](../../com.aspose.words.net.system.data/datatable/) sınıfının yeni bir örneğini başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| tableName | java.lang.String | Tabloya verilecek ad. Eğer tableName null veya boş bir dize ise, [DataTableCollection](../../com.aspose.words.net.system.data/datatablecollection/) eklendiğinde varsayılan bir ad verilir. |

### DataTable(ResultSet resultSet) {#DataTable-java.sql.ResultSet}
```
public DataTable(ResultSet resultSet)
```


Belirtilen ResultSet'i sarmalayarak bir nesne oluşturur. ResultSet'in ilk sütununun meta verilerinden tablo adını almaya çalışır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| resultSet | java.sql.ResultSet | veri kümesi |

### DataTable(ResultSet resultSet, String tableName) {#DataTable-java.sql.ResultSet-java.lang.String}
```
public DataTable(ResultSet resultSet, String tableName)
```


Belirtilen ResultSet'i sarmalayarak bir nesne oluşturur.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| resultSet | java.sql.ResultSet | veri kümesi |
| tableName | java.lang.String | tablonun adı |

### acceptChanges() {#acceptChanges}
```
public void acceptChanges()
```


Son kez [acceptChanges()](../../com.aspose.words.net.system.data/datatable/\#acceptChanges) çağrıldığından bu tabloya yapılan tüm değişiklikleri kaydeder.

### addEventListener(System.Data.DataTableEventListener listener) {#addEventListener-com.aspose.words.net.System.Data.DataTableEventListener}
```
public synchronized void addEventListener(System.Data.DataTableEventListener listener)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| listener | [DataTableEventListener](../../com.aspose.words.net.system.data/datatableeventlistener/) |  |

### clearEventListneers() {#clearEventListneers}
```
public synchronized void clearEventListneers()
```




### close() {#close}
```
public void close()
```




### containsColumn(String columnName) {#containsColumn-java.lang.String}
```
public boolean containsColumn(String columnName)
```


Verilen sütunun mevcut olup olmadığını kontrol edin

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| columnName | java.lang.String | sütunun adı |

**Returns:**
boolean - `true` ise sütun verilen `columnName` ile bulunabilir
### getChildRelations() {#getChildRelations}
```
public System.Data.DataRelationCollection getChildRelations()
```


Bu [DataTable](../../com.aspose.words.net.system.data/datatable/) için alt ilişkilerin koleksiyonunu alır.

**Returns:**
[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) - A [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) that contains the child relations for the table. An empty collection is returned if no [DataRelation](../../com.aspose.words.net.system.data/datarelation/) objects exist.
### getColumnName(int index) {#getColumnName-int}
```
public String getColumnName(int index)
```


.Net DataTable.Columns[i].ColumnName için analog.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int | \- sütunun indeksi |

**Returns:**
java.lang.String - sütunun adı indeksine göre.
### getColumns() {#getColumns}
```
public System.Data.DataColumnCollection getColumns()
```


Bu tabloya ait sütunların koleksiyonunu alır.

**Returns:**
[DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) - A [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) that contains the collection of [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) objects for the table. An empty collection is returned if no [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) objects exist.
### getColumnsCount() {#getColumnsCount}
```
public int getColumnsCount()
```




**Returns:**
int - sütun sayısı
### getConstraints() {#getConstraints}
```
public System.Data.ConstraintCollection getConstraints()
```


Bu tablo tarafından tutulan kısıtlamaların koleksiyonunu alır.

**Returns:**
[ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/) - A [ConstraintCollection](../../com.aspose.words.net.system.data/constraintcollection/) that contains the collection of [Constraint](../../com.aspose.words.net.system.data/constraint/) objects for the table. An empty collection is returned if no [Constraint](../../com.aspose.words.net.system.data/constraint/) objects exist.
### getDataSet() {#getDataSet}
```
public System.Data.DataSet getDataSet()
```


Bu tabloya ait [DataSet](../../com.aspose.words.net.system.data/dataset/) alır.

**Returns:**
[DataSet](../../com.aspose.words.net.system.data/dataset/) - The [DataSet](../../com.aspose.words.net.system.data/dataset/) to which this table belongs.
### getEnforceConstraints() {#getEnforceConstraints}
```
public boolean getEnforceConstraints()
```




**Returns:**
boolean - kısıtlama ihlali olup olmadığını gösteren bayrak
### getNamespace() {#getNamespace}
```
public String getNamespace()
```


[DataTable](../../com.aspose.words.net.system.data/datatable/) içinde depolanan verinin XML temsilinin ad alanını alır.

**Returns:**
java.lang.String - [DataTable](../../com.aspose.words.net.system.data/datatable/) öğesinin ad alanı.
### getParentRelations() {#getParentRelations}
```
public System.Data.DataRelationCollection getParentRelations()
```


Bu [DataTable](../../com.aspose.words.net.system.data/datatable/) için üst ilişkilerin koleksiyonunu alır.

**Returns:**
[DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) - A [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) that contains the parent relations for the table. An empty collection is returned if no [DataRelation](../../com.aspose.words.net.system.data/datarelation/) objects exist.
### getPrimaryKey() {#getPrimaryKey}
```
public System.Data.DataColumn[] getPrimaryKey()
```


Veri tablosu için birincil anahtar olarak işlev gören sütunların bir dizisini alır.

**Returns:**
com.aspose.words.net.System.Data.DataColumn[] - [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnelerinden oluşan bir dizi.
### getResultSet() {#getResultSet}
```
public ResultSet getResultSet()
```


Alttaki Java ResultSet nesnesini döndürür. İdeal olarak DataTable ile .Net tarzında çalışmak isteriz. Ancak bazı kullanıcılar ve hatta bazı örnek kodlarımız bu özelliği kullanıyor.

**Returns:**
java.sql.ResultSet - alttaki java.sql.ResultSet
### getRows() {#getRows}
```
public System.Data.DataRowCollection getRows()
```


Bu tabloya ait satırların koleksiyonunu alır.

**Returns:**
[DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/) - A [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/) that contains [DataRow](../../com.aspose.words.net.system.data/datarow/) objects; otherwise a null value if no [DataRow](../../com.aspose.words.net.system.data/datarow/) objects exist.
### getTableName() {#getTableName}
```
public String getTableName()
```


[DataTable](../../com.aspose.words.net.system.data/datatable/) adını alır.

**Returns:**
java.lang.String - [DataTable](../../com.aspose.words.net.system.data/datatable/) öğesinin adı.
### newRow() {#newRow}
```
public System.Data.DataRow newRow()
```


Tabloyla aynı şemaya sahip yeni bir [DataRow](../../com.aspose.words.net.system.data/datarow/) oluşturur.

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - A [DataRow](../../com.aspose.words.net.system.data/datarow/) with the same schema as the [DataTable](../../com.aspose.words.net.system.data/datatable/).
### onDataColumnDeleted(System.Data.DataColumn column) {#onDataColumnDeleted-com.aspose.words.net.System.Data.DataColumn}
```
public void onDataColumnDeleted(System.Data.DataColumn column)
```


DataColumn silindiğinde dinleyiciyi güncelle

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) |  |

### onDataColumnInserted(System.Data.DataColumn column) {#onDataColumnInserted-com.aspose.words.net.System.Data.DataColumn}
```
public void onDataColumnInserted(System.Data.DataColumn column)
```


DataColumn eklendiğinde dinleyiciyi güncelle

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) |  |

### onDataRowChanged(System.Data.DataRow row) {#onDataRowChanged-com.aspose.words.net.System.Data.DataRow}
```
public void onDataRowChanged(System.Data.DataRow row)
```


DataRow değiştirildiğinde dinleyiciyi güncelle

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

### onDataRowDeleted(System.Data.DataRow row) {#onDataRowDeleted-com.aspose.words.net.System.Data.DataRow}
```
public void onDataRowDeleted(System.Data.DataRow row)
```


DataRow silindiğinde dinleyiciyi güncelle

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

### onDataRowInserted(System.Data.DataRow row) {#onDataRowInserted-com.aspose.words.net.System.Data.DataRow}
```
public void onDataRowInserted(System.Data.DataRow row)
```


DataRow eklendiğinde dinleyiciyi güncelle

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) |  |

### refresh() {#refresh}
```
public void refresh()
```


ResultSet mevcutsa tüm verileri yeniden yükler.

### setEnforceConstraints(boolean enforceConstraints) {#setEnforceConstraints-boolean}
```
public void setEnforceConstraints(boolean enforceConstraints)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| enforceConstraints | boolean | kısıtlama ihlali olup olmadığını gösteren bayraktır |

### setNamespace(String value) {#setNamespace-java.lang.String}
```
public void setNamespace(String value)
```


[DataTable](../../com.aspose.words.net.system.data/datatable/) içinde depolanan verinin XML temsilinin ad alanını ayarlar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | java.lang.String | [DataTable](../../com.aspose.words.net.system.data/datatable/) öğesinin ad alanı. |

### setPrimaryKey(System.Data.DataColumn[] value) {#setPrimaryKey-com.aspose.words.net.System.Data.DataColumn}
```
public void setPrimaryKey(System.Data.DataColumn[] value)
```


Veri tablosu için birincil anahtar olarak işlev gören sütunların bir dizisini ayarlar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | [DataColumn\[\]](../../com.aspose.words.net.system.data/datacolumn/) | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnelerinden oluşan bir dizi. |

### setTableName(String value) {#setTableName-java.lang.String}
```
public void setTableName(String value)
```


[DataTable](../../com.aspose.words.net.system.data/datatable/) adını ayarlar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | java.lang.String | [DataTable](../../com.aspose.words.net.system.data/datatable/) öğesinin adı. |

