---
title: HtmlVersion
second_title: Aspose.Words for Java API Reference
description: Indicates the version of HTML is used when saving the document to  and  formats.
type: docs
weight: 334
url: /java/com.aspose.words/htmlversion/
---

**Inheritance:**
java.lang.Object
```
public class HtmlVersion
```

Indicates the version of HTML is used when saving the document to [SaveFormat.HTML](../../com.aspose.words/saveformat\#HTML) and [SaveFormat.MHTML](../../com.aspose.words/saveformat\#MHTML) formats.
## Fields

| Field | Description |
| --- | --- |
| [HTML_5](#HTML-5) | Saves the document in compliance with the HTML 5 standard. |
| [XHTML](#XHTML) | Saves the document in compliance with the XHTML 1.0 Transitional standard. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String htmlVersionName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int htmlVersion)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int htmlVersion)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### HTML_5 {#HTML-5}
```
public static int HTML_5
```


Saves the document in compliance with the HTML 5 standard.

### XHTML {#XHTML}
```
public static int XHTML
```


Saves the document in compliance with the XHTML 1.0 Transitional standard.

Aspose.Words aims to output XHTML according to the XHTML 1.0 Transitional standard, but the output will not always validate against the DTD. Some structures inside a Microsoft Word document are hard or impossible to map to a document that will validate against the XHTML schema. For example, XHTML does not allow nested lists (UL cannot be nested inside another UL element), but in Microsoft Word document multilevel lists occur quite often.

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
### fromName(String htmlVersionName) {#fromName-java.lang.String}
```
public static int fromName(String htmlVersionName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| htmlVersionName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int htmlVersion) {#getName-int}
```
public static String getName(int htmlVersion)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| htmlVersion | int |  |

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
### toString(int htmlVersion) {#toString-int}
```
public static String toString(int htmlVersion)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| htmlVersion | int |  |

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

