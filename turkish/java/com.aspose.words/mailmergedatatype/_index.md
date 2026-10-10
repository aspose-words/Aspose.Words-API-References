---
title: "MailMergeDataType"
linktitle: "MailMergeDataType"
second_title: "Aspose.Words Java için"
description: "Java'da harici bir birleştirme veri kaynağının türünü belirtir."
type: docs
weight: 440
url: /tr/java/com.aspose.words/mailmergedatatype/
---

**Inheritance:**
java.lang.Object
```
public class MailMergeDataType
```

Harici bir posta birleştirme veri kaynağının türünü belirtir.
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [DATABASE](#DATABASE) | Belirtilen belgenin Dinamik Veri Değişimi (DDE) sistemi aracılığıyla bir Access veritabanına bağlandığını belirtir. |
| [DEFAULT](#DEFAULT) | Şuna eşittir: [NONE](../../com.aspose.words/mailmergedatatype/\#NONE). |
| [NATIVE](#NATIVE) | Belirtilen belgenin Office Veri Kaynağı Nesnesi (ODSO) arabirimi aracılığıyla harici bir veri kaynağına bağlandığını belirtir. |
| [NONE](#NONE) | Herhangi bir birleştirme veri kaynağı belirtilmemiştir. |
| [ODBC](#ODBC) | Belirtilen belgenin Open Database Connectivity arabirimi aracılığıyla harici bir veri kaynağına bağlandığını belirtir. |
| [QUERY](#QUERY) | Belirtilen belgenin harici bir sorgu aracı kullanılarak harici bir veri kaynağına bağlandığını belirtir. |
| [SPREADSHEET](#SPREADSHEET) | Belirtilen belgenin Dinamik Veri Değişimi (DDE) sistemi aracılığıyla bir Excel çalışma sayfasına bağlandığını belirtir. |
| [TEXT_FILE](#TEXT-FILE) | Belirtilen belgenin Dinamik Veri Değişimi (DDE) sistemi aracılığıyla bir metin dosyasına bağlandığını belirtir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String mailMergeDataTypeName)](#fromName-java.lang.String) |  |
| [getName(int mailMergeDataType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int mailMergeDataType)](#toString-int) |  |
### DATABASE {#DATABASE}
```
public static int DATABASE
```


Belirtilen belgenin Dinamik Veri Değişimi (DDE) sistemi aracılığıyla bir Access veritabanına bağlandığını belirtir.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Şuna eşittir: [NONE](../../com.aspose.words/mailmergedatatype/\#NONE).

### NATIVE {#NATIVE}
```
public static int NATIVE
```


Belirtilen belgenin Office Veri Kaynağı Nesnesi (ODSO) arabirimi aracılığıyla harici bir veri kaynağına bağlandığını belirtir.

### NONE {#NONE}
```
public static int NONE
```


Herhangi bir birleştirme veri kaynağı belirtilmemiştir.

### ODBC {#ODBC}
```
public static int ODBC
```


Belirtilen belgenin Open Database Connectivity arabirimi aracılığıyla harici bir veri kaynağına bağlandığını belirtir.

### QUERY {#QUERY}
```
public static int QUERY
```


Belirtilen belgenin harici bir sorgu aracı kullanılarak harici bir veri kaynağına bağlandığını belirtir.

### SPREADSHEET {#SPREADSHEET}
```
public static int SPREADSHEET
```


Belirtilen belgenin Dinamik Veri Değişimi (DDE) sistemi aracılığıyla bir Excel çalışma sayfasına bağlandığını belirtir.

### TEXT_FILE {#TEXT-FILE}
```
public static int TEXT_FILE
```


Belirtilen belgenin Dinamik Veri Değişimi (DDE) sistemi aracılığıyla bir metin dosyasına bağlandığını belirtir.

### length {#length}
```
public static int length
```


### fromName(String mailMergeDataTypeName) {#fromName-java.lang.String}
```
public static int fromName(String mailMergeDataTypeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| mailMergeDataTypeName | java.lang.String |  |

**Returns:**
int
### getName(int mailMergeDataType) {#getName-int}
```
public static String getName(int mailMergeDataType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| mailMergeDataType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int mailMergeDataType) {#toString-int}
```
public static String toString(int mailMergeDataType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| mailMergeDataType | int |  |

**Returns:**
java.lang.String
