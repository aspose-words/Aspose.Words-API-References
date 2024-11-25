---
title: ChartSeriesType
linktitle: ChartSeriesType
second_title: Aspose.Words for Java
description: Specifies a type of a chart series in Java.
type: docs
weight: 86
url: /java/com.aspose.words/chartseriestype/
---

**Inheritance:**
java.lang.Object
```
public class ChartSeriesType
```

Specifies a type of a chart series.

 **Examples:** 

Shows how to remove specific chart serie.

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
## Fields

| Field | Description |
| --- | --- |
| [AREA](#AREA) | Represents an Area chart series. |
| [AREA_3_D](#AREA-3-D) | Represents a 3D Area chart series. |
| [AREA_3_D_PERCENT_STACKED](#AREA-3-D-PERCENT-STACKED) | Represents a 3D 100% Stacked Area chart series. |
| [AREA_3_D_STACKED](#AREA-3-D-STACKED) | Represents a 3D Stacked Area chart series. |
| [AREA_PERCENT_STACKED](#AREA-PERCENT-STACKED) | Represents a 100% Stacked Area chart series. |
| [AREA_STACKED](#AREA-STACKED) | Represents a Stacked Area chart series. |
| [BAR](#BAR) | Represents a Bar chart series. |
| [BAR_3_D](#BAR-3-D) | Represents a 3D Bar chart series. |
| [BAR_3_D_PERCENT_STACKED](#BAR-3-D-PERCENT-STACKED) | Represents a 3D 100% Stacked Bar chart series. |
| [BAR_3_D_STACKED](#BAR-3-D-STACKED) | Represents a 3D Stacked Bar chart series. |
| [BAR_PERCENT_STACKED](#BAR-PERCENT-STACKED) | Represents a 100% Stacked Bar chart series. |
| [BAR_STACKED](#BAR-STACKED) | Represents a Stacked Bar chart series. |
| [BOX_AND_WHISKER](#BOX-AND-WHISKER) | Represents a Box and Whisker chart series. |
| [BUBBLE](#BUBBLE) | Represents a Bubble chart series. |
| [BUBBLE_3_D](#BUBBLE-3-D) | Represents a 3D Bubble chart series. |
| [COLUMN](#COLUMN) | Represents a Column chart series. |
| [COLUMN_3_D](#COLUMN-3-D) | Represents a 3D Column chart series. |
| [COLUMN_3_D_CLUSTERED](#COLUMN-3-D-CLUSTERED) | Represents a 3D Clustered Column chart series. |
| [COLUMN_3_D_PERCENT_STACKED](#COLUMN-3-D-PERCENT-STACKED) | Represents a 3D 100% Stacked Column chart series. |
| [COLUMN_3_D_STACKED](#COLUMN-3-D-STACKED) | Represents a 3D Stacked Column chart series. |
| [COLUMN_PERCENT_STACKED](#COLUMN-PERCENT-STACKED) | Represents a 100% Stacked Column chart series. |
| [COLUMN_STACKED](#COLUMN-STACKED) | Represents a Stacked Column chart series. |
| [DOUGHNUT](#DOUGHNUT) | Represents a Doughnut chart series. |
| [FUNNEL](#FUNNEL) | Represents a Funnel chart series. |
| [HISTOGRAM](#HISTOGRAM) | Represents a Histogram chart series. |
| [LINE](#LINE) | Represents a Line chart series. |
| [LINE_3_D](#LINE-3-D) | Represents a 3D Line chart series. |
| [LINE_PERCENT_STACKED](#LINE-PERCENT-STACKED) | Represents a 100% Stacked Line chart series. |
| [LINE_STACKED](#LINE-STACKED) | Represents a Stacked Line chart series. |
| [PARETO](#PARETO) | Represents a Pareto chart series. |
| [PARETO_LINE](#PARETO-LINE) | Represents a Pareto Line chart series. |
| [PIE](#PIE) | Represents a Pie chart series. |
| [PIE_3_D](#PIE-3-D) | Represents a 3D Pie chart series. |
| [PIE_OF_BAR](#PIE-OF-BAR) | Represents a Pie of Bar chart series. |
| [PIE_OF_PIE](#PIE-OF-PIE) | Represents a Pie of Pie chart series. |
| [RADAR](#RADAR) | Represents a Radar chart series. |
| [REGION_MAP](#REGION-MAP) | Represents a Region Map chart series. |
| [SCATTER](#SCATTER) | Represents a Scatter chart series. |
| [STOCK](#STOCK) | Represents a Stock chart series. |
| [SUNBURST](#SUNBURST) | Represents a Sunburst chart series. |
| [SURFACE](#SURFACE) | Represents a Surface chart series. |
| [SURFACE_3_D](#SURFACE-3-D) | Represents a 3D Surface chart series. |
| [TREEMAP](#TREEMAP) | Represents a Treemap chart series. |
| [WATERFALL](#WATERFALL) | Represents a Waterfall chart series. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String chartSeriesTypeName)](#fromName-java.lang.String) |  |
| [getName(int chartSeriesType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartSeriesType)](#toString-int) |  |
### AREA {#AREA}
```
public static int AREA
```


Represents an Area chart series.

### AREA_3_D {#AREA-3-D}
```
public static int AREA_3_D
```


Represents a 3D Area chart series.

### AREA_3_D_PERCENT_STACKED {#AREA-3-D-PERCENT-STACKED}
```
public static int AREA_3_D_PERCENT_STACKED
```


Represents a 3D 100% Stacked Area chart series.

### AREA_3_D_STACKED {#AREA-3-D-STACKED}
```
public static int AREA_3_D_STACKED
```


Represents a 3D Stacked Area chart series.

### AREA_PERCENT_STACKED {#AREA-PERCENT-STACKED}
```
public static int AREA_PERCENT_STACKED
```


Represents a 100% Stacked Area chart series.

### AREA_STACKED {#AREA-STACKED}
```
public static int AREA_STACKED
```


Represents a Stacked Area chart series.

### BAR {#BAR}
```
public static int BAR
```


Represents a Bar chart series.

### BAR_3_D {#BAR-3-D}
```
public static int BAR_3_D
```


Represents a 3D Bar chart series.

### BAR_3_D_PERCENT_STACKED {#BAR-3-D-PERCENT-STACKED}
```
public static int BAR_3_D_PERCENT_STACKED
```


Represents a 3D 100% Stacked Bar chart series.

### BAR_3_D_STACKED {#BAR-3-D-STACKED}
```
public static int BAR_3_D_STACKED
```


Represents a 3D Stacked Bar chart series.

### BAR_PERCENT_STACKED {#BAR-PERCENT-STACKED}
```
public static int BAR_PERCENT_STACKED
```


Represents a 100% Stacked Bar chart series.

### BAR_STACKED {#BAR-STACKED}
```
public static int BAR_STACKED
```


Represents a Stacked Bar chart series.

### BOX_AND_WHISKER {#BOX-AND-WHISKER}
```
public static int BOX_AND_WHISKER
```


Represents a Box and Whisker chart series.

### BUBBLE {#BUBBLE}
```
public static int BUBBLE
```


Represents a Bubble chart series.

### BUBBLE_3_D {#BUBBLE-3-D}
```
public static int BUBBLE_3_D
```


Represents a 3D Bubble chart series.

### COLUMN {#COLUMN}
```
public static int COLUMN
```


Represents a Column chart series.

### COLUMN_3_D {#COLUMN-3-D}
```
public static int COLUMN_3_D
```


Represents a 3D Column chart series.

### COLUMN_3_D_CLUSTERED {#COLUMN-3-D-CLUSTERED}
```
public static int COLUMN_3_D_CLUSTERED
```


Represents a 3D Clustered Column chart series.

### COLUMN_3_D_PERCENT_STACKED {#COLUMN-3-D-PERCENT-STACKED}
```
public static int COLUMN_3_D_PERCENT_STACKED
```


Represents a 3D 100% Stacked Column chart series.

### COLUMN_3_D_STACKED {#COLUMN-3-D-STACKED}
```
public static int COLUMN_3_D_STACKED
```


Represents a 3D Stacked Column chart series.

### COLUMN_PERCENT_STACKED {#COLUMN-PERCENT-STACKED}
```
public static int COLUMN_PERCENT_STACKED
```


Represents a 100% Stacked Column chart series.

### COLUMN_STACKED {#COLUMN-STACKED}
```
public static int COLUMN_STACKED
```


Represents a Stacked Column chart series.

### DOUGHNUT {#DOUGHNUT}
```
public static int DOUGHNUT
```


Represents a Doughnut chart series.

### FUNNEL {#FUNNEL}
```
public static int FUNNEL
```


Represents a Funnel chart series.

### HISTOGRAM {#HISTOGRAM}
```
public static int HISTOGRAM
```


Represents a Histogram chart series.

### LINE {#LINE}
```
public static int LINE
```


Represents a Line chart series.

### LINE_3_D {#LINE-3-D}
```
public static int LINE_3_D
```


Represents a 3D Line chart series.

### LINE_PERCENT_STACKED {#LINE-PERCENT-STACKED}
```
public static int LINE_PERCENT_STACKED
```


Represents a 100% Stacked Line chart series.

### LINE_STACKED {#LINE-STACKED}
```
public static int LINE_STACKED
```


Represents a Stacked Line chart series.

### PARETO {#PARETO}
```
public static int PARETO
```


Represents a Pareto chart series.

### PARETO_LINE {#PARETO-LINE}
```
public static int PARETO_LINE
```


Represents a Pareto Line chart series.

### PIE {#PIE}
```
public static int PIE
```


Represents a Pie chart series.

### PIE_3_D {#PIE-3-D}
```
public static int PIE_3_D
```


Represents a 3D Pie chart series.

### PIE_OF_BAR {#PIE-OF-BAR}
```
public static int PIE_OF_BAR
```


Represents a Pie of Bar chart series.

### PIE_OF_PIE {#PIE-OF-PIE}
```
public static int PIE_OF_PIE
```


Represents a Pie of Pie chart series.

### RADAR {#RADAR}
```
public static int RADAR
```


Represents a Radar chart series.

### REGION_MAP {#REGION-MAP}
```
public static int REGION_MAP
```


Represents a Region Map chart series.

### SCATTER {#SCATTER}
```
public static int SCATTER
```


Represents a Scatter chart series.

### STOCK {#STOCK}
```
public static int STOCK
```


Represents a Stock chart series.

### SUNBURST {#SUNBURST}
```
public static int SUNBURST
```


Represents a Sunburst chart series.

### SURFACE {#SURFACE}
```
public static int SURFACE
```


Represents a Surface chart series.

### SURFACE_3_D {#SURFACE-3-D}
```
public static int SURFACE_3_D
```


Represents a 3D Surface chart series.

### TREEMAP {#TREEMAP}
```
public static int TREEMAP
```


Represents a Treemap chart series.

### WATERFALL {#WATERFALL}
```
public static int WATERFALL
```


Represents a Waterfall chart series.

### length {#length}
```
public static int length
```


### fromName(String chartSeriesTypeName) {#fromName-java.lang.String}
```
public static int fromName(String chartSeriesTypeName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| chartSeriesTypeName | java.lang.String |  |

**Returns:**
int
### getName(int chartSeriesType) {#getName-int}
```
public static String getName(int chartSeriesType)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| chartSeriesType | int |  |

**Returns:**
java.lang.String
