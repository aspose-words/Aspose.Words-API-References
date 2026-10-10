---
title: "IDataRecord"
linktitle: "IDataRecord"
second_title: "Aspose.Words Java için"
description: "Bir DataReader için her satırdaki sütun değerlerine erişim sağlar ve Java'da ilişkisel veritabanlarına erişen .NET Framework veri sağlayıcıları tarafından uygulanır."
type: docs
weight: 35
url: /tr/java/com.aspose.words.net.system.data/idatarecord/
---
```
public interface IDataRecord
```

DataReader için her satırdaki sütun değerlerine erişim sağlar ve ilişkisel veritabanlarına erişen .NET Framework veri sağlayıcıları tarafından uygulanır.
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [get(int i)](#get-int) | Belirtilen indeksteki sütunu alır. |
| [getFieldCount()](#getFieldCount) | Mevcut satırdaki sütun sayısını alır. |
| [getFieldType(int i)](#getFieldType-int) | Belirtilen [getValue(int)](../../com.aspose.words.net.system.data/idatarecord/\#getValue-int) metodundan döndürülecek java.lang.Object tipine karşılık gelen java.lang.Class bilgisini alır. |
| [getName(int i)](#getName-int) | Bulunacak alanın adını alır. |
| [getValue(int i)](#getValue-int) | Belirtilen alanın değerini döndürür. |
### get(int i) {#get-int}
```
public abstract Object get(int i)
```


Belirtilen indeksteki sütunu alır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| i | int | Alınacak sütunun sıfır tabanlı indeksidir. |

**Returns:**
java.lang.Object - Belirtilen indeksteki sütun, bir java.lang.Object olarak.
### getFieldCount() {#getFieldCount}
```
public abstract int getFieldCount()
```


Mevcut satırdaki sütun sayısını alır.

**Returns:**
int - Geçerli bir kayıt kümesinde konumlandırılmadığında 0; aksi takdirde mevcut kayıttaki sütun sayısı. Varsayılan değer -1.
### getFieldType(int i) {#getFieldType-int}
```
public abstract Class getFieldType(int i)
```


Belirtilen [getValue(int)](../../com.aspose.words.net.system.data/idatarecord/\#getValue-int) metodundan döndürülecek java.lang.Object tipine karşılık gelen java.lang.Class bilgisini alır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| i | int | Bulunacak alanın indeksi. |

**Returns:**
java.lang.Class - [getValue(int)](../../com.aspose.words.net.system.data/idatarecord/\#getValue-int) metodundan döndürülecek java.lang.Object tipine karşılık gelen java.lang.Class bilgisi.
### getName(int i) {#getName-int}
```
public abstract String getName(int i)
```


Bulunacak alanın adını alır.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| i | int | Bulunacak alanın indeksi. |

**Returns:**
java.lang.String - Alanın adı veya döndürülecek değer yoksa boş string (""),
### getValue(int i) {#getValue-int}
```
public abstract Object getValue(int i)
```


Belirtilen alanın değerini döndürür.

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| i | int | Bulunacak alanın indeksi. |

**Returns:**
java.lang.Object - Döndürüldüğünde alan değerini içerecek java.lang.Object.
