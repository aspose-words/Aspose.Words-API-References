---
title: PdfCustomPropertiesExport
linktitle: PdfCustomPropertiesExport
second_title: Aspose.Words for Java
description: Specifies the way Document.getCustomDocumentProperties are exported to PDF file in Java.
type: docs
weight: 520
url: /java/com.aspose.words/pdfcustompropertiesexport/
---

**Inheritance:**
java.lang.Object
```
public class PdfCustomPropertiesExport
```

Specifies the way [Document.getCustomDocumentProperties()](../../com.aspose.words/document/\#getCustomDocumentProperties) are exported to PDF file.

 **Examples:** 

Shows how to export custom properties while converting a document to PDF.

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
## Fields

| Field | Description |
| --- | --- |
| [METADATA](#METADATA) | Custom properties are Metadata. |
| [NONE](#NONE) | No custom properties are exported. |
| [STANDARD](#STANDARD) | Custom properties are exported as entries in /Info dictionary. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String pdfCustomPropertiesExportName)](#fromName-java.lang.String) |  |
| [getName(int pdfCustomPropertiesExport)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfCustomPropertiesExport)](#toString-int) |  |
### METADATA {#METADATA}
```
public static int METADATA
```


Custom properties are Metadata.

 **Remarks:** 

The namespace of exported properties in XMP packet is "custprops". Every property has an associated xml-element "custprops:Property1", "custprops:Property2" and so on. There is "rdf:Description" element inside property element. The description element has two elements "custprops:Name", containing custom property's name as a value of this xml-element, and "custprops:Value", containing custom property's value as value of this xml-element.

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

### length {#length}
```
public static int length
```


### fromName(String pdfCustomPropertiesExportName) {#fromName-java.lang.String}
```
public static int fromName(String pdfCustomPropertiesExportName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfCustomPropertiesExportName | java.lang.String |  |

**Returns:**
int
### getName(int pdfCustomPropertiesExport) {#getName-int}
```
public static String getName(int pdfCustomPropertiesExport)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| pdfCustomPropertiesExport | int |  |

**Returns:**
java.lang.String
