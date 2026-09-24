---
title: "ChartSeriesType"
linktitle: "ChartSeriesType"
second_title: "Aspose.Words para Java"
description: "Especifica un tipo de serie de gráfico en Java."
type: docs
weight: 89
url: /es/java/com.aspose.words/chartseriestype/
---

**Inheritance:**
java.lang.Object
```
public class ChartSeriesType
```

Especifica un tipo de serie del gráfico.

 **Examples:** 

Muestra cómo eliminar una serie de gráfico específica.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [AREA](#AREA) | Representa una serie de gráfico de Área. |
| [AREA_3_D](#AREA-3-D) | Representa una serie de gráfico de Área 3D. |
| [AREA_3_D_PERCENT_STACKED](#AREA-3-D-PERCENT-STACKED) | Representa una serie de gráfico de Área apilada al 100% 3D. |
| [AREA_3_D_STACKED](#AREA-3-D-STACKED) | Representa una serie de gráfico de Área apilada 3D. |
| [AREA_PERCENT_STACKED](#AREA-PERCENT-STACKED) | Representa una serie de gráfico de Área apilada al 100%. |
| [AREA_STACKED](#AREA-STACKED) | Representa una serie de gráfico de Área apilada. |
| [BAR](#BAR) | Representa una serie de gráfico de Barras. |
| [BAR_3_D](#BAR-3-D) | Representa una serie de gráfico de Barras 3D. |
| [BAR_3_D_PERCENT_STACKED](#BAR-3-D-PERCENT-STACKED) | Representa una serie de gráfico de Barras apilada al 100% 3D. |
| [BAR_3_D_STACKED](#BAR-3-D-STACKED) | Representa una serie de gráfico de Barras apilada 3D. |
| [BAR_PERCENT_STACKED](#BAR-PERCENT-STACKED) | Representa una serie de gráfico de Barras apilada al 100%. |
| [BAR_STACKED](#BAR-STACKED) | Representa una serie de gráfico de Barras apilada. |
| [BOX_AND_WHISKER](#BOX-AND-WHISKER) | Representa una serie de gráfico de Caja y Bigotes. |
| [BUBBLE](#BUBBLE) | Representa una serie de gráfico de Burbujas. |
| [BUBBLE_3_D](#BUBBLE-3-D) | Representa una serie de gráfico de Burbujas 3D. |
| [COLUMN](#COLUMN) | Representa una serie de gráfico de Columnas. |
| [COLUMN_3_D](#COLUMN-3-D) | Representa una serie de gráfico de columnas 3D. |
| [COLUMN_3_D_CLUSTERED](#COLUMN-3-D-CLUSTERED) | Representa una serie de gráfico de columnas agrupadas 3D. |
| [COLUMN_3_D_PERCENT_STACKED](#COLUMN-3-D-PERCENT-STACKED) | Representa una serie de gráfico de columnas apiladas al 100% 3D. |
| [COLUMN_3_D_STACKED](#COLUMN-3-D-STACKED) | Representa una serie de gráfico de columnas apiladas 3D. |
| [COLUMN_PERCENT_STACKED](#COLUMN-PERCENT-STACKED) | Representa una serie de gráfico de columnas apiladas al 100%. |
| [COLUMN_STACKED](#COLUMN-STACKED) | Representa una serie de gráfico de columnas apiladas. |
| [DOUGHNUT](#DOUGHNUT) | Representa una serie de gráfico de dona. |
| [FUNNEL](#FUNNEL) | Representa una serie de gráfico de embudo. |
| [HISTOGRAM](#HISTOGRAM) | Representa una serie de gráfico de histograma. |
| [LINE](#LINE) | Representa una serie de gráfico de líneas. |
| [LINE_3_D](#LINE-3-D) | Representa una serie de gráfico de líneas 3D. |
| [LINE_PERCENT_STACKED](#LINE-PERCENT-STACKED) | Representa una serie de gráfico de líneas apiladas al 100%. |
| [LINE_STACKED](#LINE-STACKED) | Representa una serie de gráfico de líneas apiladas. |
| [PARETO](#PARETO) | Representa una serie de gráfico de Pareto. |
| [PARETO_LINE](#PARETO-LINE) | Representa una serie de gráfico de línea Pareto. |
| [PIE](#PIE) | Representa una serie de gráfico circular. |
| [PIE_3_D](#PIE-3-D) | Representa una serie de gráfico circular 3D. |
| [PIE_OF_BAR](#PIE-OF-BAR) | Representa una serie de gráfico de pastel de barras. |
| [PIE_OF_PIE](#PIE-OF-PIE) | Representa una serie de gráfico de pastel de pastel. |
| [RADAR](#RADAR) | Representa una serie de gráfico de radar. |
| [REGION_MAP](#REGION-MAP) | Representa una serie de gráfico de mapa de región. |
| [SCATTER](#SCATTER) | Representa una serie de gráfico de dispersión. |
| [STOCK](#STOCK) | Representa una serie de gráfico de acciones. |
| [SUNBURST](#SUNBURST) | Representa una serie de gráfico de explosión radial. |
| [SURFACE](#SURFACE) | Representa una serie de gráfico de superficie. |
| [SURFACE_3_D](#SURFACE-3-D) | Representa una serie de gráfico de superficie 3D. |
| [TREEMAP](#TREEMAP) | Representa una serie de gráfico de árbol de mapas. |
| [WATERFALL](#WATERFALL) | Representa una serie de gráfico de cascada. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String chartSeriesTypeName)](#fromName-java.lang.String) |  |
| [getName(int chartSeriesType)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartSeriesType)](#toString-int) |  |
### AREA {#AREA}
```
public static int AREA
```


Representa una serie de gráfico de Área.

### AREA_3_D {#AREA-3-D}
```
public static int AREA_3_D
```


Representa una serie de gráfico de Área 3D.

### AREA_3_D_PERCENT_STACKED {#AREA-3-D-PERCENT-STACKED}
```
public static int AREA_3_D_PERCENT_STACKED
```


Representa una serie de gráfico de Área apilada al 100% 3D.

### AREA_3_D_STACKED {#AREA-3-D-STACKED}
```
public static int AREA_3_D_STACKED
```


Representa una serie de gráfico de Área apilada 3D.

### AREA_PERCENT_STACKED {#AREA-PERCENT-STACKED}
```
public static int AREA_PERCENT_STACKED
```


Representa una serie de gráfico de Área apilada al 100%.

### AREA_STACKED {#AREA-STACKED}
```
public static int AREA_STACKED
```


Representa una serie de gráfico de Área apilada.

### BAR {#BAR}
```
public static int BAR
```


Representa una serie de gráfico de Barras.

### BAR_3_D {#BAR-3-D}
```
public static int BAR_3_D
```


Representa una serie de gráfico de Barras 3D.

### BAR_3_D_PERCENT_STACKED {#BAR-3-D-PERCENT-STACKED}
```
public static int BAR_3_D_PERCENT_STACKED
```


Representa una serie de gráfico de Barras apilada al 100% 3D.

### BAR_3_D_STACKED {#BAR-3-D-STACKED}
```
public static int BAR_3_D_STACKED
```


Representa una serie de gráfico de Barras apilada 3D.

### BAR_PERCENT_STACKED {#BAR-PERCENT-STACKED}
```
public static int BAR_PERCENT_STACKED
```


Representa una serie de gráfico de Barras apilada al 100%.

### BAR_STACKED {#BAR-STACKED}
```
public static int BAR_STACKED
```


Representa una serie de gráfico de Barras apilada.

### BOX_AND_WHISKER {#BOX-AND-WHISKER}
```
public static int BOX_AND_WHISKER
```


Representa una serie de gráfico de Caja y Bigotes.

### BUBBLE {#BUBBLE}
```
public static int BUBBLE
```


Representa una serie de gráfico de Burbujas.

### BUBBLE_3_D {#BUBBLE-3-D}
```
public static int BUBBLE_3_D
```


Representa una serie de gráfico de Burbujas 3D.

### COLUMN {#COLUMN}
```
public static int COLUMN
```


Representa una serie de gráfico de Columnas.

### COLUMN_3_D {#COLUMN-3-D}
```
public static int COLUMN_3_D
```


Representa una serie de gráfico de columnas 3D.

### COLUMN_3_D_CLUSTERED {#COLUMN-3-D-CLUSTERED}
```
public static int COLUMN_3_D_CLUSTERED
```


Representa una serie de gráfico de columnas agrupadas 3D.

### COLUMN_3_D_PERCENT_STACKED {#COLUMN-3-D-PERCENT-STACKED}
```
public static int COLUMN_3_D_PERCENT_STACKED
```


Representa una serie de gráfico de columnas apiladas al 100% 3D.

### COLUMN_3_D_STACKED {#COLUMN-3-D-STACKED}
```
public static int COLUMN_3_D_STACKED
```


Representa una serie de gráfico de columnas apiladas 3D.

### COLUMN_PERCENT_STACKED {#COLUMN-PERCENT-STACKED}
```
public static int COLUMN_PERCENT_STACKED
```


Representa una serie de gráfico de columnas apiladas al 100%.

### COLUMN_STACKED {#COLUMN-STACKED}
```
public static int COLUMN_STACKED
```


Representa una serie de gráfico de columnas apiladas.

### DOUGHNUT {#DOUGHNUT}
```
public static int DOUGHNUT
```


Representa una serie de gráfico de dona.

### FUNNEL {#FUNNEL}
```
public static int FUNNEL
```


Representa una serie de gráfico de embudo.

### HISTOGRAM {#HISTOGRAM}
```
public static int HISTOGRAM
```


Representa una serie de gráfico de histograma.

### LINE {#LINE}
```
public static int LINE
```


Representa una serie de gráfico de líneas.

### LINE_3_D {#LINE-3-D}
```
public static int LINE_3_D
```


Representa una serie de gráfico de líneas 3D.

### LINE_PERCENT_STACKED {#LINE-PERCENT-STACKED}
```
public static int LINE_PERCENT_STACKED
```


Representa una serie de gráfico de líneas apiladas al 100%.

### LINE_STACKED {#LINE-STACKED}
```
public static int LINE_STACKED
```


Representa una serie de gráfico de líneas apiladas.

### PARETO {#PARETO}
```
public static int PARETO
```


Representa una serie de gráfico de Pareto.

### PARETO_LINE {#PARETO-LINE}
```
public static int PARETO_LINE
```


Representa una serie de gráfico de línea Pareto.

### PIE {#PIE}
```
public static int PIE
```


Representa una serie de gráfico circular.

### PIE_3_D {#PIE-3-D}
```
public static int PIE_3_D
```


Representa una serie de gráfico circular 3D.

### PIE_OF_BAR {#PIE-OF-BAR}
```
public static int PIE_OF_BAR
```


Representa una serie de gráfico de pastel de barras.

### PIE_OF_PIE {#PIE-OF-PIE}
```
public static int PIE_OF_PIE
```


Representa una serie de gráfico de pastel de pastel.

### RADAR {#RADAR}
```
public static int RADAR
```


Representa una serie de gráfico de radar.

### REGION_MAP {#REGION-MAP}
```
public static int REGION_MAP
```


Representa una serie de gráfico de mapa de región.

### SCATTER {#SCATTER}
```
public static int SCATTER
```


Representa una serie de gráfico de dispersión.

### STOCK {#STOCK}
```
public static int STOCK
```


Representa una serie de gráfico de acciones.

### SUNBURST {#SUNBURST}
```
public static int SUNBURST
```


Representa una serie de gráfico de explosión radial.

### SURFACE {#SURFACE}
```
public static int SURFACE
```


Representa una serie de gráfico de superficie.

### SURFACE_3_D {#SURFACE-3-D}
```
public static int SURFACE_3_D
```


Representa una serie de gráfico de superficie 3D.

### TREEMAP {#TREEMAP}
```
public static int TREEMAP
```


Representa una serie de gráfico de árbol de mapas.

### WATERFALL {#WATERFALL}
```
public static int WATERFALL
```


Representa una serie de gráfico de cascada.

### length {#length}
```
public static int length
```


### fromName(String chartSeriesTypeName) {#fromName-java.lang.String}
```
public static int fromName(String chartSeriesTypeName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| chartSeriesTypeName | java.lang.String |  |

**Returns:**
int
### getName(int chartSeriesType) {#getName-int}
```
public static String getName(int chartSeriesType)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| chartSeriesType | int |  |

**Returns:**
java.lang.String
