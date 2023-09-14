---
title: ChartSeriesCollection
linktitle: ChartSeriesCollection
second_title: Aspose.Words for Java
description: Represents collection of a ChartSeries in Java.
type: docs
weight: 74
url: /java/com.aspose.words/chartseriescollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartSeriesCollection implements Iterable
```

Represents collection of a [ChartSeries](../../com.aspose.words/chartseries/).

To learn more, visit the [ Working with Charts ][Working with Charts] documentation article.

 **Examples:** 

Shows how to add and remove series data in a chart.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a column chart that will contain three series of demo data by default.
 Shape chartShape = builder.insertChart(ChartType.COLUMN, 400.0, 300.0);
 Chart chart = chartShape.getChart();

 // Each series has four decimal values: one for each of the four categories.
 // Four clusters of three columns will represent this data.
 ChartSeriesCollection chartData = chart.getSeries();

 Assert.assertEquals(3, chartData.getCount());

 // Print the name of every series in the chart.
 Iterator enumerator = chart.getSeries().iterator();
 while (enumerator.hasNext()) {
     System.out.println(enumerator.next().getName());
 }

 // These are the names of the categories in the chart.
 String[] categories = {"Category 1", "Category 2", "Category 3", "Category 4"};

 // We can add a series with new values for existing categories.
 // This chart will now contain four clusters of four columns.
 chart.getSeries().add("Series 4", categories, new double[]{4.4, 7.0, 3.5, 2.1});
 // A chart series can also be removed by index, like this.
 // This will remove one of the three demo series that came with the chart.
 chartData.removeAt(2);

 Assert.assertFalse(IterableUtils.matchesAny(chartData, s -> s.getName() == "Series 3"));
 // We can also clear all the chart's data at once with this method.
 // When creating a new chart, this is the way to wipe all the demo data
 // before we can begin working on a blank chart.
 chartData.clear();
 
```


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## Methods

