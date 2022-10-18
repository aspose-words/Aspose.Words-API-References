---
title: ChartSeriesCollection
second_title: Aspose.Words for Java API Reference
description: Represents collection of a .
type: docs
weight: 69
url: /java/com.aspose.words/chartseriescollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartSeriesCollection implements Iterable
```

Represents collection of a [ChartSeries](../../com.aspose.words/chartseries).

To learn more, visit the **Working with Charts** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [get(int index)](#get-int-) | Returns a [ChartSeries](../../com.aspose.words/chartseries) at the specified index. |
| [iterator()](#iterator--) | Returns an enumerator object. |
| [removeAt(int index)](#removeAt-int-) | Removes a [ChartSeries](../../com.aspose.words/chartseries) at the specified index. |
| [clear()](#clear--) | Removes all [ChartSeries](../../com.aspose.words/chartseries) from this collection. |
| [add(String seriesName, String[] categories, double[] values)](#add-java.lang.String-java.lang.String---double---) | Adds new [ChartSeries](../../com.aspose.words/chartseries) to this collection. |
| [add(String seriesName, double[] xValues, double[] yValues)](#add-java.lang.String-double---double---) | Adds new [ChartSeries](../../com.aspose.words/chartseries) to this collection. |
| [add(String seriesName, Date[] dates, double[] values)](#add-java.lang.String-java.util.Date---double---) | Adds new [ChartSeries](../../com.aspose.words/chartseries) to this collection. |
| [add(String seriesName, double[] xValues, double[] yValues, double[] bubbleSizes)](#add-java.lang.String-double---double---double---) | Adds new [ChartSeries](../../com.aspose.words/chartseries) to this collection. |
| [getCount()](#getCount--) | Returns the number of [ChartSeries](../../com.aspose.words/chartseries) in this collection. |
### get(int index) {#get-int-}
```
public ChartSeries get(int index)
```


Returns a [ChartSeries](../../com.aspose.words/chartseries) at the specified index.

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the collection. |

**Returns:**
[ChartSeries](../../com.aspose.words/chartseries) - A [ChartSeries](../../com.aspose.words/chartseries) at the specified index.
### iterator() {#iterator--}
```
public Iterator iterator()
```


Returns an enumerator object.

**Returns:**
java.util.Iterator
### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


Removes a [ChartSeries](../../com.aspose.words/chartseries) at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero-based index of the ChartSeries to remove. |

### clear() {#clear--}
```
public void clear()
```


Removes all [ChartSeries](../../com.aspose.words/chartseries) from this collection.

### add(String seriesName, String[] categories, double[] values) {#add-java.lang.String-java.lang.String---double---}
```
public ChartSeries add(String seriesName, String[] categories, double[] values)
```


Adds new [ChartSeries](../../com.aspose.words/chartseries) to this collection. Use this method to add series to any type of Bar, Column, Line and Surface charts.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| seriesName | java.lang.String |  |
| categories | java.lang.String[] |  |
| values | double[] |  |

**Returns:**
[ChartSeries](../../com.aspose.words/chartseries) - Recently added [ChartSeries](../../com.aspose.words/chartseries) object.
### add(String seriesName, double[] xValues, double[] yValues) {#add-java.lang.String-double---double---}
```
public ChartSeries add(String seriesName, double[] xValues, double[] yValues)
```


Adds new [ChartSeries](../../com.aspose.words/chartseries) to this collection. Use this method to add series to any type of Scatter charts.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| seriesName | java.lang.String |  |
| xValues | double[] |  |
| yValues | double[] |  |

**Returns:**
[ChartSeries](../../com.aspose.words/chartseries) - Recently added [ChartSeries](../../com.aspose.words/chartseries) object.
### add(String seriesName, Date[] dates, double[] values) {#add-java.lang.String-java.util.Date---double---}
```
public ChartSeries add(String seriesName, Date[] dates, double[] values)
```


Adds new [ChartSeries](../../com.aspose.words/chartseries) to this collection. Use this method to add series to any type of Area, Radar and Stock charts.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| seriesName | java.lang.String |  |
| dates | java.util.Date[] |  |
| values | double[] |  |

**Returns:**
[ChartSeries](../../com.aspose.words/chartseries)
### add(String seriesName, double[] xValues, double[] yValues, double[] bubbleSizes) {#add-java.lang.String-double---double---double---}
```
public ChartSeries add(String seriesName, double[] xValues, double[] yValues, double[] bubbleSizes)
```


Adds new [ChartSeries](../../com.aspose.words/chartseries) to this collection. Use this method to add series to any type of Bubble charts.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| seriesName | java.lang.String |  |
| xValues | double[] |  |
| yValues | double[] |  |
| bubbleSizes | double[] |  |

**Returns:**
[ChartSeries](../../com.aspose.words/chartseries) - Recently added [ChartSeries](../../com.aspose.words/chartseries) object.
### getCount() {#getCount--}
```
public int getCount()
```


Returns the number of [ChartSeries](../../com.aspose.words/chartseries) in this collection.

**Returns:**
int - The number of [ChartSeries](../../com.aspose.words/chartseries) in this collection.
