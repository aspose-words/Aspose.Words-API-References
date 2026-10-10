---
title: "ExportHeadersFootersMode"
linktitle: "ExportHeadersFootersMode"
second_title: "Aspose.Words Java için"
description: "Java'da üstbilgi ve altbilgilerin HTML, MHTML veya EPUB olarak nasıl dışa aktarıldığını belirtir."
type: docs
weight: 192
url: /tr/java/com.aspose.words/exportheadersfootersmode/
---

**Inheritance:**
java.lang.Object
```
public class ExportHeadersFootersMode
```

Üstbilgi ve altbilgilerin HTML, MHTML veya EPUB formatına nasıl dışa aktarıldığını belirtir.

 **Examples:** 

Bir belgeyi HTML olarak kaydederken üstbilgi/altbilgilerin nasıl atlanacağını gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [FIRST_PAGE_HEADER_FOOTER_PER_SECTION](#FIRST-PAGE-HEADER-FOOTER-PER-SECTION) | İlk sayfa üstbilgisi ve altbilgisi, her bölümün başında ve sonunda dışa aktarılır. |
| [FIRST_SECTION_HEADER_LAST_SECTION_FOOTER](#FIRST-SECTION-HEADER-LAST-SECTION-FOOTER) | İlk bölümün birincil üstbilgisi belgenin başında, birincil altbilgisi ise sonunda dışa aktarılır. |
| [NONE](#NONE) | Üstbilgi ve altbilgiler dışa aktarılmaz. |
| [PER_SECTION](#PER-SECTION) | Birincil üstbilgi ve altbilgiler her bölümün başında ve sonunda dışa aktarılır. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String exportHeadersFootersModeName)](#fromName-java.lang.String) |  |
| [getName(int exportHeadersFootersMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int exportHeadersFootersMode)](#toString-int) |  |
### FIRST_PAGE_HEADER_FOOTER_PER_SECTION {#FIRST-PAGE-HEADER-FOOTER-PER-SECTION}
```
public static int FIRST_PAGE_HEADER_FOOTER_PER_SECTION
```


İlk sayfa üstbilgisi ve altbilgisi, her bölümün başında ve sonunda dışa aktarılır.

### FIRST_SECTION_HEADER_LAST_SECTION_FOOTER {#FIRST-SECTION-HEADER-LAST-SECTION-FOOTER}
```
public static int FIRST_SECTION_HEADER_LAST_SECTION_FOOTER
```


İlk bölümün birincil üstbilgisi belgenin başında, birincil altbilgisi ise sonunda dışa aktarılır.

### NONE {#NONE}
```
public static int NONE
```


Üstbilgi ve altbilgiler dışa aktarılmaz.

### PER_SECTION {#PER-SECTION}
```
public static int PER_SECTION
```


Birincil üstbilgi ve altbilgiler her bölümün başında ve sonunda dışa aktarılır.

### length {#length}
```
public static int length
```


### fromName(String exportHeadersFootersModeName) {#fromName-java.lang.String}
```
public static int fromName(String exportHeadersFootersModeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| exportHeadersFootersModeName | java.lang.String |  |

**Returns:**
int
### getName(int exportHeadersFootersMode) {#getName-int}
```
public static String getName(int exportHeadersFootersMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| exportHeadersFootersMode | int |  |

**Returns:**
java.lang.String
