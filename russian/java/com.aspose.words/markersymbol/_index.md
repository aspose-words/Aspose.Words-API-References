---
title: "MarkerSymbol"
linktitle: "MarkerSymbol"
second_title: "Aspose.Words для Java"
description: "Указывает стиль символа маркера в Java."
type: docs
weight: 457
url: /ru/java/com.aspose.words/markersymbol/
---

**Inheritance:**
java.lang.Object
```
public class MarkerSymbol
```

Указывает стиль символа маркера.

 **Examples:** 

Показывает, как работать с точками данных на линейной диаграмме.

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
## Поля

| Поле | Описание |
| --- | --- |
| [CIRCLE](#CIRCLE) | Указывает, что на каждой точке данных будет нарисован круг. |
| [DASH](#DASH) | Указывает, что на каждой точке данных будет нарисована черта. |
| [DEFAULT](#DEFAULT) | Указывает, что на каждой точке данных будет нарисован символ маркера по умолчанию. |
| [DIAMOND](#DIAMOND) | Указывает, что на каждой точке данных будет нарисован ромб. |
| [DOT](#DOT) | Указывает, что на каждой точке данных будет нарисована точка. |
| [NONE](#NONE) | Указывает, что на каждой точке данных ничего не будет нарисовано. |
| [PICTURE](#PICTURE) | Указывает, что на каждой точке данных будет нарисовано изображение. |
| [PLUS](#PLUS) | Указывает, что на каждой точке данных будет нарисован плюс. |
| [SQUARE](#SQUARE) | Указывает, что на каждой точке данных будет нарисован квадрат. |
| [STAR](#STAR) | Указывает, что на каждой точке данных будет нарисована звезда. |
| [TRIANGLE](#TRIANGLE) | Указывает, что на каждой точке данных будет нарисован треугольник. |
| [X](#X) | Указывает, что на каждой точке данных будет нарисована буква X. |
| [length](#length) |  |
## Методы

| Метод | Описание |
| --- | --- |
| [fromName(String markerSymbolName)](#fromName-java.lang.String) |  |
| [getName(int markerSymbol)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markerSymbol)](#toString-int) |  |
### CIRCLE {#CIRCLE}
```
public static int CIRCLE
```


Указывает, что на каждой точке данных будет нарисован круг.

### DASH {#DASH}
```
public static int DASH
```


Указывает, что на каждой точке данных будет нарисована черта.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Указывает, что на каждой точке данных будет нарисован символ маркера по умолчанию.

### DIAMOND {#DIAMOND}
```
public static int DIAMOND
```


Указывает, что на каждой точке данных будет нарисован ромб.

### DOT {#DOT}
```
public static int DOT
```


Указывает, что на каждой точке данных будет нарисована точка.

### NONE {#NONE}
```
public static int NONE
```


Указывает, что на каждой точке данных ничего не будет нарисовано.

### PICTURE {#PICTURE}
```
public static int PICTURE
```


Указывает, что на каждой точке данных будет нарисовано изображение.

### PLUS {#PLUS}
```
public static int PLUS
```


Указывает, что на каждой точке данных будет нарисован плюс.

### SQUARE {#SQUARE}
```
public static int SQUARE
```


Указывает, что на каждой точке данных будет нарисован квадрат.

### STAR {#STAR}
```
public static int STAR
```


Указывает, что на каждой точке данных будет нарисована звезда.

### TRIANGLE {#TRIANGLE}
```
public static int TRIANGLE
```


Указывает, что на каждой точке данных будет нарисован треугольник.

### X {#X}
```
public static int X
```


Указывает, что на каждой точке данных будет нарисована буква X.

### length {#length}
```
public static int length
```


### fromName(String markerSymbolName) {#fromName-java.lang.String}
```
public static int fromName(String markerSymbolName)
```




**Parameters:**
| Параметр | Тип | Описание |
| --- | --- | --- |
| markerSymbolName | java.lang.String |  |

**Returns:**
int
### getName(int markerSymbol) {#getName-int}
```
public static String getName(int markerSymbol)
```




**Parameters:**
| Параметр | Тип | Описание |
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
| Параметр | Тип | Описание |
| --- | --- | --- |
| markerSymbol | int |  |

**Returns:**
java.lang.String
