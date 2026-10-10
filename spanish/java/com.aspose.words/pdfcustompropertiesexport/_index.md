---
title: "PdfCustomPropertiesExport"
linktitle: "PdfCustomPropertiesExport"
second_title: "Aspose.Words para Java"
description: "Especifica la forma en que Document.getCustomDocumentProperties se exportan al archivo PDF en Java."
type: docs
weight: 530
url: /es/java/com.aspose.words/pdfcustompropertiesexport/
---

**Inheritance:**
java.lang.Object
```
public class PdfCustomPropertiesExport
```

Especifica la forma en que [Document.getCustomDocumentProperties()](../../com.aspose.words/document/\#getCustomDocumentProperties) se exportan al archivo PDF.

 **Examples:** 

Muestra cómo exportar propiedades personalizadas al convertir un documento a PDF.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [METADATA](#METADATA) | Las propiedades personalizadas son Metadatos. |
| [NONE](#NONE) | No se exportan propiedades personalizadas. |
| [STANDARD](#STANDARD) | Las propiedades personalizadas se exportan como entradas en el diccionario /Info. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String pdfCustomPropertiesExportName)](#fromName-java.lang.String) |  |
| [getName(int pdfCustomPropertiesExport)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfCustomPropertiesExport)](#toString-int) |  |
### METADATA {#METADATA}
```
public static int METADATA
```


Las propiedades personalizadas son Metadatos.

 **Remarks:** 

El espacio de nombres de las propiedades exportadas en el paquete XMP es "custprops". Cada propiedad tiene un elemento xml asociado "custprops:Property1", "custprops:Property2" y así sucesivamente. Hay un elemento "rdf:Description" dentro del elemento de la propiedad. El elemento de descripción tiene dos elementos "custprops:Name", que contiene el nombre de la propiedad personalizada como valor de este elemento xml, y "custprops:Value", que contiene el valor de la propiedad personalizada como valor de este elemento xml.

### NONE {#NONE}
```
public static int NONE
```


No se exportan propiedades personalizadas.

### STANDARD {#STANDARD}
```
public static int STANDARD
```


Las propiedades personalizadas se exportan como entradas en el diccionario /Info.

Las propiedades personalizadas con los siguientes nombres no se exportan: "Title", "Author", "Subject", "Keywords", "Creator", "Producer", "CreationDate", "ModDate", "Trapped".

### length {#length}
```
public static int length
```


### fromName(String pdfCustomPropertiesExportName) {#fromName-java.lang.String}
```
public static int fromName(String pdfCustomPropertiesExportName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pdfCustomPropertiesExportName | java.lang.String |  |

**Returns:**
int
### getName(int pdfCustomPropertiesExport) {#getName-int}
```
public static String getName(int pdfCustomPropertiesExport)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| pdfCustomPropertiesExport | int |  |

**Returns:**
java.lang.String
