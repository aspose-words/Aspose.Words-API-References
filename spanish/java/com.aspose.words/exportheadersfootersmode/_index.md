---
title: "ExportHeadersFootersMode"
linktitle: "ExportHeadersFootersMode"
second_title: "Aspose.Words para Java"
description: "Especifica cómo se exportan los encabezados y pies de página a HTML, MHTML o EPUB en Java."
type: docs
weight: 192
url: /es/java/com.aspose.words/exportheadersfootersmode/
---

**Inheritance:**
java.lang.Object
```
public class ExportHeadersFootersMode
```

Especifica cómo se exportan los encabezados y pies de página a HTML, MHTML o EPUB.

 **Examples:** 

Muestra cómo omitir los encabezados/pies de página al guardar un documento en HTML.

```

 Document doc = new Document(getMyDir() + "Header and footer types.docx");

 // This document contains headers and footers. We can access them via the "HeadersFooters" collection.
 Assert.assertEquals("First header", doc.getFirstSection().getHeadersFooters().getByHeaderFooterType(HeaderFooterType.HEADER_FIRST).getText().trim());

 // Formats such as .html do not split the document into pages, so headers/footers will not function the same way
 // they would when we open the document as a .docx using Microsoft Word.
 // If we convert a document with headers/footers to html, the conversion will assimilate the headers/footers into body text.
 // We can use a SaveOptions object to omit headers/footers while converting to html.
 HtmlSaveOptions saveOptions =
         new HtmlSaveOptions(SaveFormat.HTML);
 {
     saveOptions.setExportHeadersFootersMode(ExportHeadersFootersMode.NONE);
 }

 doc.save(getArtifactsDir() + "HeaderFooter.ExportMode.html", saveOptions);

 // Open our saved document and verify that it does not contain the header's text.
 doc = new Document(getArtifactsDir() + "HeaderFooter.ExportMode.html");

 Assert.assertFalse(doc.getRange().getText().contains("First header"));
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [FIRST_PAGE_HEADER_FOOTER_PER_SECTION](#FIRST-PAGE-HEADER-FOOTER-PER-SECTION) | El encabezado y pie de página de la primera página se exportan al inicio y al final de cada sección. |
| [FIRST_SECTION_HEADER_LAST_SECTION_FOOTER](#FIRST-SECTION-HEADER-LAST-SECTION-FOOTER) | El encabezado principal de la primera sección se exporta al inicio del documento y el pie de página principal al final. |
| [NONE](#NONE) | Los encabezados y pies de página no se exportan. |
| [PER_SECTION](#PER-SECTION) | Los encabezados y pies de página principales se exportan al inicio y al final de cada sección. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String exportHeadersFootersModeName)](#fromName-java.lang.String) |  |
| [getName(int exportHeadersFootersMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int exportHeadersFootersMode)](#toString-int) |  |
### FIRST_PAGE_HEADER_FOOTER_PER_SECTION {#FIRST-PAGE-HEADER-FOOTER-PER-SECTION}
```
public static int FIRST_PAGE_HEADER_FOOTER_PER_SECTION
```


El encabezado y pie de página de la primera página se exportan al inicio y al final de cada sección.

### FIRST_SECTION_HEADER_LAST_SECTION_FOOTER {#FIRST-SECTION-HEADER-LAST-SECTION-FOOTER}
```
public static int FIRST_SECTION_HEADER_LAST_SECTION_FOOTER
```


El encabezado principal de la primera sección se exporta al inicio del documento y el pie de página principal al final.

### NONE {#NONE}
```
public static int NONE
```


Los encabezados y pies de página no se exportan.

### PER_SECTION {#PER-SECTION}
```
public static int PER_SECTION
```


Los encabezados y pies de página principales se exportan al inicio y al final de cada sección.

### length {#length}
```
public static int length
```


### fromName(String exportHeadersFootersModeName) {#fromName-java.lang.String}
```
public static int fromName(String exportHeadersFootersModeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| exportHeadersFootersModeName | java.lang.String |  |

**Returns:**
int
### getName(int exportHeadersFootersMode) {#getName-int}
```
public static String getName(int exportHeadersFootersMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| exportHeadersFootersMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int exportHeadersFootersMode) {#toString-int}
```
public static String toString(int exportHeadersFootersMode)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| exportHeadersFootersMode | int |  |

**Returns:**
java.lang.String
