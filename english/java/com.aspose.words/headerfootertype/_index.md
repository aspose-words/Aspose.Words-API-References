---
title: HeaderFooterType
second_title: Aspose.Words for Java API Reference
description: A utility class providing constants.
type: docs
weight: 318
url: /java/com.aspose.words/headerfootertype/
---

**Inheritance:**
java.lang.Object
```
public class HeaderFooterType
```

A utility class providing constants. Identifies the type of header or footer found in a Word file.  This is a per section header/footer. Do not renumber as the value of the enum used as an index into plcfhdd.
## Fields

| Field | Description |
| --- | --- |
| [HEADER_EVEN](#HEADER-EVEN) | Header for even numbered pages. |
| [HEADER_PRIMARY](#HEADER-PRIMARY) | Primary header, also used for odd numbered pages. |
| [FOOTER_EVEN](#FOOTER-EVEN) | Footer for even numbered pages. |
| [FOOTER_PRIMARY](#FOOTER-PRIMARY) | Primary footer, also used for odd numbered pages. |
| [HEADER_FIRST](#HEADER-FIRST) | Header for the first page of the section. |
| [FOOTER_FIRST](#FOOTER-FIRST) | Footer for the first page of the section. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int headerFooterType)](#getName-int-) |  |
| [toString(int headerFooterType)](#toString-int-) |  |
| [fromName(String headerFooterTypeName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### HEADER_EVEN {#HEADER-EVEN}
```
public static int HEADER_EVEN
```


Header for even numbered pages.

### HEADER_PRIMARY {#HEADER-PRIMARY}
```
public static int HEADER_PRIMARY
```


Primary header, also used for odd numbered pages.

### FOOTER_EVEN {#FOOTER-EVEN}
```
public static int FOOTER_EVEN
```


Footer for even numbered pages.

### FOOTER_PRIMARY {#FOOTER-PRIMARY}
```
public static int FOOTER_PRIMARY
```


Primary footer, also used for odd numbered pages.

### HEADER_FIRST {#HEADER-FIRST}
```
public static int HEADER_FIRST
```


Header for the first page of the section.

### FOOTER_FIRST {#FOOTER-FIRST}
```
public static int FOOTER_FIRST
```


Footer for the first page of the section.

### length {#length}
```
public static int length
```


### getName(int headerFooterType) {#getName-int-}
```
public static String getName(int headerFooterType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| headerFooterType | int |  |

**Returns:**
java.lang.String
### toString(int headerFooterType) {#toString-int-}
```
public static String toString(int headerFooterType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| headerFooterType | int |  |

**Returns:**
java.lang.String
### fromName(String headerFooterTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String headerFooterTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| headerFooterTypeName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
