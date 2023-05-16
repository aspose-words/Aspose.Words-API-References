---
title: LegendPosition
linktitle: LegendPosition
second_title: Aspose.Words for Java
description: Specifies the possible positions for a chart legend in Java.
type: docs
weight: 376
url: /java/com.aspose.words/legendposition/
---

**Inheritance:**
java.lang.Object
```
public class LegendPosition
```

Specifies the possible positions for a chart legend.

 **Examples:** 

Shows how to edit the appearance of a chart's legend.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 450.0, 300.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(3, chart.getSeries().getCount());
 Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
 Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
 Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

 // Move the chart's legend to the top right corner.
 ChartLegend legend = chart.getLegend();
 legend.setPosition(LegendPosition.TOP_RIGHT);

 // Give other chart elements, such as the graph, more room by allowing them to overlap the legend.
 legend.setOverlay(true);

 doc.save(getArtifactsDir() + "Charts.ChartLegend.docx");
 
```
## Fields

| Field | Description |
| --- | --- |
| [BOTTOM](#BOTTOM) | Specifies that the legend shall be drawn at the bottom of the chart. |
| [LEFT](#LEFT) | Specifies that the legend shall be drawn at the left of the chart. |
| [NONE](#NONE) | No legend will be shown for the chart. |
| [RIGHT](#RIGHT) | Specifies that the legend shall be drawn at the right of the chart. |
| [TOP](#TOP) | Specifies that the legend shall be drawn at the top of the chart. |
| [TOP_RIGHT](#TOP-RIGHT) | Specifies that the legend shall be drawn at the top right of the chart. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String legendPositionName)](#fromName-java.lang.String) |  |
| [getName(int legendPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int legendPosition)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Specifies that the legend shall be drawn at the bottom of the chart.

### LEFT {#LEFT}
```
public static int LEFT
```


Specifies that the legend shall be drawn at the left of the chart.

### NONE {#NONE}
```
public static int NONE
```


No legend will be shown for the chart.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Specifies that the legend shall be drawn at the right of the chart.

### TOP {#TOP}
```
public static int TOP
```


Specifies that the legend shall be drawn at the top of the chart.

### TOP_RIGHT {#TOP-RIGHT}
```
public static int TOP_RIGHT
```


Specifies that the legend shall be drawn at the top right of the chart.

### length {#length}
```
public static int length
```


### fromName(String legendPositionName) {#fromName-java.lang.String}
```
public static int fromName(String legendPositionName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| legendPositionName | java.lang.String |  |

**Returns:**
int
### getName(int legendPosition) {#getName-int}
```
public static String getName(int legendPosition)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| legendPosition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int legendPosition) {#toString-int}
```
public static String toString(int legendPosition)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| legendPosition | int |  |

**Returns:**
java.lang.String
