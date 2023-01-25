---
title: RevisionTextEffect
second_title: Aspose.Words for Java API Reference
description: Allows to specify decoration effect for revisions of document text.
type: docs
weight: 493
url: /java/com.aspose.words/revisiontexteffect/
---

**Inheritance:**
java.lang.Object
```
public class RevisionTextEffect
```

Allows to specify decoration effect for revisions of document text.
## Fields

| Field | Description |
| --- | --- |
| [BOLD](#BOLD) | Revised content is made bold and colored. |
| [COLOR](#COLOR) | Revised content is highlighted with color only. |
| [DOUBLE_STRIKE_THROUGH](#DOUBLE-STRIKE-THROUGH) | Revised content is double stroked through and colored. |
| [DOUBLE_UNDERLINE](#DOUBLE-UNDERLINE) | Revised content is double underlined and colored. |
| [HIDDEN](#HIDDEN) | Revised content is hidden. |
| [ITALIC](#ITALIC) | Revised content is made italic and colored. |
| [NONE](#NONE) | Revised content has no special effects applied. |
| [STRIKE_THROUGH](#STRIKE-THROUGH) | Revised content is stroked through and colored. |
| [UNDERLINE](#UNDERLINE) | Revised content is underlined and colored. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String revisionTextEffectName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int revisionTextEffect)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int revisionTextEffect)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### BOLD {#BOLD}
```
public static int BOLD
```


Revised content is made bold and colored.

### COLOR {#COLOR}
```
public static int COLOR
```


Revised content is highlighted with color only.

### DOUBLE_STRIKE_THROUGH {#DOUBLE-STRIKE-THROUGH}
```
public static int DOUBLE_STRIKE_THROUGH
```


Revised content is double stroked through and colored. Only works for [RevisionType.DELETION](../../com.aspose.words/revisiontype\#DELETION), [RevisionType.FORMAT\_CHANGE](../../com.aspose.words/revisiontype\#FORMAT-CHANGE) and [RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING) ('move from' type).

### DOUBLE_UNDERLINE {#DOUBLE-UNDERLINE}
```
public static int DOUBLE_UNDERLINE
```


Revised content is double underlined and colored.

### HIDDEN {#HIDDEN}
```
public static int HIDDEN
```


Revised content is hidden. Only works for [RevisionType.DELETION](../../com.aspose.words/revisiontype\#DELETION) and [RevisionType.MOVING](../../com.aspose.words/revisiontype\#MOVING) ('move from' type).

### ITALIC {#ITALIC}
```
public static int ITALIC
```


Revised content is made italic and colored.

### NONE {#NONE}
```
public static int NONE
```


Revised content has no special effects applied. This corresponds to [RevisionColor.NO\_HIGHLIGHT](../../com.aspose.words/revisioncolor\#NO-HIGHLIGHT).

### STRIKE_THROUGH {#STRIKE-THROUGH}
```
public static int STRIKE_THROUGH
```


Revised content is stroked through and colored.

### UNDERLINE {#UNDERLINE}
```
public static int UNDERLINE
```


Revised content is underlined and colored.

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
### fromName(String revisionTextEffectName) {#fromName-java.lang.String}
```
public static int fromName(String revisionTextEffectName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| revisionTextEffectName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int revisionTextEffect) {#getName-int}
```
public static String getName(int revisionTextEffect)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| revisionTextEffect | int |  |

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
### toString(int revisionTextEffect) {#toString-int}
```
public static String toString(int revisionTextEffect)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| revisionTextEffect | int |  |

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

