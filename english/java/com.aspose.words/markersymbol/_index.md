---
title: MarkerSymbol
linktitle: MarkerSymbol
second_title: Aspose.Words for Java
description: Specifies marker symbol style in Java.
type: docs
weight: 406
url: /java/com.aspose.words/markersymbol/
---

**Inheritance:**
java.lang.Object
```
public class MarkerSymbol
```

Specifies marker symbol style.

 **Examples:** 

Shows how to work with data points on a line chart.

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

     // For a cleaner looking graph, we can clear format individually.
     chart.getSeries().get(1).getDataPoints().get(2).clearFormat();

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
## Fields

| Field | Description |
| --- | --- |
| [CIRCLE](#CIRCLE) | Specifies a circle shall be drawn at each data point. |
| [DASH](#DASH) | Specifies a dash shall be drawn at each data point. |
| [DEFAULT](#DEFAULT) | Specifies a default marker symbol shall be drawn at each data point. |
| [DIAMOND](#DIAMOND) | Specifies a diamond shall be drawn at each data point. |
| [DOT](#DOT) | Specifies a dot shall be drawn at each data point. |
| [NONE](#NONE) | Specifies nothing shall be drawn at each data point. |
| [PICTURE](#PICTURE) | Specifies a picture shall be drawn at each data point. |
| [PLUS](#PLUS) | Specifies a plus shall be drawn at each data point. |
| [SQUARE](#SQUARE) | Specifies a square shall be drawn at each data point. |
| [STAR](#STAR) | Specifies a star shall be drawn at each data point. |
| [TRIANGLE](#TRIANGLE) | Specifies a triangle shall be drawn at each data point. |
| [X](#X) | Specifies an X shall be drawn at each data point. |
| [length](#length) |  |
## Methods

| Method | Description |
| --- | --- |
| [fromName(String markerSymbolName)](#fromName-java.lang.String) |  |
| [getName(int markerSymbol)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markerSymbol)](#toString-int) |  |
### CIRCLE {#CIRCLE}
```
public static int CIRCLE
```


Specifies a circle shall be drawn at each data point.

### DASH {#DASH}
```
public static int DASH
```


Specifies a dash shall be drawn at each data point.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Specifies a default marker symbol shall be drawn at each data point.

### DIAMOND {#DIAMOND}
```
public static int DIAMOND
```


Specifies a diamond shall be drawn at each data point.

### DOT {#DOT}
```
public static int DOT
```


Specifies a dot shall be drawn at each data point.

### NONE {#NONE}
```
public static int NONE
```


Specifies nothing shall be drawn at each data point.

### PICTURE {#PICTURE}
```
public static int PICTURE
```


Specifies a picture shall be drawn at each data point.

### PLUS {#PLUS}
```
public static int PLUS
```


Specifies a plus shall be drawn at each data point.

### SQUARE {#SQUARE}
```
public static int SQUARE
```


Specifies a square shall be drawn at each data point.

### STAR {#STAR}
```
public static int STAR
```


Specifies a star shall be drawn at each data point.

### TRIANGLE {#TRIANGLE}
```
public static int TRIANGLE
```


Specifies a triangle shall be drawn at each data point.

### X {#X}
```
public static int X
```


Specifies an X shall be drawn at each data point.

### length {#length}
```
public static int length
```


### fromName(String markerSymbolName) {#fromName-java.lang.String}
```
public static int fromName(String markerSymbolName)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| markerSymbolName | java.lang.String |  |

**Returns:**
int
### getName(int markerSymbol) {#getName-int}
```
public static String getName(int markerSymbol)
```




**Parameters:**
| Parameter | Type | Description |
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
| Parameter | Type | Description |
| --- | --- | --- |
| markerSymbol | int |  |

**Returns:**
java.lang.String
