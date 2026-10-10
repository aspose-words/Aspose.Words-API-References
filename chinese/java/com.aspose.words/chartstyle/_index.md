---
title: "ChartStyle"
linktitle: "ChartStyle"
second_title: "Aspose.Words for Java"
description: "指定 Java 中图表的预定义样式。"
type: docs
weight: 91
url: /zh/java/com.aspose.words/chartstyle/
---

**Inheritance:**
java.lang.Object
```
public class ChartStyle
```

指定图表的预定义样式。

 **Examples:** 

展示如何设置和获取图表样式。

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
## 字段集合

| 字段 | 描述 |
| --- | --- |
| [BLACK](#BLACK) | 一种具有黑色图表背景的样式。 |
| [BLUE](#BLUE) | 一种具有蓝色图表背景的样式。 |
| [FLAT](#FLAT) | 一种具有平面数据点且无渐变的样式。 |
| [GRADIENT](#GRADIENT) | 一种具有数据点渐变填充的样式。 |
| [GREY](#GREY) | 一种具有灰色渐变图表背景的样式。 |
| [MUTED](#MUTED) | 一种具有柔和颜色的样式。 |
| [NORMAL](#NORMAL) | 表示默认的图表样式。 |
| [ORIGINAL](#ORIGINAL) | 一种具有图表原始外观的样式。 |
| [OUTLINE](#OUTLINE) | 一种数据点没有填充、仅有轮廓的样式。 |
| [OUTLINE_BLACK](#OUTLINE-BLACK) | 一种具有黑色图表背景且数据点没有填充、仅有轮廓的样式。 |
| [SATURATED](#SATURATED) | 一种颜色更饱和的样式。 |
| [SHADED](#SHADED) | 一种具有阴影数据点的样式。 |
| [SHADED_PLOT](#SHADED-PLOT) | 一种绘图区域被阴影覆盖的样式。 |
| [SHADOWED](#SHADOWED) | 带有阴影的数据点样式。 |
| [TRANSPARENT_1](#TRANSPARENT-1) | 带有透明数据点的样式。 |
| [TRANSPARENT_2](#TRANSPARENT-2) | 带有透明数据点的样式。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [fromName(String chartStyleName)](#fromName-java.lang.String) |  |
| [getName(int chartStyle)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartStyle)](#toString-int) |  |
### BLACK {#BLACK}
```
public static int BLACK
```


一种具有黑色图表背景的样式。

### BLUE {#BLUE}
```
public static int BLUE
```


一种具有蓝色图表背景的样式。

### FLAT {#FLAT}
```
public static int FLAT
```


一种具有平面数据点且无渐变的样式。

### GRADIENT {#GRADIENT}
```
public static int GRADIENT
```


一种具有数据点渐变填充的样式。

### GREY {#GREY}
```
public static int GREY
```


一种具有灰色渐变图表背景的样式。

### MUTED {#MUTED}
```
public static int MUTED
```


一种具有柔和颜色的样式。

### NORMAL {#NORMAL}
```
public static int NORMAL
```


表示默认的图表样式。

### ORIGINAL {#ORIGINAL}
```
public static int ORIGINAL
```


一种具有图表原始外观的样式。

### OUTLINE {#OUTLINE}
```
public static int OUTLINE
```


一种数据点没有填充、仅有轮廓的样式。

### OUTLINE_BLACK {#OUTLINE-BLACK}
```
public static int OUTLINE_BLACK
```


一种具有黑色图表背景且数据点没有填充、仅有轮廓的样式。

### SATURATED {#SATURATED}
```
public static int SATURATED
```


一种颜色更饱和的样式。

### SHADED {#SHADED}
```
public static int SHADED
```


一种具有阴影数据点的样式。

### SHADED_PLOT {#SHADED-PLOT}
```
public static int SHADED_PLOT
```


一种绘图区域被阴影覆盖的样式。

### SHADOWED {#SHADOWED}
```
public static int SHADOWED
```


带有阴影的数据点样式。

### TRANSPARENT_1 {#TRANSPARENT-1}
```
public static int TRANSPARENT_1
```


带有透明数据点的样式。

### TRANSPARENT_2 {#TRANSPARENT-2}
```
public static int TRANSPARENT_2
```


带有透明数据点的样式。

### length {#length}
```
public static int length
```


### fromName(String chartStyleName) {#fromName-java.lang.String}
```
public static int fromName(String chartStyleName)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| chartStyleName | java.lang.String |  |

**Returns:**
int
### getName(int chartStyle) {#getName-int}
```
public static String getName(int chartStyle)
```




**Parameters:**
| 参数 | 类型 | 描述 |
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
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| chartStyle | int |  |

**Returns:**
java.lang.String