| Method | Description |
| --- | --- |
| [add(String seriesName, double[] xValues, double[] yValues)](#add-java.lang.String-double---double) | Adds new [ChartSeries](../../com.aspose.words/chartseries/) to this collection. |
| [add(String seriesName, double[] xValues, double[] yValues, double[] bubbleSizes)](#add-java.lang.String-double---double---double) | Adds new [ChartSeries](../../com.aspose.words/chartseries/) to this collection. |
| [add(String seriesName, String[] categories, double[] values)](#add-java.lang.String-java.lang.String---double) | Adds new [ChartSeries](../../com.aspose.words/chartseries/) to this collection. |
| [add(String seriesName, Date[] dates, double[] values)](#add-java.lang.String-java.util.Date---double) | Adds new [ChartSeries](../../com.aspose.words/chartseries/) to this collection. |
| [clear()](#clear) | Removes all [ChartSeries](../../com.aspose.words/chartseries/) from this collection. |
| [get(int index)](#get-int) | Returns a [ChartSeries](../../com.aspose.words/chartseries/) at the specified index. |
| [getCount()](#getCount) | Returns the number of [ChartSeries](../../com.aspose.words/chartseries/) in this collection. |
| [iterator()](#iterator) | Returns an enumerator object. |
| [removeAt(int index)](#removeAt-int) | Removes a [ChartSeries](../../com.aspose.words/chartseries/) at the specified index. |
### add(String seriesName, double[] xValues, double[] yValues) {#add-java.lang.String-double---double}
```
public ChartSeries add(String seriesName, double[] xValues, double[] yValues)
```


Adds new [ChartSeries](../../com.aspose.words/chartseries/) to this collection. Use this method to add series to any type of Scatter charts.

 **Examples:** 

Shows how to create an appropriate type of chart series for a graph type.

```

 public void chartSeriesCollection() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // There are several ways of populating a chart's series collection.
     // Different series schemas are intended for different chart types.
     // 1 -  Column chart with columns grouped and banded along the X-axis by category:
     Chart chart = appendChart(builder, ChartType.COLUMN, 500.0, 300.0);

     String[] categories = {"Category 1", "Category 2", "Category 3"};

     // Insert two series of decimal values containing a value for each respective category.
     // This column chart will have three groups, each with two columns.
     chart.getSeries().add("Series 1", categories, new double[]{76.6, 82.1, 91.6});
     chart.getSeries().add("Series 2", categories, new double[]{64.2, 79.5, 94.0});

     // Categories are distributed along the X-axis, and values are distributed along the Y-axis.
     Assert.assertEquals(ChartAxisType.CATEGORY, chart.getAxisX().getType());
     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisY().getType());

     // 2 -  Area chart with dates distributed along the X-axis:
     chart = appendChart(builder, ChartType.AREA, 500.0, 300.0);

     Date[] dates = {DocumentHelper.createDate(2014, 3, 31),
             DocumentHelper.createDate(2017, 1, 23),
             DocumentHelper.createDate(2017, 6, 18),
             DocumentHelper.createDate(2019, 11, 22),
             DocumentHelper.createDate(2020, 9, 7)
     };

     // Insert a series with a decimal value for each respective date.
     // The dates will be distributed along a linear X-axis,
     // and the values added to this series will create data points.
     chart.getSeries().add("Series 1", dates, new double[]{15.8, 21.5, 22.9, 28.7, 33.1});

     Assert.assertEquals(ChartAxisType.CATEGORY, chart.getAxisX().getType());
     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisY().getType());

     // 3 -  2D scatter plot:
     chart = appendChart(builder, ChartType.SCATTER, 500.0, 300.0);

     // Each series will need two decimal arrays of equal length.
     // The first array contains X-values, and the second contains corresponding Y-values
     // of data points on the chart's graph.
     chart.getSeries().add("Series 1",
             new double[]{3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6},
             new double[]{3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9});
     chart.getSeries().add("Series 2",
             new double[]{2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3},
             new double[]{7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6});

     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisX().getType());
     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisY().getType());

     // 4 -  Bubble chart:
     chart = appendChart(builder, ChartType.BUBBLE, 500.0, 300.0);

     // Each series will need three decimal arrays of equal length.
     // The first array contains X-values, the second contains corresponding Y-values,
     // and the third contains diameters for each of the graph's data points.
     chart.getSeries().add("Series 1",
             new double[]{1.1, 5.0, 9.8},
             new double[]{1.2, 4.9, 9.9},
             new double[]{2.0, 4.0, 8.0});

     doc.save(getArtifactsDir() + "Charts.ChartSeriesCollection.docx");
 }

 /// 
 /// Insert a chart using a document builder of a specified ChartType, width and height, and remove its demo data.
 /// 
 private static Chart appendChart(DocumentBuilder builder, int chartType, double width, double height) throws Exception {
     Shape chartShape = builder.insertChart(chartType, width, height);
     Chart chart = chartShape.getChart();
     chart.getSeries().clear();
     return chart;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| seriesName | java.lang.String |  |
| xValues | double[] |  |
| yValues | double[] |  |

**Returns:**
[ChartSeries](../../com.aspose.words/chartseries/) - Recently added [ChartSeries](../../com.aspose.words/chartseries/) object.
### add(String seriesName, double[] xValues, double[] yValues, double[] bubbleSizes) {#add-java.lang.String-double---double---double}
```
public ChartSeries add(String seriesName, double[] xValues, double[] yValues, double[] bubbleSizes)
```


Adds new [ChartSeries](../../com.aspose.words/chartseries/) to this collection. Use this method to add series to any type of Bubble charts.

 **Examples:** 

Shows how to create an appropriate type of chart series for a graph type.

```

 public void chartSeriesCollection() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // There are several ways of populating a chart's series collection.
     // Different series schemas are intended for different chart types.
     // 1 -  Column chart with columns grouped and banded along the X-axis by category:
     Chart chart = appendChart(builder, ChartType.COLUMN, 500.0, 300.0);

     String[] categories = {"Category 1", "Category 2", "Category 3"};

     // Insert two series of decimal values containing a value for each respective category.
     // This column chart will have three groups, each with two columns.
     chart.getSeries().add("Series 1", categories, new double[]{76.6, 82.1, 91.6});
     chart.getSeries().add("Series 2", categories, new double[]{64.2, 79.5, 94.0});

     // Categories are distributed along the X-axis, and values are distributed along the Y-axis.
     Assert.assertEquals(ChartAxisType.CATEGORY, chart.getAxisX().getType());
     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisY().getType());

     // 2 -  Area chart with dates distributed along the X-axis:
     chart = appendChart(builder, ChartType.AREA, 500.0, 300.0);

     Date[] dates = {DocumentHelper.createDate(2014, 3, 31),
             DocumentHelper.createDate(2017, 1, 23),
             DocumentHelper.createDate(2017, 6, 18),
             DocumentHelper.createDate(2019, 11, 22),
             DocumentHelper.createDate(2020, 9, 7)
     };

     // Insert a series with a decimal value for each respective date.
     // The dates will be distributed along a linear X-axis,
     // and the values added to this series will create data points.
     chart.getSeries().add("Series 1", dates, new double[]{15.8, 21.5, 22.9, 28.7, 33.1});

     Assert.assertEquals(ChartAxisType.CATEGORY, chart.getAxisX().getType());
     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisY().getType());

     // 3 -  2D scatter plot:
     chart = appendChart(builder, ChartType.SCATTER, 500.0, 300.0);

     // Each series will need two decimal arrays of equal length.
     // The first array contains X-values, and the second contains corresponding Y-values
     // of data points on the chart's graph.
     chart.getSeries().add("Series 1",
             new double[]{3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6},
             new double[]{3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9});
     chart.getSeries().add("Series 2",
             new double[]{2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3},
             new double[]{7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6});

     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisX().getType());
     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisY().getType());

     // 4 -  Bubble chart:
     chart = appendChart(builder, ChartType.BUBBLE, 500.0, 300.0);

     // Each series will need three decimal arrays of equal length.
     // The first array contains X-values, the second contains corresponding Y-values,
     // and the third contains diameters for each of the graph's data points.
     chart.getSeries().add("Series 1",
             new double[]{1.1, 5.0, 9.8},
             new double[]{1.2, 4.9, 9.9},
             new double[]{2.0, 4.0, 8.0});

     doc.save(getArtifactsDir() + "Charts.ChartSeriesCollection.docx");
 }

 /// 
 /// Insert a chart using a document builder of a specified ChartType, width and height, and remove its demo data.
 /// 
 private static Chart appendChart(DocumentBuilder builder, int chartType, double width, double height) throws Exception {
     Shape chartShape = builder.insertChart(chartType, width, height);
     Chart chart = chartShape.getChart();
     chart.getSeries().clear();
     return chart;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| seriesName | java.lang.String |  |
| xValues | double[] |  |
| yValues | double[] |  |
| bubbleSizes | double[] |  |

**Returns:**
[ChartSeries](../../com.aspose.words/chartseries/) - Recently added [ChartSeries](../../com.aspose.words/chartseries/) object.
### add(String seriesName, String[] categories, double[] values) {#add-java.lang.String-java.lang.String---double}
```
public ChartSeries add(String seriesName, String[] categories, double[] values)
```


Adds new [ChartSeries](../../com.aspose.words/chartseries/) to this collection. Use this method to add series to any type of Bar, Column, Line and Surface charts.

 **Examples:** 

Shows how to create an appropriate type of chart series for a graph type.

```

 public void chartSeriesCollection() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // There are several ways of populating a chart's series collection.
     // Different series schemas are intended for different chart types.
     // 1 -  Column chart with columns grouped and banded along the X-axis by category:
     Chart chart = appendChart(builder, ChartType.COLUMN, 500.0, 300.0);

     String[] categories = {"Category 1", "Category 2", "Category 3"};

     // Insert two series of decimal values containing a value for each respective category.
     // This column chart will have three groups, each with two columns.
     chart.getSeries().add("Series 1", categories, new double[]{76.6, 82.1, 91.6});
     chart.getSeries().add("Series 2", categories, new double[]{64.2, 79.5, 94.0});

     // Categories are distributed along the X-axis, and values are distributed along the Y-axis.
     Assert.assertEquals(ChartAxisType.CATEGORY, chart.getAxisX().getType());
     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisY().getType());

     // 2 -  Area chart with dates distributed along the X-axis:
     chart = appendChart(builder, ChartType.AREA, 500.0, 300.0);

     Date[] dates = {DocumentHelper.createDate(2014, 3, 31),
             DocumentHelper.createDate(2017, 1, 23),
             DocumentHelper.createDate(2017, 6, 18),
             DocumentHelper.createDate(2019, 11, 22),
             DocumentHelper.createDate(2020, 9, 7)
     };

     // Insert a series with a decimal value for each respective date.
     // The dates will be distributed along a linear X-axis,
     // and the values added to this series will create data points.
     chart.getSeries().add("Series 1", dates, new double[]{15.8, 21.5, 22.9, 28.7, 33.1});

     Assert.assertEquals(ChartAxisType.CATEGORY, chart.getAxisX().getType());
     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisY().getType());

     // 3 -  2D scatter plot:
     chart = appendChart(builder, ChartType.SCATTER, 500.0, 300.0);

     // Each series will need two decimal arrays of equal length.
     // The first array contains X-values, and the second contains corresponding Y-values
     // of data points on the chart's graph.
     chart.getSeries().add("Series 1",
             new double[]{3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6},
             new double[]{3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9});
     chart.getSeries().add("Series 2",
             new double[]{2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3},
             new double[]{7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6});

     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisX().getType());
     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisY().getType());

     // 4 -  Bubble chart:
     chart = appendChart(builder, ChartType.BUBBLE, 500.0, 300.0);

     // Each series will need three decimal arrays of equal length.
     // The first array contains X-values, the second contains corresponding Y-values,
     // and the third contains diameters for each of the graph's data points.
     chart.getSeries().add("Series 1",
             new double[]{1.1, 5.0, 9.8},
             new double[]{1.2, 4.9, 9.9},
             new double[]{2.0, 4.0, 8.0});

     doc.save(getArtifactsDir() + "Charts.ChartSeriesCollection.docx");
 }

 /// 
 /// Insert a chart using a document builder of a specified ChartType, width and height, and remove its demo data.
 /// 
 private static Chart appendChart(DocumentBuilder builder, int chartType, double width, double height) throws Exception {
     Shape chartShape = builder.insertChart(chartType, width, height);
     Chart chart = chartShape.getChart();
     chart.getSeries().clear();
     return chart;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| seriesName | java.lang.String |  |
| categories | java.lang.String[] |  |
| values | double[] |  |

**Returns:**
[ChartSeries](../../com.aspose.words/chartseries/) - Recently added [ChartSeries](../../com.aspose.words/chartseries/) object.
### add(String seriesName, Date[] dates, double[] values) {#add-java.lang.String-java.util.Date---double}
```
public ChartSeries add(String seriesName, Date[] dates, double[] values)
```


Adds new [ChartSeries](../../com.aspose.words/chartseries/) to this collection. Use this method to add series to any type of Area, Radar and Stock charts.

 **Examples:** 

Shows how to create an appropriate type of chart series for a graph type.

```

 public void chartSeriesCollection() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // There are several ways of populating a chart's series collection.
     // Different series schemas are intended for different chart types.
     // 1 -  Column chart with columns grouped and banded along the X-axis by category:
     Chart chart = appendChart(builder, ChartType.COLUMN, 500.0, 300.0);

     String[] categories = {"Category 1", "Category 2", "Category 3"};

     // Insert two series of decimal values containing a value for each respective category.
     // This column chart will have three groups, each with two columns.
     chart.getSeries().add("Series 1", categories, new double[]{76.6, 82.1, 91.6});
     chart.getSeries().add("Series 2", categories, new double[]{64.2, 79.5, 94.0});

     // Categories are distributed along the X-axis, and values are distributed along the Y-axis.
     Assert.assertEquals(ChartAxisType.CATEGORY, chart.getAxisX().getType());
     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisY().getType());

     // 2 -  Area chart with dates distributed along the X-axis:
     chart = appendChart(builder, ChartType.AREA, 500.0, 300.0);

     Date[] dates = {DocumentHelper.createDate(2014, 3, 31),
             DocumentHelper.createDate(2017, 1, 23),
             DocumentHelper.createDate(2017, 6, 18),
             DocumentHelper.createDate(2019, 11, 22),
             DocumentHelper.createDate(2020, 9, 7)
     };

     // Insert a series with a decimal value for each respective date.
     // The dates will be distributed along a linear X-axis,
     // and the values added to this series will create data points.
     chart.getSeries().add("Series 1", dates, new double[]{15.8, 21.5, 22.9, 28.7, 33.1});

     Assert.assertEquals(ChartAxisType.CATEGORY, chart.getAxisX().getType());
     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisY().getType());

     // 3 -  2D scatter plot:
     chart = appendChart(builder, ChartType.SCATTER, 500.0, 300.0);

     // Each series will need two decimal arrays of equal length.
     // The first array contains X-values, and the second contains corresponding Y-values
     // of data points on the chart's graph.
     chart.getSeries().add("Series 1",
             new double[]{3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6},
             new double[]{3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9});
     chart.getSeries().add("Series 2",
             new double[]{2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3},
             new double[]{7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6});

     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisX().getType());
     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisY().getType());

     // 4 -  Bubble chart:
     chart = appendChart(builder, ChartType.BUBBLE, 500.0, 300.0);

     // Each series will need three decimal arrays of equal length.
     // The first array contains X-values, the second contains corresponding Y-values,
     // and the third contains diameters for each of the graph's data points.
     chart.getSeries().add("Series 1",
             new double[]{1.1, 5.0, 9.8},
             new double[]{1.2, 4.9, 9.9},
             new double[]{2.0, 4.0, 8.0});

     doc.save(getArtifactsDir() + "Charts.ChartSeriesCollection.docx");
 }

 /// 
 /// Insert a chart using a document builder of a specified ChartType, width and height, and remove its demo data.
 /// 
 private static Chart appendChart(DocumentBuilder builder, int chartType, double width, double height) throws Exception {
     Shape chartShape = builder.insertChart(chartType, width, height);
     Chart chart = chartShape.getChart();
     chart.getSeries().clear();
     return chart;
 }
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| seriesName | java.lang.String |  |
| dates | java.util.Date[] |  |
| values | double[] |  |

