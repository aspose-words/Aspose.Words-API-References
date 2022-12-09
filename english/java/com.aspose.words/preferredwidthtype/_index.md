---
title: PreferredWidthType
second_title: Aspose.Words for Java API Reference
description: Specifies the unit of measurement for the preferred width of a table or cell.
type: docs
weight: 470
url: /java/com.aspose.words/preferredwidthtype/
---

**Inheritance:**
java.lang.Object
```
public class PreferredWidthType
```

Specifies the unit of measurement for the preferred width of a table or cell.
## Fields

| Field | Description |
| --- | --- |
| [AUTO](#AUTO) | The preferred width is not specified. |
| [PERCENT](#PERCENT) | Measure the current item width using a specified percentage. |
| [POINTS](#POINTS) | Measure the current item width using a specified number of points (1/72 inch). |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String preferredWidthTypeName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int preferredWidthType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int preferredWidthType)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### AUTO {#AUTO}
```
public static int AUTO
```


The preferred width is not specified. The actual width of the table or cell is either specified using the explicit width or will be determined automatically by the table layout algorithm when the table is displayed, depending on the table auto fit setting.

### PERCENT {#PERCENT}
```
public static int PERCENT
```


Measure the current item width using a specified percentage.

### POINTS {#POINTS}
```
public static int POINTS
```


Measure the current item width using a specified number of points (1/72 inch).

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
### fromName(String preferredWidthTypeName) {#fromName-java.lang.String}
```
public static int fromName(String preferredWidthTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| preferredWidthTypeName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int preferredWidthType) {#getName-int}
```
public static String getName(int preferredWidthType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| preferredWidthType | int |  |

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
### toString(int preferredWidthType) {#toString-int}
```
public static String toString(int preferredWidthType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| preferredWidthType | int |  |

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

