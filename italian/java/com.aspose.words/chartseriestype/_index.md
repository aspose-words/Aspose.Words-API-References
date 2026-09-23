---
title: "ChartSeriesType"
linktitle: "ChartSeriesType"
second_title: "Aspose.Words per Java"
description: "Specifica un tipo di serie di grafico in Java."
type: docs
weight: 89
url: /it/java/com.aspose.words/chartseriestype/
---

**Inheritance:**
java.lang.Object
```
public class ChartSeriesType
```

Specifica un tipo di serie del grafico.

 **Examples:** 

Mostra come rimuovere una serie di grafico specifica.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [AREA](#AREA) | Rappresenta una serie di grafico ad area. |
| [AREA_3_D](#AREA-3-D) | Rappresenta una serie di grafico ad area 3D. |
| [AREA_3_D_PERCENT_STACKED](#AREA-3-D-PERCENT-STACKED) | Rappresenta una serie di grafico ad area impilata al 100% 3D. |
| [AREA_3_D_STACKED](#AREA-3-D-STACKED) | Rappresenta una serie di grafico ad area impilata 3D. |
| [AREA_PERCENT_STACKED](#AREA-PERCENT-STACKED) | Rappresenta una serie di grafico ad area impilata al 100%. |
| [AREA_STACKED](#AREA-STACKED) | Rappresenta una serie di grafico ad area impilata. |
| [BAR](#BAR) | Rappresenta una serie di grafico a barre. |
| [BAR_3_D](#BAR-3-D) | Rappresenta una serie di grafico a barre 3D. |
| [BAR_3_D_PERCENT_STACKED](#BAR-3-D-PERCENT-STACKED) | Rappresenta una serie di grafico a barre impilata al 100% 3D. |
| [BAR_3_D_STACKED](#BAR-3-D-STACKED) | Rappresenta una serie di grafico a barre impilata 3D. |
| [BAR_PERCENT_STACKED](#BAR-PERCENT-STACKED) | Rappresenta una serie di grafico a barre impilata al 100%. |
| [BAR_STACKED](#BAR-STACKED) | Rappresenta una serie di grafico a barre impilata. |
| [BOX_AND_WHISKER](#BOX-AND-WHISKER) | Rappresenta una serie di grafico a scatola e baffi. |
| [BUBBLE](#BUBBLE) | Rappresenta una serie di grafico a bolle. |
| [BUBBLE_3_D](#BUBBLE-3-D) | Rappresenta una serie di grafico a bolle 3D. |
| [COLUMN](#COLUMN) | Rappresenta una serie di grafico a colonne. |
| [COLUMN_3_D](#COLUMN-3-D) | Rappresenta una serie di grafico a colonne 3D. |
| [COLUMN_3_D_CLUSTERED](#COLUMN-3-D-CLUSTERED) | Rappresenta una serie di grafico a colonne raggruppate 3D. |
| [COLUMN_3_D_PERCENT_STACKED](#COLUMN-3-D-PERCENT-STACKED) | Rappresenta una serie di grafico a colonne impilate al 100% 3D. |
| [COLUMN_3_D_STACKED](#COLUMN-3-D-STACKED) | Rappresenta una serie di grafico a colonne impilate 3D. |
| [COLUMN_PERCENT_STACKED](#COLUMN-PERCENT-STACKED) | Rappresenta una serie di grafico a colonne impilate al 100%. |
| [COLUMN_STACKED](#COLUMN-STACKED) | Rappresenta una serie di grafico a colonne impilate. |
| [DOUGHNUT](#DOUGHNUT) | Rappresenta una serie di grafico a ciambella. |
| [FUNNEL](#FUNNEL) | Rappresenta una serie di grafico a imbuto. |
| [HISTOGRAM](#HISTOGRAM) | Rappresenta una serie di grafico a istogramma. |
| [LINE](#LINE) | Rappresenta una serie di grafico a linee. |
| [LINE_3_D](#LINE-3-D) | Rappresenta una serie di grafico a linee 3D. |
| [LINE_PERCENT_STACKED](#LINE-PERCENT-STACKED) | Rappresenta una serie di grafico a linee impilate al 100%. |
| [LINE_STACKED](#LINE-STACKED) | Rappresenta una serie di grafico a linee impilate. |
| [PARETO](#PARETO) | Rappresenta una serie di grafico Pareto. |
| [PARETO_LINE](#PARETO-LINE) | Rappresenta una serie di grafico a linee Pareto. |
| [PIE](#PIE) | Rappresenta una serie di grafico a torta. |
| [PIE_3_D](#PIE-3-D) | Rappresenta una serie di grafico a torta 3D. |
| [PIE_OF_BAR](#PIE-OF-BAR) | Rappresenta una serie di grafico a torta di barre. |
| [PIE_OF_PIE](#PIE-OF-PIE) | Rappresenta una serie di grafico a torta di torta. |
| [RADAR](#RADAR) | Rappresenta una serie di grafico radar. |
| [REGION_MAP](#REGION-MAP) | Rappresenta una serie di grafico mappa regionale. |
| [SCATTER](#SCATTER) | Rappresenta una serie di grafico a dispersione. |
| [STOCK](#STOCK) | Rappresenta una serie di grafico azionario. |
| [SUNBURST](#SUNBURST) | Rappresenta una serie di grafico a raggi. |
| [SURFACE](#SURFACE) | Rappresenta una serie di grafico di superficie. |
| [SURFACE_3_D](#SURFACE-3-D) | Rappresenta una serie di grafico 3D Surface. |
| [TREEMAP](#TREEMAP) | Rappresenta una serie di grafico Treemap. |
| [WATERFALL](#WATERFALL) | Rappresenta una serie di grafico Waterfall. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String chartSeriesTypeName)](#fromName-java.lang.String) |  |
| [getName(int chartSeriesType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartSeriesType)](#toString-int) |  |
### AREA {#AREA}
```
public static int AREA
```


Rappresenta una serie di grafico ad area.

### AREA_3_D {#AREA-3-D}
```
public static int AREA_3_D
```


Rappresenta una serie di grafico ad area 3D.

### AREA_3_D_PERCENT_STACKED {#AREA-3-D-PERCENT-STACKED}
```
public static int AREA_3_D_PERCENT_STACKED
```


Rappresenta una serie di grafico ad area impilata al 100% 3D.

### AREA_3_D_STACKED {#AREA-3-D-STACKED}
```
public static int AREA_3_D_STACKED
```


Rappresenta una serie di grafico ad area impilata 3D.

### AREA_PERCENT_STACKED {#AREA-PERCENT-STACKED}
```
public static int AREA_PERCENT_STACKED
```


Rappresenta una serie di grafico ad area impilata al 100%.

### AREA_STACKED {#AREA-STACKED}
```
public static int AREA_STACKED
```


Rappresenta una serie di grafico ad area impilata.

### BAR {#BAR}
```
public static int BAR
```


Rappresenta una serie di grafico a barre.

### BAR_3_D {#BAR-3-D}
```
public static int BAR_3_D
```


Rappresenta una serie di grafico a barre 3D.

### BAR_3_D_PERCENT_STACKED {#BAR-3-D-PERCENT-STACKED}
```
public static int BAR_3_D_PERCENT_STACKED
```


Rappresenta una serie di grafico a barre impilata al 100% 3D.

### BAR_3_D_STACKED {#BAR-3-D-STACKED}
```
public static int BAR_3_D_STACKED
```


Rappresenta una serie di grafico a barre impilata 3D.

### BAR_PERCENT_STACKED {#BAR-PERCENT-STACKED}
```
public static int BAR_PERCENT_STACKED
```


Rappresenta una serie di grafico a barre impilata al 100%.

### BAR_STACKED {#BAR-STACKED}
```
public static int BAR_STACKED
```


Rappresenta una serie di grafico a barre impilata.

### BOX_AND_WHISKER {#BOX-AND-WHISKER}
```
public static int BOX_AND_WHISKER
```


Rappresenta una serie di grafico a scatola e baffi.

### BUBBLE {#BUBBLE}
```
public static int BUBBLE
```


Rappresenta una serie di grafico a bolle.

### BUBBLE_3_D {#BUBBLE-3-D}
```
public static int BUBBLE_3_D
```


Rappresenta una serie di grafico a bolle 3D.

### COLUMN {#COLUMN}
```
public static int COLUMN
```


Rappresenta una serie di grafico a colonne.

### COLUMN_3_D {#COLUMN-3-D}
```
public static int COLUMN_3_D
```


Rappresenta una serie di grafico a colonne 3D.

### COLUMN_3_D_CLUSTERED {#COLUMN-3-D-CLUSTERED}
```
public static int COLUMN_3_D_CLUSTERED
```


Rappresenta una serie di grafico a colonne raggruppate 3D.

### COLUMN_3_D_PERCENT_STACKED {#COLUMN-3-D-PERCENT-STACKED}
```
public static int COLUMN_3_D_PERCENT_STACKED
```


Rappresenta una serie di grafico a colonne impilate al 100% 3D.

### COLUMN_3_D_STACKED {#COLUMN-3-D-STACKED}
```
public static int COLUMN_3_D_STACKED
```


Rappresenta una serie di grafico a colonne impilate 3D.

### COLUMN_PERCENT_STACKED {#COLUMN-PERCENT-STACKED}
```
public static int COLUMN_PERCENT_STACKED
```


Rappresenta una serie di grafico a colonne impilate al 100%.

### COLUMN_STACKED {#COLUMN-STACKED}
```
public static int COLUMN_STACKED
```


Rappresenta una serie di grafico a colonne impilate.

### DOUGHNUT {#DOUGHNUT}
```
public static int DOUGHNUT
```


Rappresenta una serie di grafico a ciambella.

### FUNNEL {#FUNNEL}
```
public static int FUNNEL
```


Rappresenta una serie di grafico a imbuto.

### HISTOGRAM {#HISTOGRAM}
```
public static int HISTOGRAM
```


Rappresenta una serie di grafico a istogramma.

### LINE {#LINE}
```
public static int LINE
```


Rappresenta una serie di grafico a linee.

### LINE_3_D {#LINE-3-D}
```
public static int LINE_3_D
```


Rappresenta una serie di grafico a linee 3D.

### LINE_PERCENT_STACKED {#LINE-PERCENT-STACKED}
```
public static int LINE_PERCENT_STACKED
```


Rappresenta una serie di grafico a linee impilate al 100%.

### LINE_STACKED {#LINE-STACKED}
```
public static int LINE_STACKED
```


Rappresenta una serie di grafico a linee impilate.

### PARETO {#PARETO}
```
public static int PARETO
```


Rappresenta una serie di grafico Pareto.

### PARETO_LINE {#PARETO-LINE}
```
public static int PARETO_LINE
```


Rappresenta una serie di grafico a linee Pareto.

### PIE {#PIE}
```
public static int PIE
```


Rappresenta una serie di grafico a torta.

### PIE_3_D {#PIE-3-D}
```
public static int PIE_3_D
```


Rappresenta una serie di grafico a torta 3D.

### PIE_OF_BAR {#PIE-OF-BAR}
```
public static int PIE_OF_BAR
```


Rappresenta una serie di grafico a torta di barre.

### PIE_OF_PIE {#PIE-OF-PIE}
```
public static int PIE_OF_PIE
```


Rappresenta una serie di grafico a torta di torta.

### RADAR {#RADAR}
```
public static int RADAR
```


Rappresenta una serie di grafico radar.

### REGION_MAP {#REGION-MAP}
```
public static int REGION_MAP
```


Rappresenta una serie di grafico mappa regionale.

### SCATTER {#SCATTER}
```
public static int SCATTER
```


Rappresenta una serie di grafico a dispersione.

### STOCK {#STOCK}
```
public static int STOCK
```


Rappresenta una serie di grafico azionario.

### SUNBURST {#SUNBURST}
```
public static int SUNBURST
```


Rappresenta una serie di grafico a raggi.

### SURFACE {#SURFACE}
```
public static int SURFACE
```


Rappresenta una serie di grafico di superficie.

### SURFACE_3_D {#SURFACE-3-D}
```
public static int SURFACE_3_D
```


Rappresenta una serie di grafico 3D Surface.

### TREEMAP {#TREEMAP}
```
public static int TREEMAP
```


Rappresenta una serie di grafico Treemap.

### WATERFALL {#WATERFALL}
```
public static int WATERFALL
```


Rappresenta una serie di grafico Waterfall.

### length {#length}
```
public static int length
```


### fromName(String chartSeriesTypeName) {#fromName-java.lang.String}
```
public static int fromName(String chartSeriesTypeName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| chartSeriesTypeName | java.lang.String |  |

**Returns:**
int
### getName(int chartSeriesType) {#getName-int}
```
public static String getName(int chartSeriesType)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| chartSeriesType | int |  |

**Returns:**
java.lang.String
