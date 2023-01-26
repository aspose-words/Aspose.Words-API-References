---
title: TxtExportHeadersFootersMode
second_title: Aspose.Words for Java API Reference
description: Specifies the way headers and footers are exported to plain text format.
type: docs
weight: 585
url: /java/com.aspose.words/txtexportheadersfootersmode/
---

**Inheritance:**
java.lang.Object
```
public class TxtExportHeadersFootersMode
```

Specifies the way headers and footers are exported to plain text format.
## Fields

| Field | Description |
| --- | --- |
| [ALL_AT_END](#ALL-AT-END) | All headers and footers are placed after all section bodies at the very end of a document. |
| [NONE](#NONE) | No headers and footers are exported. |
| [PRIMARY_ONLY](#PRIMARY-ONLY) | Only primary headers and footers are exported at the beginning and end of each section. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String txtExportHeadersFootersModeName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int txtExportHeadersFootersMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int txtExportHeadersFootersMode)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### ALL_AT_END {#ALL-AT-END}
```
public static int ALL_AT_END
```


All headers and footers are placed after all section bodies at the very end of a document. This mode is similar to Word.

### NONE {#NONE}
```
public static int NONE
```


No headers and footers are exported.

### PRIMARY_ONLY {#PRIMARY-ONLY}
```
public static int PRIMARY_ONLY
```


Only primary headers and footers are exported at the beginning and end of each section.

It is hard to meaningfully output headers and footers to plain text because it is not paginated.

When this mode is used, only primary headers and footers are exported at the beginning and end of each section.

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
### fromName(String txtExportHeadersFootersModeName) {#fromName-java.lang.String}
```
public static int fromName(String txtExportHeadersFootersModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| txtExportHeadersFootersModeName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int txtExportHeadersFootersMode) {#getName-int}
```
public static String getName(int txtExportHeadersFootersMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| txtExportHeadersFootersMode | int |  |

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
### toString(int txtExportHeadersFootersMode) {#toString-int}
```
public static String toString(int txtExportHeadersFootersMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| txtExportHeadersFootersMode | int |  |

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

