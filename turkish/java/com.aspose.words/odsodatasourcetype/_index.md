---
title: "OdsoDataSourceType"
linktitle: "OdsoDataSourceType"
second_title: "Aspose.Words Java için"
description: "Java'daki ODSO bağlantı bilgilerinin bir parçası olarak bağlanacak harici veri kaynağının türünü belirtir."
type: docs
weight: 488
url: /tr/java/com.aspose.words/odsodatasourcetype/
---

**Inheritance:**
java.lang.Object
```
public class OdsoDataSourceType
```

ODSO bağlantı bilgilerinin bir parçası olarak bağlanacak dış veri kaynağının türünü belirtir.

 **Remarks:** 

OOXML spesifikasyonu bu enum için çok belirsiz. Sanırım bu, WdMergeSubType enumerasyonuna karşılık gelebilir http://msdn.microsoft.com/en-us/library/bb237801.aspx.
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [ADDRESS_BOOK](#ADDRESS-BOOK) | Belirli bir belgenin bir kişi adres defterine bağlandığını belirtir. |
| [DATABASE](#DATABASE) | Belirli bir belgenin bir veritabanına bağlandığını belirtir. |
| [DEFAULT](#DEFAULT) | [NONE](../../com.aspose.words/odsodatasourcetype/#NONE) değerine eşittir. |
| [DOCUMENT_1](#DOCUMENT-1) | Belirli bir belgenin üretici uygulama tarafından desteklenen başka bir belge formatına bağlandığını belirtir. |
| [DOCUMENT_2](#DOCUMENT-2) | Belirli bir belgenin üretici uygulama tarafından desteklenen başka bir belge formatına bağlandığını belirtir. |
| [EMAIL](#EMAIL) | Belirli bir belgenin bir e-posta uygulamasına bağlandığını belirtir. |
| [LEGACY](#LEGACY) | Belirli bir belgenin üretici uygulama tarafından desteklenen eski bir belge formatına bağlandığını belirtir. Muhtemelen wdMergeSubTypeWord2000. |
| [MASTER](#MASTER) | Belirli bir belgenin diğer veri kaynaklarını toplayan bir veri kaynağına bağlandığını belirtir. |
| [NATIVE](#NATIVE) | Belirli bir belgenin üretici uygulamaya özgü başka bir belge formatına bağlandığını belirtir. |
| [NONE](#NONE) | Harici veri kaynağının türü belirtilmemiştir. |
| [TEXT](#TEXT) | Belirli bir belgenin bir metin dosyasına bağlandığını belirtir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String odsoDataSourceTypeName)](#fromName-java.lang.String) |  |
| [getName(int odsoDataSourceType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int odsoDataSourceType)](#toString-int) |  |
### ADDRESS_BOOK {#ADDRESS-BOOK}
```
public static int ADDRESS_BOOK
```


Belirli bir belgenin bir kişi adres defterine bağlandığını belirtir. Muhtemelen wdMergeSubTypeOAL.

### DATABASE {#DATABASE}
```
public static int DATABASE
```


Belirli bir belgenin bir veritabanına bağlandığını belirtir. Muhtemelen wdMergeSubTypeAccess.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


[NONE](../../com.aspose.words/odsodatasourcetype/#NONE) değerine eşittir.

### DOCUMENT_1 {#DOCUMENT-1}
```
public static int DOCUMENT_1
```


Belirli bir belgenin üretici uygulama tarafından desteklenen başka bir belge formatına bağlandığını belirtir. Muhtemelen wdMergeSubTypeOLEDBWord.

### DOCUMENT_2 {#DOCUMENT-2}
```
public static int DOCUMENT_2
```


Belirli bir belgenin üretici uygulama tarafından desteklenen başka bir belge formatına bağlandığını belirtir. Muhtemelen wdMergeSubTypeWorks.

### EMAIL {#EMAIL}
```
public static int EMAIL
```


Belirli bir belgenin bir e-posta uygulamasına bağlandığını belirtir. Muhtemelen wdMergeSubTypeOutlook.

### LEGACY {#LEGACY}
```
public static int LEGACY
```


Belirli bir belgenin üretici uygulama tarafından desteklenen eski bir belge formatına bağlandığını belirtir. Muhtemelen wdMergeSubTypeWord2000.

### MASTER {#MASTER}
```
public static int MASTER
```


Belirli bir belgenin diğer veri kaynaklarını toplayan bir veri kaynağına bağlandığını belirtir.

### NATIVE {#NATIVE}
```
public static int NATIVE
```


Belirli bir belgenin üretici uygulamaya özgü başka bir belge formatına bağlandığını belirtir. Muhtemelen wdMergeSubTypeOLEDBText

### NONE {#NONE}
```
public static int NONE
```


Harici veri kaynağının türü belirtilmemiştir. Muhtemelen wdMergeSubTypeWord.

### TEXT {#TEXT}
```
public static int TEXT
```


Belirli bir belgenin bir metin dosyasına bağlandığını belirtir. Muhtemelen wdMergeSubTypeOther.

### length {#length}
```
public static int length
```


### fromName(String odsoDataSourceTypeName) {#fromName-java.lang.String}
```
public static int fromName(String odsoDataSourceTypeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| odsoDataSourceTypeName | java.lang.String |  |

**Returns:**
int
### getName(int odsoDataSourceType) {#getName-int}
```
public static String getName(int odsoDataSourceType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| odsoDataSourceType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int odsoDataSourceType) {#toString-int}
```
public static String toString(int odsoDataSourceType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| odsoDataSourceType | int |  |

**Returns:**
java.lang.String
