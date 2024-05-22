---
title: ChartSeriesGroupCollection
linktitle: ChartSeriesGroupCollection
second_title: Aspose.Words for Java
description: Represents a collection of ChartSeriesGroup objects in Java.
type: docs
weight: 82
url: /java/com.aspose.words/chartseriesgroupcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartSeriesGroupCollection implements Iterable
```

Represents a collection of [ChartSeriesGroup](../../com.aspose.words/chartseriesgroup/) objects.

 **Remarks:** 

To learn more, visit the [ Working with Charts ][Working with Charts] documentation article.


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## Methods

| Method | Description |
| --- | --- |
| [add(int seriesType)](#add-int) |  |
| [get(int index)](#get-int) | Returns a [ChartSeriesGroup](../../com.aspose.words/chartseriesgroup/) at the specified index. |
| [getCount()](#getCount) | Returns the number of series groups in this collection. |
| [iterator()](#iterator) | Returns an enumerator object. |
| [removeAt(int index)](#removeAt-int) | Removes a series group at the specified index. |
### add(int seriesType) {#add-int}
```
public ChartSeriesGroup add(int seriesType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| seriesType | int |  |

**Returns:**
[ChartSeriesGroup](../../com.aspose.words/chartseriesgroup/)
### get(int index) {#get-int}
```
public ChartSeriesGroup get(int index)
```


Returns a [ChartSeriesGroup](../../com.aspose.words/chartseriesgroup/) at the specified index.

 **Examples:** 

Show how to remove secondary axis.

```

 Document doc = new Document(getMyDir() + "Combo chart.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Chart chart = shape.getChart();
 ChartSeriesGroupCollection seriesGroups = chart.getSeriesGroups();

 // Find secondary axis and remove from the collection.
 for (int i = 0; i < seriesGroups.getCount(); i++)
     if (seriesGroups.get(i).getAxisGroup() == AxisGroup.SECONDARY)
         seriesGroups.removeAt(i);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

**Returns:**
[ChartSeriesGroup](../../com.aspose.words/chartseriesgroup/) - A [ChartSeriesGroup](../../com.aspose.words/chartseriesgroup/) at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Returns the number of series groups in this collection.

 **Examples:** 

Show how to remove secondary axis.

```

 Document doc = new Document(getMyDir() + "Combo chart.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Chart chart = shape.getChart();
 ChartSeriesGroupCollection seriesGroups = chart.getSeriesGroups();

 // Find secondary axis and remove from the collection.
 for (int i = 0; i < seriesGroups.getCount(); i++)
     if (seriesGroups.get(i).getAxisGroup() == AxisGroup.SECONDARY)
         seriesGroups.removeAt(i);
 
```

**Returns:**
int - The number of series groups in this collection.
### iterator() {#iterator}
```
public Iterator iterator()
```


Returns an enumerator object.

**Returns:**
java.util.Iterator
### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Removes a series group at the specified index. All child series will be removed from the chart.

 **Examples:** 

Show how to remove secondary axis.

```

 Document doc = new Document(getMyDir() + "Combo chart.docx");

 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Chart chart = shape.getChart();
 ChartSeriesGroupCollection seriesGroups = chart.getSeriesGroups();

 // Find secondary axis and remove from the collection.
 for (int i = 0; i < seriesGroups.getCount(); i++)
     if (seriesGroups.get(i).getAxisGroup() == AxisGroup.SECONDARY)
         seriesGroups.removeAt(i);
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

