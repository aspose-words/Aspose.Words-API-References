---
title: "MarkerSymbol"
linktitle: "MarkerSymbol"
second_title: "Aspose.Words pour Java"
description: "Spécifie le style du symbole de marqueur en Java."
type: docs
weight: 457
url: /fr/java/com.aspose.words/markersymbol/
---

**Inheritance:**
java.lang.Object
```
public class MarkerSymbol
```

Spécifie le style du symbole du marqueur.

 **Examples:** 

Montre comment travailler avec les points de données sur un graphique en courbes.

```

 public void chartDataPoint() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape shape = builder.insertChart(ChartType.LINE, 500.0, 350.0);
     Chart chart = shape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Emphasize the chart's data points by making them appear as diamond shapes.
     for (ChartSeries series : chart.getSeries())
         applyDataPoints(series, 4, MarkerSymbol.DIAMOND, 15);

     // Smooth out the line that represents the first data series.
     chart.getSeries().get(0).setSmooth(true);

     // Verify that data points for the first series will not invert their colors if the value is negative.
     Iterator enumerator = chart.getSeries().get(0).getDataPoints().iterator();
     while (enumerator.hasNext()) {
         Assert.assertFalse(enumerator.next().getInvertIfNegative());
     }

     ChartDataPoint dataPoint = chart.getSeries().get(1).getDataPoints().get(2);
     dataPoint.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can clear format individually.
     dataPoint.clearFormat();

     // We can also strip an entire series of data points at once.
     chart.getSeries().get(2).getDataPoints().clearFormat();

     doc.save(getArtifactsDir() + "Charts.ChartDataPoint.docx");
 }

 /// 
 /// Applies a number of data points to a series.
 /// 
 private static void applyDataPoints(ChartSeries series, int dataPointsCount, int markerSymbol, int dataPointSize) {
     for (int i = 0; i < dataPointsCount; i++) {
         ChartDataPoint point = series.getDataPoints().get(i);
         point.getMarker().setSymbol(markerSymbol);
         point.getMarker().setSize(dataPointSize);

         Assert.assertEquals(point.getIndex(), i);
     }
 }
 
```
## Champs

| Champ | Description |
| --- | --- |
| [CIRCLE](#CIRCLE) | Spécifie qu'un cercle doit être dessiné à chaque point de données. |
| [DASH](#DASH) | Spécifie qu'un tiret doit être dessiné à chaque point de données. |
| [DEFAULT](#DEFAULT) | Spécifie qu'un symbole de repère par défaut doit être dessiné à chaque point de données. |
| [DIAMOND](#DIAMOND) | Spécifie qu'un losange doit être dessiné à chaque point de données. |
| [DOT](#DOT) | Spécifie qu'un point doit être dessiné à chaque point de données. |
| [NONE](#NONE) | Spécifie qu'aucun élément ne doit être dessiné à chaque point de données. |
| [PICTURE](#PICTURE) | Spécifie qu'une image doit être dessinée à chaque point de données. |
| [PLUS](#PLUS) | Spécifie qu'un plus doit être dessiné à chaque point de données. |
| [SQUARE](#SQUARE) | Spécifie qu'un carré doit être dessiné à chaque point de données. |
| [STAR](#STAR) | Spécifie qu'une étoile doit être dessinée à chaque point de données. |
| [TRIANGLE](#TRIANGLE) | Spécifie qu'un triangle doit être dessiné à chaque point de données. |
| [X](#X) | Spécifie qu'un X doit être dessiné à chaque point de données. |
| [length](#length) |  |
## Méthodes

| Méthode | Description |
| --- | --- |
| [fromName(String markerSymbolName)](#fromName-java.lang.String) |  |
| [getName(int markerSymbol)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markerSymbol)](#toString-int) |  |
### CIRCLE {#CIRCLE}
```
public static int CIRCLE
```


Spécifie qu'un cercle doit être dessiné à chaque point de données.

### DASH {#DASH}
```
public static int DASH
```


Spécifie qu'un tiret doit être dessiné à chaque point de données.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Spécifie qu'un symbole de repère par défaut doit être dessiné à chaque point de données.

### DIAMOND {#DIAMOND}
```
public static int DIAMOND
```


Spécifie qu'un losange doit être dessiné à chaque point de données.

### DOT {#DOT}
```
public static int DOT
```


Spécifie qu'un point doit être dessiné à chaque point de données.

### NONE {#NONE}
```
public static int NONE
```


Spécifie qu'aucun élément ne doit être dessiné à chaque point de données.

### PICTURE {#PICTURE}
```
public static int PICTURE
```


Spécifie qu'une image doit être dessinée à chaque point de données.

### PLUS {#PLUS}
```
public static int PLUS
```


Spécifie qu'un plus doit être dessiné à chaque point de données.

### SQUARE {#SQUARE}
```
public static int SQUARE
```


Spécifie qu'un carré doit être dessiné à chaque point de données.

### STAR {#STAR}
```
public static int STAR
```


Spécifie qu'une étoile doit être dessinée à chaque point de données.

### TRIANGLE {#TRIANGLE}
```
public static int TRIANGLE
```


Spécifie qu'un triangle doit être dessiné à chaque point de données.

### X {#X}
```
public static int X
```


Spécifie qu'un X doit être dessiné à chaque point de données.

### length {#length}
```
public static int length
```


### fromName(String markerSymbolName) {#fromName-java.lang.String}
```
public static int fromName(String markerSymbolName)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| markerSymbolName | java.lang.String |  |

**Returns:**
int
### getName(int markerSymbol) {#getName-int}
```
public static String getName(int markerSymbol)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| markerSymbol | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int markerSymbol) {#toString-int}
```
public static String toString(int markerSymbol)
```




**Parameters:**
| Paramètre | Type | Description |
| --- | --- | --- |
| markerSymbol | int |  |

**Returns:**
java.lang.String
