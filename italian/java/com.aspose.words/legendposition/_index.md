---
title: "LegendPosition"
linktitle: "LegendPosition"
second_title: "Aspose.Words per Java"
description: "Specifica le possibili posizioni per la legenda di un grafico in Java."
type: docs
weight: 420
url: /it/java/com.aspose.words/legendposition/
---

**Inheritance:**
java.lang.Object
```
public class LegendPosition
```

Specifica le posizioni possibili per la legenda di un grafico.

 **Examples:** 

Mostra come modificare l'aspetto della legenda di un grafico.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [BOTTOM](#BOTTOM) | Specifica che la legenda deve essere disegnata nella parte inferiore del grafico. |
| [LEFT](#LEFT) | Specifica che la legenda deve essere disegnata a sinistra del grafico. |
| [NONE](#NONE) | Nessuna legenda verrà mostrata per il grafico. |
| [RIGHT](#RIGHT) | Specifica che la legenda deve essere disegnata a destra del grafico. |
| [TOP](#TOP) | Specifica che la legenda deve essere disegnata nella parte superiore del grafico. |
| [TOP_RIGHT](#TOP-RIGHT) | Specifica che la legenda deve essere disegnata in alto a destra del grafico. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String legendPositionName)](#fromName-java.lang.String) |  |
| [getName(int legendPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int legendPosition)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Specifica che la legenda deve essere disegnata nella parte inferiore del grafico.

### LEFT {#LEFT}
```
public static int LEFT
```


Specifica che la legenda deve essere disegnata a sinistra del grafico.

### NONE {#NONE}
```
public static int NONE
```


Nessuna legenda verrà mostrata per il grafico.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Specifica che la legenda deve essere disegnata a destra del grafico.

### TOP {#TOP}
```
public static int TOP
```


Specifica che la legenda deve essere disegnata nella parte superiore del grafico.

### TOP_RIGHT {#TOP-RIGHT}
```
public static int TOP_RIGHT
```


Specifica che la legenda deve essere disegnata in alto a destra del grafico.

### length {#length}
```
public static int length
```


### fromName(String legendPositionName) {#fromName-java.lang.String}
```
public static int fromName(String legendPositionName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| legendPositionName | java.lang.String |  |

**Returns:**
int
### getName(int legendPosition) {#getName-int}
```
public static String getName(int legendPosition)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| legendPosition | int |  |

**Returns:**
java.lang.String
