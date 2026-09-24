---
title: "DataTableReader"
linktitle: "DataTableReader"
second_title: "Aspose.Words Java için"
description: "DataTableReader, bir veya daha fazla DataTable nesnesinin içeriğini Java'da yalnızca okunabilir, ileriye doğru tek yönlü sonuç kümeleri biçiminde elde eder."
type: docs
weight: 27
url: /tr/java/com.aspose.words.net.system.data/datatablereader/
---

**Inheritance:**
java.lang.Object, [com.aspose.words.net.System.Data.Common.DbDataReader](../../com.aspose.words.net.system.data.common/dbdatareader/)
```
public class DataTableReader extends System.Data.Common.DbDataReader
```

[DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) bir veya daha fazla [DataTable](../../com.aspose.words.net.system.data/datatable/) nesnesinin içeriğini yalnızca okunabilir, ileriye doğru tek yönlü sonuç kümeleri biçiminde elde eder.
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [DataTableReader(System.Data.DataTable dataTable)](#DataTableReader-com.aspose.words.net.System.Data.DataTable) | Sağlanan [DataTable](../../com.aspose.words.net.system.data/datatable/) verilerini kullanarak [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) sınıfının yeni bir örneğini başlatır. |
| [DataTableReader(System.Data.DataTable[] dataTables)](#DataTableReader-com.aspose.words.net.System.Data.DataTable) | Sağlanan [DataTable](../../com.aspose.words.net.system.data/datatable/) nesnelerinin dizisini kullanarak [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) sınıfının yeni bir örneğini başlatır. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [close()](#close) | Mevcut [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) öğesini kapatır. |
| [get(int ordinal)](#get-int) | Belirtilen sütun sırasına göre, belirtilen sütunun yerel formatındaki değerini alır. |
| [get(String name)](#get-java.lang.String) | Belirtilen sütun adına göre, belirtilen sütunun yerel formatındaki değerini alır. |
| [getDepth()](#getDepth) | [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) öğesinin mevcut satırı için iç içe derinlik. |
| [getFieldCount()](#getFieldCount) | Mevcut satırdaki sütun sayısını döndürür. |
| [getFieldType(int ordinal)](#getFieldType-int) | Nesnenin veri tipi olan java.lang.Class'ı alır. |
| [getName(int ordinal)](#getName-int) | Belirtilen sütunun değerini java.lang.String olarak alır. |
| [getRecordsAffected()](#getRecordsAffected) | SQL ifadesinin yürütülmesiyle eklenen, değiştirilen veya silinen satır sayısını alır. |
| [getSchemaTable()](#getSchemaTable) | [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) öğesinin sütun meta verilerini tanımlayan bir [DataTable](../../com.aspose.words.net.system.data/datatable/) döndürür. |
| [getValue(int ordinal)](#getValue-int) | Belirtilen sütunun yerel formatındaki değerini alır. |
| [hasRows()](#hasRows) | [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) bir veya daha fazla satır içerip içermediğini gösteren bir değer alır. |
| [isClosed()](#isClosed) | [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) kapalı olup olmadığını gösteren bir değer alır. |
| [iterator()](#iterator) | Öğe koleksiyonunda yineleme yapmak için kullanılabilecek bir yineleyici döndürür. |
| [nextResult()](#nextResult) | [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) varsa bir sonraki sonuç kümesine ilerletir. |
| [read()](#read) | [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) bir sonraki kayda ilerletir. |
### DataTableReader(System.Data.DataTable dataTable) {#DataTableReader-com.aspose.words.net.System.Data.DataTable}
```
public DataTableReader(System.Data.DataTable dataTable)
```


Sağlanan [DataTable](../../com.aspose.words.net.system.data/datatable/) verilerini kullanarak [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) sınıfının yeni bir örneğini başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| dataTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Yeni [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) öğesinin sonuç kümesini aldığı [DataTable](../../com.aspose.words.net.system.data/datatable/). |

### DataTableReader(System.Data.DataTable[] dataTables) {#DataTableReader-com.aspose.words.net.System.Data.DataTable}
```
public DataTableReader(System.Data.DataTable[] dataTables)
```


Sağlanan [DataTable](../../com.aspose.words.net.system.data/datatable/) nesnelerinin dizisini kullanarak [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) sınıfının yeni bir örneğini başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| dataTables | [DataTable\[\]](../../com.aspose.words.net.system.data/datatable/) | Yeni [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) nesnesine sonuçları sağlayan [DataTable](../../com.aspose.words.net.system.data/datatable/) nesnelerinin dizisi. |

### close() {#close}
```
public void close()
```


Mevcut [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) öğesini kapatır.

### get(int ordinal) {#get-int}
```
public Object get(int ordinal)
```


Belirtilen sütun sırasına göre, belirtilen sütunun yerel formatındaki değerini alır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sıra | int | Sıfır tabanlı sütun sırası. |

**Returns:**
java.lang.Object - Belirtilen sütunun yerel formatındaki değeri.
### get(String name) {#get-java.lang.String}
```
public Object get(String name)
```


Belirtilen sütun adına göre, belirtilen sütunun yerel formatındaki değerini alır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String | Sütunun adı. |

**Returns:**
java.lang.Object - Belirtilen sütunun yerel formatındaki değeri.
### getDepth() {#getDepth}
```
public int getDepth()
```


[DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) öğesinin mevcut satırı için iç içe derinlik.

**Returns:**
int - Mevcut satır için iç içe derinlik; her zaman sıfır.
### getFieldCount() {#getFieldCount}
```
public int getFieldCount()
```


Mevcut satırdaki sütun sayısını döndürür.

**Returns:**
int - Geçerli bir sonuç kümesinde konumlandırılmadığında 0; aksi takdirde mevcut satırdaki sütun sayısı.
### getFieldType(int ordinal) {#getFieldType-int}
```
public Class getFieldType(int ordinal)
```


Nesnenin veri tipi olan java.lang.Class'ı alır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sıra | int | Sıfır tabanlı sütun sırası. |

**Returns:**
java.lang.Class - Nesnenin veri tipi olan java.lang.Class.
### getName(int ordinal) {#getName-int}
```
public String getName(int ordinal)
```


Belirtilen sütunun değerini java.lang.String olarak alır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sıra | int | Sıfır tabanlı sütun sırası |

**Returns:**
java.lang.String - Belirtilen sütunun adı.
### getRecordsAffected() {#getRecordsAffected}
```
public int getRecordsAffected()
```


SQL ifadesinin yürütülmesiyle eklenen, değiştirilen veya silinen satır sayısını alır.

**Returns:**
int - Bu [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) bu özelliği desteklemez ve her zaman 0 döndürür.
### getSchemaTable() {#getSchemaTable}
```
public System.Data.DataTable getSchemaTable()
```


[DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) öğesinin sütun meta verilerini tanımlayan bir [DataTable](../../com.aspose.words.net.system.data/datatable/) döndürür.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that describes the column metadata.
### getValue(int ordinal) {#getValue-int}
```
public Object getValue(int ordinal)
```


Belirtilen sütunun yerel formatındaki değerini alır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sıra | int | Sıfır tabanlı sütun sırası |

**Returns:**
java.lang.Object - Belirtilen sütunun değeri. Bu yöntem, null sütunlar için DBNull döndürür.
### hasRows() {#hasRows}
```
public boolean hasRows()
```


[DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) bir veya daha fazla satır içerip içermediğini gösteren bir değer alır.

**Returns:**
boolean - [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) bir veya daha fazla satır içeriyorsa true; aksi takdirde false.
### isClosed() {#isClosed}
```
public boolean isClosed()
```


[DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) kapalı olup olmadığını gösteren bir değer alır.

**Returns:**
boolean - [DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) kapalıysa true döndürür; aksi takdirde false.
### iterator() {#iterator}
```
public Iterator iterator()
```


Öğe koleksiyonunda yineleme yapmak için kullanılabilecek bir yineleyici döndürür.

**Returns:**
java.util.Iterator - Öğeler koleksiyonunu temsil eden bir java.util.Iterator nesnesi.
### nextResult() {#nextResult}
```
public boolean nextResult()
```


[DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) varsa bir sonraki sonuç kümesine ilerletir.

**Returns:**
boolean - Başka bir sonuç kümesi varsa true; aksi takdirde false.
### read() {#read}
```
public boolean read()
```


[DataTableReader](../../com.aspose.words.net.system.data/datatablereader/) bir sonraki kayda ilerletir.

**Returns:**
boolean - Okunacak başka bir satır varsa true; aksi takdirde false.
