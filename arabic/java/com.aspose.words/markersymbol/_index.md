---
title: "MarkerSymbol"
linktitle: "MarkerSymbol"
second_title: "Aspose.Words لـ Java"
description: "يحدد نمط رمز العلامة في Java."
type: docs
weight: 457
url: /ar/java/com.aspose.words/markersymbol/
---

**Inheritance:**
java.lang.Object
```
public class MarkerSymbol
```

يحدد نمط رمز العلامة.

 **Examples:** 

يعرض كيفية التعامل مع نقاط البيانات في مخطط خطي.

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
## الحقول

| حقل | الوصف |
| --- | --- |
| [CIRCLE](#CIRCLE) | يحدد أنه سيتم رسم دائرة عند كل نقطة بيانات. |
| [DASH](#DASH) | يحدد أنه سيتم رسم شرطة عند كل نقطة بيانات. |
| [DEFAULT](#DEFAULT) | يحدد أنه سيتم رسم رمز علامة افتراضي عند كل نقطة بيانات. |
| [DIAMOND](#DIAMOND) | يحدد أنه سيتم رسم ماسة عند كل نقطة بيانات. |
| [DOT](#DOT) | يحدد أنه سيتم رسم نقطة عند كل نقطة بيانات. |
| [NONE](#NONE) | يحدد أنه لن يتم رسم شيء عند كل نقطة بيانات. |
| [PICTURE](#PICTURE) | يحدد أنه سيتم رسم صورة عند كل نقطة بيانات. |
| [PLUS](#PLUS) | يحدد أنه سيتم رسم علامة زائد عند كل نقطة بيانات. |
| [SQUARE](#SQUARE) | يحدد أنه سيتم رسم مربع عند كل نقطة بيانات. |
| [STAR](#STAR) | يحدد أنه سيتم رسم نجمة عند كل نقطة بيانات. |
| [TRIANGLE](#TRIANGLE) | يحدد أنه سيتم رسم مثلث عند كل نقطة بيانات. |
| [X](#X) | يحدد أنه سيتم رسم X عند كل نقطة بيانات. |
| [length](#length) |  |
## الطرق

| طريقة | الوصف |
| --- | --- |
| [fromName(String markerSymbolName)](#fromName-java.lang.String) |  |
| [getName(int markerSymbol)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int markerSymbol)](#toString-int) |  |
### CIRCLE {#CIRCLE}
```
public static int CIRCLE
```


يحدد أنه سيتم رسم دائرة عند كل نقطة بيانات.

### DASH {#DASH}
```
public static int DASH
```


يحدد أنه سيتم رسم شرطة عند كل نقطة بيانات.

### DEFAULT {#DEFAULT}
```
public static int DEFAULT
```


يحدد أنه سيتم رسم رمز علامة افتراضي عند كل نقطة بيانات.

### DIAMOND {#DIAMOND}
```
public static int DIAMOND
```


يحدد أنه سيتم رسم ماسة عند كل نقطة بيانات.

### DOT {#DOT}
```
public static int DOT
```


يحدد أنه سيتم رسم نقطة عند كل نقطة بيانات.

### NONE {#NONE}
```
public static int NONE
```


يحدد أنه لن يتم رسم شيء عند كل نقطة بيانات.

### PICTURE {#PICTURE}
```
public static int PICTURE
```


يحدد أنه سيتم رسم صورة عند كل نقطة بيانات.

### PLUS {#PLUS}
```
public static int PLUS
```


يحدد أنه سيتم رسم علامة زائد عند كل نقطة بيانات.

### SQUARE {#SQUARE}
```
public static int SQUARE
```


يحدد أنه سيتم رسم مربع عند كل نقطة بيانات.

### STAR {#STAR}
```
public static int STAR
```


يحدد أنه سيتم رسم نجمة عند كل نقطة بيانات.

### TRIANGLE {#TRIANGLE}
```
public static int TRIANGLE
```


يحدد أنه سيتم رسم مثلث عند كل نقطة بيانات.

### X {#X}
```
public static int X
```


يحدد أنه سيتم رسم X عند كل نقطة بيانات.

### length {#length}
```
public static int length
```


### fromName(String markerSymbolName) {#fromName-java.lang.String}
```
public static int fromName(String markerSymbolName)
```




**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| markerSymbolName | java.lang.String |  |

**Returns:**
int
### getName(int markerSymbol) {#getName-int}
```
public static String getName(int markerSymbol)
```




**Parameters:**
| معامل | نوع | الوصف |
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
| معامل | نوع | الوصف |
| --- | --- | --- |
| markerSymbol | int |  |

**Returns:**
java.lang.String
