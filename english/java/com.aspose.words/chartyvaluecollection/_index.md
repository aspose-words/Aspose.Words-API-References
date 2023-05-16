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
| [get(int index)](#get-int) | Gets the Y value at the specified index. |
| [getCount()](#getCount) | Gets the number of items in this collection. |
| [iterator()](#iterator) | Returns an enumerator object. |
| [set(int index, ChartYValue value)](#set-int-com.aspose.words.ChartYValue) | Sets the Y value at the specified index. |
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

