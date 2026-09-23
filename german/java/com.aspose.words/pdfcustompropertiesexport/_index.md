---
title: "PdfCustomPropertiesExport"
linktitle: "PdfCustomPropertiesExport"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie Document.getCustomDocumentProperties in Java in eine PDF‑Datei exportiert werden."
type: docs
weight: 530
url: /de/java/com.aspose.words/pdfcustompropertiesexport/
---

**Inheritance:**
java.lang.Object
```
public class PdfCustomPropertiesExport
```

Gibt an, wie [Document.getCustomDocumentProperties()](../../com.aspose.words/document/\#getCustomDocumentProperties) in eine PDF‑Datei exportiert werden.

 **Examples:** 

Zeigt, wie benutzerdefinierte Eigenschaften beim Konvertieren eines Dokuments in PDF exportiert werden.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [METADATA](#METADATA) | Benutzerdefinierte Eigenschaften sind Metadaten. |
| [NONE](#NONE) | Es werden keine benutzerdefinierten Eigenschaften exportiert. |
| [STANDARD](#STANDARD) | Benutzerdefinierte Eigenschaften werden als Einträge im /Info‑Verzeichnis exportiert. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String pdfCustomPropertiesExportName)](#fromName-java.lang.String) |  |
| [getName(int pdfCustomPropertiesExport)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfCustomPropertiesExport)](#toString-int) |  |
### METADATA {#METADATA}
```
public static int METADATA
```


Benutzerdefinierte Eigenschaften sind Metadaten.

 **Remarks:** 

Der Namensraum der exportierten Eigenschaften im XMP‑Paket ist "custprops". Jede Eigenschaft hat ein zugehöriges XML‑Element "custprops:Property1", "custprops:Property2" und so weiter. Im Eigenschaftselement befindet sich ein "rdf:Description"‑Element. Das Beschreibungs‑Element enthält zwei Elemente "custprops:Name", das den Namen der benutzerdefinierten Eigenschaft als Wert dieses XML‑Elements enthält, und "custprops:Value", das den Wert der benutzerdefinierten Eigenschaft als Wert dieses XML‑Elements enthält.

### NONE {#NONE}
```
public static int NONE
```


Es werden keine benutzerdefinierten Eigenschaften exportiert.

### STANDARD {#STANDARD}
```
public static int STANDARD
```


Benutzerdefinierte Eigenschaften werden als Einträge im /Info‑Verzeichnis exportiert.

Benutzerdefinierte Eigenschaften mit den folgenden Namen werden nicht exportiert: "Title", "Author", "Subject", "Keywords", "Creator", "Producer", "CreationDate", "ModDate", "Trapped".

### length {#length}
```
public static int length
```


### fromName(String pdfCustomPropertiesExportName) {#fromName-java.lang.String}
```
public static int fromName(String pdfCustomPropertiesExportName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pdfCustomPropertiesExportName | java.lang.String |  |

**Returns:**
int
### getName(int pdfCustomPropertiesExport) {#getName-int}
```
public static String getName(int pdfCustomPropertiesExport)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pdfCustomPropertiesExport | int |  |

**Returns:**
java.lang.String
