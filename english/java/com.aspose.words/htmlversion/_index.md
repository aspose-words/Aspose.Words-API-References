---
title: HtmlVersion
second_title: Aspose.Words for Java API Reference
description: A utility class providing constants.
type: docs
weight: 332
url: /java/com.aspose.words/htmlversion/
---

**Inheritance:**
java.lang.Object
```
public class HtmlVersion
```

A utility class providing constants. Indicates the version of HTML is used when saving the document to [SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML) and [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML) formats.
## Fields

| Field | Description |
| --- | --- |
| [XHTML](#XHTML) | Saves the document in compliance with the XHTML 1.0 Transitional standard. |
| [HTML_5](#HTML-5) | Saves the document in compliance with the HTML 5 standard. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int htmlVersion)](#getName-int-) |  |
| [toString(int htmlVersion)](#toString-int-) |  |
| [fromName(String htmlVersionName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### XHTML {#XHTML}
```
public static int XHTML
```


Saves the document in compliance with the XHTML 1.0 Transitional standard.

Aspose.Words aims to output XHTML according to the XHTML 1.0 Transitional standard, but the output will not always validate against the DTD. Some structures inside a Microsoft Word document are hard or impossible to map to a document that will validate against the XHTML schema. For example, XHTML does not allow nested lists (UL cannot be nested inside another UL element), but in Microsoft Word document multilevel lists occur quite often.

### HTML_5 {#HTML-5}
```
public static int HTML_5
```


Saves the document in compliance with the HTML 5 standard.

### length {#length}
```
public static int length
```


### getName(int htmlVersion) {#getName-int-}
```
public static String getName(int htmlVersion)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| htmlVersion | int |  |

**Returns:**
java.lang.String
### toString(int htmlVersion) {#toString-int-}
```
public static String toString(int htmlVersion)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| htmlVersion | int |  |

**Returns:**
java.lang.String
### fromName(String htmlVersionName) {#fromName-java.lang.String-}
```
public static int fromName(String htmlVersionName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| htmlVersionName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
