---
title: "KnownTypeSet"
linktitle: "KnownTypeSet"
second_title: "Aspose.Words Java için"
description: "Java'da bir sırasız küme (unordered set) temsil eder."
type: docs
weight: 412
url: /tr/java/com.aspose.words/knowntypeset/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class KnownTypeSet implements Iterable
```

Rapor şablonları içinde tam veya kısmi nitelikli adları kullanılabilen java.lang.Class nesnelerini içeren sırasız bir küme (yani benzersiz öğeler koleksiyonu) temsil eder; bu küme, ilgili tiplerin statik üyelerini çağırmak, tip dönüşümleri yapmak vb. için kullanılabilir.

Daha fazla bilgi için, [ LINQ Reporting Engine ][LINQ Reporting Engine] dokümantasyon makalesini ziyaret edin.


[LINQ Reporting Engine]: https://docs.aspose.com/words/java/linq-reporting-engine/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [add(Class type)](#add-java.lang.Class) | Belirtilen java.lang.Class nesnesini kümeye ekler. |
| [clear()](#clear) | Kümedeki tüm öğeleri kaldırır. |
| [getCount()](#getCount) | Kümedeki öğelerin sayısını alır. |
| [iterator()](#iterator) | Kümedeki öğeler üzerinde yineleme yapmak için bir java.util.Iterator nesnesi döndürür. |
| [remove(Class type)](#remove-java.lang.Class) | Belirtilen java.lang.Class nesnesini kümeden kaldırır. |
### add(Class type) {#add-java.lang.Class}
```
public void add(Class type)
```


Belirtilen java.lang.Class nesnesini kümeye ekler.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| tip | java.lang.Class | Eklenecek bir java.lang.Class nesnesi. |

### clear() {#clear}
```
public void clear()
```


Kümedeki tüm öğeleri kaldırır.

### getCount() {#getCount}
```
public int getCount()
```


Kümedeki öğelerin sayısını alır.

**Returns:**
int - Kümedeki öğelerin sayısı.
### iterator() {#iterator}
```
public Iterator iterator()
```


Kümedeki öğeler üzerinde yineleme yapmak için bir java.util.Iterator nesnesi döndürür.

**Returns:**
java.util.Iterator - Kümedeki öğeler üzerinde yineleme yapmak için bir java.util.Iterator nesnesi.
### remove(Class type) {#remove-java.lang.Class}
```
public void remove(Class type)
```


Belirtilen java.lang.Class nesnesini kümeden kaldırır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| tip | java.lang.Class | Kaldırılacak bir java.lang.Class nesnesi. |

