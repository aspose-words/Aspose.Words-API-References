---
title: "ChartStyle"
linktitle: "ChartStyle"
second_title: "Aspose.Words per Java"
description: "Specifica gli stili predefiniti di un grafico in Java."
type: docs
weight: 91
url: /it/java/com.aspose.words/chartstyle/
---

**Inheritance:**
java.lang.Object
```
public class ChartStyle
```

Specifica gli stili predefiniti di un grafico.

 **Examples:** 

Mostra come impostare e ottenere lo stile del grafico.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [BLACK](#BLACK) | Uno stile con sfondo del grafico nero. |
| [BLUE](#BLUE) | Uno stile con sfondo del grafico blu. |
| [FLAT](#FLAT) | Uno stile con punti dati piatti senza gradiente. |
| [GRADIENT](#GRADIENT) | Uno stile con riempimento a gradiente dei punti dati. |
| [GREY](#GREY) | Uno stile con sfondo del grafico a gradiente grigio. |
| [MUTED](#MUTED) | Uno stile con colori smorzati. |
| [NORMAL](#NORMAL) | Rappresenta lo stile predefinito del grafico. |
| [ORIGINAL](#ORIGINAL) | Uno stile con un aspetto originale del grafico. |
| [OUTLINE](#OUTLINE) | Uno stile con punti dati senza riempimento, ma solo un contorno. |
| [OUTLINE_BLACK](#OUTLINE-BLACK) | Uno stile con sfondo del grafico nero, in cui i punti dati non hanno riempimento, ma solo un contorno. |
| [SATURATED](#SATURATED) | Uno stile con colori più saturi. |
| [SHADED](#SHADED) | Uno stile con punti dati ombreggiati. |
| [SHADED_PLOT](#SHADED-PLOT) | Uno stile, in cui l'area del grafico è ombreggiata. |
| [SHADOWED](#SHADOWED) | Uno stile con punti dati che hanno un'ombra. |
| [TRANSPARENT_1](#TRANSPARENT-1) | Uno stile con punti dati trasparenti. |
| [TRANSPARENT_2](#TRANSPARENT-2) | Uno stile con punti dati trasparenti. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String chartStyleName)](#fromName-java.lang.String) |  |
| [getName(int chartStyle)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartStyle)](#toString-int) |  |
### BLACK {#BLACK}
```
public static int BLACK
```


Uno stile con sfondo del grafico nero.

### BLUE {#BLUE}
```
public static int BLUE
```


Uno stile con sfondo del grafico blu.

### FLAT {#FLAT}
```
public static int FLAT
```


Uno stile con punti dati piatti senza gradiente.

### GRADIENT {#GRADIENT}
```
public static int GRADIENT
```


Uno stile con riempimento a gradiente dei punti dati.

### GREY {#GREY}
```
public static int GREY
```


Uno stile con sfondo del grafico a gradiente grigio.

### MUTED {#MUTED}
```
public static int MUTED
```


Uno stile con colori smorzati.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Rappresenta lo stile predefinito del grafico.

### ORIGINAL {#ORIGINAL}
```
public static int ORIGINAL
```


Uno stile con un aspetto originale del grafico.

### OUTLINE {#OUTLINE}
```
public static int OUTLINE
```


Uno stile con punti dati senza riempimento, ma solo un contorno.

### OUTLINE_BLACK {#OUTLINE-BLACK}
```
public static int OUTLINE_BLACK
```


Uno stile con sfondo del grafico nero, in cui i punti dati non hanno riempimento, ma solo un contorno.

### SATURATED {#SATURATED}
```
public static int SATURATED
```


Uno stile con colori più saturi.

### SHADED {#SHADED}
```
public static int SHADED
```


Uno stile con punti dati ombreggiati.

### SHADED_PLOT {#SHADED-PLOT}
```
public static int SHADED_PLOT
```


Uno stile, in cui l'area del grafico è ombreggiata.

### SHADOWED {#SHADOWED}
```
public static int SHADOWED
```


Uno stile con punti dati che hanno un'ombra.

### TRANSPARENT_1 {#TRANSPARENT-1}
```
public static int TRANSPARENT_1
```


Uno stile con punti dati trasparenti.

### TRANSPARENT_2 {#TRANSPARENT-2}
```
public static int TRANSPARENT_2
```


Uno stile con punti dati trasparenti.

### length {#length}
```
public static int length
```


### fromName(String chartStyleName) {#fromName-java.lang.String}
```
public static int fromName(String chartStyleName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| chartStyleName | java.lang.String |  |

**Returns:**
int
### getName(int chartStyle) {#getName-int}
```
public static String getName(int chartStyle)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| chartStyle | int |  |

**Returns:**
java.lang.String
