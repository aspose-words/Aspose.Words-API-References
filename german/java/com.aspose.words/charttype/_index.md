---
title: "ChartType"
linktitle: "ChartType"
second_title: "Aspose.Words für Java"
description: "Gibt den Typ eines Diagramms in Java an."
type: docs
weight: 93
url: /de/java/com.aspose.words/charttype/
---

**Inheritance:**
java.lang.Object
```
public class ChartType
```

Gibt den Typ eines Diagramms an.

 **Examples:** 

Zeigt, wie man einen geeigneten Diagrammserientyp für einen Diagrammtyp erstellt.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [AREA](#AREA) | Flächendiagramm. |
| [AREA_3_D](#AREA-3-D) | 3D-Flächendiagramm. |
| [AREA_3_D_PERCENT_STACKED](#AREA-3-D-PERCENT-STACKED) | 3D 100% gestapeltes Flächendiagramm. |
| [AREA_3_D_STACKED](#AREA-3-D-STACKED) | 3D gestapeltes Flächendiagramm. |
| [AREA_PERCENT_STACKED](#AREA-PERCENT-STACKED) | 100% gestapeltes Flächendiagramm. |
| [AREA_STACKED](#AREA-STACKED) | Gestapeltes Flächendiagramm. |
| [BAR](#BAR) | Balkendiagramm. |
| [BAR_3_D](#BAR-3-D) | 3D-Balkendiagramm. |
| [BAR_3_D_PERCENT_STACKED](#BAR-3-D-PERCENT-STACKED) | 3D 100% gestapeltes Balkendiagramm. |
| [BAR_3_D_STACKED](#BAR-3-D-STACKED) | 3D gestapeltes Balkendiagramm. |
| [BAR_PERCENT_STACKED](#BAR-PERCENT-STACKED) | 100% gestapeltes Balkendiagramm. |
| [BAR_STACKED](#BAR-STACKED) | Gestapeltes Balkendiagramm. |
| [BOX_AND_WHISKER](#BOX-AND-WHISKER) | Box-Whisker-Diagramm. |
| [BUBBLE](#BUBBLE) | Blasendiagramm. |
| [BUBBLE_3_D](#BUBBLE-3-D) | 3D-Blasendiagramm. |
| [COLUMN](#COLUMN) | Säulendiagramm. |
| [COLUMN_3_D](#COLUMN-3-D) | 3D-Säulendiagramm. |
| [COLUMN_3_D_CLUSTERED](#COLUMN-3-D-CLUSTERED) | 3D gruppiertes Säulendiagramm. |
| [COLUMN_3_D_PERCENT_STACKED](#COLUMN-3-D-PERCENT-STACKED) | 3D 100% gestapeltes Säulendiagramm. |
| [COLUMN_3_D_STACKED](#COLUMN-3-D-STACKED) | 3D gestapeltes Säulendiagramm. |
| [COLUMN_PERCENT_STACKED](#COLUMN-PERCENT-STACKED) | 100% gestapeltes Säulendiagramm. |
| [COLUMN_STACKED](#COLUMN-STACKED) | Gestapeltes Säulendiagramm. |
| [DOUGHNUT](#DOUGHNUT) | Donut-Diagramm. |
| [FUNNEL](#FUNNEL) | Trichterdiagramm. |
| [HISTOGRAM](#HISTOGRAM) | Histogramm-Diagramm. |
| [LINE](#LINE) | Liniendiagramm. |
| [LINE_3_D](#LINE-3-D) | 3D-Liniendiagramm. |
| [LINE_PERCENT_STACKED](#LINE-PERCENT-STACKED) | 100% gestapeltes Liniendiagramm. |
| [LINE_STACKED](#LINE-STACKED) | Gestapeltes Liniendiagramm. |
| [PARETO](#PARETO) | Pareto-Diagramm. |
| [PIE](#PIE) | Kreisdiagramm. |
| [PIE_3_D](#PIE-3-D) | 3D-Kreisdiagramm. |
| [PIE_OF_BAR](#PIE-OF-BAR) | Kreis‑aus‑Balken-Diagramm. |
| [PIE_OF_PIE](#PIE-OF-PIE) | Kreis‑aus‑Kreis-Diagramm. |
| [RADAR](#RADAR) | Radar-Diagramm. |
| [SCATTER](#SCATTER) | Punktediagramm. |
| [STOCK](#STOCK) | Börsendiagramm. |
| [SUNBURST](#SUNBURST) | Sunburst-Diagramm. |
| [SURFACE](#SURFACE) | Oberflächendiagramm. |
| [SURFACE_3_D](#SURFACE-3-D) | 3D-Oberflächendiagramm. |
| [TREEMAP](#TREEMAP) | Baumdiagramm. |
| [WATERFALL](#WATERFALL) | Wasserfalldiagramm. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String chartTypeName)](#fromName-java.lang.String) |  |
| [getName(int chartType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartType)](#toString-int) |  |
### AREA {#AREA}
```
public static int AREA
```


Flächendiagramm.

### AREA_3_D {#AREA-3-D}
```
public static int AREA_3_D
```


3D-Flächendiagramm.

### AREA_3_D_PERCENT_STACKED {#AREA-3-D-PERCENT-STACKED}
```
public static int AREA_3_D_PERCENT_STACKED
```


3D 100% gestapeltes Flächendiagramm.

### AREA_3_D_STACKED {#AREA-3-D-STACKED}
```
public static int AREA_3_D_STACKED
```


3D gestapeltes Flächendiagramm.

### AREA_PERCENT_STACKED {#AREA-PERCENT-STACKED}
```
public static int AREA_PERCENT_STACKED
```


100% gestapeltes Flächendiagramm.

### AREA_STACKED {#AREA-STACKED}
```
public static int AREA_STACKED
```


Gestapeltes Flächendiagramm.

### BAR {#BAR}
```
public static int BAR
```


Balkendiagramm.

### BAR_3_D {#BAR-3-D}
```
public static int BAR_3_D
```


3D-Balkendiagramm.

### BAR_3_D_PERCENT_STACKED {#BAR-3-D-PERCENT-STACKED}
```
public static int BAR_3_D_PERCENT_STACKED
```


3D 100% gestapeltes Balkendiagramm.

### BAR_3_D_STACKED {#BAR-3-D-STACKED}
```
public static int BAR_3_D_STACKED
```


3D gestapeltes Balkendiagramm.

### BAR_PERCENT_STACKED {#BAR-PERCENT-STACKED}
```
public static int BAR_PERCENT_STACKED
```


100% gestapeltes Balkendiagramm.

### BAR_STACKED {#BAR-STACKED}
```
public static int BAR_STACKED
```


Gestapeltes Balkendiagramm.

### BOX_AND_WHISKER {#BOX-AND-WHISKER}
```
public static int BOX_AND_WHISKER
```


Box-Whisker-Diagramm.

### BUBBLE {#BUBBLE}
```
public static int BUBBLE
```


Blasendiagramm.

### BUBBLE_3_D {#BUBBLE-3-D}
```
public static int BUBBLE_3_D
```


3D-Blasendiagramm.

### COLUMN {#COLUMN}
```
public static int COLUMN
```


Säulendiagramm.

### COLUMN_3_D {#COLUMN-3-D}
```
public static int COLUMN_3_D
```


3D-Säulendiagramm.

### COLUMN_3_D_CLUSTERED {#COLUMN-3-D-CLUSTERED}
```
public static int COLUMN_3_D_CLUSTERED
```


3D gruppiertes Säulendiagramm.

### COLUMN_3_D_PERCENT_STACKED {#COLUMN-3-D-PERCENT-STACKED}
```
public static int COLUMN_3_D_PERCENT_STACKED
```


3D 100% gestapeltes Säulendiagramm.

### COLUMN_3_D_STACKED {#COLUMN-3-D-STACKED}
```
public static int COLUMN_3_D_STACKED
```


3D gestapeltes Säulendiagramm.

### COLUMN_PERCENT_STACKED {#COLUMN-PERCENT-STACKED}
```
public static int COLUMN_PERCENT_STACKED
```


100% gestapeltes Säulendiagramm.

### COLUMN_STACKED {#COLUMN-STACKED}
```
public static int COLUMN_STACKED
```


Gestapeltes Säulendiagramm.

### DOUGHNUT {#DOUGHNUT}
```
public static int DOUGHNUT
```


Donut-Diagramm.

### FUNNEL {#FUNNEL}
```
public static int FUNNEL
```


Trichterdiagramm.

### HISTOGRAM {#HISTOGRAM}
```
public static int HISTOGRAM
```


Histogramm-Diagramm.

### LINE {#LINE}
```
public static int LINE
```


Liniendiagramm.

### LINE_3_D {#LINE-3-D}
```
public static int LINE_3_D
```


3D-Liniendiagramm.

### LINE_PERCENT_STACKED {#LINE-PERCENT-STACKED}
```
public static int LINE_PERCENT_STACKED
```


100% gestapeltes Liniendiagramm.

### LINE_STACKED {#LINE-STACKED}
```
public static int LINE_STACKED
```


Gestapeltes Liniendiagramm.

### PARETO {#PARETO}
```
public static int PARETO
```


Pareto-Diagramm.

### PIE {#PIE}
```
public static int PIE
```


Kreisdiagramm.

### PIE_3_D {#PIE-3-D}
```
public static int PIE_3_D
```


3D-Kreisdiagramm.

### PIE_OF_BAR {#PIE-OF-BAR}
```
public static int PIE_OF_BAR
```


Kreis‑aus‑Balken-Diagramm.

### PIE_OF_PIE {#PIE-OF-PIE}
```
public static int PIE_OF_PIE
```


Kreis‑aus‑Kreis-Diagramm.

### RADAR {#RADAR}
```
public static int RADAR
```


Radar-Diagramm.

### SCATTER {#SCATTER}
```
public static int SCATTER
```


Punktediagramm.

### STOCK {#STOCK}
```
public static int STOCK
```


Börsendiagramm.

### SUNBURST {#SUNBURST}
```
public static int SUNBURST
```


Sunburst-Diagramm.

### SURFACE {#SURFACE}
```
public static int SURFACE
```


Oberflächendiagramm.

### SURFACE_3_D {#SURFACE-3-D}
```
public static int SURFACE_3_D
```


3D-Oberflächendiagramm.

### TREEMAP {#TREEMAP}
```
public static int TREEMAP
```


Baumdiagramm.

### WATERFALL {#WATERFALL}
```
public static int WATERFALL
```


Wasserfalldiagramm.

### length {#length}
```
public static int length
```


### fromName(String chartTypeName) {#fromName-java.lang.String}
```
public static int fromName(String chartTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| chartTypeName | java.lang.String |  |

**Returns:**
int
### getName(int chartType) {#getName-int}
```
public static String getName(int chartType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| chartType | int |  |

**Returns:**
java.lang.String
