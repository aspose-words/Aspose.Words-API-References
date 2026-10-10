---
title: "PdfCustomPropertiesExport"
linktitle: "PdfCustomPropertiesExport"
second_title: "Aspose.Words для Java"
description: "Указывает способ, которым Document.getCustomDocumentProperties экспортируются в PDF‑файл в Java."
type: docs
weight: 530
url: /ru/java/com.aspose.words/pdfcustompropertiesexport/
---

**Inheritance:**
java.lang.Object
```
public class PdfCustomPropertiesExport
```

Указывает способ, которым [Document.getCustomDocumentProperties()](../../com.aspose.words/document/\#getCustomDocumentProperties) экспортируются в PDF‑файл.

 **Examples:** 

Показывает, как экспортировать пользовательские свойства при конвертации документа в PDF.

```

 Document doc = new Document();

 doc.getCustomDocumentProperties().add("Company", "My value");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "CustomPropertiesExport" property to "PdfCustomPropertiesExport.None" to discard
 // custom document properties as we save the document to .PDF.
 // Set the "CustomPropertiesExport" property to "PdfCustomPropertiesExport.Standard"
 // to preserve custom properties within the output PDF document.
 // Set the "CustomPropertiesExport" property to "PdfCustomPropertiesExport.Metadata"
 // to preserve custom properties in an XMP packet.
 options.setCustomPropertiesExport(pdfCustomPropertiesExportMode);

 doc.save(getArtifactsDir() + "PdfSaveOptions.CustomPropertiesExport.pdf", options);
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [METADATA](#METADATA) | Пользовательские свойства являются метаданными. |
| [NONE](#NONE) | Пользовательские свойства не экспортируются. |
| [STANDARD](#STANDARD) | Пользовательские свойства экспортируются как записи в словаре /Info. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String pdfCustomPropertiesExportName)](#fromName-java.lang.String) |  |
| [getName(int pdfCustomPropertiesExport)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfCustomPropertiesExport)](#toString-int) |  |
### METADATA {#METADATA}
```
public static int METADATA
```


Пользовательские свойства являются метаданными.

 **Remarks:** 

Пространство имён экспортированных свойств в пакете XMP равно "custprops". Каждое свойство имеет связанный xml-элемент "custprops:Property1", "custprops:Property2" и т.д. Внутри элемента свойства находится элемент "rdf:Description". Элемент описания содержит два элемента "custprops:Name", содержащий имя пользовательского свойства как значение этого xml-элемента, и "custprops:Value", содержащий значение пользовательского свойства как значение этого xml-элемента.

### NONE {#NONE}
```
public static int NONE
```


Пользовательские свойства не экспортируются.

### STANDARD {#STANDARD}
```
public static int STANDARD
```


Пользовательские свойства экспортируются как записи в словаре /Info.

Пользовательские свойства со следующими именами не экспортируются: "Title", "Author", "Subject", "Keywords", "Creator", "Producer", "CreationDate", "ModDate", "Trapped".

### length {#length}
```
public static int length
```


### fromName(String pdfCustomPropertiesExportName) {#fromName-java.lang.String}
```
public static int fromName(String pdfCustomPropertiesExportName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfCustomPropertiesExportName | java.lang.String |  |

**Returns:**
int
### getName(int pdfCustomPropertiesExport) {#getName-int}
```
public static String getName(int pdfCustomPropertiesExport)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfCustomPropertiesExport | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pdfCustomPropertiesExport) {#toString-int}
```
public static String toString(int pdfCustomPropertiesExport)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| pdfCustomPropertiesExport | int |  |

**Returns:**
java.lang.String
