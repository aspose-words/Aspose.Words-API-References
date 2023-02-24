---
title: ContentDisposition
linktitle: ContentDisposition
second_title: Aspose.Words for Java API Reference
description: Enumerates different ways of presenting the document at the client browser in Java.
type: docs
weight: 93
url: /java/com.aspose.words/contentdisposition/
---

**Inheritance:**
java.lang.Object
```
public class ContentDisposition
```

Enumerates different ways of presenting the document at the client browser.

Note that the actual behavior on the client browser might be affected by security configuration of the browser.
## Fields

| Field | Description |
| --- | --- |
| [ATTACHMENT](#ATTACHMENT) | Send the document to the browser and present an option to save the document to disk or open in the application associated with the document's extension. |
| [INLINE](#INLINE) | Send the document to the browser and presents an option to save the document to disk or open inside the browser. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String contentDispositionName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int contentDisposition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int contentDisposition)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### ATTACHMENT {#ATTACHMENT}
```
public static int ATTACHMENT
```


Send the document to the browser and present an option to save the document to disk or open in the application associated with the document's extension.

### INLINE {#INLINE}
```
public static int INLINE
```


Send the document to the browser and presents an option to save the document to disk or open inside the browser.

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
### fromName(String contentDispositionName) {#fromName-java.lang.String}
```
public static int fromName(String contentDispositionName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| contentDispositionName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int contentDisposition) {#getName-int}
```
public static String getName(int contentDisposition)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| contentDisposition | int |  |

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
### toString(int contentDisposition) {#toString-int}
```
public static String toString(int contentDisposition)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| contentDisposition | int |  |

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

