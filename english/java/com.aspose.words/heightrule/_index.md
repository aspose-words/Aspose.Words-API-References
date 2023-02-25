---
title: HeightRule
linktitle: HeightRule
second_title: Aspose.Words for Java API Reference
description: Specifies the rule for determining the height of an object in Java.
type: docs
weight: 321
url: /java/com.aspose.words/heightrule/
---

**Inheritance:**
java.lang.Object
```
public class HeightRule
```

Specifies the rule for determining the height of an object.
## Fields

| Field | Description |
| --- | --- |
| [AT_LEAST](#AT-LEAST) | The height will be at least the specified height in points. |
| [AUTO](#AUTO) | The height will grow automatically to accommodate all text inside an object. |
| [EXACTLY](#EXACTLY) | The height is specified exactly in points. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String heightRuleName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int heightRule)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int heightRule)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### AT_LEAST {#AT-LEAST}
```
public static int AT_LEAST
```


The height will be at least the specified height in points. It will grow, if needed, to accommodate all text inside an object.

### AUTO {#AUTO}
```
public static int AUTO
```


The height will grow automatically to accommodate all text inside an object.

### EXACTLY {#EXACTLY}
```
public static int EXACTLY
```


The height is specified exactly in points. Please note that if the text cannot fit inside the object of this height, it will appear truncated.

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
### fromName(String heightRuleName) {#fromName-java.lang.String}
```
public static int fromName(String heightRuleName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| heightRuleName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int heightRule) {#getName-int}
```
public static String getName(int heightRule)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| heightRule | int |  |

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
### toString(int heightRule) {#toString-int}
```
public static String toString(int heightRule)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| heightRule | int |  |

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

