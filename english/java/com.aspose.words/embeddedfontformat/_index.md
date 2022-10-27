---
title: EmbeddedFontFormat
second_title: Aspose.Words for Java API Reference
description: Specifies format of particular embedded font inside  object.
type: docs
weight: 141
url: /java/com.aspose.words/embeddedfontformat/
---

**Inheritance:**
java.lang.Object
```
public class EmbeddedFontFormat
```

Specifies format of particular embedded font inside [FontInfo](../../com.aspose.words/fontinfo) object.

When saving a document to a file, only embedded fonts of corresponding format are written down.
## Fields

| Field | Description |
| --- | --- |
| [EMBEDDED_OPEN_TYPE](#EMBEDDED-OPEN-TYPE) | Specifies Embedded OpenType (EOT) File Format. |
| [OPEN_TYPE](#OPEN-TYPE) | Specifies font, embedded as plain copy of OpenType (TrueType) font file. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int embeddedFontFormat)](#getName-int-) |  |
| [toString(int embeddedFontFormat)](#toString-int-) |  |
| [fromName(String embeddedFontFormatName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### EMBEDDED_OPEN_TYPE {#EMBEDDED-OPEN-TYPE}
```
public static int EMBEDDED_OPEN_TYPE
```


Specifies Embedded OpenType (EOT) File Format.

This format of embedded fonts used in DOC files.

See http://www.w3.org/Submission/EOT for description of the format.

### OPEN_TYPE {#OPEN-TYPE}
```
public static int OPEN_TYPE
```


Specifies font, embedded as plain copy of OpenType (TrueType) font file.

This format of embedded fonts used in Open Office XML format, including DOCX files.

### length {#length}
```
public static int length
```


### getName(int embeddedFontFormat) {#getName-int-}
```
public static String getName(int embeddedFontFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| embeddedFontFormat | int |  |

**Returns:**
java.lang.String
### toString(int embeddedFontFormat) {#toString-int-}
```
public static String toString(int embeddedFontFormat)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| embeddedFontFormat | int |  |

**Returns:**
java.lang.String
### fromName(String embeddedFontFormatName) {#fromName-java.lang.String-}
```
public static int fromName(String embeddedFontFormatName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| embeddedFontFormatName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
