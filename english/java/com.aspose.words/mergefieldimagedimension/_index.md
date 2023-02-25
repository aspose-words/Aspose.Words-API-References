---
title: MergeFieldImageDimension
linktitle: MergeFieldImageDimension
second_title: Aspose.Words for Java API Reference
description: Represents an image dimension i.e in Java.
type: docs
weight: 400
url: /java/com.aspose.words/mergefieldimagedimension/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class MergeFieldImageDimension implements Cloneable
```

Represents an image dimension (i.e. the width or the height) used across a mail merge process.

To learn more, visit the [ Working with Fields ][Working with Fields] documentation article.

To indicate that the image should be inserted with its original dimension during a mail merge, you should assign a negative value to the [getValue()](../../com.aspose.words/mergefieldimagedimension/\#getValue) / [setValue(double)](../../com.aspose.words/mergefieldimagedimension/\#setValue-double) property.


[Working with Fields]: https://docs.aspose.com/words/java/working-with-fields/
## Constructors

| Constructor | Description |
| --- | --- |
| [MergeFieldImageDimension(double value)](#MergeFieldImageDimension-double) | Creates an image dimension instance with the given value in points. |
| [MergeFieldImageDimension(double value, int unit)](#MergeFieldImageDimension-double-int) | Initializes a new instance of this class. |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getUnit()](#getUnit) | The unit. |
| [getValue()](#getValue) | The value. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setUnit(int value)](#setUnit-int) | The unit. |
| [setValue(double value)](#setValue-double) | The value. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### MergeFieldImageDimension(double value) {#MergeFieldImageDimension-double}
```
public MergeFieldImageDimension(double value)
```


Creates an image dimension instance with the given value in points. You should use a negative value to indicate that the original value of the corresponding image dimension should be applied.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The value. |

### MergeFieldImageDimension(double value, int unit) {#MergeFieldImageDimension-double-int}
```
public MergeFieldImageDimension(double value, int unit)
```


Initializes a new instance of this class.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |
| unit | int |  |

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
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getUnit() {#getUnit}
```
public int getUnit()
```


The unit.

**Returns:**
int - The corresponding  int  value. The returned value is one of [MergeFieldImageDimensionUnit](../../com.aspose.words/mergefieldimagedimensionunit/) constants.
### getValue() {#getValue}
```
public double getValue()
```


The value. You should use a negative value to indicate that the original value of the corresponding image dimension should be applied.

**Returns:**
double - The corresponding  double  value.
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




### setUnit(int value) {#setUnit-int}
```
public void setUnit(int value)
```


The unit.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [MergeFieldImageDimensionUnit](../../com.aspose.words/mergefieldimagedimensionunit/) constants. |

### setValue(double value) {#setValue-double}
```
public void setValue(double value)
```


The value. You should use a negative value to indicate that the original value of the corresponding image dimension should be applied.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The corresponding  double  value. |

### toString() {#toString}
```
public String toString()
```




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

