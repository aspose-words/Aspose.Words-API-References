---
title: AxisCrosses
linktitle: AxisCrosses
second_title: Aspose.Words for Java
description: Specifies the possible crossing points for an axis in Java.
type: docs
weight: 19
url: /java/com.aspose.words/axiscrosses/
---

**Inheritance:**
java.lang.Object
```
public class AxisCrosses
```

Specifies the possible crossing points for an axis.

 **Examples:** 

Shows how to insert a chart and modify the appearance of its axes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a chart series with categories for the X-axis and respective numeric values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel", "GoogleDocs", "Note"},
         new double[]{640.0, 320.0, 280.0, 120.0, 150.0});

 // Chart axes have various options that can change their appearance,
 // such as their direction, major/minor unit ticks, and tick marks.
 ChartAxis xAxis = chart.getAxisX();
 xAxis.setCategoryType(AxisCategoryType.CATEGORY);
 xAxis.setCrosses(AxisCrosses.MINIMUM);
 xAxis.setReverseOrder(false);
 xAxis.setMajorTickMark(AxisTickMark.INSIDE);
 xAxis.setMinorTickMark(AxisTickMark.CROSS);
 xAxis.setMajorUnit(10.0d);
 xAxis.setMinorUnit(15.0d);
 xAxis.setTickLabelOffset(50);
 xAxis.setTickLabelPosition(AxisTickLabelPosition.LOW);
 xAxis.setTickLabelSpacingIsAuto(false);
 xAxis.setTickMarkSpacing(1);

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.setTickLabelPosition(AxisTickLabelPosition.NEXT_TO_AXIS);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [AUTOMATIC](#AUTOMATIC) | The category axis crosses at the zero point of the value axis (if possible), or at the minimum value if the minimum is greater than zero, or at the maximum if the maximum is less than zero. |
| [CUSTOM](#CUSTOM) | A perpendicular axis crosses at the specified value of the axis. |
| [MAXIMUM](#MAXIMUM) | A perpendicular axis crosses at the maximum value of the axis. |
| [MINIMUM](#MINIMUM) | A perpendicular axis crosses at the minimum value of the axis. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String axisCrossesName)](#fromName-java.lang.String) |  |
| [getName(int axisCrosses)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int axisCrosses)](#toString-int) |  |
### AUTOMATIC {#AUTOMATIC}
```
public static int AUTOMATIC
```


The category axis crosses at the zero point of the value axis (if possible), or at the minimum value if the minimum is greater than zero, or at the maximum if the maximum is less than zero.

### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


A perpendicular axis crosses at the specified value of the axis.

### MAXIMUM {#MAXIMUM}
```
public static int MAXIMUM
```


A perpendicular axis crosses at the maximum value of the axis.

### MINIMUM {#MINIMUM}
```
public static int MINIMUM
```


A perpendicular axis crosses at the minimum value of the axis.

### length {#length}
```
public static int length
```


### fromName(String axisCrossesName) {#fromName-java.lang.String}
```
public static int fromName(String axisCrossesName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| axisCrossesName | java.lang.String |  |

**Returns:**
int
### getName(int axisCrosses) {#getName-int}
```
public static String getName(int axisCrosses)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| axisCrosses | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int axisCrosses) {#toString-int}
```
public static String toString(int axisCrosses)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| axisCrosses | int |  |

**Returns:**
java.lang.String
