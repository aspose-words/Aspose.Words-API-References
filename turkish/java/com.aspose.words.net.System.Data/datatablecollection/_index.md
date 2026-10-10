---
title: "DataTableCollection"
linktitle: "DataTableCollection"
second_title: "Aspose.Words Java için"
description: "Java'daki DataSet için tablo koleksiyonunu temsil eder."
type: docs
weight: 26
url: /tr/java/com.aspose.words.net.system.data/datatablecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataTableCollection implements Iterable
```

[DataSet](../../com.aspose.words.net.system.data/dataset/) için tablo koleksiyonunu temsil eder.
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [add(System.Data.DataTable table)](#add-com.aspose.words.net.System.Data.DataTable) | Belirtilen DataTable'ı koleksiyona ekler. |
| [add(String name)](#add-java.lang.String) | Belirtilen adı kullanarak bir [DataTable](../../com.aspose.words.net.system.data/datatable/) nesnesi oluşturur ve koleksiyona ekler. |
| [contains(String name)](#contains-java.lang.String) | Belirtilen ada sahip bir [DataTable](../../com.aspose.words.net.system.data/datatable/) nesnesinin koleksiyonda bulunup bulunmadığını gösteren bir değer alır. |
| [get(int index)](#get-int) | Belirtilen indeksteki [DataTable](../../com.aspose.words.net.system.data/datatable/) nesnesini alır. |
| [get(String name)](#get-java.lang.String) | Belirtilen ada sahip [DataTable](../../com.aspose.words.net.system.data/datatable/) nesnesini alır. |
| [get(String name, String tableNamespace)](#get-java.lang.String-java.lang.String) | Belirtilen ad alanında belirtilen ada sahip [DataTable](../../com.aspose.words.net.system.data/datatable/) nesnesini alır. |
| [getCount()](#getCount) |  |
| [iterator()](#iterator) |  |
| [remove(String name)](#remove-java.lang.String) | Belirtilen ada sahip [DataTable](../../com.aspose.words.net.system.data/datatable/) nesnesini koleksiyondan kaldırır. |
### add(System.Data.DataTable table) {#add-com.aspose.words.net.System.Data.DataTable}
```
public void add(System.Data.DataTable table)
```


Belirtilen DataTable'ı koleksiyona ekler.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable/) | Eklenecek DataTable nesnesi. |

### add(String name) {#add-java.lang.String}
```
public System.Data.DataTable add(String name)
```


Belirtilen adı kullanarak bir [DataTable](../../com.aspose.words.net.system.data/datatable/) nesnesi oluşturur ve koleksiyona ekler.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String | Oluşturulan [DataTable](../../com.aspose.words.net.system.data/datatable/) nesnesine verilecek ad. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - The newly created [DataTable](../../com.aspose.words.net.system.data/datatable/).
### contains(String name) {#contains-java.lang.String}
```
public boolean contains(String name)
```


Belirtilen ada sahip bir [DataTable](../../com.aspose.words.net.system.data/datatable/) nesnesinin koleksiyonda bulunup bulunmadığını gösteren bir değer alır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String | Bulunacak [DataTable](../../com.aspose.words.net.system.data/datatable/) nesnesinin adı. |

**Returns:**
boolean - belirtilen tablo mevcutsa true; aksi takdirde false.
### get(int index) {#get-int}
```
public System.Data.DataTable get(int index)
```


Belirtilen indeksteki [DataTable](../../com.aspose.words.net.system.data/datatable/) nesnesini alır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| index | int | Bulunacak [DataTable](../../com.aspose.words.net.system.data/datatable/) nesnesinin sıfır tabanlı indeksi. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/).
### get(String name) {#get-java.lang.String}
```
public System.Data.DataTable get(String name)
```


Belirtilen ada sahip [DataTable](../../com.aspose.words.net.system.data/datatable/) nesnesini alır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String | Bulunacak DataTable'ın adı. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) with the specified name; otherwise null if the [DataTable](../../com.aspose.words.net.system.data/datatable/) does not exist.
### get(String name, String tableNamespace) {#get-java.lang.String-java.lang.String}
```
public System.Data.DataTable get(String name, String tableNamespace)
```


Belirtilen ad alanında belirtilen ada sahip [DataTable](../../com.aspose.words.net.system.data/datatable/) nesnesini alır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String | Bulunacak DataTable'ın adı. |
| tableNamespace | java.lang.String | Aranacak [DataTable](../../com.aspose.words.net.system.data/datatable/) ad alanının adı. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) with the specified name; otherwise null if the [DataTable](../../com.aspose.words.net.system.data/datatable/) does not exist.
### getCount() {#getCount}
```
public int getCount()
```




**Returns:**
int - bu koleksiyondaki toplam öğe sayısı.
### iterator() {#iterator}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator
### remove(String name) {#remove-java.lang.String}
```
public System.Data.DataTable remove(String name)
```


Belirtilen ada sahip [DataTable](../../com.aspose.words.net.system.data/datatable/) nesnesini koleksiyondan kaldırır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String | Kaldırılacak [DataTable](../../com.aspose.words.net.system.data/datatable/) nesnesinin adı. |

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/)
