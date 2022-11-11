---
title: ZoomType
second_title: Aspose.Words for Java API Reference
description: Possible values for how large or small the document appears on the screen in Microsoft Word.
type: docs
weight: 631
url: /java/com.aspose.words/zoomtype/
---

**Inheritance:**
java.lang.Object
```
public class ZoomType
```

Possible values for how large or small the document appears on the screen in Microsoft Word.
## Fields

| Field | Description |
| --- | --- |
| [CUSTOM](#CUSTOM) | Zoom percentage is set explicitly. |
| [FULL_PAGE](#FULL-PAGE) | Zoom percentage is automatically recalculated to fit one full page. |
| [NONE](#NONE) | Indicates to use the explicit zoom percentage. |
| [PAGE_WIDTH](#PAGE-WIDTH) | Zoom percentage is automatically recalculated to fit page width. |
| [TEXT_FIT](#TEXT-FIT) | Zoom percentage is automatically recalculated to fit text. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [fromName(String zoomTypeName)](#fromName-java.lang.String-) |  |
| [getClass()](#getClass--) |  |
| [getName(int zoomType)](#getName-int-) |  |
| [getValues()](#getValues--) |  |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [toString()](#toString--) |  |
| [toString(int zoomType)](#toString-int-) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


Zoom percentage is set explicitly. It is not recalculated automatically when control size changes.

### FULL_PAGE {#FULL-PAGE}
```
public static int FULL_PAGE
```


Zoom percentage is automatically recalculated to fit one full page.

### NONE {#NONE}
```
public static int NONE
```


Indicates to use the explicit zoom percentage. Same as [CUSTOM](../../com.aspose.words/zoomtype\#CUSTOM).

### PAGE_WIDTH {#PAGE-WIDTH}
```
public static int PAGE_WIDTH
```


Zoom percentage is automatically recalculated to fit page width.

### TEXT_FIT {#TEXT-FIT}
```
public static int TEXT_FIT
```


Zoom percentage is automatically recalculated to fit text.

### length {#length}
```
public static int length
```


### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### fromName(String zoomTypeName) {#fromName-java.lang.String-}
```
public static int fromName(String zoomTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| zoomTypeName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int zoomType) {#getName-int-}
```
public static String getName(int zoomType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| zoomType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues--}
```
public static int[] getValues()
```




**Returns:**
int[]
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### toString() {#toString--}
```
public String toString()
```




**Returns:**
java.lang.String
### toString(int zoomType) {#toString-int-}
```
public static String toString(int zoomType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| zoomType | int |  |

**Returns:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

