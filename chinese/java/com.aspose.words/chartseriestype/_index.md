---
title: "ChartSeriesType"
linktitle: "ChartSeriesType"
second_title: "Aspose.Words for Java"
description: "指定 Java 中图表系列的类型。"
type: docs
weight: 89
url: /zh/java/com.aspose.words/chartseriestype/
---

**Inheritance:**
java.lang.Object
```
public class ChartSeriesType
```

指定图表系列的类型。

 **Examples:** 

展示如何删除特定的图表系列。

```

 Document doc = new Document(getMyDir() + "Reporting engine template - Chart series (Java).docx");
 Chart chart = ((Shape)doc.getChild(NodeType.SHAPE, 0, true)).getChart();

 // Remove all series of the Column type.
 for (int i = chart.getSeries().getCount() - 1; i >= 0; i--)
 {
     if (chart.getSeries().get(i).getSeriesType() == ChartSeriesType.COLUMN)
         chart.getSeries().removeAt(i);
 }

 chart.getSeries().add(
         "Aspose Series",
         new String[] { "Category 1", "Category 2", "Category 3", "Category 4" },
         new double[] { 5.6, 7.1, 2.9, 8.9 });

 doc.save(getArtifactsDir() + "Charts.RemoveSpecificChartSeries.docx");
 
```
## 字段集合