**Returns:**
[ChartSeries](../../com.aspose.words/chartseries/)
### clear() {#clear}
```
public void clear()
```


Removes all [ChartSeries](../../com.aspose.words/chartseries/) from this collection.

 **Examples:** 

Shows how to add and remove series data in a chart.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a column chart that will contain three series of demo data by default.
 Shape chartShape = builder.insertChart(ChartType.COLUMN, 400.0, 300.0);
 Chart chart = chartShape.getChart();

 // Each series has four decimal values: one for each of the four categories.
 // Four clusters of three columns will represent this data.
 ChartSeriesCollection chartData = chart.getSeries();

 Assert.assertEquals(3, chartData.getCount());

 // Print the name of every series in the chart.
 Iterator enumerator = chart.getSeries().iterator();
 while (enumerator.hasNext()) {
     System.out.println(enumerator.next().getName());
 }

 // These are the names of the categories in the chart.
 String[] categories = {"Category 1", "Category 2", "Category 3", "Category 4"};

 // We can add a series with new values for existing categories.
 // This chart will now contain four clusters of four columns.
 chart.getSeries().add("Series 4", categories, new double[]{4.4, 7.0, 3.5, 2.1});
 // A chart series can also be removed by index, like this.
 // This will remove one of the three demo series that came with the chart.
 chartData.removeAt(2);

 Assert.assertFalse(IterableUtils.matchesAny(chartData, s -> s.getName() == "Series 3"));
 // We can also clear all the chart's data at once with this method.
 // When creating a new chart, this is the way to wipe all the demo data
 // before we can begin working on a blank chart.
 chartData.clear();
 
