---
title: "LegendPosition"
linktitle: "LegendPosition"
second_title: "Aspose.Words para Java"
description: "Especifica las posiciones posibles para la leyenda de un gráfico en Java."
type: docs
weight: 420
url: /es/java/com.aspose.words/legendposition/
---

**Inheritance:**
java.lang.Object
```
public class LegendPosition
```

Especifica las posiciones posibles para la leyenda de un gráfico.

 **Examples:** 

Muestra cómo editar la apariencia de la leyenda de un gráfico.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 450.0, 300.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(3, chart.getSeries().getCount());
 Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
 Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
 Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

 // Move the chart's legend to the top right corner.
 ChartLegend legend = chart.getLegend();
 legend.setPosition(LegendPosition.TOP_RIGHT);

 // Give other chart elements, such as the graph, more room by allowing them to overlap the legend.
 legend.setOverlay(true);

 doc.save(getArtifactsDir() + "Charts.ChartLegend.docx");
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [BOTTOM](#BOTTOM) | Especifica que la leyenda se dibujará en la parte inferior del gráfico. |
| [LEFT](#LEFT) | Especifica que la leyenda se dibujará a la izquierda del gráfico. |
| [NONE](#NONE) | No se mostrará ninguna leyenda para el gráfico. |
| [RIGHT](#RIGHT) | Especifica que la leyenda se dibujará a la derecha del gráfico. |
| [TOP](#TOP) | Especifica que la leyenda se dibujará en la parte superior del gráfico. |
| [TOP_RIGHT](#TOP-RIGHT) | Especifica que la leyenda se dibujará en la esquina superior derecha del gráfico. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String legendPositionName)](#fromName-java.lang.String) |  |
| [getName(int legendPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int legendPosition)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Especifica que la leyenda se dibujará en la parte inferior del gráfico.

### LEFT {#LEFT}
```
public static int LEFT
```


Especifica que la leyenda se dibujará a la izquierda del gráfico.

### NONE {#NONE}
```
public static int NONE
```


No se mostrará ninguna leyenda para el gráfico.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Especifica que la leyenda se dibujará a la derecha del gráfico.

### TOP {#TOP}
```
public static int TOP
```


Especifica que la leyenda se dibujará en la parte superior del gráfico.

### TOP_RIGHT {#TOP-RIGHT}
```
public static int TOP_RIGHT
```


Especifica que la leyenda se dibujará en la esquina superior derecha del gráfico.

### length {#length}
```
public static int length
```


### fromName(String legendPositionName) {#fromName-java.lang.String}
```
public static int fromName(String legendPositionName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| legendPositionName | java.lang.String |  |

**Returns:**
int
### getName(int legendPosition) {#getName-int}
```
public static String getName(int legendPosition)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| legendPosition | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int legendPosition) {#toString-int}
```
public static String toString(int legendPosition)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| legendPosition | int |  |

**Returns:**
java.lang.String
