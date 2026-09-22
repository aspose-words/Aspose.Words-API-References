---
title: "ChartType"
linktitle: "ChartType"
second_title: "Aspose.Words لـ Java"
description: "يحدد نوع المخطط في Java."
type: docs
weight: 93
url: /ar/java/com.aspose.words/charttype/
---

**Inheritance:**
java.lang.Object
```
public class ChartType
```

يحدد نوع المخطط.

 **Examples:** 

يوضح كيفية إنشاء نوع مناسب من سلاسل المخطط لنوع الرسم البياني.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [AREA](#AREA) | مخطط المنطقة. |
| [AREA_3_D](#AREA-3-D) | مخطط المنطقة ثلاثي الأبعاد. |
| [AREA_3_D_PERCENT_STACKED](#AREA-3-D-PERCENT-STACKED) | مخطط المنطقة المكدس 100% ثلاثي الأبعاد. |
| [AREA_3_D_STACKED](#AREA-3-D-STACKED) | مخطط المنطقة المكدس ثلاثي الأبعاد. |
| [AREA_PERCENT_STACKED](#AREA-PERCENT-STACKED) | مخطط المنطقة المكدس 100%. |
| [AREA_STACKED](#AREA-STACKED) | مخطط المنطقة المكدس. |
| [BAR](#BAR) | مخطط شريطي. |
| [BAR_3_D](#BAR-3-D) | مخطط شريطي ثلاثي الأبعاد. |
| [BAR_3_D_PERCENT_STACKED](#BAR-3-D-PERCENT-STACKED) | مخطط الشريطي المكدس 100% ثلاثي الأبعاد. |
| [BAR_3_D_STACKED](#BAR-3-D-STACKED) | مخطط الشريطي المكدس ثلاثي الأبعاد. |
| [BAR_PERCENT_STACKED](#BAR-PERCENT-STACKED) | مخطط الشريطي المكدس 100%. |
| [BAR_STACKED](#BAR-STACKED) | مخطط الشريطي المكدس. |
| [BOX_AND_WHISKER](#BOX-AND-WHISKER) | مخطط الصندوق والشارب. |
| [BUBBLE](#BUBBLE) | مخطط الفقاعات. |
| [BUBBLE_3_D](#BUBBLE-3-D) | مخطط الفقاعات ثلاثي الأبعاد. |
| [COLUMN](#COLUMN) | مخطط عمودي. |
| [COLUMN_3_D](#COLUMN-3-D) | مخطط عمودي ثلاثي الأبعاد. |
| [COLUMN_3_D_CLUSTERED](#COLUMN-3-D-CLUSTERED) | مخطط العمود المتجمع ثلاثي الأبعاد. |
| [COLUMN_3_D_PERCENT_STACKED](#COLUMN-3-D-PERCENT-STACKED) | مخطط العمود المكدس 100% ثلاثي الأبعاد. |
| [COLUMN_3_D_STACKED](#COLUMN-3-D-STACKED) | مخطط العمود المكدس ثلاثي الأبعاد. |
| [COLUMN_PERCENT_STACKED](#COLUMN-PERCENT-STACKED) | مخطط العمود المكدس 100%. |
| [COLUMN_STACKED](#COLUMN-STACKED) | مخطط العمود المكدس. |
| [DOUGHNUT](#DOUGHNUT) | مخطط الدونات. |
| [FUNNEL](#FUNNEL) | مخطط القمع. |
| [HISTOGRAM](#HISTOGRAM) | مخطط المدرج التكراري. |
| [LINE](#LINE) | مخطط خطي. |
| [LINE_3_D](#LINE-3-D) | مخطط خطي ثلاثي الأبعاد. |
| [LINE_PERCENT_STACKED](#LINE-PERCENT-STACKED) | مخطط خطي مكدس 100٪. |
| [LINE_STACKED](#LINE-STACKED) | مخطط خطي مكدس. |
| [PARETO](#PARETO) | مخطط باريتو. |
| [PIE](#PIE) | مخطط دائري. |
| [PIE_3_D](#PIE-3-D) | مخطط دائري ثلاثي الأبعاد. |
| [PIE_OF_BAR](#PIE-OF-BAR) | مخطط شريط دائري. |
| [PIE_OF_PIE](#PIE-OF-PIE) | مخطط دائري داخل دائري. |
| [RADAR](#RADAR) | مخطط راداري. |
| [SCATTER](#SCATTER) | مخطط مبعثر. |
| [STOCK](#STOCK) | مخطط الأسهم. |
| [SUNBURST](#SUNBURST) | مخطط شمسية. |
| [SURFACE](#SURFACE) | مخطط سطحي. |
| [SURFACE_3_D](#SURFACE-3-D) | مخطط سطحي ثلاثي الأبعاد. |
| [TREEMAP](#TREEMAP) | مخطط شجرة الخريطة. |
| [WATERFALL](#WATERFALL) | مخطط شلال. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String chartTypeName)](#fromName-java.lang.String) |  |
| [getName(int chartType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartType)](#toString-int) |  |
### AREA {#AREA}
```
public static int AREA
```


مخطط المنطقة.

### AREA_3_D {#AREA-3-D}
```
public static int AREA_3_D
```


مخطط المنطقة ثلاثي الأبعاد.

### AREA_3_D_PERCENT_STACKED {#AREA-3-D-PERCENT-STACKED}
```
public static int AREA_3_D_PERCENT_STACKED
```


مخطط المنطقة المكدس 100% ثلاثي الأبعاد.

### AREA_3_D_STACKED {#AREA-3-D-STACKED}
```
public static int AREA_3_D_STACKED
```


مخطط المنطقة المكدس ثلاثي الأبعاد.

### AREA_PERCENT_STACKED {#AREA-PERCENT-STACKED}
```
public static int AREA_PERCENT_STACKED
```


مخطط المنطقة المكدس 100%.

### AREA_STACKED {#AREA-STACKED}
```
public static int AREA_STACKED
```


مخطط المنطقة المكدس.

### BAR {#BAR}
```
public static int BAR
```


مخطط شريطي.

### BAR_3_D {#BAR-3-D}
```
public static int BAR_3_D
```


مخطط شريطي ثلاثي الأبعاد.

### BAR_3_D_PERCENT_STACKED {#BAR-3-D-PERCENT-STACKED}
```
public static int BAR_3_D_PERCENT_STACKED
```


مخطط الشريطي المكدس 100% ثلاثي الأبعاد.

### BAR_3_D_STACKED {#BAR-3-D-STACKED}
```
public static int BAR_3_D_STACKED
```


مخطط الشريطي المكدس ثلاثي الأبعاد.

### BAR_PERCENT_STACKED {#BAR-PERCENT-STACKED}
```
public static int BAR_PERCENT_STACKED
```


مخطط الشريطي المكدس 100%.

### BAR_STACKED {#BAR-STACKED}
```
public static int BAR_STACKED
```


مخطط الشريطي المكدس.

### BOX_AND_WHISKER {#BOX-AND-WHISKER}
```
public static int BOX_AND_WHISKER
```


مخطط الصندوق والشارب.

### BUBBLE {#BUBBLE}
```
public static int BUBBLE
```


مخطط الفقاعات.

### BUBBLE_3_D {#BUBBLE-3-D}
```
public static int BUBBLE_3_D
```


مخطط الفقاعات ثلاثي الأبعاد.

### COLUMN {#COLUMN}
```
public static int COLUMN
```


مخطط عمودي.

### COLUMN_3_D {#COLUMN-3-D}
```
public static int COLUMN_3_D
```


مخطط عمودي ثلاثي الأبعاد.

### COLUMN_3_D_CLUSTERED {#COLUMN-3-D-CLUSTERED}
```
public static int COLUMN_3_D_CLUSTERED
```


مخطط العمود المتجمع ثلاثي الأبعاد.

### COLUMN_3_D_PERCENT_STACKED {#COLUMN-3-D-PERCENT-STACKED}
```
public static int COLUMN_3_D_PERCENT_STACKED
```


مخطط العمود المكدس 100% ثلاثي الأبعاد.

### COLUMN_3_D_STACKED {#COLUMN-3-D-STACKED}
```
public static int COLUMN_3_D_STACKED
```


مخطط العمود المكدس ثلاثي الأبعاد.

### COLUMN_PERCENT_STACKED {#COLUMN-PERCENT-STACKED}
```
public static int COLUMN_PERCENT_STACKED
```


مخطط العمود المكدس 100%.

### COLUMN_STACKED {#COLUMN-STACKED}
```
public static int COLUMN_STACKED
```


مخطط العمود المكدس.

### DOUGHNUT {#DOUGHNUT}
```
public static int DOUGHNUT
```


مخطط الدونات.

### FUNNEL {#FUNNEL}
```
public static int FUNNEL
```


مخطط القمع.

### HISTOGRAM {#HISTOGRAM}
```
public static int HISTOGRAM
```


مخطط المدرج التكراري.

### LINE {#LINE}
```
public static int LINE
```


مخطط خطي.

### LINE_3_D {#LINE-3-D}
```
public static int LINE_3_D
```


مخطط خطي ثلاثي الأبعاد.

### LINE_PERCENT_STACKED {#LINE-PERCENT-STACKED}
```
public static int LINE_PERCENT_STACKED
```


مخطط خطي مكدس 100٪.

### LINE_STACKED {#LINE-STACKED}
```
public static int LINE_STACKED
```


مخطط خطي مكدس.

### PARETO {#PARETO}
```
public static int PARETO
```


مخطط باريتو.

### PIE {#PIE}
```
public static int PIE
```


مخطط دائري.

### PIE_3_D {#PIE-3-D}
```
public static int PIE_3_D
```


مخطط دائري ثلاثي الأبعاد.

### PIE_OF_BAR {#PIE-OF-BAR}
```
public static int PIE_OF_BAR
```


مخطط شريط دائري.

### PIE_OF_PIE {#PIE-OF-PIE}
```
public static int PIE_OF_PIE
```


مخطط دائري داخل دائري.

### RADAR {#RADAR}
```
public static int RADAR
```


مخطط راداري.

### SCATTER {#SCATTER}
```
public static int SCATTER
```


مخطط مبعثر.

### STOCK {#STOCK}
```
public static int STOCK
```


مخطط الأسهم.

### SUNBURST {#SUNBURST}
```
public static int SUNBURST
```


مخطط شمسية.

### SURFACE {#SURFACE}
```
public static int SURFACE
```


مخطط سطحي.

### SURFACE_3_D {#SURFACE-3-D}
```
public static int SURFACE_3_D
```


مخطط سطحي ثلاثي الأبعاد.

### TREEMAP {#TREEMAP}
```
public static int TREEMAP
```


مخطط شجرة الخريطة.

### WATERFALL {#WATERFALL}
```
public static int WATERFALL
```


مخطط شلال.

### length {#length}
```
public static int length
```


### fromName(String chartTypeName) {#fromName-java.lang.String}
```
public static int fromName(String chartTypeName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| chartTypeName | java.lang.String |  |

**Returns:**
int
### getName(int chartType) {#getName-int}
```
public static String getName(int chartType)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| chartType | int |  |

**Returns:**
java.lang.String
