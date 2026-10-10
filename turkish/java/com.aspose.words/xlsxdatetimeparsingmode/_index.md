---
title: "XlsxDateTimeParsingMode"
linktitle: "XlsxDateTimeParsingMode"
second_title: "Aspose.Words Java için"
description: "Belge metninin Java'da tarih ve saat değerlerini tanımlamak için nasıl ayrıştırıldığını belirtir."
type: docs
weight: 742
url: /tr/java/com.aspose.words/xlsxdatetimeparsingmode/
---

**Inheritance:**
java.lang.Object
```
public class XlsxDateTimeParsingMode
```

Belge metninin tarih ve saat değerlerini tanımlamak için nasıl ayrıştırıldığını belirtir.

 **Examples:** 

Tarih saat biçiminin otomatik algılanmasının nasıl belirtileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Xlsx DateTime.docx");

 XlsxSaveOptions saveOptions = new XlsxSaveOptions();
 // Specify using datetime format autodetection.
 saveOptions.setDateTimeParsingMode(XlsxDateTimeParsingMode.AUTO);

 doc.save(getArtifactsDir() + "XlsxSaveOptions.DateTimeParsingMode.xlsx", saveOptions);
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [AUTO](#AUTO) | Bir belgede kullanılan tarih saat biçimi otomatik olarak belirlenir. |
| [USE_CURRENT_LOCALE](#USE-CURRENT-LOCALE) | Mevcut iş parçacığı için ayarlanan tarih saat biçimi, dize değerlerini ayrıştırmak için önce kullanılır. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String xlsxDateTimeParsingModeName)](#fromName-java.lang.String) |  |
| [getName(int xlsxDateTimeParsingMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int xlsxDateTimeParsingMode)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Bir belgede kullanılan tarih saat biçimi otomatik olarak belirlenir. Bu ek zaman alabilir.

### USE_CURRENT_LOCALE {#USE-CURRENT-LOCALE}
```
public static int USE_CURRENT_LOCALE
```


Mevcut iş parçacığı için ayarlanan tarih saat biçimi, dize değerlerini ayrıştırmak için önce kullanılır. Ayrıştırma başarısız olursa, diğer yaygın tarih saat biçimleri denenir.

### length {#length}
```
public static int length
```


### fromName(String xlsxDateTimeParsingModeName) {#fromName-java.lang.String}
```
public static int fromName(String xlsxDateTimeParsingModeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| xlsxDateTimeParsingModeName | java.lang.String |  |

**Returns:**
int
### getName(int xlsxDateTimeParsingMode) {#getName-int}
```
public static String getName(int xlsxDateTimeParsingMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| xlsxDateTimeParsingMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int xlsxDateTimeParsingMode) {#toString-int}
```
public static String toString(int xlsxDateTimeParsingMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| xlsxDateTimeParsingMode | int |  |

**Returns:**
java.lang.String
