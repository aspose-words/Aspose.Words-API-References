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
| [UNKNOWN](#UNKNOWN) | Specifies the unknown or invalid value. |
| [INLINE](#INLINE) | The element occurs at the inline level (e.g. |
| [BLOCK](#BLOCK) | The element occurs at the block level (e.g. |
| [ROW](#ROW) | The element occurs among rows in a table. |
| [CELL](#CELL) | The element occurs among cells in a row. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int markupLevel)](#getName-int-) |  |
| [toString(int markupLevel)](#toString-int-) |  |
| [fromName(String markupLevelName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


Specifies the unknown or invalid value.

### INLINE {#INLINE}
```
public static int INLINE
```


The element occurs at the inline level (e.g. among as runs of text).

### BLOCK {#BLOCK}
```
public static int BLOCK
```


The element occurs at the block level (e.g. among tables and paragraphs).

### ROW {#ROW}
```
public static int ROW
```


The element occurs among rows in a table.

### CELL {#CELL}
```
public static int CELL
```


The element occurs among cells in a row.

### length {#length}
```
public static int length
```


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
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
