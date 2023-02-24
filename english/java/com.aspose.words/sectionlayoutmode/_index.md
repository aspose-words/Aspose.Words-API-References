---
title: SectionLayoutMode
linktitle: SectionLayoutMode
second_title: Aspose.Words for Java API Reference
description: Specifies the layout mode for a section allowing to define the document grid behavior in Java.
type: docs
weight: 517
url: /java/com.aspose.words/sectionlayoutmode/
---

**Inheritance:**
java.lang.Object
```
public class SectionLayoutMode
```

Specifies the layout mode for a section allowing to define the document grid behavior.
## Fields

| Field | Description |
| --- | --- |
| [DEFAULT](#DEFAULT) | Specifies that no document grid shall be applied to the contents of the corresponding section in the document. |
| [GRID](#GRID) | Specifies that the corresponding section shall have both the additional line pitch and character pitch added to each line and character within it in order to maintain a specific number of lines per page and characters per line. |
| [LINE_GRID](#LINE-GRID) | Specifies that the corresponding section shall have additional line pitch added to each line within it in order to maintain the specified number of lines per page. |
| [SNAP_TO_CHARS](#SNAP-TO-CHARS) | Specifies that the corresponding section shall have both the additional line pitch and character pitch added to each line and character within it in order to maintain a specific number of lines per page and characters per line. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String sectionLayoutModeName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int sectionLayoutMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int sectionLayoutMode)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Specifies that no document grid shall be applied to the contents of the corresponding section in the document.

### GRID {#GRID}
```
public static int GRID
```


Specifies that the corresponding section shall have both the additional line pitch and character pitch added to each line and character within it in order to maintain a specific number of lines per page and characters per line. Characters will not be automatically aligned with gridlines on typing.

### LINE_GRID {#LINE-GRID}
```
public static int LINE_GRID
```


Specifies that the corresponding section shall have additional line pitch added to each line within it in order to maintain the specified number of lines per page.

### SNAP_TO_CHARS {#SNAP-TO-CHARS}
```
public static int SNAP_TO_CHARS
```


Specifies that the corresponding section shall have both the additional line pitch and character pitch added to each line and character within it in order to maintain a specific number of lines per page and characters per line. Characters will be automatically aligned with gridlines on typing.

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
### fromName(String sectionLayoutModeName) {#fromName-java.lang.String}
```
public static int fromName(String sectionLayoutModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sectionLayoutModeName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int sectionLayoutMode) {#getName-int}
```
public static String getName(int sectionLayoutMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sectionLayoutMode | int |  |

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
### toString(int sectionLayoutMode) {#toString-int}
```
public static String toString(int sectionLayoutMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| sectionLayoutMode | int |  |

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

