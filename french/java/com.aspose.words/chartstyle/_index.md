---
title: "ChartStyle"
linktitle: "ChartStyle"
second_title: "Aspose.Words pour Java"
description: "Spécifie les styles prédéfinis d'un graphique en Java."
type: docs
weight: 91
url: /fr/java/com.aspose.words/chartstyle/
---

**Inheritance:**
java.lang.Object
```
public class ChartStyle
```

Spécifie les styles prédéfinis d'un graphique.

 **Examples:** 

Montre comment définir et obtenir le style du graphique.

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
## Champs

| Champ | Description |
| --- | --- |
| [BLACK](#BLACK) | Un style avec un arrière-plan de graphique noir. |
| [BLUE](#BLUE) | Un style avec un arrière-plan de graphique bleu. |
| [FLAT](#FLAT) | Un style avec des points de données plats sans dégradé. |
| [GRADIENT](#GRADIENT) | Un style avec un remplissage en dégradé des points de données. |
| [GREY](#GREY) | Un style avec un arrière-plan de graphique en dégradé gris. |
| [MUTED](#MUTED) | Un style avec des couleurs atténuées. |
| [NORMAL](#NORMAL) | Représente le style de graphique par défaut. |
| [ORIGINAL](#ORIGINAL) | Un style avec une apparence originale d'un graphique. |
| [OUTLINE](#OUTLINE) | Un style avec des points de données sans remplissage, mais uniquement un contour. |
| [OUTLINE_BLACK](#OUTLINE-BLACK) | Un style avec un arrière-plan de graphique noir, dans lequel les points de données n'ont pas de remplissage, mais uniquement un contour. |
| [SATURATED](#SATURATED) | Un style avec des couleurs plus saturées. |
| [SHADED](#SHADED) | Un style avec des points de données ombrés. |
| [SHADED_PLOT](#SHADED-PLOT) | Un style, dans lequel la zone du tracé est ombrée. |
| [SHADOWED](#SHADOWED) | Un style avec des points de données ayant une ombre. |
| [TRANSPARENT_1](#TRANSPARENT-1) | Un style avec des points de données transparents. |
| [TRANSPARENT_2](#TRANSPARENT-2) | Un style avec des points de données transparents. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String chartStyleName)](#fromName-java.lang.String) |  |
| [getName(int chartStyle)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartStyle)](#toString-int) |  |
### BLACK {#BLACK}
```
public static int BLACK
```


Un style avec un arrière-plan de graphique noir.

### BLUE {#BLUE}
```
public static int BLUE
```


Un style avec un arrière-plan de graphique bleu.

### FLAT {#FLAT}
```
public static int FLAT
```


Un style avec des points de données plats sans dégradé.

### GRADIENT {#GRADIENT}
```
public static int GRADIENT
```


Un style avec un remplissage en dégradé des points de données.

### GREY {#GREY}
```
public static int GREY
```


Un style avec un arrière-plan de graphique en dégradé gris.

### MUTED {#MUTED}
```
public static int MUTED
```


Un style avec des couleurs atténuées.

### NORMAL {#NORMAL}
```
public static int NORMAL
```


Représente le style de graphique par défaut.

### ORIGINAL {#ORIGINAL}
```
public static int ORIGINAL
```


Un style avec une apparence originale d'un graphique.

### OUTLINE {#OUTLINE}
```
public static int OUTLINE
```


Un style avec des points de données sans remplissage, mais uniquement un contour.

### OUTLINE_BLACK {#OUTLINE-BLACK}
```
public static int OUTLINE_BLACK
```


Un style avec un arrière-plan de graphique noir, dans lequel les points de données n'ont pas de remplissage, mais uniquement un contour.

### SATURATED {#SATURATED}
```
public static int SATURATED
```


Un style avec des couleurs plus saturées.

### SHADED {#SHADED}
```
public static int SHADED
```


Un style avec des points de données ombrés.

### SHADED_PLOT {#SHADED-PLOT}
```
public static int SHADED_PLOT
```


Un style, dans lequel la zone du tracé est ombrée.

### SHADOWED {#SHADOWED}
```
public static int SHADOWED
```


Un style avec des points de données ayant une ombre.

### TRANSPARENT_1 {#TRANSPARENT-1}
```
public static int TRANSPARENT_1
```


Un style avec des points de données transparents.

### TRANSPARENT_2 {#TRANSPARENT-2}
```
public static int TRANSPARENT_2
```


Un style avec des points de données transparents.

### length {#length}
```
public static int length
```


### fromName(String chartStyleName) {#fromName-java.lang.String}
```
public static int fromName(String chartStyleName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| chartStyleName | java.lang.String |  |

**Returns:**
int
### getName(int chartStyle) {#getName-int}
```
public static String getName(int chartStyle)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| chartStyle | int |  |

**Returns:**
java.lang.String
