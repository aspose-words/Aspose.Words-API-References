---
title: ExportHeadersFootersMode
linktitle: ExportHeadersFootersMode
second_title: Aspose.Words for Java
description: Specifies how headers and footers are exported to HTML MHTML or EPUB in Java.
type: docs
weight: 160
url: /java/com.aspose.words/exportheadersfootersmode/
---

**Inheritance:**
java.lang.Object
```
public class ExportHeadersFootersMode
```

Specifies how headers and footers are exported to HTML, MHTML or EPUB.

 **Examples:** 

Shows how to omit headers/footers when saving a document to HTML.

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
## Fields

| Field | Description |
| --- | --- |
| [FIRST_PAGE_HEADER_FOOTER_PER_SECTION](#FIRST-PAGE-HEADER-FOOTER-PER-SECTION) | First page header and footer are exported at the beginning and the end of each section. |
| [FIRST_SECTION_HEADER_LAST_SECTION_FOOTER](#FIRST-SECTION-HEADER-LAST-SECTION-FOOTER) | Primary header of the first section is exported at the beginning of the document and primary footer is at the end. |
| [NONE](#NONE) | Headers and footers are not exported. |
| [PER_SECTION](#PER-SECTION) | Primary headers and footers are exported at the beginning and the end of each section. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String exportHeadersFootersModeName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int exportHeadersFootersMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int exportHeadersFootersMode)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### FIRST_PAGE_HEADER_FOOTER_PER_SECTION {#FIRST-PAGE-HEADER-FOOTER-PER-SECTION}
```
public static int FIRST_PAGE_HEADER_FOOTER_PER_SECTION
```


First page header and footer are exported at the beginning and the end of each section.

### FIRST_SECTION_HEADER_LAST_SECTION_FOOTER {#FIRST-SECTION-HEADER-LAST-SECTION-FOOTER}
```
public static int FIRST_SECTION_HEADER_LAST_SECTION_FOOTER
```


Primary header of the first section is exported at the beginning of the document and primary footer is at the end.

### NONE {#NONE}
```
public static int NONE
```


Headers and footers are not exported.

### PER_SECTION {#PER-SECTION}
```
public static int PER_SECTION
```


Primary headers and footers are exported at the beginning and the end of each section.

### length {#length}
```
public static int length
```


### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### fromName(String exportHeadersFootersModeName) {#fromName-java.lang.String}
```
public static int fromName(String exportHeadersFootersModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| exportHeadersFootersModeName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int exportHeadersFootersMode) {#getName-int}
```
public static String getName(int exportHeadersFootersMode)
```




**Parameters:**
| Parameter | Type | Description |
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
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### toString(int exportHeadersFootersMode) {#toString-int}
```
public static String toString(int exportHeadersFootersMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| exportHeadersFootersMode | int |  |

**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

