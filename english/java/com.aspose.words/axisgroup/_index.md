---
title: AxisGroup
linktitle: AxisGroup
second_title: Aspose.Words for Java
description: Represents a type of a chart axis group in Java.
type: docs
weight: 26
url: /java/com.aspose.words/axisgroup/
---

**Inheritance:**
java.lang.Object
```
public class AxisGroup
```

Represents a type of a chart axis group.

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

 Assert.assertEquals(ChartSeriesType.LINE, newSeriesGroup.getSeriesType());

 // Add a series to the new series group.
 ChartSeries series3 =
         newSeriesGroup.getSeries().add("Series of secondary series group", categories, new double[] { 13.0, 11.0, 16.0 });
 series3.getFormat().getStroke().setWeight(3.5);

 doc.save(getArtifactsDir() + "Charts.SecondaryAxis.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [PRIMARY](#PRIMARY) | Specifies the primary axis group. |
| [SECONDARY](#SECONDARY) | Specifies the secondary axis group. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String axisGroupName)](#fromName-java.lang.String) |  |
| [getName(int axisGroup)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int axisGroup)](#toString-int) |  |
### PRIMARY {#PRIMARY}
```
public static int PRIMARY
```


Specifies the primary axis group.

### SECONDARY {#SECONDARY}
```
public static int SECONDARY
```


Specifies the secondary axis group.

### length {#length}
```
public static int length
```


### fromName(String axisGroupName) {#fromName-java.lang.String}
```
public static int fromName(String axisGroupName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| axisGroupName | java.lang.String |  |

**Returns:**
int
### getName(int axisGroup) {#getName-int}
```
public static String getName(int axisGroup)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| axisGroup | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int axisGroup) {#toString-int}
```
public static String toString(int axisGroup)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| axisGroup | int |  |

**Returns:**
java.lang.String
