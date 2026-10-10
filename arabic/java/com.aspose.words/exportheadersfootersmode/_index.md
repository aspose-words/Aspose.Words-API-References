---
title: "ExportHeadersFootersMode"
linktitle: "ExportHeadersFootersMode"
second_title: "Aspose.Words لـ Java"
description: "يحدد كيفية تصدير رؤوس وتذييلات الصفحات إلى HTML أو MHTML أو EPUB في Java."
type: docs
weight: 192
url: /ar/java/com.aspose.words/exportheadersfootersmode/
---

**Inheritance:**
java.lang.Object
```
public class ExportHeadersFootersMode
```

يحدد كيفية تصدير رؤوس وتذييلات الصفحات إلى HTML أو MHTML أو EPUB.

 **Examples:** 

يوضح كيفية حذف الرؤوس/التذييلات عند حفظ المستند إلى HTML.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [FIRST_PAGE_HEADER_FOOTER_PER_SECTION](#FIRST-PAGE-HEADER-FOOTER-PER-SECTION) | يتم تصدير رأس وتذييل الصفحة الأولى في بداية ونهاية كل قسم. |
| [FIRST_SECTION_HEADER_LAST_SECTION_FOOTER](#FIRST-SECTION-HEADER-LAST-SECTION-FOOTER) | يتم تصدير الرأس الأساسي للقسم الأول في بداية المستند والتذييل الأساسي في النهاية. |
| [NONE](#NONE) | لا يتم تصدير الرؤوس والتذييلات. |
| [PER_SECTION](#PER-SECTION) | يتم تصدير الرؤوس والتذييلات الأساسية في بداية ونهاية كل قسم. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String exportHeadersFootersModeName)](#fromName-java.lang.String) |  |
| [getName(int exportHeadersFootersMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int exportHeadersFootersMode)](#toString-int) |  |
### FIRST_PAGE_HEADER_FOOTER_PER_SECTION {#FIRST-PAGE-HEADER-FOOTER-PER-SECTION}
```
public static int FIRST_PAGE_HEADER_FOOTER_PER_SECTION
```


يتم تصدير رأس وتذييل الصفحة الأولى في بداية ونهاية كل قسم.

### FIRST_SECTION_HEADER_LAST_SECTION_FOOTER {#FIRST-SECTION-HEADER-LAST-SECTION-FOOTER}
```
public static int FIRST_SECTION_HEADER_LAST_SECTION_FOOTER
```


يتم تصدير الرأس الأساسي للقسم الأول في بداية المستند والتذييل الأساسي في النهاية.

### NONE {#NONE}
```
public static int NONE
```


لا يتم تصدير الرؤوس والتذييلات.

### PER_SECTION {#PER-SECTION}
```
public static int PER_SECTION
```


يتم تصدير الرؤوس والتذييلات الأساسية في بداية ونهاية كل قسم.

### length {#length}
```
public static int length
```


### fromName(String exportHeadersFootersModeName) {#fromName-java.lang.String}
```
public static int fromName(String exportHeadersFootersModeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| exportHeadersFootersModeName | java.lang.String |  |

**Returns:**
int
### getName(int exportHeadersFootersMode) {#getName-int}
```
public static String getName(int exportHeadersFootersMode)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| exportHeadersFootersMode | int |  |

**Returns:**
java.lang.String
