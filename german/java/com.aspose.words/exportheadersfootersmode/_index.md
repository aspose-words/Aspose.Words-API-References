---
title: "ExportHeadersFootersMode"
linktitle: "ExportHeadersFootersMode"
second_title: "Aspose.Words für Java"
description: "Gibt an, wie Kopf- und Fußzeilen in HTML, MHTML oder EPUB in Java exportiert werden."
type: docs
weight: 192
url: /de/java/com.aspose.words/exportheadersfootersmode/
---

**Inheritance:**
java.lang.Object
```
public class ExportHeadersFootersMode
```

Legt fest, wie Kopf- und Fußzeilen nach HTML, MHTML oder EPUB exportiert werden.

 **Examples:** 

Zeigt, wie Kopf‑/Fußzeilen beim Speichern eines Dokuments als HTML weggelassen werden.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [FIRST_PAGE_HEADER_FOOTER_PER_SECTION](#FIRST-PAGE-HEADER-FOOTER-PER-SECTION) | Kopf‑ und Fußzeile der ersten Seite werden zu Beginn und am Ende jedes Abschnitts exportiert. |
| [FIRST_SECTION_HEADER_LAST_SECTION_FOOTER](#FIRST-SECTION-HEADER-LAST-SECTION-FOOTER) | Die primäre Kopfzeile des ersten Abschnitts wird zu Beginn des Dokuments exportiert und die primäre Fußzeile am Ende. |
| [NONE](#NONE) | Kopf‑ und Fußzeilen werden nicht exportiert. |
| [PER_SECTION](#PER-SECTION) | Primäre Kopf‑ und Fußzeilen werden zu Beginn und am Ende jedes Abschnitts exportiert. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String exportHeadersFootersModeName)](#fromName-java.lang.String) |  |
| [getName(int exportHeadersFootersMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int exportHeadersFootersMode)](#toString-int) |  |
### FIRST_PAGE_HEADER_FOOTER_PER_SECTION {#FIRST-PAGE-HEADER-FOOTER-PER-SECTION}
```
public static int FIRST_PAGE_HEADER_FOOTER_PER_SECTION
```


Kopf‑ und Fußzeile der ersten Seite werden zu Beginn und am Ende jedes Abschnitts exportiert.

### FIRST_SECTION_HEADER_LAST_SECTION_FOOTER {#FIRST-SECTION-HEADER-LAST-SECTION-FOOTER}
```
public static int FIRST_SECTION_HEADER_LAST_SECTION_FOOTER
```


Die primäre Kopfzeile des ersten Abschnitts wird zu Beginn des Dokuments exportiert und die primäre Fußzeile am Ende.

### NONE {#NONE}
```
public static int NONE
```


Kopf‑ und Fußzeilen werden nicht exportiert.

### PER_SECTION {#PER-SECTION}
```
public static int PER_SECTION
```


Primäre Kopf‑ und Fußzeilen werden zu Beginn und am Ende jedes Abschnitts exportiert.

### length {#length}
```
public static int length
```


### fromName(String exportHeadersFootersModeName) {#fromName-java.lang.String}
```
public static int fromName(String exportHeadersFootersModeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| exportHeadersFootersModeName | java.lang.String |  |

**Returns:**
int
### getName(int exportHeadersFootersMode) {#getName-int}
```
public static String getName(int exportHeadersFootersMode)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| exportHeadersFootersMode | int |  |

**Returns:**
java.lang.String
