---
title: ChartStyle
linktitle: ChartStyle
second_title: Aspose.Words for Java
description: Specifies predefined styles of a chart in Java.
type: docs
weight: 91
url: /java/com.aspose.words/chartstyle/
---

**Inheritance:**
java.lang.Object
```
public class ChartStyle
```

Specifies predefined styles of a chart.

 **Examples:** 

Shows how to set and get chart style.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a chart in the Black style.
 builder.insertChart(ChartType.COLUMN, 400.0, 250.0, ChartStyle.BLACK);

 doc.save(getArtifactsDir() + "Charts.SetChartStyle.docx");

 doc = new Document(getArtifactsDir() + "Charts.SetChartStyle.docx");

 // Get a chart to update.
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Chart chart = shape.getChart();

 // Get the chart style.
 Assert.assertEquals(ChartStyle.BLACK, chart.getStyle());
 
```
## Fields

| Field | Description |
| --- | --- |
| [BLACK](#BLACK) | A style with black chart background. |
| [BLUE](#BLUE) | A style with blue chart background. |
| [FLAT](#FLAT) | A style with flat data points without gradient. |
| [GRADIENT](#GRADIENT) | A style with gradient fill of data points. |
| [GREY](#GREY) | A style with gray gradient chart background. |
| [MUTED](#MUTED) | A style with muted colors. |
| [NORMAL](#NORMAL) | Represents the default chart style. |
| [ORIGINAL](#ORIGINAL) | A style with an original appearance of a chart. |
| [OUTLINE](#OUTLINE) | A style with data points having no fill, but only an outline. |
| [OUTLINE_BLACK](#OUTLINE-BLACK) | A style with black chart background, in which data points have no fill, but only an outline. |
| [SATURATED](#SATURATED) | A style with more saturated colors. |
| [SHADED](#SHADED) | A style with shaded data points. |
| [SHADED_PLOT](#SHADED-PLOT) | A style, in which the plot area is shaded. |
| [SHADOWED](#SHADOWED) | A style with data points having a shadow. |
| [TRANSPARENT_1](#TRANSPARENT-1) | A style with transparent data points. |
| [TRANSPARENT_2](#TRANSPARENT-2) | A style with transparent data points. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String chartStyleName)](#fromName-java.lang.String) |  |
| [getName(int chartStyle)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartStyle)](#toString-int) |  |
### BLACK {#BLACK}
```
public static int BLACK
```


A style with black chart background.

### BLUE {#BLUE}
```
public static int BLUE
```


A style with blue chart background.

### FLAT {#FLAT}
```
public static int FLAT
```


A style with flat data points without gradient.

### GRADIENT {#GRADIENT}
```
public static int GRADIENT
```


A style with gradient fill of data points.

### GREY {#GREY}
```
public static int GREY
```


A style with gray gradient chart background.

### MUTED {#MUTED}
```
public static int MUTED
```


A style with muted colors.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Represents the default chart style.

### ORIGINAL {#ORIGINAL}
```
public static int ORIGINAL
```


A style with an original appearance of a chart.

### OUTLINE {#OUTLINE}
```
public static int OUTLINE
```


A style with data points having no fill, but only an outline.

### OUTLINE_BLACK {#OUTLINE-BLACK}
```
public static int OUTLINE_BLACK
```


A style with black chart background, in which data points have no fill, but only an outline.

### SATURATED {#SATURATED}
```
public static int SATURATED
```


A style with more saturated colors.

### SHADED {#SHADED}
```
public static int SHADED
```


A style with shaded data points.

### SHADED_PLOT {#SHADED-PLOT}
```
public static int SHADED_PLOT
```


A style, in which the plot area is shaded.

### SHADOWED {#SHADOWED}
```
public static int SHADOWED
```


A style with data points having a shadow.

### TRANSPARENT_1 {#TRANSPARENT-1}
```
public static int TRANSPARENT_1
```


A style with transparent data points.

### TRANSPARENT_2 {#TRANSPARENT-2}
```
public static int TRANSPARENT_2
```


A style with transparent data points.

### length {#length}
```
public static int length
```


### fromName(String chartStyleName) {#fromName-java.lang.String}
```
public static int fromName(String chartStyleName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| chartStyleName | java.lang.String |  |

**Returns:**
int
### getName(int chartStyle) {#getName-int}
```
public static String getName(int chartStyle)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| chartStyle | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int chartStyle) {#toString-int}
```
public static String toString(int chartStyle)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| chartStyle | int |  |

**Returns:**
java.lang.String
