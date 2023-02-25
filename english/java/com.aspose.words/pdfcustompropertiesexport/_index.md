---
title: PdfCustomPropertiesExport
linktitle: PdfCustomPropertiesExport
second_title: Aspose.Words for Java API Reference
description: Specifies the way  are exported to PDF file in Java.
type: docs
weight: 456
url: /java/com.aspose.words/pdfcustompropertiesexport/
---

**Inheritance:**
java.lang.Object
```
public class PdfCustomPropertiesExport
```

Specifies the way [Document.getCustomDocumentProperties()](../../com.aspose.words/document/\#getCustomDocumentProperties) are exported to PDF file.
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
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String pdfCustomPropertiesExportName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int pdfCustomPropertiesExport)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int pdfCustomPropertiesExport)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### METADATA {#METADATA}
```
public static int METADATA
```


Custom properties are Metadata.

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


### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
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
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
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
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
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
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

