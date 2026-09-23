---
title: "PdfCustomPropertiesExport"
linktitle: "PdfCustomPropertiesExport"
second_title: "Aspose.Words per Java"
description: "Specifica il modo in cui Document.getCustomDocumentProperties vengono esportate in un file PDF in Java."
type: docs
weight: 530
url: /it/java/com.aspose.words/pdfcustompropertiesexport/
---

**Inheritance:**
java.lang.Object
```
public class PdfCustomPropertiesExport
```

Specifica il modo in cui [Document.getCustomDocumentProperties()](../../com.aspose.words/document/\#getCustomDocumentProperties) vengono esportate in un file PDF.

 **Examples:** 

Mostra come esportare le proprietà personalizzate durante la conversione di un documento in PDF.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [METADATA](#METADATA) | Le proprietà personalizzate sono Metadati. |
| [NONE](#NONE) | Nessuna proprietà personalizzata viene esportata. |
| [STANDARD](#STANDARD) | Le proprietà personalizzate vengono esportate come voci nel dizionario /Info. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String pdfCustomPropertiesExportName)](#fromName-java.lang.String) |  |
| [getName(int pdfCustomPropertiesExport)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfCustomPropertiesExport)](#toString-int) |  |
### METADATA {#METADATA}
```
public static int METADATA
```


Le proprietà personalizzate sono Metadati.

 **Remarks:** 

Lo spazio dei nomi delle proprietà esportate nel pacchetto XMP è "custprops". Ogni proprietà ha un elemento xml associato "custprops:Property1", "custprops:Property2" e così via. C'è un elemento "rdf:Description" all'interno dell'elemento della proprietà. L'elemento description ha due elementi "custprops:Name", contenente il nome della proprietà personalizzata come valore di questo elemento xml, e "custprops:Value", contenente il valore della proprietà personalizzata come valore di questo elemento xml.

### NONE {#NONE}
```
public static int NONE
```


Nessuna proprietà personalizzata viene esportata.

### STANDARD {#STANDARD}
```
public static int STANDARD
```


Le proprietà personalizzate vengono esportate come voci nel dizionario /Info.

Le proprietà personalizzate con i seguenti nomi non vengono esportate: "Title", "Author", "Subject", "Keywords", "Creator", "Producer", "CreationDate", "ModDate", "Trapped".

### length {#length}
```
public static int length
```


### fromName(String pdfCustomPropertiesExportName) {#fromName-java.lang.String}
```
public static int fromName(String pdfCustomPropertiesExportName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pdfCustomPropertiesExportName | java.lang.String |  |

**Returns:**
int
### getName(int pdfCustomPropertiesExport) {#getName-int}
```
public static String getName(int pdfCustomPropertiesExport)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| pdfCustomPropertiesExport | int |  |

**Returns:**
java.lang.String
