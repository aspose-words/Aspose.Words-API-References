---
title: XlsxSectionMode
linktitle: XlsxSectionMode
second_title: Aspose.Words for Java
description: Specifies how sections are handled when saving a document in the XLSX format in Java.
type: docs
weight: 741
url: /java/com.aspose.words/xlsxsectionmode/
---

**Inheritance:**
java.lang.Object
```
public class XlsxSectionMode
```

Specifies how sections are handled when saving a document in the XLSX format.

 **Examples:** 

Shows how to save document as a separate worksheets.

```

 Document doc = new Document(getMyDir() + "Big document.docx");

 // Each section of a document will be created as a separate worksheet.
 // Use 'SingleWorksheet' to display all document on one worksheet.
 XlsxSaveOptions xlsxSaveOptions = new XlsxSaveOptions();
 xlsxSaveOptions.setSectionMode(XlsxSectionMode.MULTIPLE_WORKSHEETS);

 doc.save(getArtifactsDir() + "XlsxSaveOptions.SelectionMode.xlsx", xlsxSaveOptions);
 
```
## Fields

| Field | Description |
| --- | --- |
| [MULTIPLE_WORKSHEETS](#MULTIPLE-WORKSHEETS) | Specifies that a separate worksheet is created for each section of a document. |
| [SINGLE_WORKSHEET](#SINGLE-WORKSHEET) | Specifies that all sections of a document are saved on one worksheet. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String xlsxSectionModeName)](#fromName-java.lang.String) |  |
| [getName(int xlsxSectionMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int xlsxSectionMode)](#toString-int) |  |
### MULTIPLE_WORKSHEETS {#MULTIPLE-WORKSHEETS}
```
public static int MULTIPLE_WORKSHEETS
```


Specifies that a separate worksheet is created for each section of a document.

### SINGLE_WORKSHEET {#SINGLE-WORKSHEET}
```
public static int SINGLE_WORKSHEET
```


Specifies that all sections of a document are saved on one worksheet.

### length {#length}
```
public static int length
```


### fromName(String xlsxSectionModeName) {#fromName-java.lang.String}
```
public static int fromName(String xlsxSectionModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| xlsxSectionModeName | java.lang.String |  |

**Returns:**
int
### getName(int xlsxSectionMode) {#getName-int}
```
public static String getName(int xlsxSectionMode)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| xlsxSectionMode | int |  |

**Returns:**
java.lang.String
