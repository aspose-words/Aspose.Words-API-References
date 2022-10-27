---
title: PdfCompliance
second_title: Aspose.Words for Java API Reference
description: Specifies the PDF standards compliance level.
type: docs
weight: 449
url: /java/com.aspose.words/pdfcompliance/
---

**Inheritance:**
java.lang.Object
```
public class PdfCompliance
```

Specifies the PDF standards compliance level.
## Fields

| Field | Description |
| --- | --- |
| [PDF_17](#PDF-17) | The output file will comply with the PDF 1.7 (ISO 32000-1) standard. |
| [PDF_20](#PDF-20) | The output file will comply with the PDF 2.0 (ISO 32000-2) standard. |
| [PDF_A_1_A](#PDF-A-1-A) | The output file will comply with the PDF/A-1a (ISO 19005-1) standard. |
| [PDF_A_1_B](#PDF-A-1-B) | The output file will comply with the PDF/A-1b (ISO 19005-1) standard. |
| [PDF_A_2_A](#PDF-A-2-A) | The output file will comply with the PDF/A-2a (ISO 19005-2) standard. |
| [PDF_A_2_U](#PDF-A-2-U) | The output file will comply with the PDF/A-2u (ISO 19005-2) standard. |
| [PDF_A_4](#PDF-A-4) | The output file will comply with the PDF/A-4 (ISO 19005-4:2020) standard. |
| [PDF_UA_1](#PDF-UA-1) | The output file will comply with the PDF/UA-1 (ISO 14289-1) standard. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int pdfCompliance)](#getName-int-) |  |
| [toString(int pdfCompliance)](#toString-int-) |  |
| [fromName(String pdfComplianceName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### PDF_17 {#PDF-17}
```
public static int PDF_17
```


The output file will comply with the PDF 1.7 (ISO 32000-1) standard.

### PDF_20 {#PDF-20}
```
public static int PDF_20
```


The output file will comply with the PDF 2.0 (ISO 32000-2) standard.

### PDF_A_1_A {#PDF-A-1-A}
```
public static int PDF_A_1_A
```


The output file will comply with the PDF/A-1a (ISO 19005-1) standard. This level includes all the requirements of PDF/A-1b and additionally requires that document structure be included (also known as being "tagged"), with the objective of ensuring that document content can be searched and repurposed. Note that exporting the document structure significantly increases the memory consumption, especially for the large documents.

### PDF_A_1_B {#PDF-A-1-B}
```
public static int PDF_A_1_B
```


The output file will comply with the PDF/A-1b (ISO 19005-1) standard. PDF/A-1b has the objective of ensuring reliable reproduction of the visual appearance of the document.

### PDF_A_2_A {#PDF-A-2-A}
```
public static int PDF_A_2_A
```


The output file will comply with the PDF/A-2a (ISO 19005-2) standard. This level includes all the requirements of PDF/A-2u and additionally requires that document structure be included (also known as being "tagged"), with the objective of ensuring that document content can be searched and repurposed. Note that exporting the document structure significantly increases the memory consumption, especially for the large documents.

### PDF_A_2_U {#PDF-A-2-U}
```
public static int PDF_A_2_U
```


The output file will comply with the PDF/A-2u (ISO 19005-2) standard. PDF/A-2u has the objective of preserving document static visual appearance over time, independent of the tools and systems used for creating, storing or rendering the files. Additionally any text contained in the document can be reliably extracted as a series of Unicode codepoints.

### PDF_A_4 {#PDF-A-4}
```
public static int PDF_A_4
```


The output file will comply with the PDF/A-4 (ISO 19005-4:2020) standard. PDF/A-4 has the objective of preserving document static visual appearance over time, independent of the tools and systems used for creating, storing or rendering the files. Additionally any text contained in the document can be reliably extracted as a series of Unicode codepoints.

### PDF_UA_1 {#PDF-UA-1}
```
public static int PDF_UA_1
```


The output file will comply with the PDF/UA-1 (ISO 14289-1) standard. The primary purpose of PDF/UA is to define how to represent electronic documents in the PDF format in a manner that allows the file to be accessible.

### length {#length}
```
public static int length
```


### getName(int pdfCompliance) {#getName-int-}
```
public static String getName(int pdfCompliance)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfCompliance | int |  |

**Returns:**
java.lang.String
### toString(int pdfCompliance) {#toString-int-}
```
public static String toString(int pdfCompliance)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfCompliance | int |  |

**Returns:**
java.lang.String
### fromName(String pdfComplianceName) {#fromName-java.lang.String-}
```
public static int fromName(String pdfComplianceName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfComplianceName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
