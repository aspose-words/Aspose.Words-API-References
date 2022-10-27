---
title: ExportHeadersFootersMode
second_title: Aspose.Words for Java API Reference
description: Specifies how headers and footers are exported to HTML MHTML or EPUB.
type: docs
weight: 149
url: /java/com.aspose.words/exportheadersfootersmode/
---

**Inheritance:**
java.lang.Object
```
public class ExportHeadersFootersMode
```

Specifies how headers and footers are exported to HTML, MHTML or EPUB.
## Fields

| Field | Description |
| --- | --- |
| [NONE](#NONE) | Headers and footers are not exported. |
| [PER_SECTION](#PER-SECTION) | Primary headers and footers are exported at the beginning and the end of each section. |
| [FIRST_SECTION_HEADER_LAST_SECTION_FOOTER](#FIRST-SECTION-HEADER-LAST-SECTION-FOOTER) | Primary header of the first section is exported at the beginning of the document and primary footer is at the end. |
| [FIRST_PAGE_HEADER_FOOTER_PER_SECTION](#FIRST-PAGE-HEADER-FOOTER-PER-SECTION) | First page header and footer are exported at the beginning and the end of each section. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int exportHeadersFootersMode)](#getName-int-) |  |
| [toString(int exportHeadersFootersMode)](#toString-int-) |  |
| [fromName(String exportHeadersFootersModeName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
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

### FIRST_SECTION_HEADER_LAST_SECTION_FOOTER {#FIRST-SECTION-HEADER-LAST-SECTION-FOOTER}
```
public static int FIRST_SECTION_HEADER_LAST_SECTION_FOOTER
```


Primary header of the first section is exported at the beginning of the document and primary footer is at the end.

### FIRST_PAGE_HEADER_FOOTER_PER_SECTION {#FIRST-PAGE-HEADER-FOOTER-PER-SECTION}
```
public static int FIRST_PAGE_HEADER_FOOTER_PER_SECTION
```


First page header and footer are exported at the beginning and the end of each section.

### length {#length}
```
public static int length
```


### getName(int exportHeadersFootersMode) {#getName-int-}
```
public static String getName(int exportHeadersFootersMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| exportHeadersFootersMode | int |  |

**Returns:**
java.lang.String
### toString(int exportHeadersFootersMode) {#toString-int-}
```
public static String toString(int exportHeadersFootersMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| exportHeadersFootersMode | int |  |

**Returns:**
java.lang.String
### fromName(String exportHeadersFootersModeName) {#fromName-java.lang.String-}
```
public static int fromName(String exportHeadersFootersModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| exportHeadersFootersModeName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
