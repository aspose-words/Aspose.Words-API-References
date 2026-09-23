---
title: "ExportHeadersFootersMode"
linktitle: "ExportHeadersFootersMode"
second_title: "Aspose.Words per Java"
description: "Specifica come intestazioni e piè di pagina vengono esportati in HTML, MHTML o EPUB in Java."
type: docs
weight: 192
url: /it/java/com.aspose.words/exportheadersfootersmode/
---

**Inheritance:**
java.lang.Object
```
public class ExportHeadersFootersMode
```

Specifica come intestazioni e piè di pagina vengono esportati in HTML, MHTML o EPUB.

 **Examples:** 

Mostra come omettere intestazioni/piè di pagina durante il salvataggio di un documento in HTML.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [FIRST_PAGE_HEADER_FOOTER_PER_SECTION](#FIRST-PAGE-HEADER-FOOTER-PER-SECTION) | L'intestazione e il piè di pagina della prima pagina vengono esportati all'inizio e alla fine di ogni sezione. |
| [FIRST_SECTION_HEADER_LAST_SECTION_FOOTER](#FIRST-SECTION-HEADER-LAST-SECTION-FOOTER) | L'intestazione principale della prima sezione viene esportata all'inizio del documento e il piè di pagina principale alla fine. |
| [NONE](#NONE) | Intestazioni e piè di pagina non vengono esportati. |
| [PER_SECTION](#PER-SECTION) | Intestazioni e piè di pagina principali vengono esportati all'inizio e alla fine di ogni sezione. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String exportHeadersFootersModeName)](#fromName-java.lang.String) |  |
| [getName(int exportHeadersFootersMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int exportHeadersFootersMode)](#toString-int) |  |
### FIRST_PAGE_HEADER_FOOTER_PER_SECTION {#FIRST-PAGE-HEADER-FOOTER-PER-SECTION}
```
public static int FIRST_PAGE_HEADER_FOOTER_PER_SECTION
```


L'intestazione e il piè di pagina della prima pagina vengono esportati all'inizio e alla fine di ogni sezione.

### FIRST_SECTION_HEADER_LAST_SECTION_FOOTER {#FIRST-SECTION-HEADER-LAST-SECTION-FOOTER}
```
public static int FIRST_SECTION_HEADER_LAST_SECTION_FOOTER
```


L'intestazione principale della prima sezione viene esportata all'inizio del documento e il piè di pagina principale alla fine.

### NONE {#NONE}
```
public static int NONE
```


Intestazioni e piè di pagina non vengono esportati.

### PER_SECTION {#PER-SECTION}
```
public static int PER_SECTION
```


Intestazioni e piè di pagina principali vengono esportati all'inizio e alla fine di ogni sezione.

### length {#length}
```
public static int length
```


### fromName(String exportHeadersFootersModeName) {#fromName-java.lang.String}
```
public static int fromName(String exportHeadersFootersModeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| exportHeadersFootersModeName | java.lang.String |  |

**Returns:**
int
### getName(int exportHeadersFootersMode) {#getName-int}
```
public static String getName(int exportHeadersFootersMode)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| exportHeadersFootersMode | int |  |

**Returns:**
java.lang.String
