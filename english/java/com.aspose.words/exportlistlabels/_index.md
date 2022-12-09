---
title: ExportListLabels
second_title: Aspose.Words for Java API Reference
description: Specifies how list labels are exported to HTML MHTML and EPUB.
type: docs
weight: 151
url: /java/com.aspose.words/exportlistlabels/
---

**Inheritance:**
java.lang.Object
```
public class ExportListLabels
```

Specifies how list labels are exported to HTML, MHTML and EPUB.
## Fields

| Field | Description |
| --- | --- |
| [AS_INLINE_TEXT](#AS-INLINE-TEXT) | Outputs all list labels as inline text. |
| [AUTO](#AUTO) | Outputs list labels in auto mode. |
| [BY_HTML_TAGS](#BY-HTML-TAGS) | Outputs all list labels as HTML native elements. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String exportListLabelsName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int exportListLabels)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int exportListLabels)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### AS_INLINE_TEXT {#AS-INLINE-TEXT}
```
public static int AS_INLINE_TEXT
```


Outputs all list labels as inline text. HTML

tag is used for any list label representation.

### AUTO {#AUTO}
```
public static int AUTO
```


Outputs list labels in auto mode. Uses HTML native elements when possible. HTML

 *  tags are used for list label representation if it doesn't cause formatting loss, otherwise the HTML
    
    tag is used.

### BY_HTML_TAGS {#BY-HTML-TAGS}
```
public static int BY_HTML_TAGS
```


Outputs all list labels as HTML native elements. HTML

 *  tags are used for list label representation. Some formatting loss is possible.

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
### fromName(String exportListLabelsName) {#fromName-java.lang.String}
```
public static int fromName(String exportListLabelsName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| exportListLabelsName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int exportListLabels) {#getName-int}
```
public static String getName(int exportListLabels)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| exportListLabels | int |  |

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
### toString(int exportListLabels) {#toString-int}
```
public static String toString(int exportListLabels)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| exportListLabels | int |  |

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

