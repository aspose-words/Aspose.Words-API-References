---
title: "DataView"
linktitle: "DataView"
second_title: "Aspose.Words Java için"
description: "Java'da sıralama, filtreleme, arama, düzenleme ve gezinme için bir DataTable'ın veri bağlanabilir özelleştirilmiş görünümünü temsil eder."
type: docs
weight: 28
url: /tr/java/com.aspose.words.net.system.data/dataview/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class DataView implements Iterable
```

Sıralama, filtreleme, arama, düzenleme ve gezinme için bir [DataTable](../../com.aspose.words.net.system.data/datatable/) öğesinin veri bağlanabilir, özelleştirilmiş görünümünü temsil eder.
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [DataView(System.Data.DataTable table)](#DataView-com.aspose.words.net.System.Data.DataTable) | Belirtilen [DataTable](../../com.aspose.words.net.system.data/datatable/) ile yeni bir [DataView](../../com.aspose.words.net.system.data/dataview/) sınıfı örneği başlatır. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [close()](#close) | [DataView](../../com.aspose.words.net.system.data/dataview/) öğesini kapatır. |
| [get(int recordIndex)](#get-int) | Belirtilen bir tablodan bir veri satırı alır. |
| [getCount()](#getCount) | [DataView](../../com.aspose.words.net.system.data/dataview/) içindeki kayıt sayısını alır. |
| [getTable()](#getTable) | Kaynak [DataTable](../../com.aspose.words.net.system.data/datatable/) öğesini alır. |
| [iterator()](#iterator) | Bu [DataView](../../com.aspose.words.net.system.data/dataview/) için bir yineleyici alır. |
### DataView(System.Data.DataTable table) {#DataView-com.aspose.words.net.System.Data.DataTable}
```
public DataView(System.Data.DataTable table)
```


Belirtilen [DataTable](../../com.aspose.words.net.system.data/datatable/) ile yeni bir [DataView](../../com.aspose.words.net.system.data/dataview/) sınıfı örneği başlatır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| table | [DataTable](../../com.aspose.words.net.system.data/datatable/) | [DataView](../../com.aspose.words.net.system.data/dataview/) öğesine eklemek için bir [DataTable](../../com.aspose.words.net.system.data/datatable/). |

### close() {#close}
```
public void close()
```


[DataView](../../com.aspose.words.net.system.data/dataview/) öğesini kapatır.

### get(int recordIndex) {#get-int}
```
public System.Data.DataRowView get(int recordIndex)
```


Belirtilen bir tablodan bir veri satırı alır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| recordIndex | int | [DataTable](../../com.aspose.words.net.system.data/datatable/) içindeki bir kaydın dizini. |

**Returns:**
[DataRowView](../../com.aspose.words.net.system.data/datarowview/) - A [DataRowView](../../com.aspose.words.net.system.data/datarowview/) of the row that you want.
### getCount() {#getCount}
```
public int getCount()
```


[DataView](../../com.aspose.words.net.system.data/dataview/) içindeki kayıt sayısını alır.

**Returns:**
int - [DataView](../../com.aspose.words.net.system.data/dataview/) içindeki kayıt sayısı.
### getTable() {#getTable}
```
public System.Data.DataTable getTable()
```


Kaynak [DataTable](../../com.aspose.words.net.system.data/datatable/) öğesini alır.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that provides the data for this view.
### iterator() {#iterator}
```
public Iterator iterator()
```


Bu [DataView](../../com.aspose.words.net.system.data/dataview/) için bir yineleyici alır.

**Returns:**
java.util.Iterator - Listedeki gezinme için bir java.util.Iterator.
