---
title: ChartXValueCollection
linktitle: ChartXValueCollection
second_title: Aspose.Words for Java
description: Represents a collection of X values for a chart series in Java.
type: docs
weight: 77
url: /java/com.aspose.words/chartxvaluecollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartXValueCollection implements Iterable
```

Represents a collection of X values for a chart series.

 **Remarks:** 

All items of the collection other than **null** must have the same [ChartXValue.getValueType()](../../com.aspose.words/chartxvalue/\#getValueType).

The collection allows only changing X values. To add or insert new values to a chart series, or remove values, the appropriate methods of the [ChartSeries](../../com.aspose.words/chartseries/) class can be used.
## Methods

| Method | Description |
| --- | --- |
| [get(int index)](#get-int) | Gets the X value at the specified index. |
| [getCount()](#getCount) | Gets the number of items in this collection. |
| [iterator()](#iterator) | Returns an enumerator object. |
| [set(int index, ChartXValue value)](#set-int-com.aspose.words.ChartXValue) | Sets the X value at the specified index. |
### get(int index) {#get-int}
```
public ChartXValue get(int index)
```


Gets the X value at the specified index.

 **Remarks:** 

Empty values are represented as **null**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

**Returns:**
[ChartXValue](../../com.aspose.words/chartxvalue/) - The X value at the specified index.
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
### set(int index, ChartXValue value) {#set-int-com.aspose.words.ChartXValue}
```
public void set(int index, ChartXValue value)
```


Sets the X value at the specified index.

 **Remarks:** 

Empty values are represented as **null**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |
| value | [ChartXValue](../../com.aspose.words/chartxvalue/) | The X value at the specified index. |

