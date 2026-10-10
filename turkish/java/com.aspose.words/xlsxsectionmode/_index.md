---
title: "XlsxSectionMode"
linktitle: "XlsxSectionMode"
second_title: "Aspose.Words Java için"
description: "Bir belge XLSX formatında Java ile kaydedilirken bölümlerin nasıl işlendiğini belirtir."
type: docs
weight: 744
url: /tr/java/com.aspose.words/xlsxsectionmode/
---

**Inheritance:**
java.lang.Object
```
public class XlsxSectionMode
```

Bir belge XLSX formatında kaydedilirken bölümlerin nasıl işlendiğini belirtir.

 **Examples:** 

Belgenin ayrı çalışma sayfaları olarak nasıl kaydedileceğini gösterir.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 // Each section of a document will be created as a separate worksheet.
 // Use 'SingleWorksheet' to display all document on one worksheet.
 XlsxSaveOptions xlsxSaveOptions = new XlsxSaveOptions();
 xlsxSaveOptions.setSectionMode(XlsxSectionMode.MULTIPLE_WORKSHEETS);

 doc.save(getArtifactsDir() + "XlsxSaveOptions.SelectionMode.xlsx", xlsxSaveOptions);
 
```
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [MULTIPLE_WORKSHEETS](#MULTIPLE-WORKSHEETS) | Bir belgenin her bölümü için ayrı bir çalışma sayfası oluşturulacağını belirtir. |
| [SINGLE_WORKSHEET](#SINGLE-WORKSHEET) | Bir belgenin tüm bölümlerinin tek bir çalışma sayfasına kaydedileceğini belirtir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String xlsxSectionModeName)](#fromName-java.lang.String) |  |
| [getName(int xlsxSectionMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int xlsxSectionMode)](#toString-int) |  |
### MULTIPLE_WORKSHEETS {#MULTIPLE-WORKSHEETS}
```
public static int MULTIPLE_WORKSHEETS
```


Bir belgenin her bölümü için ayrı bir çalışma sayfası oluşturulacağını belirtir.

### SINGLE_WORKSHEET {#SINGLE-WORKSHEET}
```
public static int SINGLE_WORKSHEET
```


Bir belgenin tüm bölümlerinin tek bir çalışma sayfasına kaydedileceğini belirtir.

### length {#length}
```
public static int length
```


### fromName(String xlsxSectionModeName) {#fromName-java.lang.String}
```
public static int fromName(String xlsxSectionModeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| xlsxSectionModeName | java.lang.String |  |

**Returns:**
int
### getName(int xlsxSectionMode) {#getName-int}
```
public static String getName(int xlsxSectionMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| xlsxSectionMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int xlsxSectionMode) {#toString-int}
```
public static String toString(int xlsxSectionMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| xlsxSectionMode | int |  |

**Returns:**
java.lang.String
