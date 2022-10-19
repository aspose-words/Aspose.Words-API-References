---
title: CellMerge
second_title: Aspose.Words for Java API Reference
description: A utility class providing constants.
type: docs
weight: 51
url: /java/com.aspose.words/cellmerge/
---

**Inheritance:**
java.lang.Object
```
public class CellMerge
```

A utility class providing constants. Specifies how a cell in a table is merged with other cells.
## Fields

| Field | Description |
| --- | --- |
| [NONE](#NONE) | The cell is not merged. |
| [FIRST](#FIRST) | The cell is the first cell in a range of merged cells. |
| [PREVIOUS](#PREVIOUS) | The cell is merged to the previous cell horizontally or vertically. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int cellMerge)](#getName-int-) |  |
| [toString(int cellMerge)](#toString-int-) |  |
| [fromName(String cellMergeName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### NONE {#NONE}
```
public static int NONE
```


The cell is not merged.

### FIRST {#FIRST}
```
public static int FIRST
```


The cell is the first cell in a range of merged cells.

### PREVIOUS {#PREVIOUS}
```
public static int PREVIOUS
```


The cell is merged to the previous cell horizontally or vertically.

### length {#length}
```
public static int length
```


### getName(int cellMerge) {#getName-int-}
```
public static String getName(int cellMerge)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| cellMerge | int |  |

**Returns:**
java.lang.String
### toString(int cellMerge) {#toString-int-}
```
public static String toString(int cellMerge)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| cellMerge | int |  |

**Returns:**
java.lang.String
### fromName(String cellMergeName) {#fromName-java.lang.String-}
```
public static int fromName(String cellMergeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| cellMergeName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
