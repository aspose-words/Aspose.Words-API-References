---
title: PdfPageMode
linktitle: PdfPageMode
second_title: Aspose.Words for Java
description: Specifies how the PDF document should be displayed when opened in the PDF reader in Java.
type: docs
weight: 476
url: /java/com.aspose.words/pdfpagemode/
---

**Inheritance:**
java.lang.Object
```
public class PdfPageMode
```

Specifies how the PDF document should be displayed when opened in the PDF reader.
## Fields

| Field | Description |
| --- | --- |
| [FULL_SCREEN](#FULL-SCREEN) | Full-screen mode, with no menu bar, window controls, or any other window visible. |
| [USE_ATTACHMENTS](#USE-ATTACHMENTS) | Attachments panel is visible. |
| [USE_NONE](#USE-NONE) | Neither document outline nor thumbnail images are visible. |
| [USE_OC](#USE-OC) | Optional content group panel is visible. |
| [USE_OUTLINES](#USE-OUTLINES) | Document outline is visible. |
| [USE_THUMBS](#USE-THUMBS) | Thumbnail images are visible. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String pdfPageModeName)](#fromName-java.lang.String) |  |
| [getName(int pdfPageMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int pdfPageMode)](#toString-int) |  |
### FULL_SCREEN {#FULL-SCREEN}
```
public static int FULL_SCREEN
```


Full-screen mode, with no menu bar, window controls, or any other window visible.

### USE_ATTACHMENTS {#USE-ATTACHMENTS}
```
public static int USE_ATTACHMENTS
```


Attachments panel is visible.

 **Remarks:** 

Not supported in the following PDF versions: [PdfCompliance.PDF\_A\_1\_A](../../com.aspose.words/pdfcompliance/\#PDF-A-1-A), [PdfCompliance.PDF\_A\_1\_B](../../com.aspose.words/pdfcompliance/\#PDF-A-1-B).

### USE_NONE {#USE-NONE}
```
public static int USE_NONE
```


Neither document outline nor thumbnail images are visible.

### USE_OC {#USE-OC}
```
public static int USE_OC
```


Optional content group panel is visible.

 **Remarks:** 

Not supported in the following PDF versions: [PdfCompliance.PDF\_A\_1\_A](../../com.aspose.words/pdfcompliance/\#PDF-A-1-A), [PdfCompliance.PDF\_A\_1\_B](../../com.aspose.words/pdfcompliance/\#PDF-A-1-B).

### USE_OUTLINES {#USE-OUTLINES}
```
public static int USE_OUTLINES
```


Document outline is visible. Note that if there're no outlines in the PDF document then outline navigation pane will not be visible anyway.

### USE_THUMBS {#USE-THUMBS}
```
public static int USE_THUMBS
```


Thumbnail images are visible.

### length {#length}
```
public static int length
```


### fromName(String pdfPageModeName) {#fromName-java.lang.String}
```
public static int fromName(String pdfPageModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfPageModeName | java.lang.String |  |

**Returns:**
int
### getName(int pdfPageMode) {#getName-int}
```
public static String getName(int pdfPageMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfPageMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int pdfPageMode) {#toString-int}
```
public static String toString(int pdfPageMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfPageMode | int |  |

**Returns:**
java.lang.String
