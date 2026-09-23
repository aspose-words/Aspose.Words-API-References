---
title: "ChartStyle"
linktitle: "ChartStyle"
second_title: "Aspose.Words für Java"
description: "Gibt vordefinierte Diagramm‑Stile in Java an."
type: docs
weight: 91
url: /de/java/com.aspose.words/chartstyle/
---

**Inheritance:**
java.lang.Object
```
public class ChartStyle
```

Gibt vordefinierte Stile eines Diagramms an.

 **Examples:** 

Zeigt, wie man den Diagrammstil festlegt und abruft.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [BLACK](#BLACK) | Ein Stil mit schwarzem Diagrammhintergrund. |
| [BLUE](#BLUE) | Ein Stil mit blauem Diagrammhintergrund. |
| [FLAT](#FLAT) | Ein Stil mit flachen Datenpunkten ohne Verlauf. |
| [GRADIENT](#GRADIENT) | Ein Stil mit Farbverlauf‑Füllung der Datenpunkte. |
| [GREY](#GREY) | Ein Stil mit grauem Verlauf‑Diagrammhintergrund. |
| [MUTED](#MUTED) | Ein Stil mit gedämpften Farben. |
| [NORMAL](#NORMAL) | Stellt den Standard‑Diagrammstil dar. |
| [ORIGINAL](#ORIGINAL) | Ein Stil mit dem ursprünglichen Aussehen eines Diagramms. |
| [OUTLINE](#OUTLINE) | Ein Stil mit Datenpunkten, die keine Füllung haben, sondern nur eine Kontur. |
| [OUTLINE_BLACK](#OUTLINE-BLACK) | Ein Stil mit schwarzem Diagrammhintergrund, bei dem Datenpunkte keine Füllung haben, sondern nur eine Kontur. |
| [SATURATED](#SATURATED) | Ein Stil mit stärker gesättigten Farben. |
| [SHADED](#SHADED) | Ein Stil mit schattierten Datenpunkten. |
| [SHADED_PLOT](#SHADED-PLOT) | Ein Stil, bei dem der Plotbereich schattiert ist. |
| [SHADOWED](#SHADOWED) | Ein Stil mit Datenpunkten, die einen Schatten haben. |
| [TRANSPARENT_1](#TRANSPARENT-1) | Ein Stil mit transparenten Datenpunkten. |
| [TRANSPARENT_2](#TRANSPARENT-2) | Ein Stil mit transparenten Datenpunkten. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String chartStyleName)](#fromName-java.lang.String) |  |
| [getName(int chartStyle)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartStyle)](#toString-int) |  |
### BLACK {#BLACK}
```
public static int BLACK
```


Ein Stil mit schwarzem Diagrammhintergrund.

### BLUE {#BLUE}
```
public static int BLUE
```


Ein Stil mit blauem Diagrammhintergrund.

### FLAT {#FLAT}
```
public static int FLAT
```


Ein Stil mit flachen Datenpunkten ohne Verlauf.

### GRADIENT {#GRADIENT}
```
public static int GRADIENT
```


Ein Stil mit Farbverlauf‑Füllung der Datenpunkte.

### GREY {#GREY}
```
public static int GREY
```


Ein Stil mit grauem Verlauf‑Diagrammhintergrund.

### MUTED {#MUTED}
```
public static int MUTED
```


Ein Stil mit gedämpften Farben.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Stellt den Standard‑Diagrammstil dar.

### ORIGINAL {#ORIGINAL}
```
public static int ORIGINAL
```


Ein Stil mit dem ursprünglichen Aussehen eines Diagramms.

### OUTLINE {#OUTLINE}
```
public static int OUTLINE
```


Ein Stil mit Datenpunkten, die keine Füllung haben, sondern nur eine Kontur.

### OUTLINE_BLACK {#OUTLINE-BLACK}
```
public static int OUTLINE_BLACK
```


Ein Stil mit schwarzem Diagrammhintergrund, bei dem Datenpunkte keine Füllung haben, sondern nur eine Kontur.

### SATURATED {#SATURATED}
```
public static int SATURATED
```


Ein Stil mit stärker gesättigten Farben.

### SHADED {#SHADED}
```
public static int SHADED
```


Ein Stil mit schattierten Datenpunkten.

### SHADED_PLOT {#SHADED-PLOT}
```
public static int SHADED_PLOT
```


Ein Stil, bei dem der Plotbereich schattiert ist.

### SHADOWED {#SHADOWED}
```
public static int SHADOWED
```


Ein Stil mit Datenpunkten, die einen Schatten haben.

### TRANSPARENT_1 {#TRANSPARENT-1}
```
public static int TRANSPARENT_1
```


Ein Stil mit transparenten Datenpunkten.

### TRANSPARENT_2 {#TRANSPARENT-2}
```
public static int TRANSPARENT_2
```


Ein Stil mit transparenten Datenpunkten.

### length {#length}
```
public static int length
```


### fromName(String chartStyleName) {#fromName-java.lang.String}
```
public static int fromName(String chartStyleName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| chartStyleName | java.lang.String |  |

**Returns:**
int
### getName(int chartStyle) {#getName-int}
```
public static String getName(int chartStyle)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| chartStyle | int |  |

**Returns:**
java.lang.String
