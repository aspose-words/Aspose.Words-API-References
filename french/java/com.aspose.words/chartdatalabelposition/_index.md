---
title: "ChartDataLabelPosition"
linktitle: "ChartDataLabelPosition"
second_title: "Aspose.Words pour Java"
description: "Spécifie la position d'une étiquette de données de graphique en Java."
type: docs
weight: 74
url: /fr/java/com.aspose.words/chartdatalabelposition/
---

**Inheritance:**
java.lang.Object
```
public class ChartDataLabelPosition
```

Spécifie la position d'une étiquette de données du graphique.

 **Remarks:** 

Tous les types de séries ne permettent pas de spécifier les positions des étiquettes. Et ceux qui le permettent ne supportent pas toutes les valeurs.

 **Examples:** 

Montre comment définir la position de l'étiquette de données.

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
## Champs

| Champ | Description |
| --- | --- |
| [ABOVE](#ABOVE) | Spécifie qu'une étiquette de données doit être affichée au-dessus d'un marqueur de données. |
| [BELOW](#BELOW) | Spécifie qu'une étiquette de données doit être affichée en dessous d'un marqueur de données. |
| [BEST_FIT](#BEST-FIT) | Spécifie qu'une étiquette de données doit être affichée à la position la plus appropriée. |
| [CENTER](#CENTER) | Spécifie qu'une étiquette de données doit être affichée centrée sur un marqueur de données. |
| [INSIDE_BASE](#INSIDE-BASE) | Spécifie qu'une étiquette de données doit être affichée à l'intérieur de la base d'un marqueur de données. |
| [INSIDE_END](#INSIDE-END) | Spécifie qu'une étiquette de données doit être affichée à l'intérieur de l'extrémité d'un marqueur de données. |
| [LEFT](#LEFT) | Spécifie qu'une étiquette de données doit être affichée à gauche d'un marqueur de données. |
| [OUTSIDE_END](#OUTSIDE-END) | Spécifie qu'une étiquette de données doit être affichée à l'extérieur de l'extrémité d'un marqueur de données. |
| [RIGHT](#RIGHT) | Spécifie qu'une étiquette de données doit être affichée à droite d'un marqueur de données. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String chartDataLabelPositionName)](#fromName-java.lang.String) |  |
| [getName(int chartDataLabelPosition)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartDataLabelPosition)](#toString-int) |  |
### ABOVE {#ABOVE}
```
public static int ABOVE
```


Spécifie qu'une étiquette de données doit être affichée au-dessus d'un marqueur de données.

### BELOW {#BELOW}
```
public static int BELOW
```


Spécifie qu'une étiquette de données doit être affichée en dessous d'un marqueur de données.

### BEST_FIT {#BEST-FIT}
```
public static int BEST_FIT
```


Spécifie qu'une étiquette de données doit être affichée à la position la plus appropriée.

### CENTER {#CENTER}
```
public static int CENTER
```


Spécifie qu'une étiquette de données doit être affichée centrée sur un marqueur de données.

### INSIDE_BASE {#INSIDE-BASE}
```
public static int INSIDE_BASE
```


Spécifie qu'une étiquette de données doit être affichée à l'intérieur de la base d'un marqueur de données.

### INSIDE_END {#INSIDE-END}
```
public static int INSIDE_END
```


Spécifie qu'une étiquette de données doit être affichée à l'intérieur de l'extrémité d'un marqueur de données.

### LEFT {#LEFT}
```
public static int LEFT
```


Spécifie qu'une étiquette de données doit être affichée à gauche d'un marqueur de données.

### OUTSIDE_END {#OUTSIDE-END}
```
public static int OUTSIDE_END
```


Spécifie qu'une étiquette de données doit être affichée à l'extérieur de l'extrémité d'un marqueur de données.

### RIGHT {#RIGHT}
```
public static int RIGHT
```


Spécifie qu'une étiquette de données doit être affichée à droite d'un marqueur de données.

### length {#length}
```
public static int length
```


### fromName(String chartDataLabelPositionName) {#fromName-java.lang.String}
```
public static int fromName(String chartDataLabelPositionName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| chartDataLabelPositionName | java.lang.String |  |

**Returns:**
int
### getName(int chartDataLabelPosition) {#getName-int}
```
public static String getName(int chartDataLabelPosition)
```




**Parameters:**
| Paramètre | Type | Description |
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
| Paramètre | Type | Description |
| --- | --- | --- |
| chartDataLabelPosition | int |  |

**Returns:**
java.lang.String
