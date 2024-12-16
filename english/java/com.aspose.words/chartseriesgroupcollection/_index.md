---
title: ChartSeriesGroupCollection
linktitle: ChartSeriesGroupCollection
second_title: Aspose.Words for Java
description: Represents a collection of ChartSeriesGroup objects in Java.
type: docs
weight: 87
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

 **Examples:** 

Shows how to work with the secondary axis of chart.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 450.0, 250.0);
 Chart chart = shape.getChart();
 ChartSeriesCollection series = chart.getSeries();

 // Delete default generated series.
 series.clear();

 String[] categories = new String[] { "Category 1", "Category 2", "Category 3" };
 series.add("Series 1 of primary series group", categories, new double[] { 2.0, 3.0, 4.0 });
 series.add("Series 2 of primary series group", categories, new double[] { 5.0, 2.0, 3.0 });

 // Create an additional series group, also of the line type.
 ChartSeriesGroup newSeriesGroup = chart.getSeriesGroups().add(ChartSeriesType.LINE);
 // Specify the use of secondary axes for the new series group.
 newSeriesGroup.setAxisGroup(AxisGroup.SECONDARY);
 // Hide the secondary X axis.
 newSeriesGroup.getAxisX().setHidden(true);
 // Define title of the secondary Y axis.
 newSeriesGroup.getAxisY().getTitle().setShow(true);
 newSeriesGroup.getAxisY().getTitle().setText("Secondary Y axis");

 // Add a series to the new series group.
 ChartSeries series3 =
         newSeriesGroup.getSeries().add("Series of secondary series group", categories, new double[] { 13.0, 11.0, 16.0 });
 series3.getFormat().getStroke().setWeight(3.5);

 doc.save(getArtifactsDir() + "Charts.SecondaryAxis.docx");
 
```


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

