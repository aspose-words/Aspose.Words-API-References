---
title: AxisScaleType
linktitle: AxisScaleType
second_title: Aspose.Words for Java
description: Specifies the possible scale types for an axis in Java.
type: docs
weight: 25
url: /java/com.aspose.words/axisscaletype/
---

**Inheritance:**
java.lang.Object
```
public class AxisScaleType
```

Specifies the possible scale types for an axis.

 **Examples:** 

Shows how to apply logarithmic scaling to a chart axis.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape chartShape = builder.insertChart(ChartType.SCATTER, 450.0, 300.0);
 Chart chart = chartShape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a series with X/Y coordinates for five points.
 chart.getSeries().add("Series 1",
         new double[]{1.0, 2.0, 3.0, 4.0, 5.0},
         new double[]{1.0, 20.0, 400.0, 8000.0, 160000.0});

 // The scaling of the X-axis is linear by default,
 // displaying evenly incrementing values that cover our X-value range (0, 1, 2, 3...).
 // A linear axis is not ideal for our Y-values
 // since the points with the smaller Y-values will be harder to read.
 // A logarithmic scaling with a base of 20 (1, 20, 400, 8000...)
 // will spread the plotted points, allowing us to read their values on the chart more easily.
 chart.getAxisY().getScaling().setType(AxisScaleType.LOGARITHMIC);
 chart.getAxisY().getScaling().setLogBase(20.0);

 doc.save(getArtifactsDir() + "Charts.AxisScaling.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [LINEAR](#LINEAR) | Linear scaling. |
| [LOGARITHMIC](#LOGARITHMIC) | Logarithmic scaling. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String axisScaleTypeName)](#fromName-java.lang.String) |  |
| [getName(int axisScaleType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int axisScaleType)](#toString-int) |  |
### LINEAR {#LINEAR}
```
public static int LINEAR
```


Linear scaling.

### LOGARITHMIC {#LOGARITHMIC}
```
public static int LOGARITHMIC
```


Logarithmic scaling.

### length {#length}
```
public static int length
```


### fromName(String axisScaleTypeName) {#fromName-java.lang.String}
```
public static int fromName(String axisScaleTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| axisScaleTypeName | java.lang.String |  |

**Returns:**
int
### getName(int axisScaleType) {#getName-int}
```
public static String getName(int axisScaleType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| axisScaleType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int axisScaleType) {#toString-int}
```
public static String toString(int axisScaleType)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| axisScaleType | int |  |

**Returns:**
java.lang.String
