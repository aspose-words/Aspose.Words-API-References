---
title: PdfCustomPropertiesExport
second_title: Aspose.Words for Java API Reference
description: Specifies the way  are exported to PDF file.
type: docs
weight: 450
url: /java/com.aspose.words/pdfcustompropertiesexport/
---

**Inheritance:**
java.lang.Object
```
public class PdfCustomPropertiesExport
```

Specifies the way [Document.getCustomDocumentProperties()](../../com.aspose.words/document\#getCustomDocumentProperties--) are exported to PDF file.
## Fields

| Field | Description |
| --- | --- |
| [NONE](#NONE) | No custom properties are exported. |
| [STANDARD](#STANDARD) | Custom properties are exported as entries in /Info dictionary. |
| [METADATA](#METADATA) | Custom properties are Metadata. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int pdfCustomPropertiesExport)](#getName-int-) |  |
| [toString(int pdfCustomPropertiesExport)](#toString-int-) |  |
| [fromName(String pdfCustomPropertiesExportName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### NONE {#NONE}
```
public static int NONE
```


No custom properties are exported.

### STANDARD {#STANDARD}
```
public static int STANDARD
```


Custom properties are exported as entries in /Info dictionary.

Custom properties with the following names are not exported: "Title", "Author", "Subject", "Keywords", "Creator", "Producer", "CreationDate", "ModDate", "Trapped".

### METADATA {#METADATA}
```
public static int METADATA
```


Custom properties are Metadata.

The namespace of exported properties in XMP packet is "custprops". Every property has an associated xml-element "custprops:Property1", "custprops:Property2" and so on. There is "rdf:Description" element inside property element. The description element has two elements "custprops:Name", containing custom property's name as a value of this xml-element, and "custprops:Value", containing custom property's value as value of this xml-element.

### length {#length}
```
public static int length
```


### getName(int pdfCustomPropertiesExport) {#getName-int-}
```
public static String getName(int pdfCustomPropertiesExport)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfCustomPropertiesExport | int |  |

**Returns:**
java.lang.String
### toString(int pdfCustomPropertiesExport) {#toString-int-}
```
public static String toString(int pdfCustomPropertiesExport)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfCustomPropertiesExport | int |  |

**Returns:**
java.lang.String
### fromName(String pdfCustomPropertiesExportName) {#fromName-java.lang.String-}
```
public static int fromName(String pdfCustomPropertiesExportName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfCustomPropertiesExportName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
