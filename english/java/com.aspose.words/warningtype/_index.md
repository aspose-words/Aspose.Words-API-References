---
title: WarningType
linktitle: WarningType
second_title: Aspose.Words for Java API Reference
description: Specifies the type of a warning that is issued by Aspose.Words during document loading or saving in Java.
type: docs
weight: 613
url: /java/com.aspose.words/warningtype/
---

**Inheritance:**
java.lang.Object
```
public class WarningType
```

Specifies the type of a warning that is issued by Aspose.Words during document loading or saving.
## Fields

| Field | Description |
| --- | --- |
| [DATA_LOSS](#DATA-LOSS) | Generic data loss, no specific code. |
| [DATA_LOSS_CATEGORY](#DATA-LOSS-CATEGORY) | Some text/char/image or other data will be missing from either the document tree following load, or from the created document following save. |
| [FONT_EMBEDDING](#FONT-EMBEDDING) | Loss of embedded font information during document saving. |
| [FONT_SUBSTITUTION](#FONT-SUBSTITUTION) | Font has been substituted. |
| [HINT](#HINT) | Advises of a potential problem or suggests an improvement. |
| [MAJOR_FORMATTING_LOSS](#MAJOR-FORMATTING-LOSS) | Generic major formatting loss, no specific code. |
| [MAJOR_FORMATTING_LOSS_CATEGORY](#MAJOR-FORMATTING-LOSS-CATEGORY) | The resulting document or a particular location in it might look substantially different compared to the original document. |
| [MINOR_FORMATTING_LOSS](#MINOR-FORMATTING-LOSS) | Generic minor formatting loss, no specific code. |
| [MINOR_FORMATTING_LOSS_CATEGORY](#MINOR-FORMATTING-LOSS-CATEGORY) | The resulting document or a particular location in it might look somewhat different compared to the original document. |
| [UNEXPECTED_CONTENT](#UNEXPECTED-CONTENT) | Generic unexpected content, no specific code. |
| [UNEXPECTED_CONTENT_CATEGORY](#UNEXPECTED-CONTENT-CATEGORY) | Some content in the source document could not be recognized (i.e. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String warningTypeName)](#fromName-java.lang.String) |  |
| [fromNames(Set warningTypeNames)](#fromNames-java.util.Set) |  |
| [getClass()](#getClass) |  |
| [getName(int warningType)](#getName-int) |  |
| [getNames(int warningType)](#getNames-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int warningType)](#toString-int) |  |
| [toStringSet(int attr)](#toStringSet-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### DATA_LOSS {#DATA-LOSS}
```
public static int DATA_LOSS
```


Generic data loss, no specific code.

### DATA_LOSS_CATEGORY {#DATA-LOSS-CATEGORY}
```
public static int DATA_LOSS_CATEGORY
```


Some text/char/image or other data will be missing from either the document tree following load, or from the created document following save.

### FONT_EMBEDDING {#FONT-EMBEDDING}
```
public static int FONT_EMBEDDING
```


Loss of embedded font information during document saving.

### FONT_SUBSTITUTION {#FONT-SUBSTITUTION}
```
public static int FONT_SUBSTITUTION
```


Font has been substituted.

### HINT {#HINT}
```
public static int HINT
```


Advises of a potential problem or suggests an improvement.

### MAJOR_FORMATTING_LOSS {#MAJOR-FORMATTING-LOSS}
```
public static int MAJOR_FORMATTING_LOSS
```


Generic major formatting loss, no specific code.

### MAJOR_FORMATTING_LOSS_CATEGORY {#MAJOR-FORMATTING-LOSS-CATEGORY}
```
public static int MAJOR_FORMATTING_LOSS_CATEGORY
```


The resulting document or a particular location in it might look substantially different compared to the original document.

### MINOR_FORMATTING_LOSS {#MINOR-FORMATTING-LOSS}
```
public static int MINOR_FORMATTING_LOSS
```


Generic minor formatting loss, no specific code.

### MINOR_FORMATTING_LOSS_CATEGORY {#MINOR-FORMATTING-LOSS-CATEGORY}
```
public static int MINOR_FORMATTING_LOSS_CATEGORY
```


The resulting document or a particular location in it might look somewhat different compared to the original document.

### UNEXPECTED_CONTENT {#UNEXPECTED-CONTENT}
```
public static int UNEXPECTED_CONTENT
```


Generic unexpected content, no specific code.

### UNEXPECTED_CONTENT_CATEGORY {#UNEXPECTED-CONTENT-CATEGORY}
```
public static int UNEXPECTED_CONTENT_CATEGORY
```


Some content in the source document could not be recognized (i.e. is unsupported), this may or may not cause issues or result in data/formatting loss.

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
### fromName(String warningTypeName) {#fromName-java.lang.String}
```
public static int fromName(String warningTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| warningTypeName | java.lang.String |  |

**Returns:**
int
### fromNames(Set warningTypeNames) {#fromNames-java.util.Set}
```
public static int fromNames(Set warningTypeNames)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| warningTypeNames | java.util.Set |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int warningType) {#getName-int}
```
public static String getName(int warningType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| warningType | int |  |

**Returns:**
java.lang.String
### getNames(int warningType) {#getNames-int}
```
public static Set getNames(int warningType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| warningType | int |  |

**Returns:**
java.util.Set
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
### toString(int warningType) {#toString-int}
```
public static String toString(int warningType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| warningType | int |  |

**Returns:**
java.lang.String
### toStringSet(int attr) {#toStringSet-int}
```
public static String toStringSet(int attr)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| attr | int |  |

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

