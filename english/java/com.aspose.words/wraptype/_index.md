---
title: WrapType
second_title: Aspose.Words for Java API Reference
description: A utility class providing constants.
type: docs
weight: 622
url: /java/com.aspose.words/wraptype/
---

**Inheritance:**
java.lang.Object
```
public class WrapType
```

A utility class providing constants. Specifies how text is wrapped around a shape or picture.
## Fields

| Field | Description |
| --- | --- |
| [NONE](#NONE) | No text wrapping around the shape. |
| [INLINE](#INLINE) | The shape remains on the same layer as text and treated as a character. |
| [TOP_BOTTOM](#TOP-BOTTOM) | The text stops at the top of the shape and restarts on the line below the shape. |
| [SQUARE](#SQUARE) | Wraps text around all sides of the square bounding box of the shape. |
| [TIGHT](#TIGHT) | Wraps tightly around the edges of the shape, instead of wrapping around the bounding box. |
| [THROUGH](#THROUGH) | Same as Tight, but wraps inside any parts of the shape that are open. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int wrapType)](#getName-int-) |  |
| [toString(int wrapType)](#toString-int-) |  |
| [fromName(String wrapTypeName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### NONE {#NONE}
```
public static int NONE
```


No text wrapping around the shape. The shape is placed behind or in front of text.

### INLINE {#INLINE}
```
public static int INLINE
```


The shape remains on the same layer as text and treated as a character.

### TOP_BOTTOM {#TOP-BOTTOM}
```
public static int TOP_BOTTOM
```


The text stops at the top of the shape and restarts on the line below the shape.

### SQUARE {#SQUARE}
```
public static int SQUARE
```


Wraps text around all sides of the square bounding box of the shape.

### TIGHT {#TIGHT}
```
public static int TIGHT
```


Wraps tightly around the edges of the shape, instead of wrapping around the bounding box.

### THROUGH {#THROUGH}
```
public static int THROUGH
```


Same as Tight, but wraps inside any parts of the shape that are open.

### length {#length}
```
public static int length
```


### getName(int wrapType) {#getName-int-}
```
public static String getName(int wrapType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| wrapType | int |  |

**Returns:**
java.lang.String
### toString(int wrapType) {#toString-int-}
```
public static String toString(int wrapType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| wrapType | int |  |

**Returns:**
java.lang.String
### fromName(String wrapTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String wrapTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| wrapTypeName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
