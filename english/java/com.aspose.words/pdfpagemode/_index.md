---
title: PdfPageMode
second_title: Aspose.Words for Java API Reference
description: A utility class providing constants.
type: docs
weight: 459
url: /java/com.aspose.words/pdfpagemode/
---

**Inheritance:**
java.lang.Object
```
public class PdfPageMode
```

A utility class providing constants. Specifies how the PDF document should be displayed when opened in the PDF reader.
## Fields

| Field | Description |
| --- | --- |
| [USE_NONE](#USE-NONE) | Neither document outline nor thumbnail images are visible. |
| [USE_OUTLINES](#USE-OUTLINES) | Document outline is visible. |
| [USE_THUMBS](#USE-THUMBS) | Thumbnail images are visible. |
| [FULL_SCREEN](#FULL-SCREEN) | Full-screen mode, with no menu bar, window controls, or any other window visible. |
| [USE_OC](#USE-OC) | Optional content group panel is visible. |
| [USE_ATTACHMENTS](#USE-ATTACHMENTS) | Attachments panel is visible. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int pdfPageMode)](#getName-int-) |  |
| [toString(int pdfPageMode)](#toString-int-) |  |
| [fromName(String pdfPageModeName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### USE_NONE {#USE-NONE}
```
public static int USE_NONE
```


Neither document outline nor thumbnail images are visible.

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

### FULL_SCREEN {#FULL-SCREEN}
```
public static int FULL_SCREEN
```


Full-screen mode, with no menu bar, window controls, or any other window visible.

### USE_OC {#USE-OC}
```
public static int USE_OC
```


Optional content group panel is visible. Not supported in the following PDF versions: [PdfCompliance.PDF\_A\_1\_A](../../com.aspose.words/pdfcompliance\#PDF-A-1-A), [PdfCompliance.PDF\_A\_1\_B](../../com.aspose.words/pdfcompliance\#PDF-A-1-B).

### USE_ATTACHMENTS {#USE-ATTACHMENTS}
```
public static int USE_ATTACHMENTS
```


Attachments panel is visible. Not supported in the following PDF versions: [PdfCompliance.PDF\_A\_1\_A](../../com.aspose.words/pdfcompliance\#PDF-A-1-A), [PdfCompliance.PDF\_A\_1\_B](../../com.aspose.words/pdfcompliance\#PDF-A-1-B).

### length {#length}
```
public static int length
```


### getName(int pdfPageMode) {#getName-int-}
```
public static String getName(int pdfPageMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfPageMode | int |  |

**Returns:**
java.lang.String
### toString(int pdfPageMode) {#toString-int-}
```
public static String toString(int pdfPageMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfPageMode | int |  |

**Returns:**
java.lang.String
### fromName(String pdfPageModeName) {#fromName-java.lang.String-}
```
public static int fromName(String pdfPageModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfPageModeName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
