---
title: AxisBuiltInUnit
linktitle: AxisBuiltInUnit
second_title: Aspose.Words for Java API Reference
description: Specifies the display units for an axis in Java.
type: docs
weight: 17
url: /java/com.aspose.words/axisbuiltinunit/
---

**Inheritance:**
java.lang.Object
```
public class AxisBuiltInUnit
```

Specifies the display units for an axis.

 **Examples:** 

Shows how to manipulate the tick marks and displayed values of a chart axis.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.SCATTER, 450.0, 250.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(1, chart.getSeries().getCount());
 Assert.assertEquals("Y-Values", chart.getSeries().get(0).getName());

 // Set the minor tick marks of the Y-axis to point away from the plot area,
 // and the major tick marks to cross the axis.
 ChartAxis axis = chart.getAxisY();
 axis.setMajorTickMark(AxisTickMark.CROSS);
 axis.setMinorTickMark(AxisTickMark.OUTSIDE);

 // Set they Y-axis to show a major tick every 10 units, and a minor tick every 1 unit.
 axis.setMajorUnit(10.0);
 axis.setMinorUnit(1.0);

 // Set the Y-axis bounds to -10 and 20.
 // This Y-axis will now display 4 major tick marks and 27 minor tick marks.
 axis.getScaling().setMinimum(new AxisBound(-10));
 axis.getScaling().setMaximum(new AxisBound(20.0));

 // For the X-axis, set the major tick marks at every 10 units,
 // every minor tick mark at 2.5 units.
 axis = chart.getAxisX();
 axis.setMajorUnit(10.0);
 axis.setMinorUnit(2.5);

 // Configure both types of tick marks to appear inside the graph plot area.
 axis.setMajorTickMark(AxisTickMark.INSIDE);
 axis.setMinorTickMark(AxisTickMark.INSIDE);

 // Set the X-axis bounds so that the X-axis spans 5 major tick marks and 12 minor tick marks.
 axis.getScaling().setMinimum(new AxisBound(-10));
 axis.getScaling().setMaximum(new AxisBound(30.0));
 axis.setTickLabelAlignment(ParagraphAlignment.RIGHT);

 Assert.assertEquals(1, axis.getTickLabelSpacing());

 // Set the tick labels to display their value in millions.
 axis.getDisplayUnit().setUnit(AxisBuiltInUnit.MILLIONS);

 // We can set a more specific value by which tick labels will display their values.
 // This statement is equivalent to the one above.
 axis.getDisplayUnit().setCustomUnit(1000000.0);
 doc.save(getArtifactsDir() + "Charts.AxisDisplayUnit.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [BILLIONS](#BILLIONS) | Specifies the values on the chart shall be divided by 1,000,000,000. |
| [CUSTOM](#CUSTOM) | Specifies the values on the chart shall be divided by a user-defined divisor. |
| [HUNDREDS](#HUNDREDS) | Specifies the values on the chart shall be divided by 100. |
| [HUNDRED_MILLIONS](#HUNDRED-MILLIONS) | Specifies the values on the chart shall be divided by 100,000,000. |
| [HUNDRED_THOUSANDS](#HUNDRED-THOUSANDS) | Specifies the values on the chart shall be divided by 100,000. |
| [MILLIONS](#MILLIONS) | Specifies the values on the chart shall be divided by 1,000,000. |
| [NONE](#NONE) | Specifies the values on the chart shall displayed as is. |
| [PERCENTAGE](#PERCENTAGE) | Specifies the values on the chart shall be divided by 0.01. |
| [TEN_MILLIONS](#TEN-MILLIONS) | Specifies the values on the chart shall be divided by 10,000,000. |
| [TEN_THOUSANDS](#TEN-THOUSANDS) | Specifies the values on the chart shall be divided by 10,000. |
| [THOUSANDS](#THOUSANDS) | Specifies the values on the chart shall be divided by 1,000. |
| [TRILLIONS](#TRILLIONS) | Specifies the values on the chart shall be divided by 1,000,000,000,0000. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fromName(String axisBuiltInUnitName)](#fromName-java.lang.String) |  |
| [getClass()](#getClass) |  |
| [getName(int axisBuiltInUnit)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [toString(int axisBuiltInUnit)](#toString-int) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### BILLIONS {#BILLIONS}
```
public static int BILLIONS
```


Specifies the values on the chart shall be divided by 1,000,000,000.

### CUSTOM {#CUSTOM}
```
public static int CUSTOM
```


Specifies the values on the chart shall be divided by a user-defined divisor. This value is not supported by the new chart types of MS Office 2016.

### HUNDREDS {#HUNDREDS}
```
public static int HUNDREDS
```


Specifies the values on the chart shall be divided by 100.

### HUNDRED_MILLIONS {#HUNDRED-MILLIONS}
```
public static int HUNDRED_MILLIONS
```


Specifies the values on the chart shall be divided by 100,000,000.

### HUNDRED_THOUSANDS {#HUNDRED-THOUSANDS}
```
public static int HUNDRED_THOUSANDS
```


Specifies the values on the chart shall be divided by 100,000.

### MILLIONS {#MILLIONS}
```
public static int MILLIONS
```


Specifies the values on the chart shall be divided by 1,000,000.

### NONE {#NONE}
```
public static int NONE
```


Specifies the values on the chart shall displayed as is.

### PERCENTAGE {#PERCENTAGE}
```
public static int PERCENTAGE
```


Specifies the values on the chart shall be divided by 0.01. This value is supported only by the new chart types of MS Office 2016.

### TEN_MILLIONS {#TEN-MILLIONS}
```
public static int TEN_MILLIONS
```


Specifies the values on the chart shall be divided by 10,000,000.

### TEN_THOUSANDS {#TEN-THOUSANDS}
```
public static int TEN_THOUSANDS
```


Specifies the values on the chart shall be divided by 10,000.

### THOUSANDS {#THOUSANDS}
```
public static int THOUSANDS
```


Specifies the values on the chart shall be divided by 1,000.

### TRILLIONS {#TRILLIONS}
```
public static int TRILLIONS
```


Specifies the values on the chart shall be divided by 1,000,000,000,0000.

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
### fromName(String axisBuiltInUnitName) {#fromName-java.lang.String}
```
public static int fromName(String axisBuiltInUnitName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| axisBuiltInUnitName | java.lang.String |  |

**Returns:**
int
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getName(int axisBuiltInUnit) {#getName-int}
```
public static String getName(int axisBuiltInUnit)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| axisBuiltInUnit | int |  |

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
### toString(int axisBuiltInUnit) {#toString-int}
```
public static String toString(int axisBuiltInUnit)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| axisBuiltInUnit | int |  |

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

