---
title: "IDataReader"
linktitle: "IDataReader"
second_title: "Aspose.Words Java için"
description: "Veri kaynağında bir komut çalıştırılarak elde edilen bir veya daha fazla yalnızca ileri okuma akışı sonuç kümesini okuma imkanı sağlar ve Java'da ilişkisel veritabanlarına erişen .NET Framework veri sağlayıcıları tarafından uygulanır."
type: docs
weight: 34
url: /tr/java/com.aspose.words.net.system.data/idatareader/
---

**All Implemented Interfaces:**
[com.aspose.words.net.System.Data.IDataRecord](../../com.aspose.words.net.system.data/idatarecord/)
```
public interface IDataReader extends System.Data.IDataRecord
```

Veri kaynağında bir komut çalıştırılarak elde edilen bir veya daha fazla yalnızca ileri okuma akışı sonuç kümesini okuma imkanı sağlar ve ilişkisel veritabanlarına erişen .NET Framework veri sağlayıcıları tarafından uygulanır.
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [close()](#close) | [IDataReader](../../com.aspose.words.net.system.data/idatareader/) nesnesini kapatır. |
| [getDepth()](#getDepth) | Geçerli satır için iç içe derinliğini gösteren bir değer alır. |
| [getRecordsAffected()](#getRecordsAffected) | SQL ifadesinin yürütülmesiyle değiştirilen, eklenen veya silinen satır sayısını alır. |
| [getSchemaTable()](#getSchemaTable) | [IDataReader](../../com.aspose.words.net.system.data/idatareader/) sütun meta verilerini tanımlayan bir [DataTable](../../com.aspose.words.net.system.data/datatable/) döndürür. |
| [isClosed()](#isClosed) | Veri okuyucunun kapalı olup olmadığını gösteren bir değer alır. |
| [nextResult()](#nextResult) | Toplu SQL ifadelerinin sonuçlarını okurken veri okuyucuyu bir sonraki sonuca ilerletir. |
| [read()](#read) | [IDataReader](../../com.aspose.words.net.system.data/idatareader/) nesnesini bir sonraki kayda ilerletir. |
### close() {#close}
```
public abstract void close()
```


[IDataReader](../../com.aspose.words.net.system.data/idatareader/) nesnesini kapatır.

### getDepth() {#getDepth}
```
public abstract int getDepth()
```


Geçerli satır için iç içe derinliğini gösteren bir değer alır.

**Returns:**
int - İç içe seviyesidir.
### getRecordsAffected() {#getRecordsAffected}
```
public abstract int getRecordsAffected()
```


SQL ifadesinin yürütülmesiyle değiştirilen, eklenen veya silinen satır sayısını alır.

**Returns:**
int - Değiştirilen, eklenen veya silinen satır sayısı; hiçbir satır etkilenmemişse veya ifade başarısız olmuşsa 0; SELECT ifadeleri için -1.
### getSchemaTable() {#getSchemaTable}
```
public abstract System.Data.DataTable getSchemaTable()
```


[IDataReader](../../com.aspose.words.net.system.data/idatareader/) sütun meta verilerini tanımlayan bir [DataTable](../../com.aspose.words.net.system.data/datatable/) döndürür.

**Returns:**
[DataTable](../../com.aspose.words.net.system.data/datatable/) - A [DataTable](../../com.aspose.words.net.system.data/datatable/) that describes the column metadata.
### isClosed() {#isClosed}
```
public abstract boolean isClosed()
```


Veri okuyucunun kapalı olup olmadığını gösteren bir değer alır.

**Returns:**
boolean - veri okuyucu kapalıysa true; aksi takdirde false.
### nextResult() {#nextResult}
```
public abstract boolean nextResult()
```


Toplu SQL ifadelerinin sonuçlarını okurken veri okuyucuyu bir sonraki sonuca ilerletir.

**Returns:**
boolean - daha fazla satır varsa true; aksi takdirde false.
### read() {#read}
```
public abstract boolean read()
```


[IDataReader](../../com.aspose.words.net.system.data/idatareader/) nesnesini bir sonraki kayda ilerletir.

**Returns:**
boolean - daha fazla satır varsa true; aksi takdirde false.
