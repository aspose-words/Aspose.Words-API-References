---
title: PdfPageMode
linktitle: PdfPageMode
second_title: Aspose.Words for Java API Reference
description: Specifies how the PDF document should be displayed when opened in the PDF reader in Java.
type: docs
weight: 465
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
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String pdfPageModeName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int pdfPageMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int pdfPageMode)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### FULL_SCREEN {#FULL-SCREEN}
```
public static int FULL_SCREEN
```


Full-screen mode, with no menu bar, window controls, or any other window visible.

### USE_ATTACHMENTS {#USE-ATTACHMENTS}
```
public static int USE_ATTACHMENTS
```


Attachments panel is visible. Not supported in the following PDF versions: [PdfCompliance.PDF\_A\_1\_A](../../com.aspose.words/pdfcompliance/\#PDF-A-1-A), [PdfCompliance.PDF\_A\_1\_B](../../com.aspose.words/pdfcompliance/\#PDF-A-1-B).

### USE_NONE {#USE-NONE}
```
public static int USE_NONE
```


Neither document outline nor thumbnail images are visible.

### USE_OC {#USE-OC}
```
public static int USE_OC
```


Optional content group panel is visible. Not supported in the following PDF versions: [PdfCompliance.PDF\_A\_1\_A](../../com.aspose.words/pdfcompliance/\#PDF-A-1-A), [PdfCompliance.PDF\_A\_1\_B](../../com.aspose.words/pdfcompliance/\#PDF-A-1-B).

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
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
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

