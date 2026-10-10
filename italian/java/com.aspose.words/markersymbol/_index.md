---
title: "MarkerSymbol"
linktitle: "MarkerSymbol"
second_title: "Aspose.Words per Java"
description: "Specifica lo stile del simbolo del marcatore in Java."
type: docs
weight: 457
url: /it/java/com.aspose.words/markersymbol/
---

**Inheritance:**
java.lang.Object
```
public class MarkerSymbol
```

Specifica lo stile del simbolo del marcatore.

 **Examples:** 

Mostra come lavorare con i punti dati in un grafico a linee.

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
## Campi

| Campo | Descrizione |
| --- | --- |
| [CIRCLE](#CIRCLE) | Specifica che un cerchio deve essere disegnato in ogni punto dati. |
| [DASH](#DASH) | Specifica che una linea tratteggiata deve essere disegnata in ogni punto dati. |
| [DEFAULT](#DEFAULT) | Specifica che un simbolo marcatore predefinito deve essere disegnato in ogni punto dati. |
| [DIAMOND](#DIAMOND) | Specifica che un diamante deve essere disegnato in ogni punto dati. |
| [DOT](#DOT) | Specifica che un punto deve essere disegnato in ogni punto dati. |
| [NONE](#NONE) | Specifica che nulla deve essere disegnato in ogni punto dati. |
| [PICTURE](#PICTURE) | Specifica che un'immagine deve essere disegnata in ogni punto dati. |
| [PLUS](#PLUS) | Specifica che un segno più deve essere disegnato in ogni punto dati. |
| [SQUARE](#SQUARE) | Specifica che un quadrato deve essere disegnato in ogni punto dati. |
| [STAR](#STAR) | Specifica che una stella deve essere disegnata in ogni punto dati. |
| [TRIANGLE](#TRIANGLE) | Specifica che un triangolo deve essere disegnato in ogni punto dati. |
| [X](#X) | Specifica che una X deve essere disegnata in ogni punto dati. |
| [length](#length) |  |
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [fromName(String markerSymbolName)](#fromName-java.lang.String) |  |
| [getName(int markerSymbol)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markerSymbol)](#toString-int) |  |
### CIRCLE {#CIRCLE}
```
public static int CIRCLE
```


Specifica che un cerchio deve essere disegnato in ogni punto dati.

### DASH {#DASH}
```
public static int DASH
```


Specifica che una linea tratteggiata deve essere disegnata in ogni punto dati.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Specifica che un simbolo marcatore predefinito deve essere disegnato in ogni punto dati.

### DIAMOND {#DIAMOND}
```
public static int DIAMOND
```


Specifica che un diamante deve essere disegnato in ogni punto dati.

### DOT {#DOT}
```
public static int DOT
```


Specifica che un punto deve essere disegnato in ogni punto dati.

### NONE {#NONE}
```
public static int NONE
```


Specifica che nulla deve essere disegnato in ogni punto dati.

### PICTURE {#PICTURE}
```
public static int PICTURE
```


Specifica che un'immagine deve essere disegnata in ogni punto dati.

### PLUS {#PLUS}
```
public static int PLUS
```


Specifica che un segno più deve essere disegnato in ogni punto dati.

### SQUARE {#SQUARE}
```
public static int SQUARE
```


Specifica che un quadrato deve essere disegnato in ogni punto dati.

### STAR {#STAR}
```
public static int STAR
```


Specifica che una stella deve essere disegnata in ogni punto dati.

### TRIANGLE {#TRIANGLE}
```
public static int TRIANGLE
```


Specifica che un triangolo deve essere disegnato in ogni punto dati.

### X {#X}
```
public static int X
```


Specifica che una X deve essere disegnata in ogni punto dati.

### length {#length}
```
public static int length
```


### fromName(String markerSymbolName) {#fromName-java.lang.String}
```
public static int fromName(String markerSymbolName)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| markerSymbolName | java.lang.String |  |

**Returns:**
int
### getName(int markerSymbol) {#getName-int}
```
public static String getName(int markerSymbol)
```




**Parameters:**
| Parametro | Tipo | Descrizione |
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
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| markerSymbol | int |  |

**Returns:**
java.lang.String
