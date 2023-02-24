---
title: RevisionType
linktitle: RevisionType
second_title: Aspose.Words for Java API Reference
description: Specifies the type of change being tracked in in Java.
type: docs
weight: 496
url: /java/com.aspose.words/revisiontype/
---

**Inheritance:**
java.lang.Object
```
public class RevisionType
```

Specifies the type of change being tracked in [Revision](../../com.aspose.words/revision/).
## Fields

| Field | Description |
| --- | --- |
| [DELETION](#DELETION) | Content was removed from the document. |
| [FORMAT_CHANGE](#FORMAT-CHANGE) | Change of formatting was applied to the parent node. |
| [INSERTION](#INSERTION) | New content was inserted in the document. |
| [MOVING](#MOVING) | Content was moved in the document. |
| [STYLE_DEFINITION_CHANGE](#STYLE-DEFINITION-CHANGE) | Change of formatting was applied to the parent style. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String revisionTypeName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int revisionType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int revisionType)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### DELETION {#DELETION}
```
public static int DELETION
```


Content was removed from the document.

### FORMAT_CHANGE {#FORMAT-CHANGE}
```
public static int FORMAT_CHANGE
```


Change of formatting was applied to the parent node.

### INSERTION {#INSERTION}
```
public static int INSERTION
```


New content was inserted in the document.

### MOVING {#MOVING}
```
public static int MOVING
```


Content was moved in the document.

### STYLE_DEFINITION_CHANGE {#STYLE-DEFINITION-CHANGE}
```
public static int STYLE_DEFINITION_CHANGE
```


Change of formatting was applied to the parent style.

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
### fromName(String revisionTypeName) {#fromName-java.lang.String}
```
public static int fromName(String revisionTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| revisionTypeName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int revisionType) {#getName-int}
```
public static String getName(int revisionType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| revisionType | int |  |

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
### toString(int revisionType) {#toString-int}
```
public static String toString(int revisionType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| revisionType | int |  |

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

