---
title: "PdfCustomPropertiesExport"
linktitle: "PdfCustomPropertiesExport"
second_title: "Aspose.Words Java için"
description: "Java'da Document.getCustomDocumentProperties öğelerinin PDF dosyasına nasıl dışa aktarıldığını belirtir."
type: docs
weight: 530
url: /tr/java/com.aspose.words/pdfcustompropertiesexport/
---

**Inheritance:**
java.lang.Object
```
public class PdfCustomPropertiesExport
```

PDF dosyasına [Document.getCustomDocumentProperties()](../../com.aspose.words/document/\#getCustomDocumentProperties) öğelerinin nasıl dışa aktarıldığını belirtir.

 **Examples:** 

Bir belgeyi PDF'ye dönüştürürken özel özelliklerin nasıl dışa aktarılacağını gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [METADATA](#METADATA) | Özel özellikler Metadata'dır. |
| [NONE](#NONE) | Herhangi bir özel özellik dışa aktarılmaz. |
| [STANDARD](#STANDARD) | Özel özellikler /Info sözlüğünde girişler olarak dışa aktarılır. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String pdfCustomPropertiesExportName)](#fromName-java.lang.String) |  |
| [getName(int pdfCustomPropertiesExport)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfCustomPropertiesExport)](#toString-int) |  |
### METADATA {#METADATA}
```
public static int METADATA
```


Özel özellikler Metadata'dır.

 **Remarks:** 

XMP paketindeki dışa aktarılan özelliklerin ad alanı "custprops"'tir. Her özellik, "custprops:Property1", "custprops:Property2" vb. ilişkili bir xml-elemente sahiptir. Özellik öğesi içinde bir "rdf:Description" öğesi vardır. Açıklama öğesi iki öğe içerir: "custprops:Name", bu xml-elementin değeri olarak özel özelliğin adını içerir ve "custprops:Value", bu xml-elementin değeri olarak özel özelliğin değerini içerir.

### NONE {#NONE}
```
public static int NONE
```


Herhangi bir özel özellik dışa aktarılmaz.

### STANDARD {#STANDARD}
```
public static int STANDARD
```


Özel özellikler /Info sözlüğünde girişler olarak dışa aktarılır.

Aşağıdaki adlara sahip özel özellikler dışa aktarılmaz: "Title", "Author", "Subject", "Keywords", "Creator", "Producer", "CreationDate", "ModDate", "Trapped".

### length {#length}
```
public static int length
```


### fromName(String pdfCustomPropertiesExportName) {#fromName-java.lang.String}
```
public static int fromName(String pdfCustomPropertiesExportName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pdfCustomPropertiesExportName | java.lang.String |  |

**Returns:**
int
### getName(int pdfCustomPropertiesExport) {#getName-int}
```
public static String getName(int pdfCustomPropertiesExport)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| pdfCustomPropertiesExport | int |  |

**Returns:**
java.lang.String
