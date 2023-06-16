---
title: ScriptShapingLevel
linktitle: ScriptShapingLevel
second_title: Aspose.Words for Java
description: Describes shaping levels required by a script in Java.
type: docs
weight: 525
url: /java/com.aspose.words/scriptshapinglevel/
---

**Inheritance:**
java.lang.Object
```
public class ScriptShapingLevel
```

Describes shaping levels required by a script.
## Fields

| Field | Description |
| --- | --- |
| [FULL](#FULL) | Script requires full shaping support. |
| [MINIMUM](#MINIMUM) | Script requires minimum shaping support. |
| [NONE](#NONE) | Script does not require shaping. |
| [UNKNOWN](#UNKNOWN) | This is used when the level for the script is not specified. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String scriptShapingLevelName)](#fromName-java.lang.String) |  |
| [getName(int scriptShapingLevel)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int scriptShapingLevel)](#toString-int) |  |
### FULL {#FULL}
```
public static int FULL
```


Script requires full shaping support.

### MINIMUM {#MINIMUM}
```
public static int MINIMUM
```


Script requires minimum shaping support.

 **Remarks:** 

It is not clear, what Minimum means. Minimum is set for some very popular scripts (Latin, Cyrillic...).

### NONE {#NONE}
```
public static int NONE
```


Script does not require shaping.

### UNKNOWN {#UNKNOWN}
```
public static int UNKNOWN
```


This is used when the level for the script is not specified.

 **Remarks:** 

It should not happen.

### length {#length}
```
public static int length
```


### fromName(String scriptShapingLevelName) {#fromName-java.lang.String}
```
public static int fromName(String scriptShapingLevelName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| scriptShapingLevelName | java.lang.String |  |

**Returns:**
int
### getName(int scriptShapingLevel) {#getName-int}
```
public static String getName(int scriptShapingLevel)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| scriptShapingLevel | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int scriptShapingLevel) {#toString-int}
```
public static String toString(int scriptShapingLevel)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| scriptShapingLevel | int |  |

**Returns:**
java.lang.String
