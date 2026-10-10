---
title: "LegendPosition"
linktitle: "LegendPosition"
second_title: "Aspose.Words für Java"
description: "Gibt die möglichen Positionen einer Diagrammlegende in Java an."
type: docs
weight: 420
url: /de/java/com.aspose.words/legendposition/
---

**Inheritance:**
java.lang.Object
```
public class LegendPosition
```

Gibt die möglichen Positionen für eine Diagrammlegende an.

 **Examples:** 

Zeigt, wie man das Erscheinungsbild der Diagrammlegende bearbeitet.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [BOTTOM](#BOTTOM) | Gibt an, dass die Legende am unteren Rand des Diagramms gezeichnet wird. |
| [LEFT](#LEFT) | Gibt an, dass die Legende links vom Diagramm gezeichnet werden soll. |
| [NONE](#NONE) | Für das Diagramm wird keine Legende angezeigt. |
| [RIGHT](#RIGHT) | Gibt an, dass die Legende rechts vom Diagramm gezeichnet werden soll. |
| [TOP](#TOP) | Gibt an, dass die Legende oben im Diagramm gezeichnet werden soll. |
| [TOP_RIGHT](#TOP-RIGHT) | Gibt an, dass die Legende oben rechts im Diagramm gezeichnet werden soll. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String legendPositionName)](#fromName-java.lang.String) |  |
| [getName(int legendPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int legendPosition)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Gibt an, dass die Legende am unteren Rand des Diagramms gezeichnet wird.

### LEFT {#LEFT}
```
public static int LEFT
```


Gibt an, dass die Legende links vom Diagramm gezeichnet werden soll.

### NONE {#NONE}
```
public static int NONE
```


Für das Diagramm wird keine Legende angezeigt.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Gibt an, dass die Legende rechts vom Diagramm gezeichnet werden soll.

### TOP {#TOP}
```
public static int TOP
```


Gibt an, dass die Legende oben im Diagramm gezeichnet werden soll.

### TOP_RIGHT {#TOP-RIGHT}
```
public static int TOP_RIGHT
```


Gibt an, dass die Legende oben rechts im Diagramm gezeichnet werden soll.

### length {#length}
```
public static int length
```


### fromName(String legendPositionName) {#fromName-java.lang.String}
```
public static int fromName(String legendPositionName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| legendPositionName | java.lang.String |  |

**Returns:**
int
### getName(int legendPosition) {#getName-int}
```
public static String getName(int legendPosition)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| legendPosition | int |  |

**Returns:**
java.lang.String
