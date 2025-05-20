---
title: JustificationMode
linktitle: JustificationMode
second_title: Aspose.Words for Java
description: Specifies the character spacing adjustment for a document in Java.
type: docs
weight: 405
url: /java/com.aspose.words/justificationmode/
---

**Inheritance:**
java.lang.Object
```
public class JustificationMode
```

Specifies the character spacing adjustment for a document. The default value is  Expand .

 **Examples:** 

Shows how to manage character spacing control.

```

 Document doc = new Document(getMyDir() + "Document.docx");

 int justificationMode = doc.getJustificationMode();
 if (justificationMode == JustificationMode.EXPAND)
     doc.setJustificationMode(JustificationMode.COMPRESS);

 doc.save(getArtifactsDir() + "Document.SetJustificationMode.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [COMPRESS](#COMPRESS) | Compress character spacing. |
| [COMPRESS_KANA](#COMPRESS-KANA) | Compress, using rules of the kana syllabaries, Hiragana and Katakana. |
| [EXPAND](#EXPAND) | Do not compress character spacing. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String justificationModeName)](#fromName-java.lang.String) |  |
| [getName(int justificationMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int justificationMode)](#toString-int) |  |
### COMPRESS {#COMPRESS}
```
public static int COMPRESS
```


Compress character spacing.

### COMPRESS_KANA {#COMPRESS-KANA}
```
public static int COMPRESS_KANA
```


Compress, using rules of the kana syllabaries, Hiragana and Katakana.

### EXPAND {#EXPAND}
```
public static int EXPAND
```


Do not compress character spacing.

### length {#length}
```
public static int length
```


### fromName(String justificationModeName) {#fromName-java.lang.String}
```
public static int fromName(String justificationModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| justificationModeName | java.lang.String |  |

**Returns:**
int
### getName(int justificationMode) {#getName-int}
```
public static String getName(int justificationMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| justificationMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int justificationMode) {#toString-int}
```
public static String toString(int justificationMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| justificationMode | int |  |

**Returns:**
java.lang.String
