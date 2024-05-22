---
title: DocumentDirection
linktitle: DocumentDirection
second_title: Aspose.Words for Java
description: Allows to specify the direction to flow the text in a document in Java.
type: docs
weight: 149
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
| [AUTO](#AUTO) | Auto-detect direction. |
| [LEFT_TO_RIGHT](#LEFT-TO-RIGHT) | Left to right direction. |
| [RIGHT_TO_LEFT](#RIGHT-TO-LEFT) | Right to left direction. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String documentDirectionName)](#fromName-java.lang.String) |  |
| [getName(int documentDirection)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int documentDirection)](#toString-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


Auto-detect direction.

 **Remarks:** 

When this option is selected and text contains characters belonging to RTL scripts, the document direction will be set automatically to RTL.

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

### length {#length}
```
public static int length
```


### fromName(String documentDirectionName) {#fromName-java.lang.String}
```
public static int fromName(String documentDirectionName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentDirectionName | java.lang.String |  |

**Returns:**
int
### getName(int documentDirection) {#getName-int}
```
public static String getName(int documentDirection)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentDirection | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int documentDirection) {#toString-int}
```
public static String toString(int documentDirection)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| documentDirection | int |  |

**Returns:**
java.lang.String
