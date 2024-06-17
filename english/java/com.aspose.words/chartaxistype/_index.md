---
title: ChartAxisType
linktitle: ChartAxisType
second_title: Aspose.Words for Java
description: Specifies type of chart axis in Java.
type: docs
weight: 67
url: /java/com.aspose.words/chartaxistype/
---

**Inheritance:**
java.lang.Object
```
public class ChartAxisType
```

Specifies type of chart axis.

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
## Fields

| Field | Description |
| --- | --- |
| [CATEGORY](#CATEGORY) | Category axis of a chart. |
| [SERIES](#SERIES) | Series axis of a chart. |
| [VALUE](#VALUE) | Value axis of a chart. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String chartAxisTypeName)](#fromName-java.lang.String) |  |
| [getName(int chartAxisType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartAxisType)](#toString-int) |  |
### CATEGORY {#CATEGORY}
```
public static int CATEGORY
```


Category axis of a chart.

### SERIES {#SERIES}
```
public static int SERIES
```


Series axis of a chart.

### VALUE {#VALUE}
```
public static int VALUE
```


Value axis of a chart.

### length {#length}
```
public static int length
```


### fromName(String chartAxisTypeName) {#fromName-java.lang.String}
```
public static int fromName(String chartAxisTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| chartAxisTypeName | java.lang.String |  |

**Returns:**
int
### getName(int chartAxisType) {#getName-int}
```
public static String getName(int chartAxisType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| chartAxisType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int chartAxisType) {#toString-int}
```
public static String toString(int chartAxisType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| chartAxisType | int |  |

**Returns:**
java.lang.String
