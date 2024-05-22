---
title: Margins
linktitle: Margins
second_title: Aspose.Words for Java
description: Specifies preset margins in Java.
type: docs
weight: 417
url: /java/com.aspose.words/margins/
---

**Inheritance:**
java.lang.Object
```
public class Margins
```

Specifies preset margins.
## Fields

| Field | Description |
| --- | --- |
| [CUSTOM](#CUSTOM) | Custom margins. |
| [MIRRORED](#MIRRORED) | Mirrored margins. |
| [MODERATE](#MODERATE) | Moderate margins. |
| [NARROW](#NARROW) | Narrow margins. |
| [NORMAL](#NORMAL) | Normal margins. |
| [WIDE](#WIDE) | Wide margins. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String marginsName)](#fromName-java.lang.String) |  |
| [getName(int margins)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int margins)](#toString-int) |  |
### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


Custom margins.

### MIRRORED {#MIRRORED}
```
public static int MIRRORED
```


Mirrored margins.

 **Remarks:** 

Setting margins to Mirrored will set the appropriate value for [PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup/\#getMultiplePages) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup/\#setMultiplePages-int) property. This will affect the whole document, not just the current section.

### MODERATE {#MODERATE}
```
public static int MODERATE
```


Moderate margins.

### NARROW {#NARROW}
```
public static int NARROW
```


Narrow margins.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Normal margins.

### WIDE {#WIDE}
```
public static int WIDE
```


Wide margins.

### length {#length}
```
public static int length
```


### fromName(String marginsName) {#fromName-java.lang.String}
```
public static int fromName(String marginsName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| marginsName | java.lang.String |  |

**Returns:**
int
### getName(int margins) {#getName-int}
```
public static String getName(int margins)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| margins | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int margins) {#toString-int}
```
public static String toString(int margins)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| margins | int |  |

**Returns:**
java.lang.String
