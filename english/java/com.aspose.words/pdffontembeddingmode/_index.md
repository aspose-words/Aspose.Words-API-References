---
title: PdfFontEmbeddingMode
second_title: Aspose.Words for Java API Reference
description: A utility class providing constants.
type: docs
weight: 455
url: /java/com.aspose.words/pdffontembeddingmode/
---

**Inheritance:**
java.lang.Object
```
public class PdfFontEmbeddingMode
```

A utility class providing constants. Specifies how Aspose.Words should embed fonts.
## Fields

| Field | Description |
| --- | --- |
| [EMBED_ALL](#EMBED-ALL) | Aspose.Words embeds all fonts. |
| [EMBED_NONSTANDARD](#EMBED-NONSTANDARD) | Aspose.Words embeds all fonts excepting standard Windows fonts Arial and Times New Roman. |
| [EMBED_NONE](#EMBED-NONE) | Aspose.Words do not embed any fonts. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int pdfFontEmbeddingMode)](#getName-int-) |  |
| [toString(int pdfFontEmbeddingMode)](#toString-int-) |  |
| [fromName(String pdfFontEmbeddingModeName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### EMBED_ALL {#EMBED-ALL}
```
public static int EMBED_ALL
```


Aspose.Words embeds all fonts.

### EMBED_NONSTANDARD {#EMBED-NONSTANDARD}
```
public static int EMBED_NONSTANDARD
```


Aspose.Words embeds all fonts excepting standard Windows fonts Arial and Times New Roman. Only Arial and Times New Roman fonts are affected in this mode because MS Word doesn't embed only these fonts when saving document to PDF.

### EMBED_NONE {#EMBED-NONE}
```
public static int EMBED_NONE
```


Aspose.Words do not embed any fonts.

### length {#length}
```
public static int length
```


### getName(int pdfFontEmbeddingMode) {#getName-int-}
```
public static String getName(int pdfFontEmbeddingMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfFontEmbeddingMode | int |  |

**Returns:**
java.lang.String
### toString(int pdfFontEmbeddingMode) {#toString-int-}
```
public static String toString(int pdfFontEmbeddingMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfFontEmbeddingMode | int |  |

**Returns:**
java.lang.String
### fromName(String pdfFontEmbeddingModeName) {#fromName-java.lang.String-}
```
public static int fromName(String pdfFontEmbeddingModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| pdfFontEmbeddingModeName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
