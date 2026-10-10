---
title: "ChartType"
linktitle: "ChartType"
second_title: "Aspose.Words per Java"
description: "Specifica il tipo di un grafico in Java."
type: docs
weight: 93
url: /it/java/com.aspose.words/charttype/
---

**Inheritance:**
java.lang.Object
```
public class ChartType
```

Specifica il tipo di un grafico.

 **Examples:** 

Mostra come creare un tipo appropriato di serie di grafico per un tipo di grafico.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [AREA](#AREA) | Grafico ad area. |
| [AREA_3_D](#AREA-3-D) | Grafico ad area 3D. |
| [AREA_3_D_PERCENT_STACKED](#AREA-3-D-PERCENT-STACKED) | Grafico ad area impilato al 100% 3D. |
| [AREA_3_D_STACKED](#AREA-3-D-STACKED) | Grafico ad area impilato 3D. |
| [AREA_PERCENT_STACKED](#AREA-PERCENT-STACKED) | Grafico ad area impilato al 100%. |
| [AREA_STACKED](#AREA-STACKED) | Grafico ad area impilato. |
| [BAR](#BAR) | Grafico a barre. |
| [BAR_3_D](#BAR-3-D) | Grafico a barre 3D. |
| [BAR_3_D_PERCENT_STACKED](#BAR-3-D-PERCENT-STACKED) | Grafico a barre impilato al 100% 3D. |
| [BAR_3_D_STACKED](#BAR-3-D-STACKED) | Grafico a barre impilato 3D. |
| [BAR_PERCENT_STACKED](#BAR-PERCENT-STACKED) | Grafico a barre impilato al 100%. |
| [BAR_STACKED](#BAR-STACKED) | Grafico a barre impilato. |
| [BOX_AND_WHISKER](#BOX-AND-WHISKER) | Grafico a scatola e baffi. |
| [BUBBLE](#BUBBLE) | Grafico a bolle. |
| [BUBBLE_3_D](#BUBBLE-3-D) | Grafico a bolle 3D. |
| [COLUMN](#COLUMN) | Grafico a colonne. |
| [COLUMN_3_D](#COLUMN-3-D) | Grafico a colonne 3D. |
| [COLUMN_3_D_CLUSTERED](#COLUMN-3-D-CLUSTERED) | Grafico a colonne raggruppate 3D. |
| [COLUMN_3_D_PERCENT_STACKED](#COLUMN-3-D-PERCENT-STACKED) | Grafico a colonne impilato al 100% 3D. |
| [COLUMN_3_D_STACKED](#COLUMN-3-D-STACKED) | Grafico a colonne impilato 3D. |
| [COLUMN_PERCENT_STACKED](#COLUMN-PERCENT-STACKED) | Grafico a colonne impilato al 100%. |
| [COLUMN_STACKED](#COLUMN-STACKED) | Grafico a colonne impilato. |
| [DOUGHNUT](#DOUGHNUT) | Grafico a ciambella. |
| [FUNNEL](#FUNNEL) | Grafico a imbuto. |
| [HISTOGRAM](#HISTOGRAM) | Grafico a istogramma. |
| [LINE](#LINE) | Grafico a linee. |
| [LINE_3_D](#LINE-3-D) | Grafico a linee 3D. |
| [LINE_PERCENT_STACKED](#LINE-PERCENT-STACKED) | Grafico a linee impilate al 100%. |
| [LINE_STACKED](#LINE-STACKED) | Grafico a linee impilate. |
| [PARETO](#PARETO) | Grafico Pareto. |
| [PIE](#PIE) | Grafico a torta. |
| [PIE_3_D](#PIE-3-D) | Grafico a torta 3D. |
| [PIE_OF_BAR](#PIE-OF-BAR) | Grafico a torta di barre. |
| [PIE_OF_PIE](#PIE-OF-PIE) | Grafico a torta di torta. |
| [RADAR](#RADAR) | Grafico radar. |
| [SCATTER](#SCATTER) | Grafico a dispersione. |
| [STOCK](#STOCK) | Grafico azionario. |
| [SUNBURST](#SUNBURST) | Grafico a raggi. |
| [SURFACE](#SURFACE) | Grafico di superficie. |
| [SURFACE_3_D](#SURFACE-3-D) | Grafico di superficie 3D. |
| [TREEMAP](#TREEMAP) | Grafico a mappa ad albero. |
| [WATERFALL](#WATERFALL) | Grafico a cascata. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String chartTypeName)](#fromName-java.lang.String) |  |
| [getName(int chartType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartType)](#toString-int) |  |
### AREA {#AREA}
```
public static int AREA
```


Grafico ad area.

### AREA_3_D {#AREA-3-D}
```
public static int AREA_3_D
```


Grafico ad area 3D.

### AREA_3_D_PERCENT_STACKED {#AREA-3-D-PERCENT-STACKED}
```
public static int AREA_3_D_PERCENT_STACKED
```


Grafico ad area impilato al 100% 3D.

### AREA_3_D_STACKED {#AREA-3-D-STACKED}
```
public static int AREA_3_D_STACKED
```


Grafico ad area impilato 3D.

### AREA_PERCENT_STACKED {#AREA-PERCENT-STACKED}
```
public static int AREA_PERCENT_STACKED
```


Grafico ad area impilato al 100%.

### AREA_STACKED {#AREA-STACKED}
```
public static int AREA_STACKED
```


Grafico ad area impilato.

### BAR {#BAR}
```
public static int BAR
```


Grafico a barre.

### BAR_3_D {#BAR-3-D}
```
public static int BAR_3_D
```


Grafico a barre 3D.

### BAR_3_D_PERCENT_STACKED {#BAR-3-D-PERCENT-STACKED}
```
public static int BAR_3_D_PERCENT_STACKED
```


Grafico a barre impilato al 100% 3D.

### BAR_3_D_STACKED {#BAR-3-D-STACKED}
```
public static int BAR_3_D_STACKED
```


Grafico a barre impilato 3D.

### BAR_PERCENT_STACKED {#BAR-PERCENT-STACKED}
```
public static int BAR_PERCENT_STACKED
```


Grafico a barre impilato al 100%.

### BAR_STACKED {#BAR-STACKED}
```
public static int BAR_STACKED
```


Grafico a barre impilato.

### BOX_AND_WHISKER {#BOX-AND-WHISKER}
```
public static int BOX_AND_WHISKER
```


Grafico a scatola e baffi.

### BUBBLE {#BUBBLE}
```
public static int BUBBLE
```


Grafico a bolle.

### BUBBLE_3_D {#BUBBLE-3-D}
```
public static int BUBBLE_3_D
```


Grafico a bolle 3D.

### COLUMN {#COLUMN}
```
public static int COLUMN
```


Grafico a colonne.

### COLUMN_3_D {#COLUMN-3-D}
```
public static int COLUMN_3_D
```


Grafico a colonne 3D.

### COLUMN_3_D_CLUSTERED {#COLUMN-3-D-CLUSTERED}
```
public static int COLUMN_3_D_CLUSTERED
```


Grafico a colonne raggruppate 3D.

### COLUMN_3_D_PERCENT_STACKED {#COLUMN-3-D-PERCENT-STACKED}
```
public static int COLUMN_3_D_PERCENT_STACKED
```


Grafico a colonne impilato al 100% 3D.

### COLUMN_3_D_STACKED {#COLUMN-3-D-STACKED}
```
public static int COLUMN_3_D_STACKED
```


Grafico a colonne impilato 3D.

### COLUMN_PERCENT_STACKED {#COLUMN-PERCENT-STACKED}
```
public static int COLUMN_PERCENT_STACKED
```


Grafico a colonne impilato al 100%.

### COLUMN_STACKED {#COLUMN-STACKED}
```
public static int COLUMN_STACKED
```


Grafico a colonne impilato.

### DOUGHNUT {#DOUGHNUT}
```
public static int DOUGHNUT
```


Grafico a ciambella.

### FUNNEL {#FUNNEL}
```
public static int FUNNEL
```


Grafico a imbuto.

### HISTOGRAM {#HISTOGRAM}
```
public static int HISTOGRAM
```


Grafico a istogramma.

### LINE {#LINE}
```
public static int LINE
```


Grafico a linee.

### LINE_3_D {#LINE-3-D}
```
public static int LINE_3_D
```


Grafico a linee 3D.

### LINE_PERCENT_STACKED {#LINE-PERCENT-STACKED}
```
public static int LINE_PERCENT_STACKED
```


Grafico a linee impilate al 100%.

### LINE_STACKED {#LINE-STACKED}
```
public static int LINE_STACKED
```


Grafico a linee impilate.

### PARETO {#PARETO}
```
public static int PARETO
```


Grafico Pareto.

### PIE {#PIE}
```
public static int PIE
```


Grafico a torta.

### PIE_3_D {#PIE-3-D}
```
public static int PIE_3_D
```


Grafico a torta 3D.

### PIE_OF_BAR {#PIE-OF-BAR}
```
public static int PIE_OF_BAR
```


Grafico a torta di barre.

### PIE_OF_PIE {#PIE-OF-PIE}
```
public static int PIE_OF_PIE
```


Grafico a torta di torta.

### RADAR {#RADAR}
```
public static int RADAR
```


Grafico radar.

### SCATTER {#SCATTER}
```
public static int SCATTER
```


Grafico a dispersione.

### STOCK {#STOCK}
```
public static int STOCK
```


Grafico azionario.

### SUNBURST {#SUNBURST}
```
public static int SUNBURST
```


Grafico a raggi.

### SURFACE {#SURFACE}
```
public static int SURFACE
```


Grafico di superficie.

### SURFACE_3_D {#SURFACE-3-D}
```
public static int SURFACE_3_D
```


Grafico di superficie 3D.

### TREEMAP {#TREEMAP}
```
public static int TREEMAP
```


Grafico a mappa ad albero.

### WATERFALL {#WATERFALL}
```
public static int WATERFALL
```


Grafico a cascata.

### length {#length}
```
public static int length
```


### fromName(String chartTypeName) {#fromName-java.lang.String}
```
public static int fromName(String chartTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| chartTypeName | java.lang.String |  |

**Returns:**
int
### getName(int chartType) {#getName-int}
```
public static String getName(int chartType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| chartType | int |  |

**Returns:**
java.lang.String
