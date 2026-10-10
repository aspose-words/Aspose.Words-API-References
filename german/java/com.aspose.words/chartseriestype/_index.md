---
title: "ChartSeriesType"
linktitle: "ChartSeriesType"
second_title: "Aspose.Words für Java"
description: "Gibt einen Typ einer Diagrammserie in Java an."
type: docs
weight: 89
url: /de/java/com.aspose.words/chartseriestype/
---

**Inheritance:**
java.lang.Object
```
public class ChartSeriesType
```

Gibt den Typ einer Diagrammserie an.

 **Examples:** 

Zeigt, wie man eine bestimmte Diagrammserie entfernt.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [AREA](#AREA) | Stellt eine Flächendiagrammserie dar. |
| [AREA_3_D](#AREA-3-D) | Stellt eine 3D‑Flächendiagrammserie dar. |
| [AREA_3_D_PERCENT_STACKED](#AREA-3-D-PERCENT-STACKED) | Stellt eine 3D‑100%-gestapelte Flächendiagrammserie dar. |
| [AREA_3_D_STACKED](#AREA-3-D-STACKED) | Stellt eine 3D‑gestapelte Flächendiagrammserie dar. |
| [AREA_PERCENT_STACKED](#AREA-PERCENT-STACKED) | Stellt eine 100%-gestapelte Flächendiagrammserie dar. |
| [AREA_STACKED](#AREA-STACKED) | Stellt eine gestapelte Flächendiagrammserie dar. |
| [BAR](#BAR) | Stellt eine Balkendiagrammserie dar. |
| [BAR_3_D](#BAR-3-D) | Stellt eine 3D‑Balkendiagrammserie dar. |
| [BAR_3_D_PERCENT_STACKED](#BAR-3-D-PERCENT-STACKED) | Stellt eine 3D 100%-gestapelte Balkendiagrammserie dar. |
| [BAR_3_D_STACKED](#BAR-3-D-STACKED) | Stellt eine 3D‑gestapelte Balkendiagrammserie dar. |
| [BAR_PERCENT_STACKED](#BAR-PERCENT-STACKED) | Stellt eine 100%-gestapelte Balkendiagrammserie dar. |
| [BAR_STACKED](#BAR-STACKED) | Stellt eine gestapelte Balkendiagrammserie dar. |
| [BOX_AND_WHISKER](#BOX-AND-WHISKER) | Stellt eine Box‑Whisker‑Diagrammserie dar. |
| [BUBBLE](#BUBBLE) | Stellt eine Blasendiagrammserie dar. |
| [BUBBLE_3_D](#BUBBLE-3-D) | Stellt eine 3D‑Blasendiagrammserie dar. |
| [COLUMN](#COLUMN) | Stellt eine Säulendiagrammserie dar. |
| [COLUMN_3_D](#COLUMN-3-D) | Stellt eine 3D‑Säulendiagrammserie dar. |
| [COLUMN_3_D_CLUSTERED](#COLUMN-3-D-CLUSTERED) | Stellt eine 3D‑gruppierte Säulendiagrammserie dar. |
| [COLUMN_3_D_PERCENT_STACKED](#COLUMN-3-D-PERCENT-STACKED) | Stellt eine 3D 100%-gestapelte Säulendiagrammserie dar. |
| [COLUMN_3_D_STACKED](#COLUMN-3-D-STACKED) | Stellt eine 3D‑gestapelte Säulendiagrammserie dar. |
| [COLUMN_PERCENT_STACKED](#COLUMN-PERCENT-STACKED) | Stellt eine 100%-gestapelte Säulendiagrammserie dar. |
| [COLUMN_STACKED](#COLUMN-STACKED) | Stellt eine gestapelte Säulendiagrammserie dar. |
| [DOUGHNUT](#DOUGHNUT) | Stellt eine Donut‑Diagrammserie dar. |
| [FUNNEL](#FUNNEL) | Stellt eine Trichterdiagrammserie dar. |
| [HISTOGRAM](#HISTOGRAM) | Stellt eine Histogrammserie dar. |
| [LINE](#LINE) | Stellt eine Liniendiagrammserie dar. |
| [LINE_3_D](#LINE-3-D) | Stellt eine 3D‑Liniendiagrammserie dar. |
| [LINE_PERCENT_STACKED](#LINE-PERCENT-STACKED) | Stellt eine 100%-gestapelte Liniendiagrammserie dar. |
| [LINE_STACKED](#LINE-STACKED) | Stellt eine gestapelte Liniendiagrammserie dar. |
| [PARETO](#PARETO) | Stellt eine Pareto‑Diagrammserie dar. |
| [PARETO_LINE](#PARETO-LINE) | Stellt eine Pareto-Linien-Diagrammserie dar. |
| [PIE](#PIE) | Stellt eine Kreisdiagrammserie dar. |
| [PIE_3_D](#PIE-3-D) | Stellt eine 3D-Kreisdiagrammserie dar. |
| [PIE_OF_BAR](#PIE-OF-BAR) | Stellt eine Kreis‑aus‑Balken-Diagrammserie dar. |
| [PIE_OF_PIE](#PIE-OF-PIE) | Stellt eine Kreis‑aus‑Kreis-Diagrammserie dar. |
| [RADAR](#RADAR) | Stellt eine Radar-Diagrammserie dar. |
| [REGION_MAP](#REGION-MAP) | Stellt eine Regionen‑Karten-Diagrammserie dar. |
| [SCATTER](#SCATTER) | Stellt eine Streudiagrammserie dar. |
| [STOCK](#STOCK) | Stellt eine Aktien‑Diagrammserie dar. |
| [SUNBURST](#SUNBURST) | Stellt eine Sunburst-Diagrammserie dar. |
| [SURFACE](#SURFACE) | Stellt eine Oberflächen‑Diagrammserie dar. |
| [SURFACE_3_D](#SURFACE-3-D) | Stellt eine 3D-Oberflächen‑Diagrammserie dar. |
| [TREEMAP](#TREEMAP) | Stellt eine Treemap-Diagrammserie dar. |
| [WATERFALL](#WATERFALL) | Stellt eine Wasserfall‑Diagrammserie dar. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String chartSeriesTypeName)](#fromName-java.lang.String) |  |
| [getName(int chartSeriesType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartSeriesType)](#toString-int) |  |
### AREA {#AREA}
```
public static int AREA
```


Stellt eine Flächendiagrammserie dar.

### AREA_3_D {#AREA-3-D}
```
public static int AREA_3_D
```


Stellt eine 3D‑Flächendiagrammserie dar.

### AREA_3_D_PERCENT_STACKED {#AREA-3-D-PERCENT-STACKED}
```
public static int AREA_3_D_PERCENT_STACKED
```


Stellt eine 3D‑100%-gestapelte Flächendiagrammserie dar.

### AREA_3_D_STACKED {#AREA-3-D-STACKED}
```
public static int AREA_3_D_STACKED
```


Stellt eine 3D‑gestapelte Flächendiagrammserie dar.

### AREA_PERCENT_STACKED {#AREA-PERCENT-STACKED}
```
public static int AREA_PERCENT_STACKED
```


Stellt eine 100%-gestapelte Flächendiagrammserie dar.

### AREA_STACKED {#AREA-STACKED}
```
public static int AREA_STACKED
```


Stellt eine gestapelte Flächendiagrammserie dar.

### BAR {#BAR}
```
public static int BAR
```


Stellt eine Balkendiagrammserie dar.

### BAR_3_D {#BAR-3-D}
```
public static int BAR_3_D
```


Stellt eine 3D‑Balkendiagrammserie dar.

### BAR_3_D_PERCENT_STACKED {#BAR-3-D-PERCENT-STACKED}
```
public static int BAR_3_D_PERCENT_STACKED
```


Stellt eine 3D 100%-gestapelte Balkendiagrammserie dar.

### BAR_3_D_STACKED {#BAR-3-D-STACKED}
```
public static int BAR_3_D_STACKED
```


Stellt eine 3D‑gestapelte Balkendiagrammserie dar.

### BAR_PERCENT_STACKED {#BAR-PERCENT-STACKED}
```
public static int BAR_PERCENT_STACKED
```


Stellt eine 100%-gestapelte Balkendiagrammserie dar.

### BAR_STACKED {#BAR-STACKED}
```
public static int BAR_STACKED
```


Stellt eine gestapelte Balkendiagrammserie dar.

### BOX_AND_WHISKER {#BOX-AND-WHISKER}
```
public static int BOX_AND_WHISKER
```


Stellt eine Box‑Whisker‑Diagrammserie dar.

### BUBBLE {#BUBBLE}
```
public static int BUBBLE
```


Stellt eine Blasendiagrammserie dar.

### BUBBLE_3_D {#BUBBLE-3-D}
```
public static int BUBBLE_3_D
```


Stellt eine 3D‑Blasendiagrammserie dar.

### COLUMN {#COLUMN}
```
public static int COLUMN
```


Stellt eine Säulendiagrammserie dar.

### COLUMN_3_D {#COLUMN-3-D}
```
public static int COLUMN_3_D
```


Stellt eine 3D‑Säulendiagrammserie dar.

### COLUMN_3_D_CLUSTERED {#COLUMN-3-D-CLUSTERED}
```
public static int COLUMN_3_D_CLUSTERED
```


Stellt eine 3D‑gruppierte Säulendiagrammserie dar.

### COLUMN_3_D_PERCENT_STACKED {#COLUMN-3-D-PERCENT-STACKED}
```
public static int COLUMN_3_D_PERCENT_STACKED
```


Stellt eine 3D 100%-gestapelte Säulendiagrammserie dar.

### COLUMN_3_D_STACKED {#COLUMN-3-D-STACKED}
```
public static int COLUMN_3_D_STACKED
```


Stellt eine 3D‑gestapelte Säulendiagrammserie dar.

### COLUMN_PERCENT_STACKED {#COLUMN-PERCENT-STACKED}
```
public static int COLUMN_PERCENT_STACKED
```


Stellt eine 100%-gestapelte Säulendiagrammserie dar.

### COLUMN_STACKED {#COLUMN-STACKED}
```
public static int COLUMN_STACKED
```


Stellt eine gestapelte Säulendiagrammserie dar.

### DOUGHNUT {#DOUGHNUT}
```
public static int DOUGHNUT
```


Stellt eine Donut‑Diagrammserie dar.

### FUNNEL {#FUNNEL}
```
public static int FUNNEL
```


Stellt eine Trichterdiagrammserie dar.

### HISTOGRAM {#HISTOGRAM}
```
public static int HISTOGRAM
```


Stellt eine Histogrammserie dar.

### LINE {#LINE}
```
public static int LINE
```


Stellt eine Liniendiagrammserie dar.

### LINE_3_D {#LINE-3-D}
```
public static int LINE_3_D
```


Stellt eine 3D‑Liniendiagrammserie dar.

### LINE_PERCENT_STACKED {#LINE-PERCENT-STACKED}
```
public static int LINE_PERCENT_STACKED
```


Stellt eine 100%-gestapelte Liniendiagrammserie dar.

### LINE_STACKED {#LINE-STACKED}
```
public static int LINE_STACKED
```


Stellt eine gestapelte Liniendiagrammserie dar.

### PARETO {#PARETO}
```
public static int PARETO
```


Stellt eine Pareto‑Diagrammserie dar.

### PARETO_LINE {#PARETO-LINE}
```
public static int PARETO_LINE
```


Stellt eine Pareto-Linien-Diagrammserie dar.

### PIE {#PIE}
```
public static int PIE
```


Stellt eine Kreisdiagrammserie dar.

### PIE_3_D {#PIE-3-D}
```
public static int PIE_3_D
```


Stellt eine 3D-Kreisdiagrammserie dar.

### PIE_OF_BAR {#PIE-OF-BAR}
```
public static int PIE_OF_BAR
```


Stellt eine Kreis‑aus‑Balken-Diagrammserie dar.

### PIE_OF_PIE {#PIE-OF-PIE}
```
public static int PIE_OF_PIE
```


Stellt eine Kreis‑aus‑Kreis-Diagrammserie dar.

### RADAR {#RADAR}
```
public static int RADAR
```


Stellt eine Radar-Diagrammserie dar.

### REGION_MAP {#REGION-MAP}
```
public static int REGION_MAP
```


Stellt eine Regionen‑Karten-Diagrammserie dar.

### SCATTER {#SCATTER}
```
public static int SCATTER
```


Stellt eine Streudiagrammserie dar.

### STOCK {#STOCK}
```
public static int STOCK
```


Stellt eine Aktien‑Diagrammserie dar.

### SUNBURST {#SUNBURST}
```
public static int SUNBURST
```


Stellt eine Sunburst-Diagrammserie dar.

### SURFACE {#SURFACE}
```
public static int SURFACE
```


Stellt eine Oberflächen‑Diagrammserie dar.

### SURFACE_3_D {#SURFACE-3-D}
```
public static int SURFACE_3_D
```


Stellt eine 3D-Oberflächen‑Diagrammserie dar.

### TREEMAP {#TREEMAP}
```
public static int TREEMAP
```


Stellt eine Treemap-Diagrammserie dar.

### WATERFALL {#WATERFALL}
```
public static int WATERFALL
```


Stellt eine Wasserfall‑Diagrammserie dar.

### length {#length}
```
public static int length
```


### fromName(String chartSeriesTypeName) {#fromName-java.lang.String}
```
public static int fromName(String chartSeriesTypeName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| chartSeriesTypeName | java.lang.String |  |

**Returns:**
int
### getName(int chartSeriesType) {#getName-int}
```
public static String getName(int chartSeriesType)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| chartSeriesType | int |  |

**Returns:**
java.lang.String
