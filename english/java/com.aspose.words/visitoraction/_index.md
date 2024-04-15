---
title: VisitorAction
linktitle: VisitorAction
second_title: Aspose.Words for Java
description: Allows the visitor to control the enumeration of nodes in Java.
type: docs
weight: 646
url: /java/com.aspose.words/visitoraction/
---

**Inheritance:**
java.lang.Object
```
public class VisitorAction
```

Allows the visitor to control the enumeration of nodes.
## Fields

| Field | Description |
| --- | --- |
| [CONTINUE](#CONTINUE) | The visitor requests the enumeration to continue. |
| [SKIP_THIS_NODE](#SKIP-THIS-NODE) | The visitor requests to skip the current node and continue enumeration. |
| [STOP](#STOP) | The visitor requests the enumeration of nodes to stop. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String visitorActionName)](#fromName-java.lang.String) |  |
| [getName(int visitorAction)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int visitorAction)](#toString-int) |  |
### CONTINUE {#CONTINUE}
```
public static int CONTINUE
```


The visitor requests the enumeration to continue.

### SKIP_THIS_NODE {#SKIP-THIS-NODE}
```
public static int SKIP_THIS_NODE
```


The visitor requests to skip the current node and continue enumeration.

### STOP {#STOP}
```
public static int STOP
```


The visitor requests the enumeration of nodes to stop.

### length {#length}
```
public static int length
```


### fromName(String visitorActionName) {#fromName-java.lang.String}
```
public static int fromName(String visitorActionName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitorActionName | java.lang.String |  |

**Returns:**
int
### getName(int visitorAction) {#getName-int}
```
public static String getName(int visitorAction)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitorAction | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int visitorAction) {#toString-int}
```
public static String toString(int visitorAction)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| visitorAction | int |  |

**Returns:**
java.lang.String
