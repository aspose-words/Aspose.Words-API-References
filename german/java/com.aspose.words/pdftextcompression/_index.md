---
title: "PdfTextCompression"
linktitle: "PdfTextCompression"
second_title: "Aspose.Words für Java"
description: "Gibt einen Kompressionstyp an, der auf alle Inhalte der PDF-Datei außer Bildern in Java angewendet wird."
type: docs
weight: 543
url: /de/java/com.aspose.words/pdftextcompression/
---

**Inheritance:**
java.lang.Object
```
public class PdfTextCompression
```

Gibt einen Kompressionstyp an, der auf alle Inhalte in der PDF-Datei außer Bildern angewendet wird.

 **Examples:** 

Zeigt, wie man Textkompression beim Speichern eines Dokuments als PDF anwendet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 for (int i = 0; i < 100; i++)
     builder.writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
             "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions options = new PdfSaveOptions();

 // Set the "TextCompression" property to "PdfTextCompression.None" to not apply any
 // compression to text when we save the document to PDF.
 // Set the "TextCompression" property to "PdfTextCompression.Flate" to apply ZIP compression
 // to text when we save the document to PDF. The larger the document, the bigger the impact that this will have.
 options.setTextCompression(pdfTextCompression);

 doc.save(getArtifactsDir() + "PdfSaveOptions.TextCompression.pdf", options);
 
```
## Felder

| Feld | Beschreibung |
| --- | --- |
| [FLATE](#FLATE) | Flate (ZIP)-Kompression. |
| [NONE](#NONE) | Keine Kompression. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String pdfTextCompressionName)](#fromName-java.lang.String) |  |
| [getName(int pdfTextCompression)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfTextCompression)](#toString-int) |  |
### FLATE {#FLATE}
```
public static int FLATE
```


Flate (ZIP)-Kompression.

### NONE {#NONE}
```
public static int NONE
```


Keine Kompression.

### length {#length}
```
public static int length
```


### fromName(String pdfTextCompressionName) {#fromName-java.lang.String}
```
public static int fromName(String pdfTextCompressionName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pdfTextCompressionName | java.lang.String |  |

**Returns:**
int
### getName(int pdfTextCompression) {#getName-int}
```
public static String getName(int pdfTextCompression)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pdfTextCompression | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pdfTextCompression) {#toString-int}
```
public static String toString(int pdfTextCompression)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| pdfTextCompression | int |  |

**Returns:**
java.lang.String
