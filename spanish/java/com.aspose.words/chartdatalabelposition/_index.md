---
title: "ChartDataLabelPosition"
linktitle: "ChartDataLabelPosition"
second_title: "Aspose.Words para Java"
description: "Especifica la posición de una etiqueta de datos de gráfico en Java."
type: docs
weight: 74
url: /es/java/com.aspose.words/chartdatalabelposition/
---

**Inheritance:**
java.lang.Object
```
public class ChartDataLabelPosition
```

Especifica la posición de una etiqueta de datos del gráfico.

 **Remarks:** 

No todos los tipos de series permiten especificar posiciones de etiquetas. Y los que lo permiten, no admiten todos los valores.

 **Examples:** 

Muestra cómo establecer la posición de la etiqueta de datos.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert column chart.
 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();

 // Delete default generated series.
 seriesColl.clear();

 // Add series.
 ChartSeries series = seriesColl.add(
         "Series 1",
         new String[] { "Category 1", "Category 2", "Category 3" },
         new double[] { 4.0, 5.0, 6.0 });

 // Show data labels and set font color.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.getFont().setColor(Color.WHITE);

 // Set data label position.
 dataLabels.setPosition(ChartDataLabelPosition.INSIDE_BASE);
 dataLabels.get(0).setPosition(ChartDataLabelPosition.OUTSIDE_END);
 dataLabels.get(0).getFont().setColor(Color.RED);

 doc.save(getArtifactsDir() + "Charts.LabelPosition.docx");
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [ABOVE](#ABOVE) | Especifica que una etiqueta de datos debe mostrarse encima de un marcador de datos. |
| [BELOW](#BELOW) | Especifica que una etiqueta de datos debe mostrarse debajo de un marcador de datos. |
| [BEST_FIT](#BEST-FIT) | Especifica que una etiqueta de datos debe mostrarse en la posición más apropiada. |
| [CENTER](#CENTER) | Especifica que una etiqueta de datos debe mostrarse centrada en un marcador de datos. |
| [INSIDE_BASE](#INSIDE-BASE) | Especifica que una etiqueta de datos debe mostrarse dentro de la base de un marcador de datos. |
| [INSIDE_END](#INSIDE-END) | Especifica que una etiqueta de datos debe mostrarse dentro del extremo de un marcador de datos. |
| [LEFT](#LEFT) | Especifica que una etiqueta de datos debe mostrarse a la izquierda de un marcador de datos. |
| [OUTSIDE_END](#OUTSIDE-END) | Especifica que una etiqueta de datos debe mostrarse fuera del extremo de un marcador de datos. |
| [RIGHT](#RIGHT) | Especifica que una etiqueta de datos debe mostrarse a la derecha de un marcador de datos. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String chartDataLabelPositionName)](#fromName-java.lang.String) |  |
| [getName(int chartDataLabelPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartDataLabelPosition)](#toString-int) |  |
### ABOVE {#ABOVE}
```
public static int ABOVE
```


Especifica que una etiqueta de datos debe mostrarse encima de un marcador de datos.

### BELOW {#BELOW}
```
public static int BELOW
```


Especifica que una etiqueta de datos debe mostrarse debajo de un marcador de datos.

### BEST_FIT {#BEST-FIT}
```
public static int BEST_FIT
```


Especifica que una etiqueta de datos debe mostrarse en la posición más apropiada.

### CENTER {#CENTER}
```
public static int CENTER
```


Especifica que una etiqueta de datos debe mostrarse centrada en un marcador de datos.

### INSIDE_BASE {#INSIDE-BASE}
```
public static int INSIDE_BASE
```


Especifica que una etiqueta de datos debe mostrarse dentro de la base de un marcador de datos.

### INSIDE_END {#INSIDE-END}
```
public static int INSIDE_END
```


Especifica que una etiqueta de datos debe mostrarse dentro del extremo de un marcador de datos.

### LEFT {#LEFT}
```
public static int LEFT
```


Especifica que una etiqueta de datos debe mostrarse a la izquierda de un marcador de datos.

### OUTSIDE_END {#OUTSIDE-END}
```
public static int OUTSIDE_END
```


Especifica que una etiqueta de datos debe mostrarse fuera del extremo de un marcador de datos.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Especifica que una etiqueta de datos debe mostrarse a la derecha de un marcador de datos.

### length {#length}
```
public static int length
```


### fromName(String chartDataLabelPositionName) {#fromName-java.lang.String}
```
public static int fromName(String chartDataLabelPositionName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| chartDataLabelPositionName | java.lang.String |  |

**Returns:**
int
### getName(int chartDataLabelPosition) {#getName-int}
```
public static String getName(int chartDataLabelPosition)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| chartDataLabelPosition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int chartDataLabelPosition) {#toString-int}
```
public static String toString(int chartDataLabelPosition)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| chartDataLabelPosition | int |  |

**Returns:**
java.lang.String
