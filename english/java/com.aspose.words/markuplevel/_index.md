---
title: MarkupLevel
second_title: Aspose.Words for Java API Reference
description: Specifies the level in the document tree where a particular  can occur.
type: docs
weight: 390
url: /java/com.aspose.words/markuplevel/
---

**Inheritance:**
java.lang.Object
```
public class MarkupLevel
```

Specifies the level in the document tree where a particular [StructuredDocumentTag](../../com.aspose.words/structureddocumenttag) can occur.
## Fields

| Field | Description |
| --- | --- |
| [BLOCK](#BLOCK) | The element occurs at the block level (e.g. |
| [CELL](#CELL) | The element occurs among cells in a row. |
| [INLINE](#INLINE) | The element occurs at the inline level (e.g. |
| [ROW](#ROW) | The element occurs among rows in a table. |
| [UNKNOWN](#UNKNOWN) | Specifies the unknown or invalid value. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String markupLevelName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int markupLevel)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int markupLevel)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### BLOCK {#BLOCK}
```
public static int BLOCK
```


The element occurs at the block level (e.g. among tables and paragraphs).

### CELL {#CELL}
```
public static int CELL
```


The element occurs among cells in a row.

### INLINE {#INLINE}
```
public static int INLINE
```


The element occurs at the inline level (e.g. among as runs of text).

### ROW {#ROW}
```
public static int ROW
```


The element occurs among rows in a table.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Specifies the unknown or invalid value.

### length {#length}
```
public static int length
```


### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### fromName(String markupLevelName) {#fromName-java.lang.String-}
```
public static int fromName(String markupLevelName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| markupLevelName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int markupLevel) {#getName-int-}
```
public static String getName(int markupLevel)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| markupLevel | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### toString() {#toString--}
```
public String toString()
```




**Returns:**
java.lang.String
### toString(int markupLevel) {#toString-int-}
```
public static String toString(int markupLevel)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| markupLevel | int |  |

**Returns:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

