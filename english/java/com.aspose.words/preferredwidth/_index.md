---
title: PreferredWidth
linktitle: PreferredWidth
second_title: Aspose.Words for Java API Reference
description: Represents a value and its unit of measure that is used to specify the preferred width of a table or a cell in Java.
type: docs
weight: 472
url: /java/com.aspose.words/preferredwidth/
---

**Inheritance:**
java.lang.Object
```
public class PreferredWidth
```

Represents a value and its unit of measure that is used to specify the preferred width of a table or a cell.

To learn more, visit the [ Working with Tables ][Working with Tables] documentation article.

Preferred width can be specified as a percentage, number of points or a special "none/auto" value.

The instances of this class are immutable.


[Working with Tables]: https://docs.aspose.com/words/java/working-with-tables/
## Fields

| Field | Description |
| --- | --- |
| [AUTO](#AUTO) | Returns an instance that represents the "preferred width is not specified" value. |
## Methods

| Method | Description |
| --- | --- |
| [equals(PreferredWidth other)](#equals-com.aspose.words.PreferredWidth) | Determines whether the specified [PreferredWidth](../../com.aspose.words/preferredwidth/) is equal in value to the current [PreferredWidth](../../com.aspose.words/preferredwidth/). |
| [equals(Object obj)](#equals-java.lang.Object) | Determines whether the specified object is equal in value to the current object. |
| [fromPercent(double percent)](#fromPercent-double) | A creation method that returns a new instance that represents a preferred width specified as a percentage. |
| [fromPoints(double points)](#fromPoints-double) | A creation method that returns a new instance that represents a preferred width specified using a number of points. |
| [getClass()](#getClass) |  |
| [getType()](#getType) | Gets the unit of measure used for this preferred width value. |
| [getValue()](#getValue) | Gets the preferred width value. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) | Returns a user-friendly string that displays the value of this object. |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### AUTO {#AUTO}
```
public static PreferredWidth AUTO
```


Returns an instance that represents the "preferred width is not specified" value.

### equals(PreferredWidth other) {#equals-com.aspose.words.PreferredWidth}
```
public boolean equals(PreferredWidth other)
```


Determines whether the specified [PreferredWidth](../../com.aspose.words/preferredwidth/) is equal in value to the current [PreferredWidth](../../com.aspose.words/preferredwidth/).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| other | [PreferredWidth](../../com.aspose.words/preferredwidth/) |  |

**Returns:**
boolean
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Determines whether the specified object is equal in value to the current object.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### fromPercent(double percent) {#fromPercent-double}
```
public static PreferredWidth fromPercent(double percent)
```


A creation method that returns a new instance that represents a preferred width specified as a percentage.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| percent | double | The value must be from 0 to 100. |

**Returns:**
[PreferredWidth](../../com.aspose.words/preferredwidth/)
### fromPoints(double points) {#fromPoints-double}
```
public static PreferredWidth fromPoints(double points)
```


A creation method that returns a new instance that represents a preferred width specified using a number of points.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| points | double | The value must be from 0 to 22 inches (22 \* 72 points). |

**Returns:**
[PreferredWidth](../../com.aspose.words/preferredwidth/)
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getType() {#getType}
```
public int getType()
```


Gets the unit of measure used for this preferred width value.

**Returns:**
int - The unit of measure used for this preferred width value. The returned value is one of [PreferredWidthType](../../com.aspose.words/preferredwidthtype/) constants.
### getValue() {#getValue}
```
public double getValue()
```


Gets the preferred width value. The unit of measure is specified in the [getType()](../../com.aspose.words/preferredwidth/\#getType) property.

**Returns:**
double - The preferred width value.
### hashCode() {#hashCode}
```
public int hashCode()
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


Returns a user-friendly string that displays the value of this object.

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

