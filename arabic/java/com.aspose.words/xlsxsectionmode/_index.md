---
title: "XlsxSectionMode"
linktitle: "XlsxSectionMode"
second_title: "Aspose.Words لـ Java"
description: "يحدد كيفية معالجة الأقسام عند حفظ مستند بتنسيق XLSX في Java."
type: docs
weight: 744
url: /ar/java/com.aspose.words/xlsxsectionmode/
---

**Inheritance:**
java.lang.Object
```
public class XlsxSectionMode
```

يحدد كيفية معالجة الأقسام عند حفظ مستند بتنسيق XLSX.

 **Examples:** 

يوضح كيفية حفظ المستند كأوراق عمل منفصلة.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 // Each section of a document will be created as a separate worksheet.
 // Use 'SingleWorksheet' to display all document on one worksheet.
 XlsxSaveOptions xlsxSaveOptions = new XlsxSaveOptions();
 xlsxSaveOptions.setSectionMode(XlsxSectionMode.MULTIPLE_WORKSHEETS);

 doc.save(getArtifactsDir() + "XlsxSaveOptions.SelectionMode.xlsx", xlsxSaveOptions);
 
```
## الحقول

| حقل | الوصف |
| --- | --- |
| [MULTIPLE_WORKSHEETS](#MULTIPLE-WORKSHEETS) | يحدد إنشاء ورقة عمل منفصلة لكل قسم من المستند. |
| [SINGLE_WORKSHEET](#SINGLE-WORKSHEET) | يحدد حفظ جميع أقسام المستند في ورقة عمل واحدة. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String xlsxSectionModeName)](#fromName-java.lang.String) |  |
| [getName(int xlsxSectionMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int xlsxSectionMode)](#toString-int) |  |
### MULTIPLE_WORKSHEETS {#MULTIPLE-WORKSHEETS}
```
public static int MULTIPLE_WORKSHEETS
```


يحدد إنشاء ورقة عمل منفصلة لكل قسم من المستند.

### SINGLE_WORKSHEET {#SINGLE-WORKSHEET}
```
public static int SINGLE_WORKSHEET
```


يحدد حفظ جميع أقسام المستند في ورقة عمل واحدة.

### length {#length}
```
public static int length
```


### fromName(String xlsxSectionModeName) {#fromName-java.lang.String}
```
public static int fromName(String xlsxSectionModeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| xlsxSectionModeName | java.lang.String |  |

**Returns:**
int
### getName(int xlsxSectionMode) {#getName-int}
```
public static String getName(int xlsxSectionMode)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| xlsxSectionMode | int |  |

**Returns:**
java.lang.String
