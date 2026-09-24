---
title: "MarkerSymbol"
linktitle: "MarkerSymbol"
second_title: "Aspose.Words Java için"
description: "Java'da işaretçi sembol stilini belirtir."
type: docs
weight: 457
url: /tr/java/com.aspose.words/markersymbol/
---

**Inheritance:**
java.lang.Object
```
public class MarkerSymbol
```

İşaretçi sembol stilini belirtir.

 **Examples:** 

Çizgi grafiğindeki veri noktalarıyla nasıl çalışılacağını gösterir.

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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [CIRCLE](#CIRCLE) | Her veri noktasında bir daire çizileceğini belirtir. |
| [DASH](#DASH) | Her veri noktasında bir tire çizileceğini belirtir. |
| [DEFAULT](#DEFAULT) | Her veri noktasında varsayılan işaretçi simgesi çizileceğini belirtir. |
| [DIAMOND](#DIAMOND) | Her veri noktasında bir elmas çizileceğini belirtir. |
| [DOT](#DOT) | Her veri noktasında bir nokta çizileceğini belirtir. |
| [NONE](#NONE) | Her veri noktasında hiçbir şey çizilmeyeceğini belirtir. |
| [PICTURE](#PICTURE) | Her veri noktasında bir resim çizileceğini belirtir. |
| [PLUS](#PLUS) | Her veri noktasında bir artı işareti çizileceğini belirtir. |
| [SQUARE](#SQUARE) | Her veri noktasında bir kare çizileceğini belirtir. |
| [STAR](#STAR) | Her veri noktasında bir yıldız çizileceğini belirtir. |
| [TRIANGLE](#TRIANGLE) | Her veri noktasında bir üçgen çizileceğini belirtir. |
| [X](#X) | Her veri noktasında bir X çizileceğini belirtir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String markerSymbolName)](#fromName-java.lang.String) |  |
| [getName(int markerSymbol)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markerSymbol)](#toString-int) |  |
### CIRCLE {#CIRCLE}
```
public static int CIRCLE
```


Her veri noktasında bir daire çizileceğini belirtir.

### DASH {#DASH}
```
public static int DASH
```


Her veri noktasında bir tire çizileceğini belirtir.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


Her veri noktasında varsayılan işaretçi simgesi çizileceğini belirtir.

### DIAMOND {#DIAMOND}
```
public static int DIAMOND
```


Her veri noktasında bir elmas çizileceğini belirtir.

### DOT {#DOT}
```
public static int DOT
```


Her veri noktasında bir nokta çizileceğini belirtir.

### NONE {#NONE}
```
public static int NONE
```


Her veri noktasında hiçbir şey çizilmeyeceğini belirtir.

### PICTURE {#PICTURE}
```
public static int PICTURE
```


Her veri noktasında bir resim çizileceğini belirtir.

### PLUS {#PLUS}
```
public static int PLUS
```


Her veri noktasında bir artı işareti çizileceğini belirtir.

### SQUARE {#SQUARE}
```
public static int SQUARE
```


Her veri noktasında bir kare çizileceğini belirtir.

### STAR {#STAR}
```
public static int STAR
```


Her veri noktasında bir yıldız çizileceğini belirtir.

### TRIANGLE {#TRIANGLE}
```
public static int TRIANGLE
```


Her veri noktasında bir üçgen çizileceğini belirtir.

### X {#X}
```
public static int X
```


Her veri noktasında bir X çizileceğini belirtir.

### length {#length}
```
public static int length
```


### fromName(String markerSymbolName) {#fromName-java.lang.String}
```
public static int fromName(String markerSymbolName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| markerSymbolName | java.lang.String |  |

**Returns:**
int
### getName(int markerSymbol) {#getName-int}
```
public static String getName(int markerSymbol)
```




**Parameters:**
| Parametre | Tür | Açıklama |
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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| markerSymbol | int |  |

**Returns:**
java.lang.String
