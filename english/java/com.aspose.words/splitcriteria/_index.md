---
title: SplitCriteria
linktitle: SplitCriteria
second_title: Aspose.Words for Java
description: Specifies how the document is split into parts in Java.
type: docs
weight: 620
url: /java/com.aspose.words/splitcriteria/
---

**Inheritance:**
java.lang.Object
```
public class SplitCriteria
```

Specifies how the document is split into parts.

 **Examples:** 

Shows how to split document by pages.

```

 String doc = getMyDir() + "Big document.docx";

 SplitOptions options = new SplitOptions();
 options.setSplitCriteria(SplitCriteria.PAGE);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.1.docx", options);
 Splitter.split(doc, getArtifactsDir() + "LowCode.SplitDocument.2.docx", SaveFormat.DOCX, options);
 
```
## Fields

| Field | Description |
| --- | --- |
| [PAGE](#PAGE) | Specifies that the document is split into pages. |
| [SECTION_BREAK](#SECTION-BREAK) | Specifies that the document is split into parts at a section break of any type. |
| [STYLE](#STYLE) | Specifies that the document is split into parts at a paragraph formatted using the style specified in [SplitOptions.getSplitStyle()](../../com.aspose.words/splitoptions/\#getSplitStyle) / [SplitOptions.setSplitStyle(java.lang.String)](../../com.aspose.words/splitoptions/\#setSplitStyle-java.lang.String). |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String splitCriteriaName)](#fromName-java.lang.String) |  |
| [getName(int splitCriteria)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int splitCriteria)](#toString-int) |  |
### PAGE {#PAGE}
```
public static int PAGE
```


Specifies that the document is split into pages.

### SECTION_BREAK {#SECTION-BREAK}
```
public static int SECTION_BREAK
```


Specifies that the document is split into parts at a section break of any type.

### STYLE {#STYLE}
```
public static int STYLE
```


Specifies that the document is split into parts at a paragraph formatted using the style specified in [SplitOptions.getSplitStyle()](../../com.aspose.words/splitoptions/\#getSplitStyle) / [SplitOptions.setSplitStyle(java.lang.String)](../../com.aspose.words/splitoptions/\#setSplitStyle-java.lang.String).

### length {#length}
```
public static int length
```


### fromName(String splitCriteriaName) {#fromName-java.lang.String}
```
public static int fromName(String splitCriteriaName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| splitCriteriaName | java.lang.String |  |

**Returns:**
int
### getName(int splitCriteria) {#getName-int}
```
public static String getName(int splitCriteria)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| splitCriteria | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int splitCriteria) {#toString-int}
```
public static String toString(int splitCriteria)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| splitCriteria | int |  |

**Returns:**
java.lang.String
