---
title: AxisTickLabelPosition
linktitle: AxisTickLabelPosition
second_title: Aspose.Words for Java API Reference
description: Specifies the possible positions for tick labels in Java.
type: docs
weight: 23
url: /java/com.aspose.words/axisticklabelposition/
---

**Inheritance:**
java.lang.Object
```
public class AxisTickLabelPosition
```

Specifies the possible positions for tick labels.

 **Examples:** 

Shows how to insert chart with date/time values.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series containing date/time values for the X-axis, and respective decimal values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new Date[]
                 {
                         DocumentHelper.createDate(2017, 11, 6), DocumentHelper.createDate(2017, 11, 9), DocumentHelper.createDate(2017, 11, 15),
                         DocumentHelper.createDate(2017, 11, 21), DocumentHelper.createDate(2017, 11, 25), DocumentHelper.createDate(2017, 11, 29)
                 },
         new double[]{1.2, 0.3, 2.1, 2.9, 4.2, 5.3});

 // Set lower and upper bounds for the X-axis.
 ChartAxis xAxis = chart.getAxisX();
 xAxis.getScaling().setMinimum(new AxisBound(DocumentHelper.createDate(2017, 11, 5)));
 xAxis.getScaling().setMaximum(new AxisBound(DocumentHelper.createDate(2017, 12, 3)));

 // Set the major units of the X-axis to a week, and the minor units to a day.
 xAxis.setBaseTimeUnit(AxisTimeUnit.DAYS);
 xAxis.setMajorUnit(7.0d);
 xAxis.setMajorTickMark(AxisTickMark.CROSS);
 xAxis.setMinorUnit(1.0d);
 xAxis.setMinorTickMark(AxisTickMark.OUTSIDE);
 xAxis.hasMajorGridlines(true);
 xAxis.hasMinorGridlines(true);

 // Define Y-axis properties for decimal values.
 ChartAxis yAxis = chart.getAxisY();
 yAxis.setTickLabelPosition(AxisTickLabelPosition.HIGH);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(50.0d);
 yAxis.getDisplayUnit().setUnit(AxisBuiltInUnit.HUNDREDS);
 yAxis.getScaling().setMinimum(new AxisBound(100.0));
 yAxis.getScaling().setMaximum(new AxisBound(700.0));
 yAxis.hasMajorGridlines(true);
 yAxis.hasMinorGridlines(true);

 doc.save(getArtifactsDir() + "Charts.DateTimeValues.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [DEFAULT](#DEFAULT) | Specifies default value of tick labels position. |
| [HIGH](#HIGH) | Specifies the axis labels shall be at the high end of the perpendicular axis. |
| [LOW](#LOW) | Specifies the axis labels shall be at the low end of the perpendicular axis. |
| [NEXT_TO_AXIS](#NEXT-TO-AXIS) | Specifies the axis labels shall be next to the axis. |
| [NONE](#NONE) | Specifies the axis labels are not drawn. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String axisTickLabelPositionName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int axisTickLabelPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int axisTickLabelPosition)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Specifies default value of tick labels position.

### HIGH {#HIGH}
```
public static int HIGH
```


Specifies the axis labels shall be at the high end of the perpendicular axis.

### LOW {#LOW}
```
public static int LOW
```


Specifies the axis labels shall be at the low end of the perpendicular axis.

### NEXT_TO_AXIS {#NEXT-TO-AXIS}
```
public static int NEXT_TO_AXIS
```


Specifies the axis labels shall be next to the axis.

### NONE {#NONE}
```
public static int NONE
```


Specifies the axis labels are not drawn.

### length {#length}
```
public static int length
```


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
### fromName(String axisTickLabelPositionName) {#fromName-java.lang.String}
```
public static int fromName(String axisTickLabelPositionName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| axisTickLabelPositionName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int axisTickLabelPosition) {#getName-int}
```
public static String getName(int axisTickLabelPosition)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| axisTickLabelPosition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### toString(int axisTickLabelPosition) {#toString-int}
```
public static String toString(int axisTickLabelPosition)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| axisTickLabelPosition | int |  |

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

