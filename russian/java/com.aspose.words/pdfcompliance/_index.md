---
title: "PdfCompliance"
linktitle: "PdfCompliance"
second_title: "Aspose.Words для Java"
description: "Указывает уровень соответствия стандартам PDF в Java."
type: docs
weight: 529
url: /ru/java/com.aspose.words/pdfcompliance/
---

**Inheritance:**
java.lang.Object
```
public class PdfCompliance
```

Указывает уровень соответствия стандартам PDF.

 **Examples:** 

Показывает, как установить уровень соответствия стандартам PDF для сохраняемых PDF‑документов.

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
## Поля

| Поле | Описание |
| --- | --- |
| [PDF_17](#PDF-17) | Выходной файл будет соответствовать стандарту PDF 1.7 (ISO 32000-1). |
| [PDF_20](#PDF-20) | Выходной файл будет соответствовать стандарту PDF 2.0 (ISO 32000-2). |
| [PDF_A_1_A](#PDF-A-1-A) | Выходной файл будет соответствовать стандарту PDF/A-1a (ISO 19005-1). |
| [PDF_A_1_B](#PDF-A-1-B) | Выходной файл будет соответствовать стандарту PDF/A-1b (ISO 19005-1). |
| [PDF_A_2_A](#PDF-A-2-A) | Выходной файл будет соответствовать стандарту PDF/A-2a (ISO 19005-2). |
| [PDF_A_2_U](#PDF-A-2-U) | Выходной файл будет соответствовать стандарту PDF/A-2u (ISO 19005-2). |
| [PDF_A_3_A](#PDF-A-3-A) | Выходной файл будет соответствовать стандарту PDF/A-3a (ISO 19005-3). |
| [PDF_A_3_U](#PDF-A-3-U) | Выходной файл будет соответствовать стандарту PDF/A-3u (ISO 19005-3). |
| [PDF_A_4](#PDF-A-4) | Выходной файл будет соответствовать стандарту PDF/A-4 (ISO 19005-4:2020). |
| [PDF_A_4_F](#PDF-A-4-F) | Выходной файл будет соответствовать стандарту PDF/A-4f (ISO 19005-4:2020). |
| [PDF_A_4_UA_2](#PDF-A-4-UA-2) | Выходной файл будет соответствовать обоим стандартам PDF/A-4 (ISO 19005-4:2020) и PDF/UA-2 (ISO 14289-2:2024). |
| [PDF_UA_1](#PDF-UA-1) | Выходной файл будет соответствовать стандарту PDF/UA-1 (ISO 14289-1). |
| [PDF_UA_2](#PDF-UA-2) | Выходной файл будет соответствовать стандарту PDF/UA-2 (ISO 14289-2:2024). |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String pdfComplianceName)](#fromName-java.lang.String) |  |
| [getName(int pdfCompliance)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfCompliance)](#toString-int) |  |
### PDF_17 {#PDF-17}
```
public static int PDF_17
```


Выходной файл будет соответствовать стандарту PDF 1.7 (ISO 32000-1).

### PDF_20 {#PDF-20}
```
public static int PDF_20
```


Выходной файл будет соответствовать стандарту PDF 2.0 (ISO 32000-2).

### PDF_A_1_A {#PDF-A-1-A}
```
public static int PDF_A_1_A
```


Выходной файл будет соответствовать стандарту PDF/A-1a (ISO 19005-1). Этот уровень включает все требования PDF/A-1b и дополнительно требует, чтобы структура документа была включена (также известна как "tagged"), с целью обеспечения возможности поиска и повторного использования содержимого документа.

 **Remarks:** 

Обратите внимание, что экспорт структуры документа значительно увеличивает потребление памяти, особенно для больших документов.

### PDF_A_1_B {#PDF-A-1-B}
```
public static int PDF_A_1_B
```


Выходной файл будет соответствовать стандарту PDF/A-1b (ISO 19005-1). Цель PDF/A-1b — обеспечить надёжное воспроизведение визуального вида документа.

### PDF_A_2_A {#PDF-A-2-A}
```
public static int PDF_A_2_A
```


Выходной файл будет соответствовать стандарту PDF/A-2a (ISO 19005-2). Этот уровень включает все требования PDF/A-2u и дополнительно требует включения структуры документа (также известна как "tagged"), с целью обеспечения возможности поиска и повторного использования содержимого документа.

 **Remarks:** 

Обратите внимание, что экспорт структуры документа значительно увеличивает потребление памяти, особенно для больших документов.

### PDF_A_2_U {#PDF-A-2-U}
```
public static int PDF_A_2_U
```


Выходной файл будет соответствовать стандарту PDF/A-2u (ISO 19005-2). Цель PDF/A-2u — сохранять статический визуальный вид документа во времени, независимо от используемых инструментов и систем создания, хранения или отображения файлов. Кроме того, любой текст, содержащийся в документе, может быть надёжно извлечён в виде последовательности кодовых точек Unicode.

### PDF_A_3_A {#PDF-A-3-A}
```
public static int PDF_A_3_A
```


Выходной файл будет соответствовать стандарту PDF/A-3a (ISO 19005-3). Этот уровень включает все требования PDF/A-3u и дополнительно требует включения структуры документа (также известна как "tagged"), с целью обеспечения возможности поиска и повторного использования содержимого документа.

 **Remarks:** 

Обратите внимание, что экспорт структуры документа значительно увеличивает потребление памяти, особенно для больших документов.

### PDF_A_3_U {#PDF-A-3-U}
```
public static int PDF_A_3_U
```


Выходной файл будет соответствовать стандарту PDF/A-3u (ISO 19005-3). PDF/A-3u (как и PDF/A-2u) имеет цель сохранять статический визуальный вид документа во времени, независимо от используемых инструментов и систем создания, хранения или отображения файлов. Кроме того, любой текст, содержащийся в документе, может быть надёжно извлечён в виде последовательности кодовых точек Unicode. Помимо PDF/A-2u, PDF/A-3u позволяет встраивать вложения в PDF‑документ.

### PDF_A_4 {#PDF-A-4}
```
public static int PDF_A_4
```


Выходной файл будет соответствовать стандарту PDF/A-4 (ISO 19005-4:2020). PDF/A-4 имеет цель сохранять статический визуальный вид документа во времени, независимо от используемых инструментов и систем создания, хранения или отображения файлов. Кроме того, любой текст, содержащийся в документе, может быть надёжно извлечён в виде последовательности кодовых точек Unicode.

### PDF_A_4_F {#PDF-A-4-F}
```
public static int PDF_A_4_F
```


Выходной файл будет соответствовать стандарту PDF/A-4f (ISO 19005-4:2020). Этот уровень включает все требования PDF/A-4 и дополнительно позволяет встраивать вложения в PDF‑документ.

### PDF_A_4_UA_2 {#PDF-A-4-UA-2}
```
public static int PDF_A_4_UA_2
```


Выходной файл будет соответствовать обоим стандартам PDF/A-4 (ISO 19005-4:2020) и PDF/UA-2 (ISO 14289-2:2024). PDF/A-4 имеет цель сохранять статический визуальный вид документа во времени, независимо от используемых инструментов и систем создания, хранения или отображения файлов. Основная цель PDF/UA — определить, как представлять электронные документы в формате PDF таким образом, чтобы файл был доступным.

 **Remarks:** 

Обратите внимание, что экспорт структуры документа значительно увеличивает потребление памяти, особенно для больших документов.

### PDF_UA_1 {#PDF-UA-1}
```
public static int PDF_UA_1
```


Выходной файл будет соответствовать стандарту PDF/UA-1 (ISO 14289-1). Основная цель PDF/UA — определить, как представлять электронные документы в формате PDF таким образом, чтобы файл был доступным.

 **Remarks:** 

Обратите внимание, что экспорт структуры документа значительно увеличивает потребление памяти, особенно для больших документов.

### PDF_UA_2 {#PDF-UA-2}
```
public static int PDF_UA_2
```


Выходной файл будет соответствовать стандарту PDF/UA-2 (ISO 14289-2:2024). Основная цель PDF/UA — определить, как представлять электронные документы в формате PDF таким образом, чтобы файл был доступным.

 **Remarks:** 

Обратите внимание, что экспорт структуры документа значительно увеличивает потребление памяти, особенно для больших документов.

### length {#length}
```
public static int length
```


### fromName(String pdfComplianceName) {#fromName-java.lang.String}
```
public static int fromName(String pdfComplianceName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfComplianceName | java.lang.String |  |

**Returns:**
int
### getName(int pdfCompliance) {#getName-int}
```
public static String getName(int pdfCompliance)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfCompliance | int |  |

**Returns:**
java.lang.String
