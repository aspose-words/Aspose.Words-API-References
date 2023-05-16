---
title: ChartType
linktitle: ChartType
second_title: Aspose.Words for Java
description: Specifies type of a chart in Java.
type: docs
weight: 75
url: /java/com.aspose.words/charttype/
---

**Inheritance:**
java.lang.Object
```
public class ChartType
```

Specifies type of a chart.

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
| [AREA](#AREA) | Area chart. |
| [AREA_3_D](#AREA-3-D) | 3D Area chart. |
| [AREA_3_D_PERCENT_STACKED](#AREA-3-D-PERCENT-STACKED) | 3D 100% Stacked Area chart. |
| [AREA_3_D_STACKED](#AREA-3-D-STACKED) | 3D Stacked Area chart. |
| [AREA_PERCENT_STACKED](#AREA-PERCENT-STACKED) | 100% Stacked Area chart. |
| [AREA_STACKED](#AREA-STACKED) | Stacked Area chart. |
| [BAR](#BAR) | Bar chart. |
| [BAR_3_D](#BAR-3-D) | 3D Bar chart. |
| [BAR_3_D_PERCENT_STACKED](#BAR-3-D-PERCENT-STACKED) | 3D 100% Stacked Bar chart. |
| [BAR_3_D_STACKED](#BAR-3-D-STACKED) | 3D Stacked Bar chart. |
| [BAR_PERCENT_STACKED](#BAR-PERCENT-STACKED) | 100% Stacked Bar chart. |
| [BAR_STACKED](#BAR-STACKED) | Stacked Bar chart. |
| [BUBBLE](#BUBBLE) | Bubble chart. |
| [BUBBLE_3_D](#BUBBLE-3-D) | 3D Bubble chart. |
| [COLUMN](#COLUMN) | Column chart. |
| [COLUMN_3_D](#COLUMN-3-D) | 3D Column chart. |
| [COLUMN_3_D_CLUSTERED](#COLUMN-3-D-CLUSTERED) | 3D Clustered Column chart. |
| [COLUMN_3_D_PERCENT_STACKED](#COLUMN-3-D-PERCENT-STACKED) | 3D 100% Stacked Column chart. |
| [COLUMN_3_D_STACKED](#COLUMN-3-D-STACKED) | 3D Stacked Column chart. |
| [COLUMN_PERCENT_STACKED](#COLUMN-PERCENT-STACKED) | 100% Stacked Column chart. |
| [COLUMN_STACKED](#COLUMN-STACKED) | Stacked Column chart. |
| [DOUGHNUT](#DOUGHNUT) | Doughnut chart. |
| [LINE](#LINE) | Line chart. |
| [LINE_3_D](#LINE-3-D) | 3D Line chart. |
| [LINE_PERCENT_STACKED](#LINE-PERCENT-STACKED) | 100% Stacked Line chart. |
| [LINE_STACKED](#LINE-STACKED) | Stacked Line chart. |
| [PIE](#PIE) | Pie chart. |
| [PIE_3_D](#PIE-3-D) | 3D Pie chart. |
| [PIE_OF_BAR](#PIE-OF-BAR) | Pie of Bar chart. |
| [PIE_OF_PIE](#PIE-OF-PIE) | Pie of Pie chart. |
| [RADAR](#RADAR) | Radar chart. |
| [SCATTER](#SCATTER) | Scatter chart. |
| [STOCK](#STOCK) | Stock chart. |
| [SURFACE](#SURFACE) | Surface chart. |
| [SURFACE_3_D](#SURFACE-3-D) | 3D Surface chart. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String chartTypeName)](#fromName-java.lang.String) |  |
| [getName(int chartType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartType)](#toString-int) |  |
### AREA {#AREA}
```
public static int AREA
```


Area chart.

### AREA_3_D {#AREA-3-D}
```
public static int AREA_3_D
```


3D Area chart.

### AREA_3_D_PERCENT_STACKED {#AREA-3-D-PERCENT-STACKED}
```
public static int AREA_3_D_PERCENT_STACKED
```


3D 100% Stacked Area chart.

### AREA_3_D_STACKED {#AREA-3-D-STACKED}
```
public static int AREA_3_D_STACKED
```


3D Stacked Area chart.

### AREA_PERCENT_STACKED {#AREA-PERCENT-STACKED}
```
public static int AREA_PERCENT_STACKED
```


100% Stacked Area chart.

### AREA_STACKED {#AREA-STACKED}
```
public static int AREA_STACKED
```


Stacked Area chart.

### BAR {#BAR}
```
public static int BAR
```


Bar chart.

### BAR_3_D {#BAR-3-D}
```
public static int BAR_3_D
```


3D Bar chart.

### BAR_3_D_PERCENT_STACKED {#BAR-3-D-PERCENT-STACKED}
```
public static int BAR_3_D_PERCENT_STACKED
```


3D 100% Stacked Bar chart.

### BAR_3_D_STACKED {#BAR-3-D-STACKED}
```
public static int BAR_3_D_STACKED
```


3D Stacked Bar chart.

### BAR_PERCENT_STACKED {#BAR-PERCENT-STACKED}
```
public static int BAR_PERCENT_STACKED
```


100% Stacked Bar chart.

### BAR_STACKED {#BAR-STACKED}
```
public static int BAR_STACKED
```


Stacked Bar chart.

### BUBBLE {#BUBBLE}
```
public static int BUBBLE
```


Bubble chart.

### BUBBLE_3_D {#BUBBLE-3-D}
```
public static int BUBBLE_3_D
```


3D Bubble chart.

### COLUMN {#COLUMN}
```
public static int COLUMN
```


Column chart.

### COLUMN_3_D {#COLUMN-3-D}
```
public static int COLUMN_3_D
```


3D Column chart.

### COLUMN_3_D_CLUSTERED {#COLUMN-3-D-CLUSTERED}
```
public static int COLUMN_3_D_CLUSTERED
```


3D Clustered Column chart.

### COLUMN_3_D_PERCENT_STACKED {#COLUMN-3-D-PERCENT-STACKED}
```
public static int COLUMN_3_D_PERCENT_STACKED
```


3D 100% Stacked Column chart.

### COLUMN_3_D_STACKED {#COLUMN-3-D-STACKED}
```
public static int COLUMN_3_D_STACKED
```


3D Stacked Column chart.

### COLUMN_PERCENT_STACKED {#COLUMN-PERCENT-STACKED}
```
public static int COLUMN_PERCENT_STACKED
```


100% Stacked Column chart.

### COLUMN_STACKED {#COLUMN-STACKED}
```
public static int COLUMN_STACKED
```


Stacked Column chart.

### DOUGHNUT {#DOUGHNUT}
```
public static int DOUGHNUT
```


Doughnut chart.

### LINE {#LINE}
```
public static int LINE
```


Line chart.

### LINE_3_D {#LINE-3-D}
```
public static int LINE_3_D
```


3D Line chart.

### LINE_PERCENT_STACKED {#LINE-PERCENT-STACKED}
```
public static int LINE_PERCENT_STACKED
```


100% Stacked Line chart.

### LINE_STACKED {#LINE-STACKED}
```
public static int LINE_STACKED
```


Stacked Line chart.

### PIE {#PIE}
```
public static int PIE
```


Pie chart.

### PIE_3_D {#PIE-3-D}
```
public static int PIE_3_D
```


3D Pie chart.

### PIE_OF_BAR {#PIE-OF-BAR}
```
public static int PIE_OF_BAR
```


Pie of Bar chart.

### PIE_OF_PIE {#PIE-OF-PIE}
```
public static int PIE_OF_PIE
```


Pie of Pie chart.

### RADAR {#RADAR}
```
public static int RADAR
```


Radar chart.

### SCATTER {#SCATTER}
```
public static int SCATTER
```


Scatter chart.

### STOCK {#STOCK}
```
public static int STOCK
```


Stock chart.

### SURFACE {#SURFACE}
```
public static int SURFACE
```


Surface chart.

### SURFACE_3_D {#SURFACE-3-D}
```
public static int SURFACE_3_D
```


3D Surface chart.

### length {#length}
```
public static int length
```


### fromName(String chartTypeName) {#fromName-java.lang.String}
```
public static int fromName(String chartTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| chartTypeName | java.lang.String |  |

**Returns:**
int
### getName(int chartType) {#getName-int}
```
public static String getName(int chartType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| chartType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int chartType) {#toString-int}
```
public static String toString(int chartType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| chartType | int |  |

**Returns:**
java.lang.String