```

### get(int index) {#get-int}
```
public ChartSeries get(int index)
```


Returns a [ChartSeries](../../com.aspose.words/chartseries/) at the specified index.

 **Remarks:** 

The index is zero-based.

Negative indexes are allowed and indicate access from the back of the collection. For example -1 means the last item, -2 means the second before last and so on.

If index is greater than or equal to the number of items in the list, this returns a null reference.

If index is negative and its absolute value is greater than the number of items in the list, this returns a null reference.

 **Examples:** 

Shows how to add and remove series data in a chart.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a column chart that will contain three series of demo data by default.
 Shape chartShape = builder.insertChart(ChartType.COLUMN, 400.0, 300.0);
 Chart chart = chartShape.getChart();

 // Each series has four decimal values: one for each of the four categories.
 // Four clusters of three columns will represent this data.
 ChartSeriesCollection chartData = chart.getSeries();

 Assert.assertEquals(3, chartData.getCount());

 // Print the name of every series in the chart.
 Iterator enumerator = chart.getSeries().iterator();
 while (enumerator.hasNext()) {
     System.out.println(enumerator.next().getName());
 }

 // These are the names of the categories in the chart.
 String[] categories = {"Category 1", "Category 2", "Category 3", "Category 4"};

 // We can add a series with new values for existing categories.
 // This chart will now contain four clusters of four columns.
 chart.getSeries().add("Series 4", categories, new double[]{4.4, 7.0, 3.5, 2.1});
 // A chart series can also be removed by index, like this.
 // This will remove one of the three demo series that came with the chart.
 chartData.removeAt(2);

 Assert.assertFalse(IterableUtils.matchesAny(chartData, s -> s.getName() == "Series 3"));
 // We can also clear all the chart's data at once with this method.
 // When creating a new chart, this is the way to wipe all the demo data
 // before we can begin working on a blank chart.
 chartData.clear();
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | An index into the collection. |

**Returns:**
[ChartSeries](../../com.aspose.words/chartseries/) - A [ChartSeries](../../com.aspose.words/chartseries/) at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Returns the number of [ChartSeries](../../com.aspose.words/chartseries/) in this collection.

 **Examples:** 

Shows how to add and remove series data in a chart.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a column chart that will contain three series of demo data by default.
 Shape chartShape = builder.insertChart(ChartType.COLUMN, 400.0, 300.0);
 Chart chart = chartShape.getChart();

 // Each series has four decimal values: one for each of the four categories.
 // Four clusters of three columns will represent this data.
 ChartSeriesCollection chartData = chart.getSeries();

 Assert.assertEquals(3, chartData.getCount());

 // Print the name of every series in the chart.
 Iterator enumerator = chart.getSeries().iterator();
 while (enumerator.hasNext()) {
     System.out.println(enumerator.next().getName());
 }

 // These are the names of the categories in the chart.
 String[] categories = {"Category 1", "Category 2", "Category 3", "Category 4"};

 // We can add a series with new values for existing categories.
 // This chart will now contain four clusters of four columns.
 chart.getSeries().add("Series 4", categories, new double[]{4.4, 7.0, 3.5, 2.1});
 // A chart series can also be removed by index, like this.
 // This will remove one of the three demo series that came with the chart.
 chartData.removeAt(2);

 Assert.assertFalse(IterableUtils.matchesAny(chartData, s -> s.getName() == "Series 3"));
 // We can also clear all the chart's data at once with this method.
 // When creating a new chart, this is the way to wipe all the demo data
 // before we can begin working on a blank chart.
 chartData.clear();
 
```

