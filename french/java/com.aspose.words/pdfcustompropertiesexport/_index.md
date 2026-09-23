---
title: "PdfCustomPropertiesExport"
linktitle: "PdfCustomPropertiesExport"
second_title: "Aspose.Words pour Java"
description: "Spécifie la manière dont Document.getCustomDocumentProperties sont exportées vers le fichier PDF en Java."
type: docs
weight: 530
url: /fr/java/com.aspose.words/pdfcustompropertiesexport/
---

**Inheritance:**
java.lang.Object
```
public class PdfCustomPropertiesExport
```

Spécifie la manière dont [Document.getCustomDocumentProperties()](../../com.aspose.words/document/\#getCustomDocumentProperties) sont exportées vers le fichier PDF.

 **Examples:** 

Montre comment exporter les propriétés personnalisées lors de la conversion d'un document en PDF.

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
## Champs

| Champ | Description |
| --- | --- |
| [METADATA](#METADATA) | Les propriétés personnalisées sont des métadonnées. |
| [NONE](#NONE) | Aucune propriété personnalisée n'est exportée. |
| [STANDARD](#STANDARD) | Les propriétés personnalisées sont exportées comme entrées dans le dictionnaire /Info. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String pdfCustomPropertiesExportName)](#fromName-java.lang.String) |  |
| [getName(int pdfCustomPropertiesExport)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfCustomPropertiesExport)](#toString-int) |  |
### METADATA {#METADATA}
```
public static int METADATA
```


Les propriétés personnalisées sont des métadonnées.

 **Remarks:** 

L'espace de noms des propriétés exportées dans le paquet XMP est "custprops". Chaque propriété possède un élément xml associé "custprops:Property1", "custprops:Property2" et ainsi de suite. Il y a un élément "rdf:Description" à l'intérieur de l'élément de propriété. L'élément de description contient deux éléments "custprops:Name", contenant le nom de la propriété personnalisée comme valeur de cet élément xml, et "custprops:Value", contenant la valeur de la propriété personnalisée comme valeur de cet élément xml.

### NONE {#NONE}
```
public static int NONE
```


Aucune propriété personnalisée n'est exportée.

### STANDARD {#STANDARD}
```
public static int STANDARD
```


Les propriétés personnalisées sont exportées comme entrées dans le dictionnaire /Info.

Les propriétés personnalisées avec les noms suivants ne sont pas exportées : "Title", "Author", "Subject", "Keywords", "Creator", "Producer", "CreationDate", "ModDate", "Trapped".

### length {#length}
```
public static int length
```


### fromName(String pdfCustomPropertiesExportName) {#fromName-java.lang.String}
```
public static int fromName(String pdfCustomPropertiesExportName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| pdfCustomPropertiesExportName | java.lang.String |  |

**Returns:**
int
### getName(int pdfCustomPropertiesExport) {#getName-int}
```
public static String getName(int pdfCustomPropertiesExport)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| pdfCustomPropertiesExport | int |  |

**Returns:**
java.lang.String
