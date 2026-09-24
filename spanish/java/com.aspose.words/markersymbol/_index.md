---
title: "MarkerSymbol"
linktitle: "MarkerSymbol"
second_title: "Aspose.Words para Java"
description: "Especifica el estilo del símbolo de marcador en Java."
type: docs
weight: 457
url: /es/java/com.aspose.words/markersymbol/
---

**Inheritance:**
java.lang.Object
```
public class MarkerSymbol
```

Especifica el estilo del símbolo del marcador.

 **Examples:** 

Muestra cómo trabajar con puntos de datos en un gráfico de líneas.

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
## Campos

| Campo | Descripción |
| --- | --- |
| [CIRCLE](#CIRCLE) | Especifica que se dibuje un círculo en cada punto de datos. |
| [DASH](#DASH) | Especifica que se dibuje un guion en cada punto de datos. |
| [DEFAULT](#DEFAULT) | Especifica que se dibuje un símbolo de marcador predeterminado en cada punto de datos. |
| [DIAMOND](#DIAMOND) | Especifica que se dibuje un diamante en cada punto de datos. |
| [DOT](#DOT) | Especifica que se dibuje un punto en cada punto de datos. |
| [NONE](#NONE) | Especifica que no se dibuje nada en cada punto de datos. |
| [PICTURE](#PICTURE) | Especifica que se dibuje una imagen en cada punto de datos. |
| [PLUS](#PLUS) | Especifica que se dibuje un signo más en cada punto de datos. |
| [SQUARE](#SQUARE) | Especifica que se dibuje un cuadrado en cada punto de datos. |
| [STAR](#STAR) | Especifica que se dibuje una estrella en cada punto de datos. |
| [TRIANGLE](#TRIANGLE) | Especifica que se dibuje un triángulo en cada punto de datos. |
| [X](#X) | Especifica que se dibuje una X en cada punto de datos. |
| [length](#length) |  |
## Métodos

| Método | Descripción |
| --- | --- |
| [fromName(String markerSymbolName)](#fromName-java.lang.String) |  |
| [getName(int markerSymbol)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markerSymbol)](#toString-int) |  |
### CIRCLE {#CIRCLE}
```
public static int CIRCLE
```


Especifica que se dibuje un círculo en cada punto de datos.

### DASH {#DASH}
```
public static int DASH
```


Especifica que se dibuje un guion en cada punto de datos.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Especifica que se dibuje un símbolo de marcador predeterminado en cada punto de datos.

### DIAMOND {#DIAMOND}
```
public static int DIAMOND
```


Especifica que se dibuje un diamante en cada punto de datos.

### DOT {#DOT}
```
public static int DOT
```


Especifica que se dibuje un punto en cada punto de datos.

### NONE {#NONE}
```
public static int NONE
```


Especifica que no se dibuje nada en cada punto de datos.

### PICTURE {#PICTURE}
```
public static int PICTURE
```


Especifica que se dibuje una imagen en cada punto de datos.

### PLUS {#PLUS}
```
public static int PLUS
```


Especifica que se dibuje un signo más en cada punto de datos.

### SQUARE {#SQUARE}
```
public static int SQUARE
```


Especifica que se dibuje un cuadrado en cada punto de datos.

### STAR {#STAR}
```
public static int STAR
```


Especifica que se dibuje una estrella en cada punto de datos.

### TRIANGLE {#TRIANGLE}
```
public static int TRIANGLE
```


Especifica que se dibuje un triángulo en cada punto de datos.

### X {#X}
```
public static int X
```


Especifica que se dibuje una X en cada punto de datos.

### length {#length}
```
public static int length
```


### fromName(String markerSymbolName) {#fromName-java.lang.String}
```
public static int fromName(String markerSymbolName)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| markerSymbolName | java.lang.String |  |

**Returns:**
int
### getName(int markerSymbol) {#getName-int}
```
public static String getName(int markerSymbol)
```




**Parameters:**
| Parámetro | Tipo | Descripción |
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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| markerSymbol | int |  |

**Returns:**
java.lang.String
