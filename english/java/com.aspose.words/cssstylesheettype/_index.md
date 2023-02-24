---
title: CssStyleSheetType
linktitle: CssStyleSheetType
second_title: Aspose.Words for Java API Reference
description: Specifies how CSS Cascading Style Sheet styles are exported to HTML in Java.
type: docs
weight: 98
url: /java/com.aspose.words/cssstylesheettype/
---

**Inheritance:**
java.lang.Object
```
public class CssStyleSheetType
```

Specifies how CSS (Cascading Style Sheet) styles are exported to HTML.
## Fields

| Field | Description |
| --- | --- |
| [EMBEDDED](#EMBEDDED) | CSS styles are written separately from the content in a style sheet embedded in the HTML file. |
| [EXTERNAL](#EXTERNAL) | CSS styles are written separately from the content in a style sheet in an external file. |
| [INLINE](#INLINE) | CSS styles are written inline (as a value of the **style** attribute on every element). |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String cssStyleSheetTypeName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int cssStyleSheetType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int cssStyleSheetType)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### EMBEDDED {#EMBEDDED}
```
public static int EMBEDDED
```


CSS styles are written separately from the content in a style sheet embedded in the HTML file.

### EXTERNAL {#EXTERNAL}
```
public static int EXTERNAL
```


CSS styles are written separately from the content in a style sheet in an external file. The HTML file links the style sheet.

### INLINE {#INLINE}
```
public static int INLINE
```


CSS styles are written inline (as a value of the **style** attribute on every element).

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
### fromName(String cssStyleSheetTypeName) {#fromName-java.lang.String}
```
public static int fromName(String cssStyleSheetTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| cssStyleSheetTypeName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int cssStyleSheetType) {#getName-int}
```
public static String getName(int cssStyleSheetType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| cssStyleSheetType | int |  |

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
### toString(int cssStyleSheetType) {#toString-int}
```
public static String toString(int cssStyleSheetType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| cssStyleSheetType | int |  |

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

