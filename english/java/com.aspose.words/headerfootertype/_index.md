---
title: HeaderFooterType
linktitle: HeaderFooterType
second_title: Aspose.Words for Java
description: Identifies the type of header or footer found in a Word file in Java.
type: docs
weight: 331
url: /java/com.aspose.words/headerfootertype/
---

**Inheritance:**
java.lang.Object
```
public class HeaderFooterType
```

Identifies the type of header or footer found in a Word file.  This is a per section header/footer. Do not renumber as the value of the enum used as an index into plcfhdd.

 **Examples:** 

Shows how to create headers and footers in a document using DocumentBuilder.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Specify that we want different headers and footers for first, even and odd pages.
 builder.getPageSetup().setDifferentFirstPageHeaderFooter(true);
 builder.getPageSetup().setOddAndEvenPagesHeaderFooter(true);

 // Create the headers, then add three pages to the document to display each header type.
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_FIRST);
 builder.write("Header for the first page");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_EVEN);
 builder.write("Header for even pages");
 builder.moveToHeaderFooter(HeaderFooterType.HEADER_PRIMARY);
 builder.write("Header for all other pages");

 builder.moveToSection(0);
 builder.writeln("Page1");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page2");
 builder.insertBreak(BreakType.PAGE_BREAK);
 builder.writeln("Page3");

 doc.save(getArtifactsDir() + "DocumentBuilder.HeadersAndFooters.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [FOOTER_EVEN](#FOOTER-EVEN) | Footer for even numbered pages. |
| [FOOTER_FIRST](#FOOTER-FIRST) | Footer for the first page of the section. |
| [FOOTER_PRIMARY](#FOOTER-PRIMARY) | Primary footer, also used for odd numbered pages. |
| [HEADER_EVEN](#HEADER-EVEN) | Header for even numbered pages. |
| [HEADER_FIRST](#HEADER-FIRST) | Header for the first page of the section. |
| [HEADER_PRIMARY](#HEADER-PRIMARY) | Primary header, also used for odd numbered pages. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String headerFooterTypeName)](#fromName-java.lang.String) |  |
| [getName(int headerFooterType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int headerFooterType)](#toString-int) |  |
### FOOTER_EVEN {#FOOTER-EVEN}
```
public static int FOOTER_EVEN
```


Footer for even numbered pages.

### FOOTER_FIRST {#FOOTER-FIRST}
```
public static int FOOTER_FIRST
```


Footer for the first page of the section.

### FOOTER_PRIMARY {#FOOTER-PRIMARY}
```
public static int FOOTER_PRIMARY
```


Primary footer, also used for odd numbered pages.

### HEADER_EVEN {#HEADER-EVEN}
```
public static int HEADER_EVEN
```


Header for even numbered pages.

### HEADER_FIRST {#HEADER-FIRST}
```
public static int HEADER_FIRST
```


Header for the first page of the section.

### HEADER_PRIMARY {#HEADER-PRIMARY}
```
public static int HEADER_PRIMARY
```


Primary header, also used for odd numbered pages.

### length {#length}
```
public static int length
```


### fromName(String headerFooterTypeName) {#fromName-java.lang.String}
```
public static int fromName(String headerFooterTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| headerFooterTypeName | java.lang.String |  |

**Returns:**
int
### getName(int headerFooterType) {#getName-int}
```
public static String getName(int headerFooterType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| headerFooterType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int headerFooterType) {#toString-int}
```
public static String toString(int headerFooterType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| headerFooterType | int |  |

**Returns:**
java.lang.String
