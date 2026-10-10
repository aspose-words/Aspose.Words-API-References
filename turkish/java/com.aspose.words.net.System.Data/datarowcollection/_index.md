---
title: "DataRowCollection"
linktitle: "DataRowCollection"
second_title: "Aspose.Words Java için"
description: "Java'da bir DataTable için satır koleksiyonunu temsil eder."
type: docs
weight: 21
url: /tr/java/com.aspose.words.net.system.data/datarowcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataRowCollection implements Iterable
```

Bir [DataTable](../../com.aspose.words.net.system.data/datatable/) için satır koleksiyonunu temsil eder.
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [add(System.Data.DataRow row)](#add-com.aspose.words.net.System.Data.DataRow) | Belirtilen [DataRow](../../com.aspose.words.net.system.data/datarow/) nesnesini [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/) nesnesine ekler. |
| [add(Object[] values)](#add-java.lang.Object...) | Belirtilen değerleri kullanarak bir satır oluşturur ve bunu [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/) nesnesine ekler. |
| [clear()](#clear) | Koleksiyondaki tüm satırları temizler. |
| [find(Object[] keys)](#find-java.lang.Object) | Belirtilen birincil anahtar değerlerini içeren satırı alır. |
| [find(String primaryKeyValue)](#find-java.lang.String) | Birincil anahtar değeriyle belirtilen satırı alır. |
| [get(int index)](#get-int) | Belirtilen indeksteki satırı alır. |
| [get(Object[] values)](#get-java.lang.Object) | Belirtilen değerleri içeren satırı alır. |
| [getCount()](#getCount) | Bu koleksiyondaki toplam [DataRow](../../com.aspose.words.net.system.data/datarow/) nesne sayısını alır. |
| [insertAt(System.Data.DataRow row, int pos)](#insertAt-com.aspose.words.net.System.Data.DataRow-int) | Belirtilen konuma yeni bir satır ekler. |
| [iterator()](#iterator) | Bu koleksiyon için bir java.util.Iterator alır. |
| [removeAt(int index)](#removeAt-int) | Koleksiyondan belirtilen indeksteki satırı kaldırır. |
### add(System.Data.DataRow row) {#add-com.aspose.words.net.System.Data.DataRow}
```
public void add(System.Data.DataRow row)
```


Belirtilen [DataRow](../../com.aspose.words.net.system.data/datarow/) nesnesini [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/) nesnesine ekler.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) | Eklenecek [DataRow](../../com.aspose.words.net.system.data/datarow/) nesnesi. |

### add(Object[] values) {#add-java.lang.Object...}
```
public void add(Object[] values)
```


Belirtilen değerleri kullanarak bir satır oluşturur ve bunu [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/) nesnesine ekler.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değerler | java.lang.Object[] | Yeni satırı oluşturmak için kullanılan değerler dizisi. |

### clear() {#clear}
```
public void clear()
```


Koleksiyondaki tüm satırları temizler.

### find(Object[] keys) {#find-java.lang.Object}
```
public System.Data.DataRow find(Object[] keys)
```


Belirtilen birincil anahtar değerlerini içeren satırı alır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| anahtarlar | java.lang.Object[] | Bulmak için birincil anahtar değerlerinin dizisi. Dizinin tipi Object'tir. |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - A [DataRow](../../com.aspose.words.net.system.data/datarow/) object that contains the primary key values specified; otherwise a null value if the primary key value does not exist in the [DataRowCollection](../../com.aspose.words.net.system.data/datarowcollection/).
### find(String primaryKeyValue) {#find-java.lang.String}
```
public System.Data.DataRow find(String primaryKeyValue)
```


Birincil anahtar değeriyle belirtilen satırı alır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| primaryKeyValue | java.lang.String | Bulunacak DataRow'un birincil anahtar değeri. |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - A DataRow that contains the primary key value specified; otherwise a null value if the primary key value does not exist in the DataRowCollection.
### get(int index) {#get-int}
```
public System.Data.DataRow get(int index)
```


Belirtilen indeksteki satırı alır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int | Döndürülecek satırın sıfır tabanlı indeksi. |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - The specified [DataRow](../../com.aspose.words.net.system.data/datarow/).
### get(Object[] values) {#get-java.lang.Object}
```
public System.Data.DataRow get(Object[] values)
```


Belirtilen değerleri içeren satırı alır. Eğer birincil anahtarın sütun(ları) mevcutsa indeks kullanılacaktır. Eğer indeks yoksa basit lineer tarama kullanılacaktır. Buna dikkat edin, çünkü bu önemli miktarda zaman alabilir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değerler | java.lang.Object[] | satırın verileri |

**Returns:**
[DataRow](../../com.aspose.words.net.system.data/datarow/) - found row or `null`
### getCount() {#getCount}
```
public int getCount()
```


Bu koleksiyondaki toplam [DataRow](../../com.aspose.words.net.system.data/datarow/) nesne sayısını alır.

**Returns:**
int - Bu koleksiyondaki toplam [DataRow](../../com.aspose.words.net.system.data/datarow/) nesnesi sayısı.
### insertAt(System.Data.DataRow row, int pos) {#insertAt-com.aspose.words.net.System.Data.DataRow-int}
```
public void insertAt(System.Data.DataRow row, int pos)
```


Belirtilen konuma yeni bir satır ekler.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| row | [DataRow](../../com.aspose.words.net.system.data/datarow/) | Eklenecek [DataRow](../../com.aspose.words.net.system.data/datarow/) nesnesi. |
| pos | int | DataRow'u eklemek istediğiniz koleksiyondaki (sıfır tabanlı) konum. |

### iterator() {#iterator}
```
public Iterator iterator()
```


Bu koleksiyon için bir java.util.Iterator alır.

**Returns:**
java.util.Iterator - Bu koleksiyon için bir java.util.Iterator.
### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Koleksiyondan belirtilen indeksteki satırı kaldırır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int | Silinecek satırın indeksi. |

