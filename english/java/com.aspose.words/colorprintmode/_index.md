---
title: ColorPrintMode
second_title: Aspose.Words for Java API Reference
description: Specifies how non-colored pages are printed if the device supports color printing.
type: docs
weight: 76
url: /java/com.aspose.words/colorprintmode/
---

**Inheritance:**
java.lang.Object
```
public class ColorPrintMode
```

Specifies how non-colored pages are printed if the device supports color printing.
## Fields

| Field | Description |
| --- | --- |
| [GRAYSCALE_AUTO](#GRAYSCALE-AUTO) | Non-colored pages if detected are printed in grayscale. |
| [NORMAL](#NORMAL) | All pages are printed according to the printer's capabilities and settings. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String colorPrintModeName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int colorPrintMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int colorPrintMode)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### GRAYSCALE_AUTO {#GRAYSCALE-AUTO}
```
public static int GRAYSCALE_AUTO
```


Non-colored pages if detected are printed in grayscale. PageSettings\#getColor().getColor() / PageSettings\#setColor(boolean).setColor(boolean) is automatically set false for detected non-colored pages. If the printer does not support color printing, this setting is ignored.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


All pages are printed according to the printer's capabilities and settings.

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
### fromName(String colorPrintModeName) {#fromName-java.lang.String}
```
public static int fromName(String colorPrintModeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| colorPrintModeName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int colorPrintMode) {#getName-int}
```
public static String getName(int colorPrintMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| colorPrintMode | int |  |

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
### toString(int colorPrintMode) {#toString-int}
```
public static String toString(int colorPrintMode)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| colorPrintMode | int |  |

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

