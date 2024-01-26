---
title: BubbleSizeCollection
linktitle: BubbleSizeCollection
second_title: Aspose.Words for Java
description: Represents a collection of bubble sizes for a chart series in Java.
type: docs
weight: 42
url: /java/com.aspose.words/bubblesizecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class BubbleSizeCollection implements Iterable
```

Represents a collection of bubble sizes for a chart series.

 **Remarks:** 

The collection allows only changing bubble sizes. To add or insert new values to a chart series, or remove values, the appropriate methods of the [ChartSeries](../../com.aspose.words/chartseries/) class can be used.

Empty bubble size values are represented as double\#NA\_N.NA\_N.
## Methods

| Method | Description |
| --- | --- |
| [get(int index)](#get-int) | Gets the bubble size value at the specified index. |
| [getCount()](#getCount) | Gets the number of items in this collection. |
| [iterator()](#iterator) | Returns an enumerator object. |
| [set(int index, double value)](#set-int-double) | Sets the bubble size value at the specified index. |
### get(int index) {#get-int}
```
public double get(int index)
```


Gets the bubble size value at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

**Returns:**
double - The bubble size value at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Gets the number of items in this collection.

**Returns:**
int - The number of items in this collection.
### iterator() {#iterator}
```
public Iterator iterator()
```


Returns an enumerator object.

**Returns:**
java.util.Iterator
### set(int index, double value) {#set-int-double}
```
public void set(int index, double value)
```


Sets the bubble size value at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |
| value | double | The bubble size value at the specified index. |

