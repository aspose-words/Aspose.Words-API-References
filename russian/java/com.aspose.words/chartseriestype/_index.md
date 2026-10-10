---
title: "ChartSeriesType"
linktitle: "ChartSeriesType"
second_title: "Aspose.Words для Java"
description: "Указывает тип серии диаграммы в Java."
type: docs
weight: 89
url: /ru/java/com.aspose.words/chartseriestype/
---

**Inheritance:**
java.lang.Object
```
public class ChartSeriesType
```

Указывает тип серии диаграммы.

 **Examples:** 

Показывает, как удалить конкретную серию диаграммы.

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
## Поля

| Поле | Описание |
| --- | --- |
| [AREA](#AREA) | Представляет серию диаграммы Area. |
| [AREA_3_D](#AREA-3-D) | Представляет серию 3D Area диаграммы. |
| [AREA_3_D_PERCENT_STACKED](#AREA-3-D-PERCENT-STACKED) | Представляет серию 3D 100% Stacked Area диаграммы. |
| [AREA_3_D_STACKED](#AREA-3-D-STACKED) | Представляет серию 3D Stacked Area диаграммы. |
| [AREA_PERCENT_STACKED](#AREA-PERCENT-STACKED) | Представляет серию 100% Stacked Area диаграммы. |
| [AREA_STACKED](#AREA-STACKED) | Представляет серию Stacked Area диаграммы. |
| [BAR](#BAR) | Представляет серию диаграммы Bar. |
| [BAR_3_D](#BAR-3-D) | Представляет серию 3D Bar диаграммы. |
| [BAR_3_D_PERCENT_STACKED](#BAR-3-D-PERCENT-STACKED) | Представляет серию 3D 100% Stacked Bar диаграммы. |
| [BAR_3_D_STACKED](#BAR-3-D-STACKED) | Представляет серию 3D Stacked Bar диаграммы. |
| [BAR_PERCENT_STACKED](#BAR-PERCENT-STACKED) | Представляет серию 100% Stacked Bar диаграммы. |
| [BAR_STACKED](#BAR-STACKED) | Представляет серию Stacked Bar диаграммы. |
| [BOX_AND_WHISKER](#BOX-AND-WHISKER) | Представляет серию диаграммы Box and Whisker. |
| [BUBBLE](#BUBBLE) | Представляет серию диаграммы Bubble. |
| [BUBBLE_3_D](#BUBBLE-3-D) | Представляет серию 3D Bubble диаграммы. |
| [COLUMN](#COLUMN) | Представляет серию диаграммы Column. |
| [COLUMN_3_D](#COLUMN-3-D) | Представляет серию диаграммы 3D Column. |
| [COLUMN_3_D_CLUSTERED](#COLUMN-3-D-CLUSTERED) | Представляет серию диаграммы 3D Clustered Column. |
| [COLUMN_3_D_PERCENT_STACKED](#COLUMN-3-D-PERCENT-STACKED) | Представляет серию диаграммы 3D 100% Stacked Column. |
| [COLUMN_3_D_STACKED](#COLUMN-3-D-STACKED) | Представляет серию диаграммы 3D Stacked Column. |
| [COLUMN_PERCENT_STACKED](#COLUMN-PERCENT-STACKED) | Представляет серию диаграммы 100% Stacked Column. |
| [COLUMN_STACKED](#COLUMN-STACKED) | Представляет серию диаграммы Stacked Column. |
| [DOUGHNUT](#DOUGHNUT) | Представляет серию диаграммы Doughnut. |
| [FUNNEL](#FUNNEL) | Представляет серию диаграммы Funnel. |
| [HISTOGRAM](#HISTOGRAM) | Представляет серию диаграммы Histogram. |
| [LINE](#LINE) | Представляет серию диаграммы Line. |
| [LINE_3_D](#LINE-3-D) | Представляет серию диаграммы 3D Line. |
| [LINE_PERCENT_STACKED](#LINE-PERCENT-STACKED) | Представляет серию диаграммы 100% Stacked Line. |
| [LINE_STACKED](#LINE-STACKED) | Представляет серию диаграммы Stacked Line. |
| [PARETO](#PARETO) | Представляет серию диаграммы Pareto. |
| [PARETO_LINE](#PARETO-LINE) | Представляет серию диаграммы Pareto Line. |
| [PIE](#PIE) | Представляет серию диаграммы Pie. |
| [PIE_3_D](#PIE-3-D) | Представляет серию диаграммы 3D Pie. |
| [PIE_OF_BAR](#PIE-OF-BAR) | Представляет серию диаграммы Pie of Bar. |
| [PIE_OF_PIE](#PIE-OF-PIE) | Представляет серию диаграммы Pie of Pie. |
| [RADAR](#RADAR) | Представляет серию диаграммы Radar. |
| [REGION_MAP](#REGION-MAP) | Представляет серию диаграммы Region Map. |
| [SCATTER](#SCATTER) | Представляет серию диаграммы Scatter. |
| [STOCK](#STOCK) | Представляет серию диаграммы Stock. |
| [SUNBURST](#SUNBURST) | Представляет серию диаграммы Sunburst. |
| [SURFACE](#SURFACE) | Представляет серию диаграммы Surface. |
| [SURFACE_3_D](#SURFACE-3-D) | Представляет серию 3D Surface диаграммы. |
| [TREEMAP](#TREEMAP) | Представляет серию Treemap диаграммы. |
| [WATERFALL](#WATERFALL) | Представляет серию Waterfall диаграммы. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String chartSeriesTypeName)](#fromName-java.lang.String) |  |
| [getName(int chartSeriesType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartSeriesType)](#toString-int) |  |
### AREA {#AREA}
```
public static int AREA
```


Представляет серию диаграммы Area.

### AREA_3_D {#AREA-3-D}
```
public static int AREA_3_D
```


Представляет серию 3D Area диаграммы.

### AREA_3_D_PERCENT_STACKED {#AREA-3-D-PERCENT-STACKED}
```
public static int AREA_3_D_PERCENT_STACKED
```


Представляет серию 3D 100% Stacked Area диаграммы.

### AREA_3_D_STACKED {#AREA-3-D-STACKED}
```
public static int AREA_3_D_STACKED
```


Представляет серию 3D Stacked Area диаграммы.

### AREA_PERCENT_STACKED {#AREA-PERCENT-STACKED}
```
public static int AREA_PERCENT_STACKED
```


Представляет серию 100% Stacked Area диаграммы.

### AREA_STACKED {#AREA-STACKED}
```
public static int AREA_STACKED
```


Представляет серию Stacked Area диаграммы.

### BAR {#BAR}
```
public static int BAR
```


Представляет серию диаграммы Bar.

### BAR_3_D {#BAR-3-D}
```
public static int BAR_3_D
```


Представляет серию 3D Bar диаграммы.

### BAR_3_D_PERCENT_STACKED {#BAR-3-D-PERCENT-STACKED}
```
public static int BAR_3_D_PERCENT_STACKED
```


Представляет серию 3D 100% Stacked Bar диаграммы.

### BAR_3_D_STACKED {#BAR-3-D-STACKED}
```
public static int BAR_3_D_STACKED
```


Представляет серию 3D Stacked Bar диаграммы.

### BAR_PERCENT_STACKED {#BAR-PERCENT-STACKED}
```
public static int BAR_PERCENT_STACKED
```


Представляет серию 100% Stacked Bar диаграммы.

### BAR_STACKED {#BAR-STACKED}
```
public static int BAR_STACKED
```


Представляет серию Stacked Bar диаграммы.

### BOX_AND_WHISKER {#BOX-AND-WHISKER}
```
public static int BOX_AND_WHISKER
```


Представляет серию диаграммы Box and Whisker.

### BUBBLE {#BUBBLE}
```
public static int BUBBLE
```


Представляет серию диаграммы Bubble.

### BUBBLE_3_D {#BUBBLE-3-D}
```
public static int BUBBLE_3_D
```


Представляет серию 3D Bubble диаграммы.

### COLUMN {#COLUMN}
```
public static int COLUMN
```


Представляет серию диаграммы Column.

### COLUMN_3_D {#COLUMN-3-D}
```
public static int COLUMN_3_D
```


Представляет серию диаграммы 3D Column.

### COLUMN_3_D_CLUSTERED {#COLUMN-3-D-CLUSTERED}
```
public static int COLUMN_3_D_CLUSTERED
```


Представляет серию диаграммы 3D Clustered Column.

### COLUMN_3_D_PERCENT_STACKED {#COLUMN-3-D-PERCENT-STACKED}
```
public static int COLUMN_3_D_PERCENT_STACKED
```


Представляет серию диаграммы 3D 100% Stacked Column.

### COLUMN_3_D_STACKED {#COLUMN-3-D-STACKED}
```
public static int COLUMN_3_D_STACKED
```


Представляет серию диаграммы 3D Stacked Column.

### COLUMN_PERCENT_STACKED {#COLUMN-PERCENT-STACKED}
```
public static int COLUMN_PERCENT_STACKED
```


Представляет серию диаграммы 100% Stacked Column.

### COLUMN_STACKED {#COLUMN-STACKED}
```
public static int COLUMN_STACKED
```


Представляет серию диаграммы Stacked Column.

### DOUGHNUT {#DOUGHNUT}
```
public static int DOUGHNUT
```


Представляет серию диаграммы Doughnut.

### FUNNEL {#FUNNEL}
```
public static int FUNNEL
```


Представляет серию диаграммы Funnel.

### HISTOGRAM {#HISTOGRAM}
```
public static int HISTOGRAM
```


Представляет серию диаграммы Histogram.

### LINE {#LINE}
```
public static int LINE
```


Представляет серию диаграммы Line.

### LINE_3_D {#LINE-3-D}
```
public static int LINE_3_D
```


Представляет серию диаграммы 3D Line.

### LINE_PERCENT_STACKED {#LINE-PERCENT-STACKED}
```
public static int LINE_PERCENT_STACKED
```


Представляет серию диаграммы 100% Stacked Line.

### LINE_STACKED {#LINE-STACKED}
```
public static int LINE_STACKED
```


Представляет серию диаграммы Stacked Line.

### PARETO {#PARETO}
```
public static int PARETO
```


Представляет серию диаграммы Pareto.

### PARETO_LINE {#PARETO-LINE}
```
public static int PARETO_LINE
```


Представляет серию диаграммы Pareto Line.

### PIE {#PIE}
```
public static int PIE
```


Представляет серию диаграммы Pie.

### PIE_3_D {#PIE-3-D}
```
public static int PIE_3_D
```


Представляет серию диаграммы 3D Pie.

### PIE_OF_BAR {#PIE-OF-BAR}
```
public static int PIE_OF_BAR
```


Представляет серию диаграммы Pie of Bar.

### PIE_OF_PIE {#PIE-OF-PIE}
```
public static int PIE_OF_PIE
```


Представляет серию диаграммы Pie of Pie.

### RADAR {#RADAR}
```
public static int RADAR
```


Представляет серию диаграммы Radar.

### REGION_MAP {#REGION-MAP}
```
public static int REGION_MAP
```


Представляет серию диаграммы Region Map.

### SCATTER {#SCATTER}
```
public static int SCATTER
```


Представляет серию диаграммы Scatter.

### STOCK {#STOCK}
```
public static int STOCK
```


Представляет серию диаграммы Stock.

### SUNBURST {#SUNBURST}
```
public static int SUNBURST
```


Представляет серию диаграммы Sunburst.

### SURFACE {#SURFACE}
```
public static int SURFACE
```


Представляет серию диаграммы Surface.

### SURFACE_3_D {#SURFACE-3-D}
```
public static int SURFACE_3_D
```


Представляет серию 3D Surface диаграммы.

### TREEMAP {#TREEMAP}
```
public static int TREEMAP
```


Представляет серию Treemap диаграммы.

### WATERFALL {#WATERFALL}
```
public static int WATERFALL
```


Представляет серию Waterfall диаграммы.

### length {#length}
```
public static int length
```


### fromName(String chartSeriesTypeName) {#fromName-java.lang.String}
```
public static int fromName(String chartSeriesTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| chartSeriesTypeName | java.lang.String |  |

**Returns:**
int
### getName(int chartSeriesType) {#getName-int}
```
public static String getName(int chartSeriesType)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| chartSeriesType | int |  |

**Returns:**
java.lang.String
