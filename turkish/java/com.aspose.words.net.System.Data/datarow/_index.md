---
title: "DataRow"
linktitle: "DataRow"
second_title: "Aspose.Words Java için"
description: "Java'da bir DataTable içindeki veri satırını temsil eder."
type: docs
weight: 20
url: /tr/java/com.aspose.words.net.system.data/datarow/
---

**Inheritance:**
java.lang.Object
```
public class DataRow
```

Bir [DataTable](../../com.aspose.words.net.system.data/datatable/) içindeki veri satırını temsil eder.
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [delete()](#delete) | [DataRow](../../com.aspose.words.net.system.data/datarow/) öğesini siler. |
| [get(System.Data.DataColumn column)](#get-com.aspose.words.net.System.Data.DataColumn) | Belirtilen [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) içinde depolanan veriyi alır. |
| [get(int columnIndex)](#get-int) | İndeks ile belirtilen sütunda depolanan veriyi alır. |
| [get(String columnName)](#get-java.lang.String) | İsim ile belirtilen sütunda depolanan veriyi alır. |
| [getChildRows(System.Data.DataRelation relation)](#getChildRows-com.aspose.words.net.System.Data.DataRelation) | Belirtilen [DataRelation](../../com.aspose.words.net.system.data/datarelation/) kullanarak bu [DataRow](../../com.aspose.words.net.system.data/datarow/) öğesinin alt satırlarını alır. |
| [getItemArray()](#getItemArray) | Bu satır için tüm değerleri bir dizi aracılığıyla alır. |
| [getKeyValues(System.Data.DataKey childKey)](#getKeyValues-com.aspose.words.net.System.Data.DataKey) |  |
| [getOriginalValue(String columnName)](#getOriginalValue-java.lang.String) |  |
| [getParentRow(System.Data.DataRelation relation)](#getParentRow-com.aspose.words.net.System.Data.DataRelation) | Belirtilen [DataRelation](../../com.aspose.words.net.system.data/datarelation/) kullanarak bir [DataRow](../../com.aspose.words.net.system.data/datarow/) öğesinin üst satırını alır. |
| [getParentRows(System.Data.DataRelation relation)](#getParentRows-com.aspose.words.net.System.Data.DataRelation) | Belirtilen [DataRelation](../../com.aspose.words.net.system.data/datarelation/) kullanarak bir [DataRow](../../com.aspose.words.net.system.data/datarow/) öğesinin üst satırlarını alır. |
| [getRowState()](#getRowState) | Satırın [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/) ile ilişkisine göre mevcut durumunu alır. |
| [getTable()](#getTable) | Bu satırın şeması olan [DataTable](../../com.aspose.words.net.system.data/datatable/) öğesini alır. |
| [readFrom(ResultSet resultSet)](#readFrom-java.sql.ResultSet) | java.sql.ResultSet'ten değerleri okur |
| [remove(int index)](#remove-int) |  |
| [set(System.Data.DataColumn column, Object value)](#set-com.aspose.words.net.System.Data.DataColumn-java.lang.Object) | Belirtilen [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) içinde depolanan veriyi ayarlar. |
| [set(int columnIndex, Object value)](#set-int-java.lang.Object) | İndeks ile belirtilen sütunda depolanan veriyi ayarlar. |
| [set(String columnName, Object value)](#set-java.lang.String-java.lang.Object) | İsim ile belirtilen sütunda depolanan veriyi ayarlar. |
| [setItemArray(Object[] value)](#setItemArray-java.lang.Object) | Bu satır için tüm değerleri bir dizi aracılığıyla ayarlar. |
| [setOriginalValue(String columnName, Object data)](#setOriginalValue-java.lang.String-java.lang.Object) |  |
| [setRowState(int state)](#setRowState-int) |  |
| [toString()](#toString) |  |
### delete() {#delete}
```
public void delete()
```


[DataRow](../../com.aspose.words.net.system.data/datarow/) öğesini siler.

### get(System.Data.DataColumn column) {#get-com.aspose.words.net.System.Data.DataColumn}
```
public Object get(System.Data.DataColumn column)
```


Belirtilen [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) içinde depolanan veriyi alır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Veriyi içeren bir [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |

**Returns:**
java.lang.Object - Veriyi içeren bir java.lang.Object.
### get(int columnIndex) {#get-int}
```
public Object get(int columnIndex)
```


İndeks ile belirtilen sütunda depolanan veriyi alır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| columnIndex | int | Sütunun sıfır tabanlı indeksi. |

**Returns:**
java.lang.Object - Veriyi içeren bir java.lang.Object.
### get(String columnName) {#get-java.lang.String}
```
public Object get(String columnName)
```


İsim ile belirtilen sütunda depolanan veriyi alır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| columnName | java.lang.String | Sütunun adı. |

**Returns:**
java.lang.Object - Veriyi içeren bir java.lang.Object.
### getChildRows(System.Data.DataRelation relation) {#getChildRows-com.aspose.words.net.System.Data.DataRelation}
```
public System.Data.DataRow[] getChildRows(System.Data.DataRelation relation)
```


Belirtilen [DataRelation](../../com.aspose.words.net.system.data/datarelation/) kullanarak bu [DataRow](../../com.aspose.words.net.system.data/datarow/) öğesinin alt satırlarını alır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | Kullanılacak [DataRelation](../../com.aspose.words.net.system.data/datarelation/). |

**Returns:**
com.aspose.words.net.System.Data.DataRow[] - [DataRow](../../com.aspose.words.net.system.data/datarow/) nesnelerinden oluşan bir dizi veya uzunluğu sıfır olan bir dizi.
### getItemArray() {#getItemArray}
```
public Object[] getItemArray()
```


Bu satır için tüm değerleri bir dizi aracılığıyla alır.

**Returns:**
java.lang.Object[] - java.lang.Object tipinde bir dizi.
### getKeyValues(System.Data.DataKey childKey) {#getKeyValues-com.aspose.words.net.System.Data.DataKey}
```
public Object[] getKeyValues(System.Data.DataKey childKey)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| childKey | [DataKey](../../com.aspose.words.net.system.data/datakey/) |  |

**Returns:**
java.lang.Object[]
### getOriginalValue(String columnName) {#getOriginalValue-java.lang.String}
```
public Object getOriginalValue(String columnName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| columnName | java.lang.String |  |

**Returns:**
java.lang.Object
### getParentRow(System.Data.DataRelation relation) {#getParentRow-com.aspose.words.net.System.Data.DataRelation}
```
public System.Data.DataRow getParentRow(System.Data.DataRelation relation)
```


Belirtilen [DataRelation](../../com.aspose.words.net.system.data/datarelation/) kullanarak bir [DataRow](../../com.aspose.words.net.system.data/datarow/) öğesinin üst satırını alır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | Kullanılacak [DataRelation](../../com.aspose.words.net.system.data/datarelation/). |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - The parent [DataRow](../../com.aspose.words.net.system.data/datarow/) of the current row.
### getParentRows(System.Data.DataRelation relation) {#getParentRows-com.aspose.words.net.System.Data.DataRelation}
```
public System.Data.DataRow[] getParentRows(System.Data.DataRelation relation)
```


Belirtilen [DataRelation](../../com.aspose.words.net.system.data/datarelation/) kullanarak bir [DataRow](../../com.aspose.words.net.system.data/datarow/) öğesinin üst satırlarını alır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | Kullanılacak [DataRelation](../../com.aspose.words.net.system.data/datarelation/). |

**Returns:**
com.aspose.words.net.System.Data.DataRow[] - [DataRow](../../com.aspose.words.net.system.data/datarow/) nesnelerinden oluşan bir dizi veya uzunluğu sıfır olan bir dizi.
### getRowState() {#getRowState}
```
public int getRowState()
```


Satırın [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/) ile ilişkisine göre mevcut durumunu alır.

**Returns:**
int - [DataRowState](../../com.aspose.words.net.system.data/datarowstate/) değerlerinden biri. Döndürülen değer, [DataRowState](../../com.aspose.words.net.system.data/datarowstate/) sabitlerinin bit düzeyinde bir birleşimidir.
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


Bu satırın şeması olan [DataTable](../../com.aspose.words.net.system.data/datatable/) öğesini alır.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The [DataTable](../../com.aspose.words.net.system.data/datatable/) to which this row belongs.
### readFrom(ResultSet resultSet) {#readFrom-java.sql.ResultSet}
```
public boolean readFrom(ResultSet resultSet)
```


java.sql.ResultSet'ten değerleri okur

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| resultSet | java.sql.ResultSet | okunacak depolama |

**Returns:**
boolean - okuma hatası oluşmadıysa true
### remove(int index) {#remove-int}
```
public void remove(int index)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int |  |

### set(System.Data.DataColumn column, Object value) {#set-com.aspose.words.net.System.Data.DataColumn-java.lang.Object}
```
public void set(System.Data.DataColumn column, Object value)
```


Belirtilen [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) içinde depolanan veriyi ayarlar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Veriyi içeren bir [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |
| değer | java.lang.Object | Veriyi içeren bir java.lang.Object. |

### set(int columnIndex, Object value) {#set-int-java.lang.Object}
```
public void set(int columnIndex, Object value)
```


İndeks ile belirtilen sütunda depolanan veriyi ayarlar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| columnIndex | int | Sütunun sıfır tabanlı indeksi. |
| değer | java.lang.Object | Veriyi içeren bir java.lang.Object. |

### set(String columnName, Object value) {#set-java.lang.String-java.lang.Object}
```
public void set(String columnName, Object value)
```


İsim ile belirtilen sütunda depolanan veriyi ayarlar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| columnName | java.lang.String | Sütunun adı. |
| değer | java.lang.Object | Veriyi içeren bir java.lang.Object. |

### setItemArray(Object[] value) {#setItemArray-java.lang.Object}
```
public void setItemArray(Object[] value)
```


Bu satır için tüm değerleri bir dizi aracılığıyla ayarlar.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.Object[] | java.lang.Object tipinde bir dizi. |

### setOriginalValue(String columnName, Object data) {#setOriginalValue-java.lang.String-java.lang.Object}
```
public void setOriginalValue(String columnName, Object data)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| columnName | java.lang.String |  |
| veri | java.lang.Object |  |

### setRowState(int state) {#setRowState-int}
```
public void setRowState(int state)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| durum | int |  |

### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
