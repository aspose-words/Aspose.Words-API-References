---
title: "DataColumnCollection"
linktitle: "DataColumnCollection"
second_title: "Aspose.Words Java için"
description: "Java'da bir DataTable için DataColumn nesnelerinin bir koleksiyonunu temsil eder."
type: docs
weight: 15
url: /tr/java/com.aspose.words.net.system.data/datacolumncollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataColumnCollection implements Iterable
```

Bir [DataTable](../../com.aspose.words.net.system.data/datatable/) için [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnelerinin bir koleksiyonunu temsil eder.
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [add(System.Data.DataColumn column)](#add-com.aspose.words.net.System.Data.DataColumn) | Belirtilen [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnesini oluşturur ve [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) koleksiyonuna ekler. |
| [add(String columnName)](#add-java.lang.String) | Belirtilen ada sahip bir [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnesini oluşturur ve [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) koleksiyonuna ekler. |
| [add(String columnName, Class type)](#add-java.lang.String-java.lang.Class) | Belirtilen ada ve türe sahip bir [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnesini oluşturur ve [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) koleksiyonuna ekler. |
| [add(String columnName, Class type, int columnMapping, boolean allowAutoIncrement, boolean allowDBNull)](#add-java.lang.String-java.lang.Class-int-boolean-boolean) | Belirtilen ad, tip ve belirli değerlere sahip bir [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnesini oluşturur ve sütun koleksiyonuna ekler. |
| [clear()](#clear) | Koleksiyondaki tüm sütunları temizler. |
| [contains(String name)](#contains-java.lang.String) | Koleksiyonun belirtilen ada sahip bir sütun içerip içermediğini kontrol eder. |
| [get(int index)](#get-int) | Belirtilen indeksteki koleksiyondan [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnesini alır. |
| [get(String name)](#get-java.lang.String) | Belirtilen ada sahip koleksiyondan [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnesini alır. |
| [getCount()](#getCount) |  |
| [indexOf(System.Data.DataColumn column)](#indexOf-com.aspose.words.net.System.Data.DataColumn) | İsimle belirtilen bir sütunun indeksini alır. |
| [indexOf(String columnName)](#indexOf-java.lang.String) | Belirli isimli sütunun indeksini alır (isim büyük/küçük harfe duyarlı değildir). |
| [iterator()](#iterator) |  |
| [remove(System.Data.DataColumn column)](#remove-com.aspose.words.net.System.Data.DataColumn) | Belirtilen [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnesini koleksiyondan kaldırır. |
| [remove(String name)](#remove-java.lang.String) | Belirtilen isme sahip [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnesini koleksiyondan kaldırır. |
### add(System.Data.DataColumn column) {#add-com.aspose.words.net.System.Data.DataColumn}
```
public void add(System.Data.DataColumn column)
```


Belirtilen [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnesini oluşturur ve [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) koleksiyonuna ekler.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Eklenecek [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |

### add(String columnName) {#add-java.lang.String}
```
public void add(String columnName)
```


Belirtilen ada sahip bir [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnesini oluşturur ve [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) koleksiyonuna ekler.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| columnName | java.lang.String | Sütunun adı. |

### add(String columnName, Class type) {#add-java.lang.String-java.lang.Class}
```
public System.Data.DataColumn add(String columnName, Class type)
```


Belirtilen ada ve türe sahip bir [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnesini oluşturur ve [DataColumnCollection](../../com.aspose.words.net.system.data/datacolumncollection/) koleksiyonuna ekler.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| columnName | java.lang.String | Sütun oluştururken kullanılacak [DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String). |
| type | java.lang.Class | Yeni sütunun [DataColumn.getDataType()](../../com.aspose.words.net.system.data/datacolumn/\#getDataType) / [DataColumn.setDataType(java.lang.Class)](../../com.aspose.words.net.system.data/datacolumn/\#setDataType-java.lang.Class) özelliği. |

**Returns:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn/) - The newly created [DataColumn](../../com.aspose.words.net.system.data/datacolumn/).
### add(String columnName, Class type, int columnMapping, boolean allowAutoIncrement, boolean allowDBNull) {#add-java.lang.String-java.lang.Class-int-boolean-boolean}
```
public System.Data.DataColumn add(String columnName, Class type, int columnMapping, boolean allowAutoIncrement, boolean allowDBNull)
```


Belirtilen ad, tip ve belirli değerlere sahip bir [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnesini oluşturur ve sütun koleksiyonuna ekler.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| columnName | java.lang.String | name |
| tip | java.lang.Class | veri türü |
| sütunEşlemesi | int | sütun eşleme türü |
| autoArtışİzinVer | boolean | otomatik artışa izin verilip verilmediği |
| DBNullİzinVer | boolean | DBNull değeri izin verilip verilmediği |

**Returns:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn/) - created a [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) instance.
### clear() {#clear}
```
public void clear()
```


Koleksiyondaki tüm sütunları temizler.

### contains(String name) {#contains-java.lang.String}
```
public boolean contains(String name)
```


Koleksiyonun belirtilen ada sahip bir sütun içerip içermediğini kontrol eder.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String | Aranacak sütunun [DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String) özelliği. |

**Returns:**
boolean - bu isimde bir sütun varsa true; aksi takdirde false.
### get(int index) {#get-int}
```
public System.Data.DataColumn get(int index)
```


Belirtilen indeksteki koleksiyondan [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnesini alır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int | Döndürülecek sütunun sıfır tabanlı indeksi. |

**Returns:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn/) - The [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) at the specified index.
### get(String name) {#get-java.lang.String}
```
public System.Data.DataColumn get(String name)
```


Belirtilen ada sahip koleksiyondan [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnesini alır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String | Döndürülecek sütunun [DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String) özelliği. |

**Returns:**
[DataColumn](../../com.aspose.words.net.system.data/datacolumn/) - The [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) in the collection with the specified [DataColumn.getColumnName()](../../com.aspose.words.net.system.data/datacolumn/\#getColumnName) / [DataColumn.setColumnName(java.lang.String)](../../com.aspose.words.net.system.data/datacolumn/\#setColumnName-java.lang.String); otherwise a null value if the [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) does not exist.
### getCount() {#getCount}
```
public int getCount()
```




**Returns:**
int - bir koleksiyondaki toplam öğe sayısı.
### indexOf(System.Data.DataColumn column) {#indexOf-com.aspose.words.net.System.Data.DataColumn}
```
public int indexOf(System.Data.DataColumn column)
```


İsimle belirtilen bir sütunun indeksini alır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Döndürülecek sütunun adı. |

**Returns:**
int - bulunursa,  column  tarafından belirtilen sütunun indeksi; aksi takdirde -1.
### indexOf(String columnName) {#indexOf-java.lang.String}
```
public int indexOf(String columnName)
```


Belirli isimli sütunun indeksini alır (isim büyük/küçük harfe duyarlı değildir).

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| columnName | java.lang.String | Bulunacak sütunun adı. |

**Returns:**
int - belirtilen isimli sütunun sıfır tabanlı indeksi, veya sütun koleksiyonda yoksa -1.
### iterator() {#iterator}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator
### remove(System.Data.DataColumn column) {#remove-com.aspose.words.net.System.Data.DataColumn}
```
public void remove(System.Data.DataColumn column)
```


Belirtilen [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnesini koleksiyondan kaldırır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| column | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | Kaldırılacak [DataColumn](../../com.aspose.words.net.system.data/datacolumn/). |

### remove(String name) {#remove-java.lang.String}
```
public void remove(String name)
```


Belirtilen isme sahip [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) nesnesini koleksiyondan kaldırır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String | Kaldırılacak sütunun adı. |

