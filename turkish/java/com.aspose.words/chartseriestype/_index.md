---
title: "ChartSeriesType"
linktitle: "ChartSeriesType"
second_title: "Aspose.Words Java için"
description: "Java'da bir grafik serisi türünü belirtir."
type: docs
weight: 89
url: /tr/java/com.aspose.words/chartseriestype/
---

**Inheritance:**
java.lang.Object
```
public class ChartSeriesType
```

Bir grafik serisinin tipini belirtir.

 **Examples:** 

Belirli bir grafik serisinin nasıl kaldırılacağını gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [AREA](#AREA) | Bir Alan grafik serisini temsil eder. |
| [AREA_3_D](#AREA-3-D) | Bir 3D Alan grafik serisini temsil eder. |
| [AREA_3_D_PERCENT_STACKED](#AREA-3-D-PERCENT-STACKED) | Bir 3D %100 Yığılmış Alan grafik serisini temsil eder. |
| [AREA_3_D_STACKED](#AREA-3-D-STACKED) | Bir 3D Yığılmış Alan grafik serisini temsil eder. |
| [AREA_PERCENT_STACKED](#AREA-PERCENT-STACKED) | %100 Yığılmış Alan grafik serisini temsil eder. |
| [AREA_STACKED](#AREA-STACKED) | Yığılmış Alan grafik serisini temsil eder. |
| [BAR](#BAR) | Bir Çubuk grafik serisini temsil eder. |
| [BAR_3_D](#BAR-3-D) | Bir 3D Çubuk grafik serisini temsil eder. |
| [BAR_3_D_PERCENT_STACKED](#BAR-3-D-PERCENT-STACKED) | Bir 3D %100 Yığılmış Çubuk grafik serisini temsil eder. |
| [BAR_3_D_STACKED](#BAR-3-D-STACKED) | Bir 3D Yığılmış Çubuk grafik serisini temsil eder. |
| [BAR_PERCENT_STACKED](#BAR-PERCENT-STACKED) | %100 Yığılmış Çubuk grafik serisini temsil eder. |
| [BAR_STACKED](#BAR-STACKED) | Yığılmış Çubuk grafik serisini temsil eder. |
| [BOX_AND_WHISKER](#BOX-AND-WHISKER) | Bir Kutu ve Bıyık grafik serisini temsil eder. |
| [BUBBLE](#BUBBLE) | Bir Balon grafik serisini temsil eder. |
| [BUBBLE_3_D](#BUBBLE-3-D) | Bir 3D Balon grafik serisini temsil eder. |
| [COLUMN](#COLUMN) | Bir Sütun grafik serisini temsil eder. |
| [COLUMN_3_D](#COLUMN-3-D) | 3D Sütun grafik serisini temsil eder. |
| [COLUMN_3_D_CLUSTERED](#COLUMN-3-D-CLUSTERED) | 3D Küme Sütun grafik serisini temsil eder. |
| [COLUMN_3_D_PERCENT_STACKED](#COLUMN-3-D-PERCENT-STACKED) | 3D %100 Yığılmış Sütun grafik serisini temsil eder. |
| [COLUMN_3_D_STACKED](#COLUMN-3-D-STACKED) | 3D Yığılmış Sütun grafik serisini temsil eder. |
| [COLUMN_PERCENT_STACKED](#COLUMN-PERCENT-STACKED) | %100 Yığılmış Sütun grafik serisini temsil eder. |
| [COLUMN_STACKED](#COLUMN-STACKED) | Yığılmış Sütun grafik serisini temsil eder. |
| [DOUGHNUT](#DOUGHNUT) | Halka grafik serisini temsil eder. |
| [FUNNEL](#FUNNEL) | Huni grafik serisini temsil eder. |
| [HISTOGRAM](#HISTOGRAM) | Histogram grafik serisini temsil eder. |
| [LINE](#LINE) | Çizgi grafik serisini temsil eder. |
| [LINE_3_D](#LINE-3-D) | 3D Çizgi grafik serisini temsil eder. |
| [LINE_PERCENT_STACKED](#LINE-PERCENT-STACKED) | %100 Yığılmış Çizgi grafik serisini temsil eder. |
| [LINE_STACKED](#LINE-STACKED) | Yığılmış Çizgi grafik serisini temsil eder. |
| [PARETO](#PARETO) | Pareto grafik serisini temsil eder. |
| [PARETO_LINE](#PARETO-LINE) | Pareto Çizgi grafik serisini temsil eder. |
| [PIE](#PIE) | Pasta grafik serisini temsil eder. |
| [PIE_3_D](#PIE-3-D) | 3D Pasta grafik serisini temsil eder. |
| [PIE_OF_BAR](#PIE-OF-BAR) | Bar Pasta grafik serisini temsil eder. |
| [PIE_OF_PIE](#PIE-OF-PIE) | Pasta içinde Pasta grafik serisini temsil eder. |
| [RADAR](#RADAR) | Radar grafik serisini temsil eder. |
| [REGION_MAP](#REGION-MAP) | Bölge Haritası grafik serisini temsil eder. |
| [SCATTER](#SCATTER) | Saçılım grafik serisini temsil eder. |
| [STOCK](#STOCK) | Hisse senedi grafik serisini temsil eder. |
| [SUNBURST](#SUNBURST) | Güneş Patlaması grafik serisini temsil eder. |
| [SURFACE](#SURFACE) | Yüzey grafik serisini temsil eder. |
| [SURFACE_3_D](#SURFACE-3-D) | 3D Yüzey grafik serisini temsil eder. |
| [TREEMAP](#TREEMAP) | Treemap grafik serisini temsil eder. |
| [WATERFALL](#WATERFALL) | Waterfall grafik serisini temsil eder. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String chartSeriesTypeName)](#fromName-java.lang.String) |  |
| [getName(int chartSeriesType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartSeriesType)](#toString-int) |  |
### AREA {#AREA}
```
public static int AREA
```


Bir Alan grafik serisini temsil eder.

### AREA_3_D {#AREA-3-D}
```
public static int AREA_3_D
```


Bir 3D Alan grafik serisini temsil eder.

### AREA_3_D_PERCENT_STACKED {#AREA-3-D-PERCENT-STACKED}
```
public static int AREA_3_D_PERCENT_STACKED
```


Bir 3D %100 Yığılmış Alan grafik serisini temsil eder.

### AREA_3_D_STACKED {#AREA-3-D-STACKED}
```
public static int AREA_3_D_STACKED
```


Bir 3D Yığılmış Alan grafik serisini temsil eder.

### AREA_PERCENT_STACKED {#AREA-PERCENT-STACKED}
```
public static int AREA_PERCENT_STACKED
```


%100 Yığılmış Alan grafik serisini temsil eder.

### AREA_STACKED {#AREA-STACKED}
```
public static int AREA_STACKED
```


Yığılmış Alan grafik serisini temsil eder.

### BAR {#BAR}
```
public static int BAR
```


Bir Çubuk grafik serisini temsil eder.

### BAR_3_D {#BAR-3-D}
```
public static int BAR_3_D
```


Bir 3D Çubuk grafik serisini temsil eder.

### BAR_3_D_PERCENT_STACKED {#BAR-3-D-PERCENT-STACKED}
```
public static int BAR_3_D_PERCENT_STACKED
```


Bir 3D %100 Yığılmış Çubuk grafik serisini temsil eder.

### BAR_3_D_STACKED {#BAR-3-D-STACKED}
```
public static int BAR_3_D_STACKED
```


Bir 3D Yığılmış Çubuk grafik serisini temsil eder.

### BAR_PERCENT_STACKED {#BAR-PERCENT-STACKED}
```
public static int BAR_PERCENT_STACKED
```


%100 Yığılmış Çubuk grafik serisini temsil eder.

### BAR_STACKED {#BAR-STACKED}
```
public static int BAR_STACKED
```


Yığılmış Çubuk grafik serisini temsil eder.

### BOX_AND_WHISKER {#BOX-AND-WHISKER}
```
public static int BOX_AND_WHISKER
```


Bir Kutu ve Bıyık grafik serisini temsil eder.

### BUBBLE {#BUBBLE}
```
public static int BUBBLE
```


Bir Balon grafik serisini temsil eder.

### BUBBLE_3_D {#BUBBLE-3-D}
```
public static int BUBBLE_3_D
```


Bir 3D Balon grafik serisini temsil eder.

### COLUMN {#COLUMN}
```
public static int COLUMN
```


Bir Sütun grafik serisini temsil eder.

### COLUMN_3_D {#COLUMN-3-D}
```
public static int COLUMN_3_D
```


3D Sütun grafik serisini temsil eder.

### COLUMN_3_D_CLUSTERED {#COLUMN-3-D-CLUSTERED}
```
public static int COLUMN_3_D_CLUSTERED
```


3D Küme Sütun grafik serisini temsil eder.

### COLUMN_3_D_PERCENT_STACKED {#COLUMN-3-D-PERCENT-STACKED}
```
public static int COLUMN_3_D_PERCENT_STACKED
```


3D %100 Yığılmış Sütun grafik serisini temsil eder.

### COLUMN_3_D_STACKED {#COLUMN-3-D-STACKED}
```
public static int COLUMN_3_D_STACKED
```


3D Yığılmış Sütun grafik serisini temsil eder.

### COLUMN_PERCENT_STACKED {#COLUMN-PERCENT-STACKED}
```
public static int COLUMN_PERCENT_STACKED
```


%100 Yığılmış Sütun grafik serisini temsil eder.

### COLUMN_STACKED {#COLUMN-STACKED}
```
public static int COLUMN_STACKED
```


Yığılmış Sütun grafik serisini temsil eder.

### DOUGHNUT {#DOUGHNUT}
```
public static int DOUGHNUT
```


Halka grafik serisini temsil eder.

### FUNNEL {#FUNNEL}
```
public static int FUNNEL
```


Huni grafik serisini temsil eder.

### HISTOGRAM {#HISTOGRAM}
```
public static int HISTOGRAM
```


Histogram grafik serisini temsil eder.

### LINE {#LINE}
```
public static int LINE
```


Çizgi grafik serisini temsil eder.

### LINE_3_D {#LINE-3-D}
```
public static int LINE_3_D
```


3D Çizgi grafik serisini temsil eder.

### LINE_PERCENT_STACKED {#LINE-PERCENT-STACKED}
```
public static int LINE_PERCENT_STACKED
```


%100 Yığılmış Çizgi grafik serisini temsil eder.

### LINE_STACKED {#LINE-STACKED}
```
public static int LINE_STACKED
```


Yığılmış Çizgi grafik serisini temsil eder.

### PARETO {#PARETO}
```
public static int PARETO
```


Pareto grafik serisini temsil eder.

### PARETO_LINE {#PARETO-LINE}
```
public static int PARETO_LINE
```


Pareto Çizgi grafik serisini temsil eder.

### PIE {#PIE}
```
public static int PIE
```


Pasta grafik serisini temsil eder.

### PIE_3_D {#PIE-3-D}
```
public static int PIE_3_D
```


3D Pasta grafik serisini temsil eder.

### PIE_OF_BAR {#PIE-OF-BAR}
```
public static int PIE_OF_BAR
```


Bar Pasta grafik serisini temsil eder.

### PIE_OF_PIE {#PIE-OF-PIE}
```
public static int PIE_OF_PIE
```


Pasta içinde Pasta grafik serisini temsil eder.

### RADAR {#RADAR}
```
public static int RADAR
```


Radar grafik serisini temsil eder.

### REGION_MAP {#REGION-MAP}
```
public static int REGION_MAP
```


Bölge Haritası grafik serisini temsil eder.

### SCATTER {#SCATTER}
```
public static int SCATTER
```


Saçılım grafik serisini temsil eder.

### STOCK {#STOCK}
```
public static int STOCK
```


Hisse senedi grafik serisini temsil eder.

### SUNBURST {#SUNBURST}
```
public static int SUNBURST
```


Güneş Patlaması grafik serisini temsil eder.

### SURFACE {#SURFACE}
```
public static int SURFACE
```


Yüzey grafik serisini temsil eder.

### SURFACE_3_D {#SURFACE-3-D}
```
public static int SURFACE_3_D
```


3D Yüzey grafik serisini temsil eder.

### TREEMAP {#TREEMAP}
```
public static int TREEMAP
```


Treemap grafik serisini temsil eder.

### WATERFALL {#WATERFALL}
```
public static int WATERFALL
```


Waterfall grafik serisini temsil eder.

### length {#length}
```
public static int length
```


### fromName(String chartSeriesTypeName) {#fromName-java.lang.String}
```
public static int fromName(String chartSeriesTypeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| chartSeriesTypeName | java.lang.String |  |

**Returns:**
int
### getName(int chartSeriesType) {#getName-int}
```
public static String getName(int chartSeriesType)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| chartSeriesType | int |  |

**Returns:**
java.lang.String
