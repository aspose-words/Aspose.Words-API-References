---
title: WarningType
second_title: Aspose.Words for Java API Reference
description: A utility class providing constants.
type: docs
weight: 607
url: /java/com.aspose.words/warningtype/
---

**Inheritance:**
java.lang.Object
```
public class WarningType
```

A utility class providing constants. Specifies the type of a warning that is issued by Aspose.Words during document loading or saving.
## Fields

| Field | Description |
| --- | --- |
| [DATA_LOSS_CATEGORY](#DATA-LOSS-CATEGORY) | Some text/char/image or other data will be missing from either the document tree following load, or from the created document following save. |
| [DATA_LOSS](#DATA-LOSS) | Generic data loss, no specific code. |
| [MAJOR_FORMATTING_LOSS_CATEGORY](#MAJOR-FORMATTING-LOSS-CATEGORY) | The resulting document or a particular location in it might look substantially different compared to the original document. |
| [MAJOR_FORMATTING_LOSS](#MAJOR-FORMATTING-LOSS) | Generic major formatting loss, no specific code. |
| [MINOR_FORMATTING_LOSS_CATEGORY](#MINOR-FORMATTING-LOSS-CATEGORY) | The resulting document or a particular location in it might look somewhat different compared to the original document. |
| [MINOR_FORMATTING_LOSS](#MINOR-FORMATTING-LOSS) | Generic minor formatting loss, no specific code. |
| [FONT_SUBSTITUTION](#FONT-SUBSTITUTION) | Font has been substituted. |
| [FONT_EMBEDDING](#FONT-EMBEDDING) | Loss of embedded font information during document saving. |
| [UNEXPECTED_CONTENT_CATEGORY](#UNEXPECTED-CONTENT-CATEGORY) | Some content in the source document could not be recognized (i.e. |
| [UNEXPECTED_CONTENT](#UNEXPECTED-CONTENT) | Generic unexpected content, no specific code. |
| [HINT](#HINT) | Advises of a potential problem or suggests an improvement. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int warningType)](#getName-int-) |  |
| [getNames(int warningType)](#getNames-int-) |  |
| [toString(int warningType)](#toString-int-) |  |
| [toStringSet(int attr)](#toStringSet-int-) |  |
| [fromName(String warningTypeName)](#fromName-java.lang.String-) |  |
| [fromNames(Set warningTypeNames)](#fromNames-java.util.Set-) |  |
| [getValues()](#getValues--) |  |
### DATA_LOSS_CATEGORY {#DATA-LOSS-CATEGORY}
```
public static int DATA_LOSS_CATEGORY
```


Some text/char/image or other data will be missing from either the document tree following load, or from the created document following save.

### DATA_LOSS {#DATA-LOSS}
```
public static int DATA_LOSS
```


Generic data loss, no specific code.

### MAJOR_FORMATTING_LOSS_CATEGORY {#MAJOR-FORMATTING-LOSS-CATEGORY}
```
public static int MAJOR_FORMATTING_LOSS_CATEGORY
```


The resulting document or a particular location in it might look substantially different compared to the original document.

### MAJOR_FORMATTING_LOSS {#MAJOR-FORMATTING-LOSS}
```
public static int MAJOR_FORMATTING_LOSS
```


Generic major formatting loss, no specific code.

### MINOR_FORMATTING_LOSS_CATEGORY {#MINOR-FORMATTING-LOSS-CATEGORY}
```
public static int MINOR_FORMATTING_LOSS_CATEGORY
```


The resulting document or a particular location in it might look somewhat different compared to the original document.

### MINOR_FORMATTING_LOSS {#MINOR-FORMATTING-LOSS}
```
public static int MINOR_FORMATTING_LOSS
```


Generic minor formatting loss, no specific code.

### FONT_SUBSTITUTION {#FONT-SUBSTITUTION}
```
public static int FONT_SUBSTITUTION
```


Font has been substituted.

### FONT_EMBEDDING {#FONT-EMBEDDING}
```
public static int FONT_EMBEDDING
```


Loss of embedded font information during document saving.

### UNEXPECTED_CONTENT_CATEGORY {#UNEXPECTED-CONTENT-CATEGORY}
```
public static int UNEXPECTED_CONTENT_CATEGORY
```


Some content in the source document could not be recognized (i.e. is unsupported), this may or may not cause issues or result in data/formatting loss.

### UNEXPECTED_CONTENT {#UNEXPECTED-CONTENT}
```
public static int UNEXPECTED_CONTENT
```


Generic unexpected content, no specific code.

### HINT {#HINT}
```
public static int HINT
```


Advises of a potential problem or suggests an improvement.

### length {#length}
```
public static int length
```


### getName(int warningType) {#getName-int-}
```
public static String getName(int warningType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| warningType | int |  |

**Returns:**
java.lang.String
### getNames(int warningType) {#getNames-int-}
```
public static Set getNames(int warningType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| warningType | int |  |

**Returns:**
java.util.Set
### toString(int warningType) {#toString-int-}
```
public static String toString(int warningType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| warningType | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int-}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| attr | int |  |

**Returns:**
java.lang.String
### fromName(String warningTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String warningTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| warningTypeName | java.lang.String |  |

**Returns:**
int
### fromNames(Set warningTypeNames) {#fromNames-java.util.Set-}
```
public static int fromNames(Set warningTypeNames)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| warningTypeNames | java.util.Set |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
