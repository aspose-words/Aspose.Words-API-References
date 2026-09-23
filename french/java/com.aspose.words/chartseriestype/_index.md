---
title: "ChartSeriesType"
linktitle: "ChartSeriesType"
second_title: "Aspose.Words pour Java"
description: "Spécifie un type de série de graphique en Java."
type: docs
weight: 89
url: /fr/java/com.aspose.words/chartseriestype/
---

**Inheritance:**
java.lang.Object
```
public class ChartSeriesType
```

Spécifie un type de série de graphique.

 **Examples:** 

Montre comment supprimer une série de graphique spécifique.

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
## Champs

| Champ | Description |
| --- | --- |
| [AREA](#AREA) | Représente une série de graphique en aires. |
| [AREA_3_D](#AREA-3-D) | Représente une série de graphique en aires 3D. |
| [AREA_3_D_PERCENT_STACKED](#AREA-3-D-PERCENT-STACKED) | Représente une série de graphique en aires empilées à 100 % 3D. |
| [AREA_3_D_STACKED](#AREA-3-D-STACKED) | Représente une série de graphique en aires empilées 3D. |
| [AREA_PERCENT_STACKED](#AREA-PERCENT-STACKED) | Représente une série de graphique en aires empilées à 100 %. |
| [AREA_STACKED](#AREA-STACKED) | Représente une série de graphique en aires empilées. |
| [BAR](#BAR) | Représente une série de graphique à barres. |
| [BAR_3_D](#BAR-3-D) | Représente une série de graphique à barres 3D. |
| [BAR_3_D_PERCENT_STACKED](#BAR-3-D-PERCENT-STACKED) | Représente une série de graphique à barres empilées à 100 % 3D. |
| [BAR_3_D_STACKED](#BAR-3-D-STACKED) | Représente une série de graphique à barres empilées 3D. |
| [BAR_PERCENT_STACKED](#BAR-PERCENT-STACKED) | Représente une série de graphique à barres empilées à 100 %. |
| [BAR_STACKED](#BAR-STACKED) | Représente une série de graphique à barres empilées. |
| [BOX_AND_WHISKER](#BOX-AND-WHISKER) | Représente une série de graphique en boîte à moustaches. |
| [BUBBLE](#BUBBLE) | Représente une série de graphique à bulles. |
| [BUBBLE_3_D](#BUBBLE-3-D) | Représente une série de graphique à bulles 3D. |
| [COLUMN](#COLUMN) | Représente une série de graphique en colonnes. |
| [COLUMN_3_D](#COLUMN-3-D) | Représente une série de graphique à colonnes 3D. |
| [COLUMN_3_D_CLUSTERED](#COLUMN-3-D-CLUSTERED) | Représente une série de graphique à colonnes groupées 3D. |
| [COLUMN_3_D_PERCENT_STACKED](#COLUMN-3-D-PERCENT-STACKED) | Représente une série de graphique à colonnes empilées à 100 % 3D. |
| [COLUMN_3_D_STACKED](#COLUMN-3-D-STACKED) | Représente une série de graphique à colonnes empilées 3D. |
| [COLUMN_PERCENT_STACKED](#COLUMN-PERCENT-STACKED) | Représente une série de graphique à colonnes empilées à 100 %. |
| [COLUMN_STACKED](#COLUMN-STACKED) | Représente une série de graphique à colonnes empilées. |
| [DOUGHNUT](#DOUGHNUT) | Représente une série de graphique en anneau. |
| [FUNNEL](#FUNNEL) | Représente une série de graphique en entonnoir. |
| [HISTOGRAM](#HISTOGRAM) | Représente une série de graphique histogramme. |
| [LINE](#LINE) | Représente une série de graphique en courbes. |
| [LINE_3_D](#LINE-3-D) | Représente une série de graphique en courbes 3D. |
| [LINE_PERCENT_STACKED](#LINE-PERCENT-STACKED) | Représente une série de graphique en courbes empilées à 100 %. |
| [LINE_STACKED](#LINE-STACKED) | Représente une série de graphique en courbes empilées. |
| [PARETO](#PARETO) | Représente une série de graphique Pareto. |
| [PARETO_LINE](#PARETO-LINE) | Représente une série de graphique en courbes Pareto. |
| [PIE](#PIE) | Représente une série de graphique en secteurs. |
| [PIE_3_D](#PIE-3-D) | Représente une série de graphique en secteurs 3D. |
| [PIE_OF_BAR](#PIE-OF-BAR) | Représente une série de graphique en secteurs sur barres. |
| [PIE_OF_PIE](#PIE-OF-PIE) | Représente une série de graphique en secteurs imbriqués. |
| [RADAR](#RADAR) | Représente une série de graphique radar. |
| [REGION_MAP](#REGION-MAP) | Représente une série de graphique carte régionale. |
| [SCATTER](#SCATTER) | Représente une série de graphique en nuage de points. |
| [STOCK](#STOCK) | Représente une série de graphique boursier. |
| [SUNBURST](#SUNBURST) | Représente une série de graphique en rayons. |
| [SURFACE](#SURFACE) | Représente une série de graphique de surface. |
| [SURFACE_3_D](#SURFACE-3-D) | Représente une série de graphique de surface 3D. |
| [TREEMAP](#TREEMAP) | Représente une série de graphique en treemap. |
| [WATERFALL](#WATERFALL) | Représente une série de graphique en cascade. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String chartSeriesTypeName)](#fromName-java.lang.String) |  |
| [getName(int chartSeriesType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartSeriesType)](#toString-int) |  |
### AREA {#AREA}
```
public static int AREA
```


Représente une série de graphique en aires.

### AREA_3_D {#AREA-3-D}
```
public static int AREA_3_D
```


Représente une série de graphique en aires 3D.

### AREA_3_D_PERCENT_STACKED {#AREA-3-D-PERCENT-STACKED}
```
public static int AREA_3_D_PERCENT_STACKED
```


Représente une série de graphique en aires empilées à 100 % 3D.

### AREA_3_D_STACKED {#AREA-3-D-STACKED}
```
public static int AREA_3_D_STACKED
```


Représente une série de graphique en aires empilées 3D.

### AREA_PERCENT_STACKED {#AREA-PERCENT-STACKED}
```
public static int AREA_PERCENT_STACKED
```


Représente une série de graphique en aires empilées à 100 %.

### AREA_STACKED {#AREA-STACKED}
```
public static int AREA_STACKED
```


Représente une série de graphique en aires empilées.

### BAR {#BAR}
```
public static int BAR
```


Représente une série de graphique à barres.

### BAR_3_D {#BAR-3-D}
```
public static int BAR_3_D
```


Représente une série de graphique à barres 3D.

### BAR_3_D_PERCENT_STACKED {#BAR-3-D-PERCENT-STACKED}
```
public static int BAR_3_D_PERCENT_STACKED
```


Représente une série de graphique à barres empilées à 100 % 3D.

### BAR_3_D_STACKED {#BAR-3-D-STACKED}
```
public static int BAR_3_D_STACKED
```


Représente une série de graphique à barres empilées 3D.

### BAR_PERCENT_STACKED {#BAR-PERCENT-STACKED}
```
public static int BAR_PERCENT_STACKED
```


Représente une série de graphique à barres empilées à 100 %.

### BAR_STACKED {#BAR-STACKED}
```
public static int BAR_STACKED
```


Représente une série de graphique à barres empilées.

### BOX_AND_WHISKER {#BOX-AND-WHISKER}
```
public static int BOX_AND_WHISKER
```


Représente une série de graphique en boîte à moustaches.

### BUBBLE {#BUBBLE}
```
public static int BUBBLE
```


Représente une série de graphique à bulles.

### BUBBLE_3_D {#BUBBLE-3-D}
```
public static int BUBBLE_3_D
```


Représente une série de graphique à bulles 3D.

### COLUMN {#COLUMN}
```
public static int COLUMN
```


Représente une série de graphique en colonnes.

### COLUMN_3_D {#COLUMN-3-D}
```
public static int COLUMN_3_D
```


Représente une série de graphique à colonnes 3D.

### COLUMN_3_D_CLUSTERED {#COLUMN-3-D-CLUSTERED}
```
public static int COLUMN_3_D_CLUSTERED
```


Représente une série de graphique à colonnes groupées 3D.

### COLUMN_3_D_PERCENT_STACKED {#COLUMN-3-D-PERCENT-STACKED}
```
public static int COLUMN_3_D_PERCENT_STACKED
```


Représente une série de graphique à colonnes empilées à 100 % 3D.

### COLUMN_3_D_STACKED {#COLUMN-3-D-STACKED}
```
public static int COLUMN_3_D_STACKED
```


Représente une série de graphique à colonnes empilées 3D.

### COLUMN_PERCENT_STACKED {#COLUMN-PERCENT-STACKED}
```
public static int COLUMN_PERCENT_STACKED
```


Représente une série de graphique à colonnes empilées à 100 %.

### COLUMN_STACKED {#COLUMN-STACKED}
```
public static int COLUMN_STACKED
```


Représente une série de graphique à colonnes empilées.

### DOUGHNUT {#DOUGHNUT}
```
public static int DOUGHNUT
```


Représente une série de graphique en anneau.

### FUNNEL {#FUNNEL}
```
public static int FUNNEL
```


Représente une série de graphique en entonnoir.

### HISTOGRAM {#HISTOGRAM}
```
public static int HISTOGRAM
```


Représente une série de graphique histogramme.

### LINE {#LINE}
```
public static int LINE
```


Représente une série de graphique en courbes.

### LINE_3_D {#LINE-3-D}
```
public static int LINE_3_D
```


Représente une série de graphique en courbes 3D.

### LINE_PERCENT_STACKED {#LINE-PERCENT-STACKED}
```
public static int LINE_PERCENT_STACKED
```


Représente une série de graphique en courbes empilées à 100 %.

### LINE_STACKED {#LINE-STACKED}
```
public static int LINE_STACKED
```


Représente une série de graphique en courbes empilées.

### PARETO {#PARETO}
```
public static int PARETO
```


Représente une série de graphique Pareto.

### PARETO_LINE {#PARETO-LINE}
```
public static int PARETO_LINE
```


Représente une série de graphique en courbes Pareto.

### PIE {#PIE}
```
public static int PIE
```


Représente une série de graphique en secteurs.

### PIE_3_D {#PIE-3-D}
```
public static int PIE_3_D
```


Représente une série de graphique en secteurs 3D.

### PIE_OF_BAR {#PIE-OF-BAR}
```
public static int PIE_OF_BAR
```


Représente une série de graphique en secteurs sur barres.

### PIE_OF_PIE {#PIE-OF-PIE}
```
public static int PIE_OF_PIE
```


Représente une série de graphique en secteurs imbriqués.

### RADAR {#RADAR}
```
public static int RADAR
```


Représente une série de graphique radar.

### REGION_MAP {#REGION-MAP}
```
public static int REGION_MAP
```


Représente une série de graphique carte régionale.

### SCATTER {#SCATTER}
```
public static int SCATTER
```


Représente une série de graphique en nuage de points.

### STOCK {#STOCK}
```
public static int STOCK
```


Représente une série de graphique boursier.

### SUNBURST {#SUNBURST}
```
public static int SUNBURST
```


Représente une série de graphique en rayons.

### SURFACE {#SURFACE}
```
public static int SURFACE
```


Représente une série de graphique de surface.

### SURFACE_3_D {#SURFACE-3-D}
```
public static int SURFACE_3_D
```


Représente une série de graphique de surface 3D.

### TREEMAP {#TREEMAP}
```
public static int TREEMAP
```


Représente une série de graphique en treemap.

### WATERFALL {#WATERFALL}
```
public static int WATERFALL
```


Représente une série de graphique en cascade.

### length {#length}
```
public static int length
```


### fromName(String chartSeriesTypeName) {#fromName-java.lang.String}
```
public static int fromName(String chartSeriesTypeName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| chartSeriesTypeName | java.lang.String |  |

**Returns:**
int
### getName(int chartSeriesType) {#getName-int}
```
public static String getName(int chartSeriesType)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| chartSeriesType | int |  |

**Returns:**
java.lang.String
