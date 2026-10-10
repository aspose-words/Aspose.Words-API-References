---
title: "ChartType"
linktitle: "ChartType"
second_title: "Aspose.Words pour Java"
description: "Spécifie le type d'un graphique en Java."
type: docs
weight: 93
url: /fr/java/com.aspose.words/charttype/
---

**Inheritance:**
java.lang.Object
```
public class ChartType
```

Spécifie le type d'un graphique.

 **Examples:** 

Montre comment créer un type de série de graphique approprié pour un type de graphique.

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
## Champs

| Champ | Description |
| --- | --- |
| [AREA](#AREA) | Diagramme en aires. |
| [AREA_3_D](#AREA-3-D) | Diagramme en aires 3D. |
| [AREA_3_D_PERCENT_STACKED](#AREA-3-D-PERCENT-STACKED) | Diagramme en aires empilées à 100 % 3D. |
| [AREA_3_D_STACKED](#AREA-3-D-STACKED) | Diagramme en aires empilées 3D. |
| [AREA_PERCENT_STACKED](#AREA-PERCENT-STACKED) | Diagramme en aires empilées à 100 %. |
| [AREA_STACKED](#AREA-STACKED) | Diagramme en aires empilées. |
| [BAR](#BAR) | Diagramme à barres. |
| [BAR_3_D](#BAR-3-D) | Diagramme à barres 3D. |
| [BAR_3_D_PERCENT_STACKED](#BAR-3-D-PERCENT-STACKED) | Diagramme à barres empilées à 100 % 3D. |
| [BAR_3_D_STACKED](#BAR-3-D-STACKED) | Diagramme à barres empilées 3D. |
| [BAR_PERCENT_STACKED](#BAR-PERCENT-STACKED) | Diagramme à barres empilées à 100 %. |
| [BAR_STACKED](#BAR-STACKED) | Diagramme à barres empilées. |
| [BOX_AND_WHISKER](#BOX-AND-WHISKER) | Diagramme à boîte et moustaches. |
| [BUBBLE](#BUBBLE) | Diagramme à bulles. |
| [BUBBLE_3_D](#BUBBLE-3-D) | Diagramme à bulles 3D. |
| [COLUMN](#COLUMN) | Diagramme en colonnes. |
| [COLUMN_3_D](#COLUMN-3-D) | Diagramme en colonnes 3D. |
| [COLUMN_3_D_CLUSTERED](#COLUMN-3-D-CLUSTERED) | Diagramme en colonnes groupées 3D. |
| [COLUMN_3_D_PERCENT_STACKED](#COLUMN-3-D-PERCENT-STACKED) | Diagramme en colonnes empilées à 100 % 3D. |
| [COLUMN_3_D_STACKED](#COLUMN-3-D-STACKED) | Diagramme en colonnes empilées 3D. |
| [COLUMN_PERCENT_STACKED](#COLUMN-PERCENT-STACKED) | Diagramme en colonnes empilées à 100 %. |
| [COLUMN_STACKED](#COLUMN-STACKED) | Diagramme en colonnes empilées. |
| [DOUGHNUT](#DOUGHNUT) | Graphique en beignet. |
| [FUNNEL](#FUNNEL) | Graphique en entonnoir. |
| [HISTOGRAM](#HISTOGRAM) | Graphique histogramme. |
| [LINE](#LINE) | Graphique en lignes. |
| [LINE_3_D](#LINE-3-D) | Graphique en lignes 3D. |
| [LINE_PERCENT_STACKED](#LINE-PERCENT-STACKED) | Graphique en lignes empilées à 100 %. |
| [LINE_STACKED](#LINE-STACKED) | Graphique en lignes empilées. |
| [PARETO](#PARETO) | Graphique de Pareto. |
| [PIE](#PIE) | Graphique circulaire. |
| [PIE_3_D](#PIE-3-D) | Graphique circulaire 3D. |
| [PIE_OF_BAR](#PIE-OF-BAR) | Graphique en anneau de barres. |
| [PIE_OF_PIE](#PIE-OF-PIE) | Graphique en anneau de secteurs. |
| [RADAR](#RADAR) | Graphique radar. |
| [SCATTER](#SCATTER) | Graphique en nuage de points. |
| [STOCK](#STOCK) | Graphique boursier. |
| [SUNBURST](#SUNBURST) | Graphique en rayons. |
| [SURFACE](#SURFACE) | Graphique de surface. |
| [SURFACE_3_D](#SURFACE-3-D) | Graphique de surface 3D. |
| [TREEMAP](#TREEMAP) | Graphique en carte d'arbre. |
| [WATERFALL](#WATERFALL) | Graphique en cascade. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String chartTypeName)](#fromName-java.lang.String) |  |
| [getName(int chartType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartType)](#toString-int) |  |
### AREA {#AREA}
```
public static int AREA
```


Diagramme en aires.

### AREA_3_D {#AREA-3-D}
```
public static int AREA_3_D
```


Diagramme en aires 3D.

### AREA_3_D_PERCENT_STACKED {#AREA-3-D-PERCENT-STACKED}
```
public static int AREA_3_D_PERCENT_STACKED
```


Diagramme en aires empilées à 100 % 3D.

### AREA_3_D_STACKED {#AREA-3-D-STACKED}
```
public static int AREA_3_D_STACKED
```


Diagramme en aires empilées 3D.

### AREA_PERCENT_STACKED {#AREA-PERCENT-STACKED}
```
public static int AREA_PERCENT_STACKED
```


Diagramme en aires empilées à 100 %.

### AREA_STACKED {#AREA-STACKED}
```
public static int AREA_STACKED
```


Diagramme en aires empilées.

### BAR {#BAR}
```
public static int BAR
```


Diagramme à barres.

### BAR_3_D {#BAR-3-D}
```
public static int BAR_3_D
```


Diagramme à barres 3D.

### BAR_3_D_PERCENT_STACKED {#BAR-3-D-PERCENT-STACKED}
```
public static int BAR_3_D_PERCENT_STACKED
```


Diagramme à barres empilées à 100 % 3D.

### BAR_3_D_STACKED {#BAR-3-D-STACKED}
```
public static int BAR_3_D_STACKED
```


Diagramme à barres empilées 3D.

### BAR_PERCENT_STACKED {#BAR-PERCENT-STACKED}
```
public static int BAR_PERCENT_STACKED
```


Diagramme à barres empilées à 100 %.

### BAR_STACKED {#BAR-STACKED}
```
public static int BAR_STACKED
```


Diagramme à barres empilées.

### BOX_AND_WHISKER {#BOX-AND-WHISKER}
```
public static int BOX_AND_WHISKER
```


Diagramme à boîte et moustaches.

### BUBBLE {#BUBBLE}
```
public static int BUBBLE
```


Diagramme à bulles.

### BUBBLE_3_D {#BUBBLE-3-D}
```
public static int BUBBLE_3_D
```


Diagramme à bulles 3D.

### COLUMN {#COLUMN}
```
public static int COLUMN
```


Diagramme en colonnes.

### COLUMN_3_D {#COLUMN-3-D}
```
public static int COLUMN_3_D
```


Diagramme en colonnes 3D.

### COLUMN_3_D_CLUSTERED {#COLUMN-3-D-CLUSTERED}
```
public static int COLUMN_3_D_CLUSTERED
```


Diagramme en colonnes groupées 3D.

### COLUMN_3_D_PERCENT_STACKED {#COLUMN-3-D-PERCENT-STACKED}
```
public static int COLUMN_3_D_PERCENT_STACKED
```


Diagramme en colonnes empilées à 100 % 3D.

### COLUMN_3_D_STACKED {#COLUMN-3-D-STACKED}
```
public static int COLUMN_3_D_STACKED
```


Diagramme en colonnes empilées 3D.

### COLUMN_PERCENT_STACKED {#COLUMN-PERCENT-STACKED}
```
public static int COLUMN_PERCENT_STACKED
```


Diagramme en colonnes empilées à 100 %.

### COLUMN_STACKED {#COLUMN-STACKED}
```
public static int COLUMN_STACKED
```


Diagramme en colonnes empilées.

### DOUGHNUT {#DOUGHNUT}
```
public static int DOUGHNUT
```


Graphique en beignet.

### FUNNEL {#FUNNEL}
```
public static int FUNNEL
```


Graphique en entonnoir.

### HISTOGRAM {#HISTOGRAM}
```
public static int HISTOGRAM
```


Graphique histogramme.

### LINE {#LINE}
```
public static int LINE
```


Graphique en lignes.

### LINE_3_D {#LINE-3-D}
```
public static int LINE_3_D
```


Graphique en lignes 3D.

### LINE_PERCENT_STACKED {#LINE-PERCENT-STACKED}
```
public static int LINE_PERCENT_STACKED
```


Graphique en lignes empilées à 100 %.

### LINE_STACKED {#LINE-STACKED}
```
public static int LINE_STACKED
```


Graphique en lignes empilées.

### PARETO {#PARETO}
```
public static int PARETO
```


Graphique de Pareto.

### PIE {#PIE}
```
public static int PIE
```


Graphique circulaire.

### PIE_3_D {#PIE-3-D}
```
public static int PIE_3_D
```


Graphique circulaire 3D.

### PIE_OF_BAR {#PIE-OF-BAR}
```
public static int PIE_OF_BAR
```


Graphique en anneau de barres.

### PIE_OF_PIE {#PIE-OF-PIE}
```
public static int PIE_OF_PIE
```


Graphique en anneau de secteurs.

### RADAR {#RADAR}
```
public static int RADAR
```


Graphique radar.

### SCATTER {#SCATTER}
```
public static int SCATTER
```


Graphique en nuage de points.

### STOCK {#STOCK}
```
public static int STOCK
```


Graphique boursier.

### SUNBURST {#SUNBURST}
```
public static int SUNBURST
```


Graphique en rayons.

### SURFACE {#SURFACE}
```
public static int SURFACE
```


Graphique de surface.

### SURFACE_3_D {#SURFACE-3-D}
```
public static int SURFACE_3_D
```


Graphique de surface 3D.

### TREEMAP {#TREEMAP}
```
public static int TREEMAP
```


Graphique en carte d'arbre.

### WATERFALL {#WATERFALL}
```
public static int WATERFALL
```


Graphique en cascade.

### length {#length}
```
public static int length
```


### fromName(String chartTypeName) {#fromName-java.lang.String}
```
public static int fromName(String chartTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| chartTypeName | java.lang.String |  |

**Returns:**
int
### getName(int chartType) {#getName-int}
```
public static String getName(int chartType)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| chartType | int |  |

**Returns:**
java.lang.String
