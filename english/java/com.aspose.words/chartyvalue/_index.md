---
title: ChartYValue
linktitle: ChartYValue
second_title: Aspose.Words for Java
description: Represents an Y value for a chart series in Java.
type: docs
weight: 79
url: /java/com.aspose.words/chartyvalue/
---

**Inheritance:**
java.lang.Object
```
public class ChartYValue
```

Represents an Y value for a chart series.

 **Remarks:** 

This class contains a number of static methods for creating an Y value of a particular type. The [getValueType()](../../com.aspose.words/chartyvalue/\#getValueType) property allows you to determine the type of an existing Y value.

All non-null Y values of a chart series must be of the same [ChartYValueType](../../com.aspose.words/chartyvaluetype/) type.
## Methods

| Method | Description |
| --- | --- |
| [equals(Object obj)](#equals-java.lang.Object) | Gets a flag indicating whether the specified object is equal to the current Y value object. |
| [fromDateTime(Date value)](#fromDateTime-java.util.Date) | Creates a [ChartYValue](../../com.aspose.words/chartyvalue/) instance of the [ChartYValueType.DATE\_TIME](../../com.aspose.words/chartyvaluetype/\#DATE-TIME) type. |
| [fromDouble(double value)](#fromDouble-double) | Creates a [ChartYValue](../../com.aspose.words/chartyvalue/) instance of the [ChartYValueType.DOUBLE](../../com.aspose.words/chartyvaluetype/\#DOUBLE) type. |
| [fromTimeSpan(long value)](#fromTimeSpan-long) | Creates a [ChartYValue](../../com.aspose.words/chartyvalue/) instance of the [ChartYValueType.TIME](../../com.aspose.words/chartyvaluetype/\#TIME) type. |
| [getClass()](#getClass) |  |
| [getDateTimeValue()](#getDateTimeValue) | Gets the stored datetime value. |
| [getDoubleValue()](#getDoubleValue) | Gets the stored numeric value. |
| [getTimeValue()](#getTimeValue) | Gets the stored time value. |
| [getValueType()](#getValueType) | Gets the type of the Y value stored in the object. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### equals(Object obj) {#equals-java.lang.Object}
```
public boolean equals(Object obj)
```


Gets a flag indicating whether the specified object is equal to the current Y value object.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| obj | java.lang.Object |  |

**Returns:**
boolean
### fromDateTime(Date value) {#fromDateTime-java.util.Date}
```
public static ChartYValue fromDateTime(Date value)
```


Creates a [ChartYValue](../../com.aspose.words/chartyvalue/) instance of the [ChartYValueType.DATE\_TIME](../../com.aspose.words/chartyvaluetype/\#DATE-TIME) type.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.util.Date |  |

**Returns:**
[ChartYValue](../../com.aspose.words/chartyvalue/)
### fromDouble(double value) {#fromDouble-double}
```
public static ChartYValue fromDouble(double value)
```


Creates a [ChartYValue](../../com.aspose.words/chartyvalue/) instance of the [ChartYValueType.DOUBLE](../../com.aspose.words/chartyvaluetype/\#DOUBLE) type.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double |  |

**Returns:**
[ChartYValue](../../com.aspose.words/chartyvalue/)
### fromTimeSpan(long value) {#fromTimeSpan-long}
```
public static ChartYValue fromTimeSpan(long value)
```


Creates a [ChartYValue](../../com.aspose.words/chartyvalue/) instance of the [ChartYValueType.TIME](../../com.aspose.words/chartyvaluetype/\#TIME) type.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | long |  |

**Returns:**
[ChartYValue](../../com.aspose.words/chartyvalue/)
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getDateTimeValue() {#getDateTimeValue}
```
public Date getDateTimeValue()
```


Gets the stored datetime value.

**Returns:**
java.util.Date - The stored datetime value.
### getDoubleValue() {#getDoubleValue}
```
public double getDoubleValue()
```


Gets the stored numeric value.

**Returns:**
double - The stored numeric value.
### getTimeValue() {#getTimeValue}
```
public long getTimeValue()
```


Gets the stored time value.

**Returns:**
long - The stored time value.
### getValueType() {#getValueType}
```
public int getValueType()
```


Gets the type of the Y value stored in the object.

**Returns:**
int - The type of the Y value stored in the object. The returned value is one of [ChartYValueType](../../com.aspose.words/chartyvaluetype/) constants.
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