| 字段 | 描述 |
| --- | --- |
| [AREA](#AREA) | 表示面积图系列。 |
| [AREA_3_D](#AREA-3-D) | 表示 3D 面积图系列。 |
| [AREA_3_D_PERCENT_STACKED](#AREA-3-D-PERCENT-STACKED) | 表示 3D 100% 堆叠面积图系列。 |
| [AREA_3_D_STACKED](#AREA-3-D-STACKED) | 表示 3D 堆叠面积图系列。 |
| [AREA_PERCENT_STACKED](#AREA-PERCENT-STACKED) | 表示 100% 堆叠面积图系列。 |
| [AREA_STACKED](#AREA-STACKED) | 表示堆叠面积图系列。 |
| [BAR](#BAR) | 表示条形图系列。 |
| [BAR_3_D](#BAR-3-D) | 表示 3D 条形图系列。 |
| [BAR_3_D_PERCENT_STACKED](#BAR-3-D-PERCENT-STACKED) | 表示 3D 100% 堆叠条形图系列。 |
| [BAR_3_D_STACKED](#BAR-3-D-STACKED) | 表示 3D 堆叠条形图系列。 |
| [BAR_PERCENT_STACKED](#BAR-PERCENT-STACKED) | 表示 100% 堆叠条形图系列。 |
| [BAR_STACKED](#BAR-STACKED) | 表示堆叠条形图系列。 |
| [BOX_AND_WHISKER](#BOX-AND-WHISKER) | 表示箱线图系列。 |
| [BUBBLE](#BUBBLE) | 表示气泡图系列。 |
| [BUBBLE_3_D](#BUBBLE-3-D) | 表示 3D 气泡图系列。 |
| [COLUMN](#COLUMN) | 表示柱形图系列。 |
| [COLUMN_3_D](#COLUMN-3-D) | 表示 3D 柱形图系列。 |
| [COLUMN_3_D_CLUSTERED](#COLUMN-3-D-CLUSTERED) | 表示 3D 簇状柱形图系列。 |
| [COLUMN_3_D_PERCENT_STACKED](#COLUMN-3-D-PERCENT-STACKED) | 表示 3D 100% 堆叠柱形图系列。 |
| [COLUMN_3_D_STACKED](#COLUMN-3-D-STACKED) | 表示 3D 堆叠柱形图系列。 |
| [COLUMN_PERCENT_STACKED](#COLUMN-PERCENT-STACKED) | 表示 100% 堆叠柱形图系列。 |
| [COLUMN_STACKED](#COLUMN-STACKED) | 表示堆叠柱形图系列。 |
| [DOUGHNUT](#DOUGHNUT) | 表示环形图系列。 |
| [FUNNEL](#FUNNEL) | 表示漏斗图系列。 |
| [HISTOGRAM](#HISTOGRAM) | 表示直方图系列。 |
| [LINE](#LINE) | 表示折线图系列。 |
| [LINE_3_D](#LINE-3-D) | 表示3D折线图系列。 |
| [LINE_PERCENT_STACKED](#LINE-PERCENT-STACKED) | 表示100%堆叠折线图系列。 |
| [LINE_STACKED](#LINE-STACKED) | 表示堆叠折线图系列。 |
| [PARETO](#PARETO) | 表示帕累托图系列。 |
| [PARETO_LINE](#PARETO-LINE) | 表示帕累托折线图系列。 |
| [PIE](#PIE) | 表示饼图系列。 |
| [PIE_3_D](#PIE-3-D) | 表示3D饼图系列。 |
| [PIE_OF_BAR](#PIE-OF-BAR) | 表示条形图饼图系列。 |
| [PIE_OF_PIE](#PIE-OF-PIE) | 表示饼中饼图系列。 |
| [RADAR](#RADAR) | 表示雷达图系列。 |
| [REGION_MAP](#REGION-MAP) | 表示地区地图图系列。 |
| [SCATTER](#SCATTER) | 表示散点图系列。 |
| [STOCK](#STOCK) | 表示股票图系列。 |
| [SUNBURST](#SUNBURST) | 表示旭日图系列。 |
| [SURFACE](#SURFACE) | 表示曲面图系列。 |
| [SURFACE_3_D](#SURFACE-3-D) | 表示3D曲面图系列。 |
| [TREEMAP](#TREEMAP) | 表示树状图系列。 |
| [WATERFALL](#WATERFALL) | 表示瀑布图系列。 |
| [length](#length) |  |
## 方法

| 方法 | 描述 |
| --- | --- |
| [fromName(String chartSeriesTypeName)](#fromName-java.lang.String) |  |
| [getName(int chartSeriesType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartSeriesType)](#toString-int) |  |
### AREA {#AREA}
```
public static int AREA
```


表示面积图系列。

### AREA_3_D {#AREA-3-D}
```
public static int AREA_3_D
```


表示 3D 面积图系列。

### AREA_3_D_PERCENT_STACKED {#AREA-3-D-PERCENT-STACKED}
```
public static int AREA_3_D_PERCENT_STACKED
```


表示 3D 100% 堆叠面积图系列。

### AREA_3_D_STACKED {#AREA-3-D-STACKED}
```
public static int AREA_3_D_STACKED
```


表示 3D 堆叠面积图系列。

### AREA_PERCENT_STACKED {#AREA-PERCENT-STACKED}
```
public static int AREA_PERCENT_STACKED
```


表示 100% 堆叠面积图系列。

### AREA_STACKED {#AREA-STACKED}
```
public static int AREA_STACKED
```


表示堆叠面积图系列。

### BAR {#BAR}
```
public static int BAR
```


表示条形图系列。

### BAR_3_D {#BAR-3-D}
```
public static int BAR_3_D
```


表示 3D 条形图系列。

### BAR_3_D_PERCENT_STACKED {#BAR-3-D-PERCENT-STACKED}
```
public static int BAR_3_D_PERCENT_STACKED
```


表示 3D 100% 堆叠条形图系列。

### BAR_3_D_STACKED {#BAR-3-D-STACKED}
```
public static int BAR_3_D_STACKED
```


表示 3D 堆叠条形图系列。

### BAR_PERCENT_STACKED {#BAR-PERCENT-STACKED}
```
public static int BAR_PERCENT_STACKED
```


表示 100% 堆叠条形图系列。

### BAR_STACKED {#BAR-STACKED}
```
public static int BAR_STACKED
```


表示堆叠条形图系列。

### BOX_AND_WHISKER {#BOX-AND-WHISKER}
```
public static int BOX_AND_WHISKER
```


表示箱线图系列。

### BUBBLE {#BUBBLE}
```
public static int BUBBLE
```


表示气泡图系列。

### BUBBLE_3_D {#BUBBLE-3-D}
```
public static int BUBBLE_3_D
```


表示 3D 气泡图系列。

### COLUMN {#COLUMN}
```
public static int COLUMN
```


表示柱形图系列。

### COLUMN_3_D {#COLUMN-3-D}
```
public static int COLUMN_3_D
```


表示 3D 柱形图系列。

### COLUMN_3_D_CLUSTERED {#COLUMN-3-D-CLUSTERED}
```
public static int COLUMN_3_D_CLUSTERED
```


表示 3D 簇状柱形图系列。

### COLUMN_3_D_PERCENT_STACKED {#COLUMN-3-D-PERCENT-STACKED}
```
public static int COLUMN_3_D_PERCENT_STACKED
```


表示 3D 100% 堆叠柱形图系列。

### COLUMN_3_D_STACKED {#COLUMN-3-D-STACKED}
```
public static int COLUMN_3_D_STACKED
```


表示 3D 堆叠柱形图系列。

### COLUMN_PERCENT_STACKED {#COLUMN-PERCENT-STACKED}
```
public static int COLUMN_PERCENT_STACKED
```


表示 100% 堆叠柱形图系列。

### COLUMN_STACKED {#COLUMN-STACKED}
```
public static int COLUMN_STACKED
```


表示堆叠柱形图系列。

### DOUGHNUT {#DOUGHNUT}
```
public static int DOUGHNUT
```


表示环形图系列。

### FUNNEL {#FUNNEL}
```
public static int FUNNEL
```


表示漏斗图系列。

### HISTOGRAM {#HISTOGRAM}
```
public static int HISTOGRAM
```


表示直方图系列。

### LINE {#LINE}
```
public static int LINE
```


表示折线图系列。

### LINE_3_D {#LINE-3-D}
```
public static int LINE_3_D
```


表示3D折线图系列。

### LINE_PERCENT_STACKED {#LINE-PERCENT-STACKED}
```
public static int LINE_PERCENT_STACKED
```


表示100%堆叠折线图系列。

### LINE_STACKED {#LINE-STACKED}
```
public static int LINE_STACKED
```


表示堆叠折线图系列。

### PARETO {#PARETO}
```
public static int PARETO
```


表示帕累托图系列。

### PARETO_LINE {#PARETO-LINE}
```
public static int PARETO_LINE
```


表示帕累托折线图系列。

### PIE {#PIE}
```
public static int PIE
```


表示饼图系列。

### PIE_3_D {#PIE-3-D}
```
public static int PIE_3_D
```


表示3D饼图系列。

### PIE_OF_BAR {#PIE-OF-BAR}
```
public static int PIE_OF_BAR
```


表示条形图饼图系列。

### PIE_OF_PIE {#PIE-OF-PIE}
```
public static int PIE_OF_PIE
```


表示饼中饼图系列。

### RADAR {#RADAR}
```
public static int RADAR
```


表示雷达图系列。

### REGION_MAP {#REGION-MAP}
```
public static int REGION_MAP
```


表示地区地图图系列。

### SCATTER {#SCATTER}
```
public static int SCATTER
```


表示散点图系列。

### STOCK {#STOCK}
```
public static int STOCK
```


表示股票图系列。

### SUNBURST {#SUNBURST}
```
public static int SUNBURST
```


表示旭日图系列。

### SURFACE {#SURFACE}
```
public static int SURFACE
```


表示曲面图系列。

### SURFACE_3_D {#SURFACE-3-D}
```
public static int SURFACE_3_D
```


表示3D曲面图系列。

### TREEMAP {#TREEMAP}
```
public static int TREEMAP
```


表示树状图系列。

### WATERFALL {#WATERFALL}
```
public static int WATERFALL
```


表示瀑布图系列。

### length {#length}
```
public static int length
```


### fromName(String chartSeriesTypeName) {#fromName-java.lang.String}
```
public static int fromName(String chartSeriesTypeName)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| chartSeriesTypeName | java.lang.String |  |

**Returns:**
int
### getName(int chartSeriesType) {#getName-int}
```
public static String getName(int chartSeriesType)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| chartSeriesType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int chartSeriesType) {#toString-int}
```
public static String toString(int chartSeriesType)
```




**Parameters:**
| 参数 | 类型 | 描述 |
| --- | --- | --- |
| chartSeriesType | int |  |

**Returns:**
java.lang.String
