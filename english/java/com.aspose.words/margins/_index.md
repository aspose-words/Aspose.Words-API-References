---
title: Margins
linktitle: Margins
second_title: Aspose.Words for Java API Reference
description: Specifies preset margins in Java.
type: docs
weight: 391
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
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String marginsName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int margins)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int margins)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


Custom margins.

### MIRRORED {#MIRRORED}
```
public static int MIRRORED
```


Mirrored margins. Setting margins to Mirrored will set the appropriate value for [PageSetup.getMultiplePages()](../../com.aspose.words/pagesetup/\#getMultiplePages) / [PageSetup.setMultiplePages(int)](../../com.aspose.words/pagesetup/\#setMultiplePages-int) property. This will affect the whole document, not just the current section.

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
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
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

