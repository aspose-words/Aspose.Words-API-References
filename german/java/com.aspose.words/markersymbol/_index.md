---
title: "MarkerSymbol"
linktitle: "MarkerSymbol"
second_title: "Aspose.Words für Java"
description: "Gibt den Stil des Markersymbols in Java an."
type: docs
weight: 457
url: /de/java/com.aspose.words/markersymbol/
---

**Inheritance:**
java.lang.Object
```
public class MarkerSymbol
```

Gibt den Stil des Markierungssymbols an.

 **Examples:** 

Zeigt, wie man mit Datenpunkten in einem Liniendiagramm arbeitet.

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
## Felder

| Feld | Beschreibung |
| --- | --- |
| [CIRCLE](#CIRCLE) | Gibt an, dass an jedem Datenpunkt ein Kreis gezeichnet werden soll. |
| [DASH](#DASH) | Gibt an, dass an jedem Datenpunkt ein Strich gezeichnet werden soll. |
| [DEFAULT](#DEFAULT) | Gibt an, dass an jedem Datenpunkt ein Standardsymbol gezeichnet werden soll. |
| [DIAMOND](#DIAMOND) | Gibt an, dass an jedem Datenpunkt ein Diamant gezeichnet werden soll. |
| [DOT](#DOT) | Gibt an, dass an jedem Datenpunkt ein Punkt gezeichnet werden soll. |
| [NONE](#NONE) | Gibt an, dass an jedem Datenpunkt nichts gezeichnet werden soll. |
| [PICTURE](#PICTURE) | Gibt an, dass an jedem Datenpunkt ein Bild gezeichnet werden soll. |
| [PLUS](#PLUS) | Gibt an, dass an jedem Datenpunkt ein Pluszeichen gezeichnet werden soll. |
| [SQUARE](#SQUARE) | Gibt an, dass an jedem Datenpunkt ein Quadrat gezeichnet werden soll. |
| [STAR](#STAR) | Gibt an, dass an jedem Datenpunkt ein Stern gezeichnet werden soll. |
| [TRIANGLE](#TRIANGLE) | Gibt an, dass an jedem Datenpunkt ein Dreieck gezeichnet werden soll. |
| [X](#X) | Gibt an, dass ein X an jedem Datenpunkt gezeichnet werden soll. |
| [length](#length) |  |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [fromName(String markerSymbolName)](#fromName-java.lang.String) |  |
| [getName(int markerSymbol)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markerSymbol)](#toString-int) |  |
### CIRCLE {#CIRCLE}
```
public static int CIRCLE
```


Gibt an, dass an jedem Datenpunkt ein Kreis gezeichnet werden soll.

### DASH {#DASH}
```
public static int DASH
```


Gibt an, dass an jedem Datenpunkt ein Strich gezeichnet werden soll.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Gibt an, dass an jedem Datenpunkt ein Standardsymbol gezeichnet werden soll.

### DIAMOND {#DIAMOND}
```
public static int DIAMOND
```


Gibt an, dass an jedem Datenpunkt ein Diamant gezeichnet werden soll.

### DOT {#DOT}
```
public static int DOT
```


Gibt an, dass an jedem Datenpunkt ein Punkt gezeichnet werden soll.

### NONE {#NONE}
```
public static int NONE
```


Gibt an, dass an jedem Datenpunkt nichts gezeichnet werden soll.

### PICTURE {#PICTURE}
```
public static int PICTURE
```


Gibt an, dass an jedem Datenpunkt ein Bild gezeichnet werden soll.

### PLUS {#PLUS}
```
public static int PLUS
```


Gibt an, dass an jedem Datenpunkt ein Pluszeichen gezeichnet werden soll.

### SQUARE {#SQUARE}
```
public static int SQUARE
```


Gibt an, dass an jedem Datenpunkt ein Quadrat gezeichnet werden soll.

### STAR {#STAR}
```
public static int STAR
```


Gibt an, dass an jedem Datenpunkt ein Stern gezeichnet werden soll.

### TRIANGLE {#TRIANGLE}
```
public static int TRIANGLE
```


Gibt an, dass an jedem Datenpunkt ein Dreieck gezeichnet werden soll.

### X {#X}
```
public static int X
```


Gibt an, dass ein X an jedem Datenpunkt gezeichnet werden soll.

### length {#length}
```
public static int length
```


### fromName(String markerSymbolName) {#fromName-java.lang.String}
```
public static int fromName(String markerSymbolName)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| markerSymbolName | java.lang.String |  |

**Returns:**
int
### getName(int markerSymbol) {#getName-int}
```
public static String getName(int markerSymbol)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| markerSymbol | int |  |

**Returns:**
java.lang.String
