---
title: ChartDataLabelPosition
linktitle: ChartDataLabelPosition
second_title: Aspose.Words for Java
description: Specifies the position for a chart data label in Java.
type: docs
weight: 74
url: /java/com.aspose.words/chartdatalabelposition/
---

**Inheritance:**
java.lang.Object
```
public class ChartDataLabelPosition
```

Specifies the position for a chart data label.

 **Remarks:** 

Not all series types allow you to specify label positions. And those that do, do not support all values.

 **Examples:** 

Shows how to set the position of the data label.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert column chart.
 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();

 // Delete default generated series.
 seriesColl.clear();

 // Add series.
 ChartSeries series = seriesColl.add(
         "Series 1",
         new String[] { "Category 1", "Category 2", "Category 3" },
         new double[] { 4.0, 5.0, 6.0 });

 // Show data labels and set font color.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.getFont().setColor(Color.WHITE);

 // Set data label position.
 dataLabels.setPosition(ChartDataLabelPosition.INSIDE_BASE);
 dataLabels.get(0).setPosition(ChartDataLabelPosition.OUTSIDE_END);
 dataLabels.get(0).getFont().setColor(Color.RED);

 doc.save(getArtifactsDir() + "Charts.LabelPosition.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [ABOVE](#ABOVE) | Specifies that a data label should be displayed above a data marker. |
| [BELOW](#BELOW) | Specifies that a data label should be displayed below a data marker. |
| [BEST_FIT](#BEST-FIT) | Specifies that a data label should be displayed in the most appropriate position. |
| [CENTER](#CENTER) | Specifies that a data label should be displayed centered on a data marker. |
| [INSIDE_BASE](#INSIDE-BASE) | Specifies that a data label should be displayed inside the base of a data marker. |
| [INSIDE_END](#INSIDE-END) | Specifies that a data label should be displayed inside the end of a data marker. |
| [LEFT](#LEFT) | Specifies that a data label should be displayed to the left of a data marker. |
| [OUTSIDE_END](#OUTSIDE-END) | Specifies that a data label should be displayed outside the end of a data marker. |
| [RIGHT](#RIGHT) | Specifies that a data label should be displayed to the right of a data marker. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String chartDataLabelPositionName)](#fromName-java.lang.String) |  |
| [getName(int chartDataLabelPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartDataLabelPosition)](#toString-int) |  |
### ABOVE {#ABOVE}
```
public static int ABOVE
```


Specifies that a data label should be displayed above a data marker.

### BELOW {#BELOW}
```
public static int BELOW
```


Specifies that a data label should be displayed below a data marker.

### BEST_FIT {#BEST-FIT}
```
public static int BEST_FIT
```


Specifies that a data label should be displayed in the most appropriate position.

### CENTER {#CENTER}
```
public static int CENTER
```


Specifies that a data label should be displayed centered on a data marker.

### INSIDE_BASE {#INSIDE-BASE}
```
public static int INSIDE_BASE
```


Specifies that a data label should be displayed inside the base of a data marker.

### INSIDE_END {#INSIDE-END}
```
public static int INSIDE_END
```


Specifies that a data label should be displayed inside the end of a data marker.

### LEFT {#LEFT}
```
public static int LEFT
```


Specifies that a data label should be displayed to the left of a data marker.

### OUTSIDE_END {#OUTSIDE-END}
```
public static int OUTSIDE_END
```


Specifies that a data label should be displayed outside the end of a data marker.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Specifies that a data label should be displayed to the right of a data marker.

### length {#length}
```
public static int length
```


### fromName(String chartDataLabelPositionName) {#fromName-java.lang.String}
```
public static int fromName(String chartDataLabelPositionName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| chartDataLabelPositionName | java.lang.String |  |

**Returns:**
int
### getName(int chartDataLabelPosition) {#getName-int}
```
public static String getName(int chartDataLabelPosition)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| chartDataLabelPosition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int chartDataLabelPosition) {#toString-int}
```
public static String toString(int chartDataLabelPosition)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| chartDataLabelPosition | int |  |

**Returns:**
java.lang.String
