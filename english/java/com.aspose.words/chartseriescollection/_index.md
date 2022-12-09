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

To learn more, visit the [ Working with Charts ][Working with Charts] documentation article.


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## Methods

| Method | Description |
| --- | --- |
| [add(String seriesName, double[] xValues, double[] yValues)](#add-java.lang.String-double---double) | Adds new [ChartSeries](../../com.aspose.words/chartseries) to this collection. |
| [add(String seriesName, double[] xValues, double[] yValues, double[] bubbleSizes)](#add-java.lang.String-double---double---double) | Adds new [ChartSeries](../../com.aspose.words/chartseries) to this collection. |
| [add(String seriesName, String[] categories, double[] values)](#add-java.lang.String-java.lang.String---double) | Adds new [ChartSeries](../../com.aspose.words/chartseries) to this collection. |
| [add(String seriesName, Date[] dates, double[] values)](#add-java.lang.String-java.util.Date---double) | Adds new [ChartSeries](../../com.aspose.words/chartseries) to this collection. |
| [clear()](#clear) | Removes all [ChartSeries](../../com.aspose.words/chartseries) from this collection. |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [get(int index)](#get-int) | Returns a [ChartSeries](../../com.aspose.words/chartseries) at the specified index. |
| [getClass()](#getClass) |  |
| [getCount()](#getCount) | Returns the number of [ChartSeries](../../com.aspose.words/chartseries) in this collection. |
| [hashCode()](#hashCode) |  |
| [iterator()](#iterator) | Returns an enumerator object. |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [removeAt(int index)](#removeAt-int) | Removes a [ChartSeries](../../com.aspose.words/chartseries) at the specified index. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### add(String seriesName, double[] xValues, double[] yValues) {#add-java.lang.String-double---double}
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
### add(String seriesName, double[] xValues, double[] yValues, double[] bubbleSizes) {#add-java.lang.String-double---double---double}
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
### add(String seriesName, String[] categories, double[] values) {#add-java.lang.String-java.lang.String---double}
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
### add(String seriesName, Date[] dates, double[] values) {#add-java.lang.String-java.util.Date---double}
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
### clear() {#clear}
```
public void clear()
```


Removes all [ChartSeries](../../com.aspose.words/chartseries) from this collection.

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


Returns the number of [ChartSeries](../../com.aspose.words/chartseries) in this collection.

**Returns:**
int - The number of [ChartSeries](../../com.aspose.words/chartseries) in this collection.
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




### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Removes a [ChartSeries](../../com.aspose.words/chartseries) at the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero-based index of the [ChartSeries](../../com.aspose.words/chartseries) to remove. |

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

