---
title: DocumentDirection
second_title: Aspose.Words for Java API Reference
description: Allows to specify the direction to flow the text in a document.
type: docs
weight: 123
url: /java/com.aspose.words/documentdirection/
---

**Inheritance:**
java.lang.Object
```
public class DocumentDirection
```

Allows to specify the direction to flow the text in a document.
## Fields

| Field | Description |
| --- | --- |
| [LEFT_TO_RIGHT](#LEFT-TO-RIGHT) | Left to right direction. |
| [RIGHT_TO_LEFT](#RIGHT-TO-LEFT) | Right to left direction. |
| [AUTO](#AUTO) | Auto-detect direction. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [getName(int documentDirection)](#getName-int-) |  |
| [toString(int documentDirection)](#toString-int-) |  |
| [fromName(String documentDirectionName)](#fromName-java.lang.String-) |  |
| [getValues()](#getValues--) |  |
### LEFT_TO_RIGHT {#LEFT-TO-RIGHT}
```
public static int LEFT_TO_RIGHT
```


Left to right direction.

### RIGHT_TO_LEFT {#RIGHT-TO-LEFT}
```
public static int RIGHT_TO_LEFT
```


Right to left direction.

### AUTO {#AUTO}
```
public static int AUTO
```


Auto-detect direction. When this option is selected and text contains characters belonging to RTL scripts, the document direction will be set automatically to RTL.

### length {#length}
```
public static int length
```


### getName(int documentDirection) {#getName-int-}
```
public static String getName(int documentDirection)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentDirection | int |  |

**Returns:**
java.lang.String
### toString(int documentDirection) {#toString-int-}
```
public static String toString(int documentDirection)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentDirection | int |  |

**Returns:**
java.lang.String
### fromName(String documentDirectionName) {#fromName-java.lang.String-}
```
public static int fromName(String documentDirectionName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentDirectionName | java.lang.String |  |

**Returns:**
int
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
