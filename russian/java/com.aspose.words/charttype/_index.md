---
title: "ChartType"
linktitle: "ChartType"
second_title: "Aspose.Words для Java"
description: "Указывает тип диаграммы в Java."
type: docs
weight: 93
url: /ru/java/com.aspose.words/charttype/
---

**Inheritance:**
java.lang.Object
```
public class ChartType
```

Указывает тип диаграммы.

 **Examples:** 

Показывает, как создать подходящий тип серии диаграммы для определённого типа графика.

```

 public void chartSeriesCollection() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // There are several ways of populating a chart's series collection.
     // Different series schemas are intended for different chart types.
     // 1 -  Column chart with columns grouped and banded along the X-axis by category:
     Chart chart = appendChart(builder, ChartType.COLUMN, 500.0, 300.0);

     String[] categories = {"Category 1", "Category 2", "Category 3"};

     // Insert two series of decimal values containing a value for each respective category.
     // This column chart will have three groups, each with two columns.
     chart.getSeries().add("Series 1", categories, new double[]{76.6, 82.1, 91.6});
     chart.getSeries().add("Series 2", categories, new double[]{64.2, 79.5, 94.0});

     // Categories are distributed along the X-axis, and values are distributed along the Y-axis.
     Assert.assertEquals(ChartAxisType.CATEGORY, chart.getAxisX().getType());
     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisY().getType());

     // 2 -  Area chart with dates distributed along the X-axis:
     chart = appendChart(builder, ChartType.AREA, 500.0, 300.0);

     Date[] dates = {DocumentHelper.createDate(2014, 3, 31),
             DocumentHelper.createDate(2017, 1, 23),
             DocumentHelper.createDate(2017, 6, 18),
             DocumentHelper.createDate(2019, 11, 22),
             DocumentHelper.createDate(2020, 9, 7)
     };

     // Insert a series with a decimal value for each respective date.
     // The dates will be distributed along a linear X-axis,
     // and the values added to this series will create data points.
     chart.getSeries().add("Series 1", dates, new double[]{15.8, 21.5, 22.9, 28.7, 33.1});

     Assert.assertEquals(ChartAxisType.CATEGORY, chart.getAxisX().getType());
     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisY().getType());

     // 3 -  2D scatter plot:
     chart = appendChart(builder, ChartType.SCATTER, 500.0, 300.0);

     // Each series will need two decimal arrays of equal length.
     // The first array contains X-values, and the second contains corresponding Y-values
     // of data points on the chart's graph.
     chart.getSeries().add("Series 1",
             new double[]{3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6},
             new double[]{3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9});
     chart.getSeries().add("Series 2",
             new double[]{2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3},
             new double[]{7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6});

     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisX().getType());
     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisY().getType());

     // 4 -  Bubble chart:
     chart = appendChart(builder, ChartType.BUBBLE, 500.0, 300.0);

     // Each series will need three decimal arrays of equal length.
     // The first array contains X-values, the second contains corresponding Y-values,
     // and the third contains diameters for each of the graph's data points.
     chart.getSeries().add("Series 1",
             new double[]{1.1, 5.0, 9.8},
             new double[]{1.2, 4.9, 9.9},
             new double[]{2.0, 4.0, 8.0});

     doc.save(getArtifactsDir() + "Charts.ChartSeriesCollection.docx");
 }

 /// 
 /// Insert a chart using a document builder of a specified ChartType, width and height, and remove its demo data.
 /// 
 private static Chart appendChart(DocumentBuilder builder, int chartType, double width, double height) throws Exception {
     Shape chartShape = builder.insertChart(chartType, width, height);
     Chart chart = chartShape.getChart();
     chart.getSeries().clear();
     return chart;
 }
 
```
## Поля

