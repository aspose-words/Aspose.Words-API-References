---
title: "LegendPosition"
linktitle: "LegendPosition"
second_title: "Aspose.Words pour Java"
description: "Spécifie les positions possibles pour une légende de graphique en Java."
type: docs
weight: 420
url: /fr/java/com.aspose.words/legendposition/
---

**Inheritance:**
java.lang.Object
```
public class LegendPosition
```

Spécifie les positions possibles pour la légende d'un graphique.

 **Examples:** 

Montre comment modifier l'apparence de la légende d'un graphique.

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
## Champs

| Champ | Description |
| --- | --- |
| [BOTTOM](#BOTTOM) | Spécifie que la légende doit être dessinée en bas du graphique. |
| [LEFT](#LEFT) | Spécifie que la légende doit être dessinée à gauche du graphique. |
| [NONE](#NONE) | Aucune légende ne sera affichée pour le graphique. |
| [RIGHT](#RIGHT) | Spécifie que la légende doit être dessinée à droite du graphique. |
| [TOP](#TOP) | Spécifie que la légende doit être dessinée en haut du graphique. |
| [TOP_RIGHT](#TOP-RIGHT) | Spécifie que la légende doit être dessinée en haut à droite du graphique. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String legendPositionName)](#fromName-java.lang.String) |  |
| [getName(int legendPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int legendPosition)](#toString-int) |  |
### BOTTOM {#BOTTOM}
```
public static int BOTTOM
```


Spécifie que la légende doit être dessinée en bas du graphique.

### LEFT {#LEFT}
```
public static int LEFT
```


Spécifie que la légende doit être dessinée à gauche du graphique.

### NONE {#NONE}
```
public static int NONE
```


Aucune légende ne sera affichée pour le graphique.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Spécifie que la légende doit être dessinée à droite du graphique.

### TOP {#TOP}
```
public static int TOP
```


Spécifie que la légende doit être dessinée en haut du graphique.

### TOP_RIGHT {#TOP-RIGHT}
```
public static int TOP_RIGHT
```


Spécifie que la légende doit être dessinée en haut à droite du graphique.

### length {#length}
```
public static int length
```


### fromName(String legendPositionName) {#fromName-java.lang.String}
```
public static int fromName(String legendPositionName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| legendPositionName | java.lang.String |  |

**Returns:**
int
### getName(int legendPosition) {#getName-int}
```
public static String getName(int legendPosition)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| legendPosition | int |  |

**Returns:**
java.lang.String