**Returns:**
int - The number of [ChartSeries](../../com.aspose.words/chartseries/) in this collection.
### iterator() {#iterator}
```
public Iterator iterator()
```


Returns an enumerator object.

 **Examples:** 

Shows how to add and remove series data in a chart.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a column chart that will contain three series of demo data by default.
 Shape chartShape = builder.insertChart(ChartType.COLUMN, 400.0, 300.0);
 Chart chart = chartShape.getChart();

 // Each series has four decimal values: one for each of the four categories.
 // Four clusters of three columns will represent this data.
 ChartSeriesCollection chartData = chart.getSeries();

 Assert.assertEquals(3, chartData.getCount());

 // Print the name of every series in the chart.
 Iterator enumerator = chart.getSeries().iterator();
 while (enumerator.hasNext()) {
     System.out.println(enumerator.next().getName());
 }

 // These are the names of the categories in the chart.
 String[] categories = {"Category 1", "Category 2", "Category 3", "Category 4"};

 // We can add a series with new values for existing categories.
 // This chart will now contain four clusters of four columns.
 chart.getSeries().add("Series 4", categories, new double[]{4.4, 7.0, 3.5, 2.1});
 // A chart series can also be removed by index, like this.
 // This will remove one of the three demo series that came with the chart.
 chartData.removeAt(2);

 Assert.assertFalse(IterableUtils.matchesAny(chartData, s -> s.getName() == "Series 3"));
 // We can also clear all the chart's data at once with this method.
 // When creating a new chart, this is the way to wipe all the demo data
 // before we can begin working on a blank chart.
 chartData.clear();
 