| Поле | Описание |
| --- | --- |
| [AREA](#AREA) | Диаграмма области. |
| [AREA_3_D](#AREA-3-D) | 3D-диаграмма области. |
| [AREA_3_D_PERCENT_STACKED](#AREA-3-D-PERCENT-STACKED) | 3D 100% сложенная диаграмма области. |
| [AREA_3_D_STACKED](#AREA-3-D-STACKED) | 3D сложенная диаграмма области. |
| [AREA_PERCENT_STACKED](#AREA-PERCENT-STACKED) | 100% сложенная диаграмма области. |
| [AREA_STACKED](#AREA-STACKED) | Сложенная диаграмма области. |
| [BAR](#BAR) | Гистограмма. |
| [BAR_3_D](#BAR-3-D) | 3D гистограмма. |
| [BAR_3_D_PERCENT_STACKED](#BAR-3-D-PERCENT-STACKED) | 3D 100% сложенная гистограмма. |
| [BAR_3_D_STACKED](#BAR-3-D-STACKED) | 3D сложенная гистограмма. |
| [BAR_PERCENT_STACKED](#BAR-PERCENT-STACKED) | 100% сложенная гистограмма. |
| [BAR_STACKED](#BAR-STACKED) | Сложенная гистограмма. |
| [BOX_AND_WHISKER](#BOX-AND-WHISKER) | Диаграмма «ящик с усами». |
| [BUBBLE](#BUBBLE) | Пузырьковая диаграмма. |
| [BUBBLE_3_D](#BUBBLE-3-D) | 3D пузырьковая диаграмма. |
| [COLUMN](#COLUMN) | Столбчатая диаграмма. |
| [COLUMN_3_D](#COLUMN-3-D) | 3D столбчатая диаграмма. |
| [COLUMN_3_D_CLUSTERED](#COLUMN-3-D-CLUSTERED) | 3D сгруппированная столбчатая диаграмма. |
| [COLUMN_3_D_PERCENT_STACKED](#COLUMN-3-D-PERCENT-STACKED) | 3D 100% сложенная столбчатая диаграмма. |
| [COLUMN_3_D_STACKED](#COLUMN-3-D-STACKED) | 3D сложенная столбчатая диаграмма. |
| [COLUMN_PERCENT_STACKED](#COLUMN-PERCENT-STACKED) | 100% сложенная столбчатая диаграмма. |
| [COLUMN_STACKED](#COLUMN-STACKED) | Сложенная столбчатая диаграмма. |
| [DOUGHNUT](#DOUGHNUT) | Кольцевая диаграмма. |
| [FUNNEL](#FUNNEL) | Воронкообразная диаграмма. |
| [HISTOGRAM](#HISTOGRAM) | Гистограмма. |
| [LINE](#LINE) | Линейная диаграмма. |
| [LINE_3_D](#LINE-3-D) | 3D линейная диаграмма. |
| [LINE_PERCENT_STACKED](#LINE-PERCENT-STACKED) | 100% сложенная линейная диаграмма. |
| [LINE_STACKED](#LINE-STACKED) | Сложенная линейная диаграмма. |
| [PARETO](#PARETO) | Диаграмма Парето. |
| [PIE](#PIE) | Круговая диаграмма. |
| [PIE_3_D](#PIE-3-D) | 3D круговая диаграмма. |
| [PIE_OF_BAR](#PIE-OF-BAR) | Круговая диаграмма в виде столбца. |
| [PIE_OF_PIE](#PIE-OF-PIE) | Круговая диаграмма в виде круговой диаграммы. |
| [RADAR](#RADAR) | Радарная диаграмма. |
| [SCATTER](#SCATTER) | Точечная диаграмма. |
| [STOCK](#STOCK) | График акций. |
| [SUNBURST](#SUNBURST) | Диаграмма лучевого разбиения. |
| [SURFACE](#SURFACE) | Поверхностная диаграмма. |
| [SURFACE_3_D](#SURFACE-3-D) | 3D поверхностная диаграмма. |
| [TREEMAP](#TREEMAP) | Диаграмма дерево-карта. |
| [WATERFALL](#WATERFALL) | Водопадная диаграмма. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String chartTypeName)](#fromName-java.lang.String) |  |
| [getName(int chartType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartType)](#toString-int) |  |
### AREA {#AREA}
```
public static int AREA
```


Диаграмма области.

### AREA_3_D {#AREA-3-D}
```
public static int AREA_3_D
```


3D-диаграмма области.

### AREA_3_D_PERCENT_STACKED {#AREA-3-D-PERCENT-STACKED}
```
public static int AREA_3_D_PERCENT_STACKED
```


3D 100% сложенная диаграмма области.

### AREA_3_D_STACKED {#AREA-3-D-STACKED}
```
public static int AREA_3_D_STACKED
```


3D сложенная диаграмма области.

### AREA_PERCENT_STACKED {#AREA-PERCENT-STACKED}
```
public static int AREA_PERCENT_STACKED
```


100% сложенная диаграмма области.

### AREA_STACKED {#AREA-STACKED}
```
public static int AREA_STACKED
```


Сложенная диаграмма области.

### BAR {#BAR}
```
public static int BAR
```


Гистограмма.

### BAR_3_D {#BAR-3-D}
```
public static int BAR_3_D
```


3D гистограмма.

### BAR_3_D_PERCENT_STACKED {#BAR-3-D-PERCENT-STACKED}
```
public static int BAR_3_D_PERCENT_STACKED
```


3D 100% сложенная гистограмма.

### BAR_3_D_STACKED {#BAR-3-D-STACKED}
```
public static int BAR_3_D_STACKED
```


3D сложенная гистограмма.

### BAR_PERCENT_STACKED {#BAR-PERCENT-STACKED}
```
public static int BAR_PERCENT_STACKED
```


100% сложенная гистограмма.

### BAR_STACKED {#BAR-STACKED}
```
public static int BAR_STACKED
```


Сложенная гистограмма.

### BOX_AND_WHISKER {#BOX-AND-WHISKER}
```
public static int BOX_AND_WHISKER
```


Диаграмма «ящик с усами».

### BUBBLE {#BUBBLE}
```
public static int BUBBLE
```


Пузырьковая диаграмма.

### BUBBLE_3_D {#BUBBLE-3-D}
```
public static int BUBBLE_3_D
```


3D пузырьковая диаграмма.

### COLUMN {#COLUMN}
```
public static int COLUMN
```


Столбчатая диаграмма.

### COLUMN_3_D {#COLUMN-3-D}
```
public static int COLUMN_3_D
```


3D столбчатая диаграмма.

### COLUMN_3_D_CLUSTERED {#COLUMN-3-D-CLUSTERED}
```
public static int COLUMN_3_D_CLUSTERED
```


3D сгруппированная столбчатая диаграмма.

### COLUMN_3_D_PERCENT_STACKED {#COLUMN-3-D-PERCENT-STACKED}
```
public static int COLUMN_3_D_PERCENT_STACKED
```


3D 100% сложенная столбчатая диаграмма.

### COLUMN_3_D_STACKED {#COLUMN-3-D-STACKED}
```
public static int COLUMN_3_D_STACKED
```


3D сложенная столбчатая диаграмма.

### COLUMN_PERCENT_STACKED {#COLUMN-PERCENT-STACKED}
```
public static int COLUMN_PERCENT_STACKED
```


100% сложенная столбчатая диаграмма.

### COLUMN_STACKED {#COLUMN-STACKED}
```
public static int COLUMN_STACKED
```


Сложенная столбчатая диаграмма.

### DOUGHNUT {#DOUGHNUT}
```
public static int DOUGHNUT
```


Кольцевая диаграмма.

### FUNNEL {#FUNNEL}
```
public static int FUNNEL
```


Воронкообразная диаграмма.

### HISTOGRAM {#HISTOGRAM}
```
public static int HISTOGRAM
```


Гистограмма.

### LINE {#LINE}
```
public static int LINE
```


Линейная диаграмма.

### LINE_3_D {#LINE-3-D}
```
public static int LINE_3_D
```


3D линейная диаграмма.

### LINE_PERCENT_STACKED {#LINE-PERCENT-STACKED}
```
public static int LINE_PERCENT_STACKED
```


100% сложенная линейная диаграмма.

### LINE_STACKED {#LINE-STACKED}
```
public static int LINE_STACKED
```


Сложенная линейная диаграмма.

### PARETO {#PARETO}
```
public static int PARETO
```


Диаграмма Парето.

### PIE {#PIE}
```
public static int PIE
```


Круговая диаграмма.

### PIE_3_D {#PIE-3-D}
```
public static int PIE_3_D
```


3D круговая диаграмма.

### PIE_OF_BAR {#PIE-OF-BAR}
```
public static int PIE_OF_BAR
```


Круговая диаграмма в виде столбца.

### PIE_OF_PIE {#PIE-OF-PIE}
```
public static int PIE_OF_PIE
```


Круговая диаграмма в виде круговой диаграммы.

### RADAR {#RADAR}
```
public static int RADAR
```


Радарная диаграмма.

### SCATTER {#SCATTER}
```
public static int SCATTER
```


Точечная диаграмма.

### STOCK {#STOCK}
```
public static int STOCK
```


График акций.

### SUNBURST {#SUNBURST}
```
public static int SUNBURST
```


Диаграмма лучевого разбиения.

### SURFACE {#SURFACE}
```
public static int SURFACE
```


Поверхностная диаграмма.

### SURFACE_3_D {#SURFACE-3-D}
```
public static int SURFACE_3_D
```


3D поверхностная диаграмма.

### TREEMAP {#TREEMAP}
```
public static int TREEMAP
```


Диаграмма дерево-карта.

### WATERFALL {#WATERFALL}
```
public static int WATERFALL
```


Водопадная диаграмма.

### length {#length}
```
public static int length
```


### fromName(String chartTypeName) {#fromName-java.lang.String}
```
public static int fromName(String chartTypeName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| chartTypeName | java.lang.String |  |

**Returns:**
int
### getName(int chartType) {#getName-int}
```
public static String getName(int chartType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| chartType | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int chartType) {#toString-int}
```
public static String toString(int chartType)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| chartType | int |  |

**Returns:**
java.lang.String
