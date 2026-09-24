---
title: "ConstraintCollection"
linktitle: "ConstraintCollection"
second_title: "Aspose.Words Java için"
description: "Java'da bir DataTable için kısıtlamaların bir koleksiyonunu temsil eder."
type: docs
weight: 11
url: /tr/java/com.aspose.words.net.system.data/constraintcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ConstraintCollection implements Iterable
```

Bir [DataTable](../../com.aspose.words.net.system.data/datatable/) için kısıtlamaların bir koleksiyonunu temsil eder.
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [add(System.Data.Constraint constraint)](#add-com.aspose.words.net.System.Data.Constraint) | Belirtilen [Constraint](../../com.aspose.words.net.system.data/constraint/) nesnesini koleksiyona ekler. |
| [contains(System.Data.Constraint cc)](#contains-com.aspose.words.net.System.Data.Constraint) | İsimle belirtilen Constraint nesnesinin koleksiyonda bulunup bulunmadığını gösterir. |
| [get(int index)](#get-int) | Belirtilen indeksteki koleksiyondan [Constraint](../../com.aspose.words.net.system.data/constraint/) alır. |
| [get(String name)](#get-java.lang.String) | Belirtilen isimle koleksiyondan [Constraint](../../com.aspose.words.net.system.data/constraint/) alır. |
| [getCount()](#getCount) | Bir koleksiyondaki toplam öğe sayısını alır. |
| [iterator()](#iterator) |  |
| [remove(System.Data.Constraint constraint)](#remove-com.aspose.words.net.System.Data.Constraint) | Belirtilen [Constraint](../../com.aspose.words.net.system.data/constraint/) nesnesini koleksiyondan kaldırır. |
### add(System.Data.Constraint constraint) {#add-com.aspose.words.net.System.Data.Constraint}
```
public void add(System.Data.Constraint constraint)
```


Belirtilen [Constraint](../../com.aspose.words.net.system.data/constraint/) nesnesini koleksiyona ekler.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| constraint | [Constraint](../../com.aspose.words.net.system.data/constraint/) | Eklenecek Constraint. |

### contains(System.Data.Constraint cc) {#contains-com.aspose.words.net.System.Data.Constraint}
```
public boolean contains(System.Data.Constraint cc)
```


İsimle belirtilen Constraint nesnesinin koleksiyonda bulunup bulunmadığını gösterir.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| cc | [Constraint](../../com.aspose.words.net.system.data/constraint/) | Kaldırılacak Constraint. |

**Returns:**
boolean - koleksiyon belirtilen kısıtlamayı içeriyorsa true; aksi takdirde false.
### get(int index) {#get-int}
```
public System.Data.Constraint get(int index)
```


Belirtilen indeksteki koleksiyondan [Constraint](../../com.aspose.words.net.system.data/constraint/) alır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int | Döndürülecek kısıtlamanın indeksi. |

**Returns:**
[Constraint](../../com.aspose.words.net.system.data/constraint/) - The [Constraint](../../com.aspose.words.net.system.data/constraint/) at the specified index.
### get(String name) {#get-java.lang.String}
```
public System.Data.Constraint get(String name)
```


Belirtilen isimle koleksiyondan [Constraint](../../com.aspose.words.net.system.data/constraint/) alır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| name | java.lang.String | Döndürülecek kısıtlamanın [Constraint.getConstraintName()](../../com.aspose.words.net.system.data/constraint/\#getConstraintName) / [Constraint.setConstraintName(java.lang.String)](../../com.aspose.words.net.system.data/constraint/\#setConstraintName-java.lang.String) |

**Returns:**
[Constraint](../../com.aspose.words.net.system.data/constraint/) - The [Constraint](../../com.aspose.words.net.system.data/constraint/) with the specified name; otherwise a null value if the [Constraint](../../com.aspose.words.net.system.data/constraint/) does not exist.
### getCount() {#getCount}
```
public int getCount()
```


Bir koleksiyondaki toplam öğe sayısını alır.

**Returns:**
int - Bir koleksiyondaki toplam öğe sayısı.
### iterator() {#iterator}
```
public Iterator iterator()
```




**Returns:**
java.util.Iterator
### remove(System.Data.Constraint constraint) {#remove-com.aspose.words.net.System.Data.Constraint}
```
public void remove(System.Data.Constraint constraint)
```


Belirtilen [Constraint](../../com.aspose.words.net.system.data/constraint/) nesnesini koleksiyondan kaldırır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| constraint | [Constraint](../../com.aspose.words.net.system.data/constraint/) | Kaldırılacak [Constraint](../../com.aspose.words.net.system.data/constraint/). |

