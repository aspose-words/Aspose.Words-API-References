---
title: ChartLegendEntryCollection
linktitle: ChartLegendEntryCollection
second_title: Aspose.Words for Java
description: Represents a collection of chart legend entries in Java.
type: docs
weight: 75
url: /java/com.aspose.words/chartlegendentrycollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartLegendEntryCollection implements Iterable
```

Represents a collection of chart legend entries.

To learn more, visit the [ Working with Charts ][Working with Charts] documentation article.

 **Examples:** 

Shows how to work with a legend entry for chart series.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);

 Chart chart = shape.getChart();
 ChartSeriesCollection series = chart.getSeries();
 series.clear();

 String[] categories = new String[] { "AW Category 1", "AW Category 2" };

 ChartSeries series1 = series.add("Series 1", categories, new double[] { 1.0, 2.0 });
 series.add("Series 2", categories, new double[] { 3.0, 4.0 });
 series.add("Series 3", categories, new double[] { 5.0, 6.0 });
 series.add("Series 4", categories, new double[] { 0.0, 0.0 });

 ChartLegendEntryCollection legendEntries = chart.getLegend().getLegendEntries();
 legendEntries.get(3).isHidden(true);

 doc.save(getArtifactsDir() + "Charts.LegendEntries.docx");
 
```


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## Methods

| Method | Description |
| --- | --- |
| [get(int index)](#get-int) | Returns [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) for the specified index. |
| [getCount()](#getCount) | Returns the number of [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) in this collection. |
| [iterator()](#iterator) | Returns an enumerator object. |
### get(int index) {#get-int}
```
public ChartLegendEntry get(int index)
```


Returns [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) for the specified index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

**Returns:**
[ChartLegendEntry](../../com.aspose.words/chartlegendentry/) - [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) for the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Returns the number of [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) in this collection.

**Returns:**
int - The number of [ChartLegendEntry](../../com.aspose.words/chartlegendentry/) in this collection.
### iterator() {#iterator}
```
public Iterator iterator()
```


Returns an enumerator object.

**Returns:**
java.util.Iterator
