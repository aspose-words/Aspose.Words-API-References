---
title: "HeaderFooterBookmarksExportMode"
linktitle: "HeaderFooterBookmarksExportMode"
second_title: "Aspose.Words para Java"
description: "Especifica cómo se exportan los marcadores en encabezados/pies de página en Java."
type: docs
weight: 370
url: /es/java/com.aspose.words/headerfooterbookmarksexportmode/
---

**Inheritance:**
java.lang.Object
```
public class HeaderFooterBookmarksExportMode
```

Especifica cómo se exportan los marcadores en encabezados/pies de página.

 **Examples:** 

Muestra cómo procesar los marcadores en encabezados/pies de página en un documento que estamos renderizando a PDF.

```

 Document doc = new Document(getMyDir() + "Bookmarks in headers and footers.docx");

 // Create a "PdfSaveOptions" object that we can pass to the document's "Save" method
 // to modify how that method converts the document to .PDF.
 PdfSaveOptions saveOptions = new PdfSaveOptions();

 // Set the "PageMode" property to "PdfPageMode.UseOutlines" to display the outline navigation pane in the output PDF.
 saveOptions.setPageMode(PdfPageMode.USE_OUTLINES);

 // Set the "DefaultBookmarksOutlineLevel" property to "1" to display all
 // bookmarks at the first level of the outline in the output PDF.
 saveOptions.getOutlineOptions().setDefaultBookmarksOutlineLevel(1);

 // Set the "HeaderFooterBookmarksExportMode" property to "HeaderFooterBookmarksExportMode.None" to
 // not export any bookmarks that are inside headers/footers.
 // Set the "HeaderFooterBookmarksExportMode" property to "HeaderFooterBookmarksExportMode.First" to
 // only export bookmarks in the first section's header/footers.
 // Set the "HeaderFooterBookmarksExportMode" property to "HeaderFooterBookmarksExportMode.All" to
 // export bookmarks that are in all headers/footers.
 saveOptions.setHeaderFooterBookmarksExportMode(headerFooterBookmarksExportMode);

 doc.save(getArtifactsDir() + "PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [ALL](#ALL) | Los marcadores en todos los encabezados/pies de página se exportan. |
| [FIRST](#FIRST) | Solo el marcador en el primer encabezado/pie de página de la sección se exporta. |
| [NONE](#NONE) | Los marcadores en encabezados/pies de página no se exportan. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String headerFooterBookmarksExportModeName)](#fromName-java.lang.String) |  |
| [getName(int headerFooterBookmarksExportMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int headerFooterBookmarksExportMode)](#toString-int) |  |
### ALL {#ALL}
```
public static int ALL
```


Los marcadores en todos los encabezados/pies de página se exportan.

### FIRST {#FIRST}
```
public static int FIRST
```


Solo el marcador en el primer encabezado/pie de página de la sección se exporta.

### NONE {#NONE}
```
public static int NONE
```


Los marcadores en encabezados/pies de página no se exportan.

### length {#length}
```
public static int length
```


### fromName(String headerFooterBookmarksExportModeName) {#fromName-java.lang.String}
```
public static int fromName(String headerFooterBookmarksExportModeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| headerFooterBookmarksExportModeName | java.lang.String |  |

**Returns:**
int
### getName(int headerFooterBookmarksExportMode) {#getName-int}
```
public static String getName(int headerFooterBookmarksExportMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| headerFooterBookmarksExportMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int headerFooterBookmarksExportMode) {#toString-int}
```
public static String toString(int headerFooterBookmarksExportMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| headerFooterBookmarksExportMode | int |  |

**Returns:**
java.lang.String
