---
title: ChartYValueCollection
linktitle: ChartYValueCollection
second_title: Aspose.Words for Java
description: Represents a collection of Y values for a chart series in Java.
type: docs
weight: 80
url: /java/com.aspose.words/chartyvaluecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartYValueCollection implements Iterable
```

Represents a collection of Y values for a chart series.

 **Remarks:** 

All items of the collection other than **null** must have the same [ChartYValue.getValueType()](../../com.aspose.words/chartyvalue/\#getValueType).

The collection allows only changing Y values. To add or insert new values to a chart series, or remove values, the appropriate methods of the [ChartSeries](../../com.aspose.words/chartseries/) class can be used.
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [get(int index)](#get-int) | Gets the Y value at the specified index. |
| [getClass()](#getClass) |  |
| [getCount()](#getCount) | Gets the number of items in this collection. |
| [hashCode()](#hashCode) |  |
| [iterator()](#iterator) | Returns an enumerator object. |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [set(int index, ChartYValue value)](#set-int-com.aspose.words.ChartYValue) | Sets the Y value at the specified index. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
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
### get(int index) {#get-int}
```
public ChartYValue get(int index)
```


Gets the Y value at the specified index.

 **Remarks:** 

Empty values are represented as **null**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

**Returns:**
[ChartYValue](../../com.aspose.words/chartyvalue/) - The Y value at the specified index.
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getCount() {#getCount}
```
public int getCount()
```


Gets the number of items in this collection.

**Returns:**
int - The number of items in this collection.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### iterator() {#iterator}
```
public Iterator iterator()
```


Returns an enumerator object.

**Returns:**
java.util.Iterator
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### set(int index, ChartYValue value) {#set-int-com.aspose.words.ChartYValue}
```
public void set(int index, ChartYValue value)
```


Sets the Y value at the specified index.

 **Remarks:** 

Empty values are represented as **null**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |
| value | [ChartYValue](../../com.aspose.words/chartyvalue/) | The Y value at the specified index. |

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

