---
title: ContinuousSectionRestart
linktitle: ContinuousSectionRestart
second_title: Aspose.Words for Java API Reference
description: Represents different behaviors when computing page numbers in a continuous section that restarts page numbering in Java.
type: docs
weight: 94
url: /java/com.aspose.words/continuoussectionrestart/
---

**Inheritance:**
java.lang.Object
```
public class ContinuousSectionRestart
```

Represents different behaviors when computing page numbers in a continuous section that restarts page numbering.
## Fields

| Field | Description |
| --- | --- |
| [ALWAYS](#ALWAYS) | Page numbering always restarts regardless of content flow. |
| [FROM_NEW_PAGE_ONLY](#FROM-NEW-PAGE-ONLY) | Page numbering restarts only if there is no other content before the section on the page where the section starts. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String continuousSectionRestartName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int continuousSectionRestart)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int continuousSectionRestart)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### ALWAYS {#ALWAYS}
```
public static int ALWAYS
```


Page numbering always restarts regardless of content flow. This behavior is demonstrated by all MS Word versions, except Word 2016.

### FROM_NEW_PAGE_ONLY {#FROM-NEW-PAGE-ONLY}
```
public static int FROM_NEW_PAGE_ONLY
```


Page numbering restarts only if there is no other content before the section on the page where the section starts. The behavior is demonstrated by MS Word 2016.

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
### fromName(String continuousSectionRestartName) {#fromName-java.lang.String}
```
public static int fromName(String continuousSectionRestartName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| continuousSectionRestartName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int continuousSectionRestart) {#getName-int}
```
public static String getName(int continuousSectionRestart)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| continuousSectionRestart | int |  |

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
### toString(int continuousSectionRestart) {#toString-int}
```
public static String toString(int continuousSectionRestart)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| continuousSectionRestart | int |  |

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

