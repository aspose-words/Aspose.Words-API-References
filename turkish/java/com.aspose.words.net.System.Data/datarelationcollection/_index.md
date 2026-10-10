---
title: "DataRelationCollection"
linktitle: "DataRelationCollection"
second_title: "Aspose.Words Java için"
description: "Java'da bu DataSet için DataRelation nesnelerinin koleksiyonunu temsil eder."
type: docs
weight: 19
url: /tr/java/com.aspose.words.net.system.data/datarelationcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataRelationCollection implements Iterable
```

Bu [DataSet](../../com.aspose.words.net.system.data/dataset/) için [DataRelation](../../com.aspose.words.net.system.data/datarelation/) nesnelerinin koleksiyonunu temsil eder.
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [add(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#add-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | Belirtilen bir üst ve alt sütunla bir [DataRelation](../../com.aspose.words.net.system.data/datarelation/) oluşturur ve koleksiyona ekler. |
| [add(System.Data.DataRelation relation)](#add-com.aspose.words.net.System.Data.DataRelation) | Bir [DataRelation](../../com.aspose.words.net.system.data/datarelation/) öğesini [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) koleksiyonuna ekler. |
| [add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String parentColumnName, String childColumnName)](#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String-java.lang.String) | Koleksiyona bir ilişki ekler. |
| [add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)](#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String) | Koleksiyona bir ilişki ekler. |
| [add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)](#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn) | Belirtilen ad, üst ve alt sütunlarla bir [DataRelation](../../com.aspose.words.net.system.data/datarelation/) oluşturur ve koleksiyona ekler. |
| [add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)](#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean) | Belirtilen ad, üst ve alt sütunlarla, createConstraints parametresinin değerine göre isteğe bağlı kısıtlamalarla bir [DataRelation](../../com.aspose.words.net.system.data/datarelation/) oluşturur ve koleksiyona ekler. |
| [clear()](#clear) | Koleksiyondaki tüm ilişkileri temizler. |
| [contains(System.Data.DataRelation relation)](#contains-com.aspose.words.net.System.Data.DataRelation) | Koleksiyonda belirli bir ada (büyük/küçük harf duyarsız) sahip bir DataRelation olup olmadığını doğrular. |
| [get(int index)](#get-int) | Belirtilen indeksteki [DataRelation](../../com.aspose.words.net.system.data/datarelation/) nesnesini alır. |
| [get(String name)](#get-java.lang.String) | İsimle belirtilen [DataRelation](../../com.aspose.words.net.system.data/datarelation/) nesnesini alır. |
| [getCount()](#getCount) |  |
| [indexOf(System.Data.DataRelation relation)](#indexOf-com.aspose.words.net.System.Data.DataRelation) | Belirtilen [DataRelation](../../com.aspose.words.net.system.data/datarelation/) nesnesinin indeksini alır. |
| [iterator()](#iterator) |  |
| [removeAt(int index)](#removeAt-int) | Koleksiyondan belirtilen indeksteki ilişkiyi kaldırır. |
### add(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#add-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public void add(System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


Belirtilen bir üst ve alt sütunla bir [DataRelation](../../com.aspose.words.net.system.data/datarelation/) oluşturur ve koleksiyona ekler.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | İlişkinin üst sütunu. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | İlişkinin alt sütunu. |

### add(System.Data.DataRelation relation) {#add-com.aspose.words.net.System.Data.DataRelation}
```
public void add(System.Data.DataRelation relation)
```


Bir [DataRelation](../../com.aspose.words.net.system.data/datarelation/) öğesini [DataRelationCollection](../../com.aspose.words.net.system.data/datarelationcollection/) koleksiyonuna ekler.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | Koleksiyona eklenecek DataRelation. |

### add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String parentColumnName, String childColumnName) {#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String-java.lang.String}
```
public void add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String parentColumnName, String childColumnName)
```


Koleksiyona bir ilişki ekler. Çoğaltma vb. kontrolleri yapmaz.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| parentTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | İlişkinin üst tablosu. |
| childTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | İlişkinin alt tablosu. |
| parentColumnName | java.lang.String | İlişkinin üst sütununun adı. |
| childColumnName | java.lang.String | İlişkinin alt sütununun adı. |

### add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames) {#add-com.aspose.words.net.System.Data.DataTable-com.aspose.words.net.System.Data.DataTable-java.lang.String---java.lang.String}
```
public void add(System.Data.DataTable parentTable, System.Data.DataTable childTable, String[] parentColumnNames, String[] childColumnNames)
```


Koleksiyona bir ilişki ekler. Çoğaltma vb. kontrolleri yapmaz.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| parentTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | İlişkinin üst tablosu. |
| childTable | [DataTable](../../com.aspose.words.net.system.data/datatable/) | İlişkinin alt tablosu. |
| parentColumnNames | java.lang.String[] | İlişkinin üst sütun adlarının dizisi. |
| childColumnNames | java.lang.String[] | İlişkinin alt sütun adlarının dizisi. |

### add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn) {#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn}
```
public void add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn)
```


Belirtilen ad, üst ve alt sütunlarla bir [DataRelation](../../com.aspose.words.net.system.data/datarelation/) oluşturur ve koleksiyona ekler.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String | İlişkinin adı. |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | İlişkinin üst sütunu. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | İlişkinin alt sütunu. |

### add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints) {#add-java.lang.String-com.aspose.words.net.System.Data.DataColumn-com.aspose.words.net.System.Data.DataColumn-boolean}
```
public void add(String name, System.Data.DataColumn parentColumn, System.Data.DataColumn childColumn, boolean createConstraints)
```


Belirtilen ad, üst ve alt sütunlarla, createConstraints parametresinin değerine göre isteğe bağlı kısıtlamalarla bir [DataRelation](../../com.aspose.words.net.system.data/datarelation/) oluşturur ve koleksiyona ekler.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String | İlişkinin adı. |
| parentColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | İlişkinin üst sütunu. |
| childColumn | [DataColumn](../../com.aspose.words.net.system.data/datacolumn/) | İlişkinin alt sütunu. |
| createConstraints | boolean | Kısıtlamaları oluşturmak için true; aksi takdirde false. (Varsayılan true'dur). |

### clear() {#clear}
```
public void clear()
```


Koleksiyondaki tüm ilişkileri temizler.

### contains(System.Data.DataRelation relation) {#contains-com.aspose.words.net.System.Data.DataRelation}
```
public boolean contains(System.Data.DataRelation relation)
```


Koleksiyonda belirli bir ada (büyük/küçük harf duyarsız) sahip bir DataRelation olup olmadığını doğrular.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | Bulunacak ilişkinin adı. |

**Returns:**
boolean - belirtilen ada sahip bir ilişki varsa true; aksi takdirde false.
### get(int index) {#get-int}
```
public System.Data.DataRelation get(int index)
```


Belirtilen indeksteki [DataRelation](../../com.aspose.words.net.system.data/datarelation/) nesnesini alır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int | Bulunacak sıfır tabanlı indeks. |

**Returns:**
[DataRelation](../../com.aspose.words.net.system.data/datarelation/) - The [DataRelation](../../com.aspose.words.net.system.data/datarelation/), or a null value if the specified [DataRelation](../../com.aspose.words.net.system.data/datarelation/) does not exist.
### get(String name) {#get-java.lang.String}
```
public System.Data.DataRelation get(String name)
```


İsimle belirtilen [DataRelation](../../com.aspose.words.net.system.data/datarelation/) nesnesini alır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String | Bulunacak ilişkinin adı. |

**Returns:**
[DataRelation](../../com.aspose.words.net.system.data/datarelation/) - The named [DataRelation](../../com.aspose.words.net.system.data/datarelation/), or a null value if the specified [DataRelation](../../com.aspose.words.net.system.data/datarelation/) does not exist.
### getCount() {#getCount}
```
public int getCount()
```




**Returns:**
int - bir koleksiyondaki toplam öğe sayısı
### indexOf(System.Data.DataRelation relation) {#indexOf-com.aspose.words.net.System.Data.DataRelation}
```
public int indexOf(System.Data.DataRelation relation)
```


Belirtilen [DataRelation](../../com.aspose.words.net.system.data/datarelation/) nesnesinin indeksini alır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| relation | [DataRelation](../../com.aspose.words.net.system.data/datarelation/) | Aranacak ilişki. |

**Returns:**
int - ilişkinin 0 tabanlı indeksi, veya koleksiyonda bulunamazsa -1.
### iterator() {#iterator}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator
### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Koleksiyondan belirtilen indeksteki ilişkiyi kaldırır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int | Kaldırılacak ilişkinin indeksi. |