```

**Returns:**
java.util.Iterator
### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Removes a [ChartSeries](../../com.aspose.words/chartseries/) at the specified index.

 **Examples:** 

Shows how to add and remove series data in a chart.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a column chart that will contain three series of demo data by default.
 Shape chartShape = builder.insertChart(ChartType.COLUMN, 400.0, 300.0);
 Chart chart = chartShape.getChart();

 // Each series has four decimal values: one for each of the four categories.
 // Four clusters of three columns will represent this data.
 ChartSeriesCollection chartData = chart.getSeries();

 Assert.assertEquals(3, chartData.getCount());

 // Print the name of every series in the chart.
 Iterator enumerator = chart.getSeries().iterator();
 while (enumerator.hasNext()) {
     System.out.println(enumerator.next().getName());
 }

 // These are the names of the categories in the chart.
 String[] categories = {"Category 1", "Category 2", "Category 3", "Category 4"};

 // We can add a series with new values for existing categories.
 // This chart will now contain four clusters of four columns.
 chart.getSeries().add("Series 4", categories, new double[]{4.4, 7.0, 3.5, 2.1});
 // A chart series can also be removed by index, like this.
 // This will remove one of the three demo series that came with the chart.
 chartData.removeAt(2);

 Assert.assertFalse(IterableUtils.matchesAny(chartData, s -> s.getName() == "Series 3"));
 // We can also clear all the chart's data at once with this method.
 // When creating a new chart, this is the way to wipe all the demo data
 // before we can begin working on a blank chart.
 chartData.clear();
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int | The zero-based index of the [ChartSeries](../../com.aspose.words/chartseries/) to remove. |

