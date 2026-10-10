---
title: "ChartStyle"
linktitle: "ChartStyle"
second_title: "Aspose.Words para Java"
description: "Especifica estilos predefinidos de un gráfico en Java."
type: docs
weight: 91
url: /es/java/com.aspose.words/chartstyle/
---

**Inheritance:**
java.lang.Object
```
public class ChartStyle
```

Especifica estilos predefinidos de un gráfico.

 **Examples:** 

Muestra cómo establecer y obtener el estilo del gráfico.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a chart in the Black style.
 builder.insertChart(ChartType.COLUMN, 400.0, 250.0, ChartStyle.BLACK);

 doc.save(getArtifactsDir() + "Charts.SetChartStyle.docx");

 doc = new Document(getArtifactsDir() + "Charts.SetChartStyle.docx");

 // Get a chart to update.
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 Chart chart = shape.getChart();

 // Get the chart style.
 Assert.assertEquals(ChartStyle.BLACK, chart.getStyle());
 
```
## Campos

| Campo | Descripción |
| --- | --- |
| [BLACK](#BLACK) | Un estilo con fondo de gráfico negro. |
| [BLUE](#BLUE) | Un estilo con fondo de gráfico azul. |
| [FLAT](#FLAT) | Un estilo con puntos de datos planos sin degradado. |
| [GRADIENT](#GRADIENT) | Un estilo con relleno degradado de los puntos de datos. |
| [GREY](#GREY) | Un estilo con fondo de gráfico degradado gris. |
| [MUTED](#MUTED) | Un estilo con colores apagados. |
| [NORMAL](#NORMAL) | Representa el estilo de gráfico predeterminado. |
| [ORIGINAL](#ORIGINAL) | Un estilo con una apariencia original de un gráfico. |
| [OUTLINE](#OUTLINE) | Un estilo con puntos de datos sin relleno, pero solo con contorno. |
| [OUTLINE_BLACK](#OUTLINE-BLACK) | Un estilo con fondo de gráfico negro, en el que los puntos de datos no tienen relleno, sino solo un contorno. |
| [SATURATED](#SATURATED) | Un estilo con colores más saturados. |
| [SHADED](#SHADED) | Un estilo con puntos de datos sombreados. |
| [SHADED_PLOT](#SHADED-PLOT) | Un estilo, en el que el área del trazado está sombreada. |
| [SHADOWED](#SHADOWED) | Un estilo con puntos de datos que tienen sombra. |
| [TRANSPARENT_1](#TRANSPARENT-1) | Un estilo con puntos de datos transparentes. |
| [TRANSPARENT_2](#TRANSPARENT-2) | Un estilo con puntos de datos transparentes. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String chartStyleName)](#fromName-java.lang.String) |  |
| [getName(int chartStyle)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartStyle)](#toString-int) |  |
### BLACK {#BLACK}
```
public static int BLACK
```


Un estilo con fondo de gráfico negro.

### BLUE {#BLUE}
```
public static int BLUE
```


Un estilo con fondo de gráfico azul.

### FLAT {#FLAT}
```
public static int FLAT
```


Un estilo con puntos de datos planos sin degradado.

### GRADIENT {#GRADIENT}
```
public static int GRADIENT
```


Un estilo con relleno degradado de los puntos de datos.

### GREY {#GREY}
```
public static int GREY
```


Un estilo con fondo de gráfico degradado gris.

### MUTED {#MUTED}
```
public static int MUTED
```


Un estilo con colores apagados.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Representa el estilo de gráfico predeterminado.

### ORIGINAL {#ORIGINAL}
```
public static int ORIGINAL
```


Un estilo con una apariencia original de un gráfico.

### OUTLINE {#OUTLINE}
```
public static int OUTLINE
```


Un estilo con puntos de datos sin relleno, pero solo con contorno.

### OUTLINE_BLACK {#OUTLINE-BLACK}
```
public static int OUTLINE_BLACK
```


Un estilo con fondo de gráfico negro, en el que los puntos de datos no tienen relleno, sino solo un contorno.

### SATURATED {#SATURATED}
```
public static int SATURATED
```


Un estilo con colores más saturados.

### SHADED {#SHADED}
```
public static int SHADED
```


Un estilo con puntos de datos sombreados.

### SHADED_PLOT {#SHADED-PLOT}
```
public static int SHADED_PLOT
```


Un estilo, en el que el área del trazado está sombreada.

### SHADOWED {#SHADOWED}
```
public static int SHADOWED
```


Un estilo con puntos de datos que tienen sombra.

### TRANSPARENT_1 {#TRANSPARENT-1}
```
public static int TRANSPARENT_1
```


Un estilo con puntos de datos transparentes.

### TRANSPARENT_2 {#TRANSPARENT-2}
```
public static int TRANSPARENT_2
```


Un estilo con puntos de datos transparentes.

### length {#length}
```
public static int length
```


### fromName(String chartStyleName) {#fromName-java.lang.String}
```
public static int fromName(String chartStyleName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| chartStyleName | java.lang.String |  |

**Returns:**
int
### getName(int chartStyle) {#getName-int}
```
public static String getName(int chartStyle)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| chartStyle | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int chartStyle) {#toString-int}
```
public static String toString(int chartStyle)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| chartStyle | int |  |

**Returns:**
java.lang.String
