---
title: PdfCompliance
linktitle: PdfCompliance
second_title: Aspose.Words for Java
description: Specifies the PDF standards compliance level in Java.
type: docs
weight: 514
url: /java/com.aspose.words/pdfcompliance/
---

**Inheritance:**
java.lang.Object
```
public class PdfCompliance
```

Specifies the PDF standards compliance level.

 **Examples:** 

Shows how to set the PDF standards compliance level of saved PDF documents.

```

 Document doc = new Document(getMyDir() + "Images.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 // Note that some PdfSaveOptions are prohibited when saving to one of the standards and automatically fixed.
 // Use IWarningCallback to know which options are automatically fixed.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Set the "Compliance" property to "PdfCompliance.PdfA1b" to comply with the "PDF/A-1b" standard,
 // which aims to preserve the visual appearance of the document as Aspose.Words convert it to PDF.
 // Set the "Compliance" property to "PdfCompliance.Pdf17" to comply with the "1.7" standard.
 // Set the "Compliance" property to "PdfCompliance.PdfA1a" to comply with the "PDF/A-1a" standard,
 // which complies with "PDF/A-1b" as well as preserving the document structure of the original document.
 // Set the "Compliance" property to "PdfCompliance.PdfUa1" to comply with the "PDF/UA-1" (ISO 14289-1) standard,
 // which aims to define represent electronic documents in PDF that allow the file to be accessible.
 // Set the "Compliance" property to "PdfCompliance.Pdf20" to comply with the "PDF 2.0" (ISO 32000-2) standard.
 // Set the "Compliance" property to "PdfCompliance.PdfA4" to comply with the "PDF/A-4" (ISO 19004:2020) standard,
 // which preserving document static visual appearance over time.
 // Set the "Compliance" property to "PdfCompliance.PdfA4Ua2" to comply with both PDF/A-4 (ISO 19005-4:2020)
 // and PDF/UA-2 (ISO 14289-2:2024) standards.
 // Set the "Compliance" property to "PdfCompliance.PdfUa2" to comply with the PDF/UA-2 (ISO 14289-2:2024) standard.
 // This helps with making documents searchable but may significantly increase the size of already large documents.
 saveOptions.setCompliance(pdfCompliance);

 doc.save(getArtifactsDir() + "PdfSaveOptions.Compliance.pdf", saveOptions);
 
```
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
| [PDF_A_4_UA_2](#PDF-A-4-UA-2) | The output file will comply with both PDF/A-4 (ISO 19005-4:2020) and PDF/UA-2 (ISO 14289-2:2024) standards. |
| [PDF_UA_1](#PDF-UA-1) | The output file will comply with the PDF/UA-1 (ISO 14289-1) standard. |
| [PDF_UA_2](#PDF-UA-2) | The output file will comply with the PDF/UA-2 (ISO 14289-2:2024) standard. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String pdfComplianceName)](#fromName-java.lang.String) |  |
| [getName(int pdfCompliance)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfCompliance)](#toString-int) |  |
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


The output file will comply with the PDF/A-1a (ISO 19005-1) standard. This level includes all the requirements of PDF/A-1b and additionally requires that document structure be included (also known as being "tagged"), with the objective of ensuring that document content can be searched and repurposed.

 **Remarks:** 

Note that exporting the document structure significantly increases the memory consumption, especially for the large documents.

### PDF_A_1_B {#PDF-A-1-B}
```
public static int PDF_A_1_B
```


The output file will comply with the PDF/A-1b (ISO 19005-1) standard. PDF/A-1b has the objective of ensuring reliable reproduction of the visual appearance of the document.

### PDF_A_2_A {#PDF-A-2-A}
```
public static int PDF_A_2_A
```


The output file will comply with the PDF/A-2a (ISO 19005-2) standard. This level includes all the requirements of PDF/A-2u and additionally requires that document structure be included (also known as being "tagged"), with the objective of ensuring that document content can be searched and repurposed.

 **Remarks:** 

Note that exporting the document structure significantly increases the memory consumption, especially for the large documents.

### PDF_A_2_U {#PDF-A-2-U}
```
public static int PDF_A_2_U
```


The output file will comply with the PDF/A-2u (ISO 19005-2) standard. PDF/A-2u has the objective of preserving document static visual appearance over time, independent of the tools and systems used for creating, storing or rendering the files. Additionally, any text contained in the document can be reliably extracted as a series of Unicode codepoints.

### PDF_A_4 {#PDF-A-4}
```
public static int PDF_A_4
```


The output file will comply with the PDF/A-4 (ISO 19005-4:2020) standard. PDF/A-4 has the objective of preserving document static visual appearance over time, independent of the tools and systems used for creating, storing or rendering the files. Additionally, any text contained in the document can be reliably extracted as a series of Unicode codepoints.

### PDF_A_4_UA_2 {#PDF-A-4-UA-2}
```
public static int PDF_A_4_UA_2
```


The output file will comply with both PDF/A-4 (ISO 19005-4:2020) and PDF/UA-2 (ISO 14289-2:2024) standards. PDF/A-4 has the objective of preserving document static visual appearance over time, independent of the tools and systems used for creating, storing or rendering the files. The primary purpose of PDF/UA is to define how to represent electronic documents in the PDF format in a manner that allows the file to be accessible.

 **Remarks:** 

Note that exporting the document structure significantly increases the memory consumption, especially for the large documents.

### PDF_UA_1 {#PDF-UA-1}
```
public static int PDF_UA_1
```


The output file will comply with the PDF/UA-1 (ISO 14289-1) standard. The primary purpose of PDF/UA is to define how to represent electronic documents in the PDF format in a manner that allows the file to be accessible.

 **Remarks:** 

Note that exporting the document structure significantly increases the memory consumption, especially for the large documents.

### PDF_UA_2 {#PDF-UA-2}
```
public static int PDF_UA_2
```


The output file will comply with the PDF/UA-2 (ISO 14289-2:2024) standard. The primary purpose of PDF/UA is to define how to represent electronic documents in the PDF format in a manner that allows the file to be accessible.

 **Remarks:** 

Note that exporting the document structure significantly increases the memory consumption, especially for the large documents.

### length {#length}
```
public static int length
```


### fromName(String pdfComplianceName) {#fromName-java.lang.String}
```
public static int fromName(String pdfComplianceName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfComplianceName | java.lang.String |  |

**Returns:**
int
### getName(int pdfCompliance) {#getName-int}
```
public static String getName(int pdfCompliance)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfCompliance | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pdfCompliance) {#toString-int}
```
public static String toString(int pdfCompliance)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfCompliance | int |  |

**Returns:**
java.lang.String
