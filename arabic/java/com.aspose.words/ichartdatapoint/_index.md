---
title: "IChartDataPoint"
linktitle: "IChartDataPoint"
second_title: "Aspose.Words لـ Java"
description: "يحتوي على خصائص نقطة بيانات واحدة على المخطط في Java."
type: docs
weight: 754
url: /ar/java/com.aspose.words/ichartdatapoint/
---
```
public interface IChartDataPoint
```

يحتوي على خصائص نقطة بيانات واحدة على المخطط.

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
## الطرق

| طريقة | الوصف |
| --- | --- |
| [getBubble3D()](#getBubble3D) | يحدد ما إذا كان يجب تطبيق تأثير ثلاثي الأبعاد على الفقاعات في مخطط الفقاعات. |
| [getExplosion()](#getExplosion) | يحدد مقدار تحريك نقطة البيانات من مركز مخطط الفطيرة. |
| [getInvertIfNegative()](#getInvertIfNegative) | يحدد ما إذا كان العنصر الأب سيعكس ألوانه إذا كانت القيمة سلبية. |
| [getMarker()](#getMarker) | يحدد علامة بيانات. |
| [setBubble3D(boolean value)](#setBubble3D-boolean) | يحدد ما إذا كان يجب تطبيق تأثير ثلاثي الأبعاد على الفقاعات في مخطط الفقاعات. |
| [setExplosion(int value)](#setExplosion-int) | يحدد مقدار تحريك نقطة البيانات من مركز مخطط الفطيرة. |
| [setInvertIfNegative(boolean value)](#setInvertIfNegative-boolean) | يحدد ما إذا كان العنصر الأب سيعكس ألوانه إذا كانت القيمة سلبية. |
### getBubble3D() {#getBubble3D}
```
public abstract boolean getBubble3D()
```


يحدد ما إذا كان يجب تطبيق تأثير ثلاثي الأبعاد على الفقاعات في مخطط الفقاعات.

 **Examples:** 

يعرض كيفية استخدام تأثيرات ثلاثية الأبعاد مع مخططات الفقاعات.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.BUBBLE_3_D, 500.0, 350.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(1, chart.getSeries().getCount());
 Assert.assertEquals("Y-Values", chart.getSeries().get(0).getName());
 Assert.assertTrue(chart.getSeries().get(0).getBubble3D());

 // Apply a data label to each bubble that displays its diameter.
 for (int i = 0; i < 3; i++) {
     chart.getSeries().get(0).hasDataLabels(true);
     ChartDataLabel cdl = chart.getSeries().get(0).getDataLabels().get(i);
     chart.getSeries().get(0).getDataLabels().get(i).getFont().setSize(12.0);
     cdl.setShowBubbleSize(true);
 }

 doc.save(getArtifactsDir() + "Charts.Bubble3D.docx");
 
```

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getExplosion() {#getExplosion}
```
public abstract int getExplosion()
```


يحدد مقدار تحريك نقطة البيانات من مركز الفطيرة. يمكن أن يكون سالبًا، السالب يعني أن الخاصية غير مضبوطة ولا يجب تطبيق الانفجار. ينطبق فقط على مخططات الفطيرة.

 **Examples:** 

يعرض كيفية تحريك شرائح مخطط الدائرة بعيدًا عن المركز.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.PIE, 500.0, 350.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(1, chart.getSeries().getCount());
 Assert.assertEquals("Sales", chart.getSeries().get(0).getName());

 // "Slices" of a pie chart may be moved away from the center by a distance via the respective data point's Explosion attribute.
 // Add a data point to the first portion of the pie chart and move it away from the center by 10 points.
 // Aspose.Words create data points automatically if them does not exist.
 ChartDataPoint dataPoint = chart.getSeries().get(0).getDataPoints().get(0);
 dataPoint.setExplosion(10);

 // Displace the second portion by a greater distance.
 dataPoint = chart.getSeries().get(0).getDataPoints().get(1);
 dataPoint.setExplosion(40);

 doc.save(getArtifactsDir() + "Charts.PieChartExplosion.docx");
 
```

**Returns:**
int - القيمة المقابلة  int .
### getInvertIfNegative() {#getInvertIfNegative}
```
public abstract boolean getInvertIfNegative()
```


يحدد ما إذا كان العنصر الأب سيعكس ألوانه إذا كانت القيمة سلبية.

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

**Returns:**
boolean - القيمة المنطقية المقابلة.
### getMarker() {#getMarker}
```
public abstract ChartMarker getMarker()
```


يحدد علامة بيانات. يتم إنشاء العلامة تلقائيًا عند الطلب.

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

**Returns:**
[ChartMarker](../../com.aspose.words/chartmarker/) - The corresponding [ChartMarker](../../com.aspose.words/chartmarker/) value.
### setBubble3D(boolean value) {#setBubble3D-boolean}
```
public abstract void setBubble3D(boolean value)
```


يحدد ما إذا كان يجب تطبيق تأثير ثلاثي الأبعاد على الفقاعات في مخطط الفقاعات.

 **Examples:** 

يعرض كيفية استخدام تأثيرات ثلاثية الأبعاد مع مخططات الفقاعات.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.BUBBLE_3_D, 500.0, 350.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(1, chart.getSeries().getCount());
 Assert.assertEquals("Y-Values", chart.getSeries().get(0).getName());
 Assert.assertTrue(chart.getSeries().get(0).getBubble3D());

 // Apply a data label to each bubble that displays its diameter.
 for (int i = 0; i < 3; i++) {
     chart.getSeries().get(0).hasDataLabels(true);
     ChartDataLabel cdl = chart.getSeries().get(0).getDataLabels().get(i);
     chart.getSeries().get(0).getDataLabels().get(i).getFont().setSize(12.0);
     cdl.setShowBubbleSize(true);
 }

 doc.save(getArtifactsDir() + "Charts.Bubble3D.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

### setExplosion(int value) {#setExplosion-int}
```
public abstract void setExplosion(int value)
```


يحدد مقدار تحريك نقطة البيانات من مركز الفطيرة. يمكن أن يكون سالبًا، السالب يعني أن الخاصية غير مضبوطة ولا يجب تطبيق الانفجار. ينطبق فقط على مخططات الفطيرة.

 **Examples:** 

يعرض كيفية تحريك شرائح مخطط الدائرة بعيدًا عن المركز.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.PIE, 500.0, 350.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(1, chart.getSeries().getCount());
 Assert.assertEquals("Sales", chart.getSeries().get(0).getName());

 // "Slices" of a pie chart may be moved away from the center by a distance via the respective data point's Explosion attribute.
 // Add a data point to the first portion of the pie chart and move it away from the center by 10 points.
 // Aspose.Words create data points automatically if them does not exist.
 ChartDataPoint dataPoint = chart.getSeries().get(0).getDataPoints().get(0);
 dataPoint.setExplosion(10);

 // Displace the second portion by a greater distance.
 dataPoint = chart.getSeries().get(0).getDataPoints().get(1);
 dataPoint.setExplosion(40);

 doc.save(getArtifactsDir() + "Charts.PieChartExplosion.docx");
 
```

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | int | القيمة  int  المقابلة. |

### setInvertIfNegative(boolean value) {#setInvertIfNegative-boolean}
```
public abstract void setInvertIfNegative(boolean value)
```


يحدد ما إذا كان العنصر الأب سيعكس ألوانه إذا كانت القيمة سلبية.

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

**Parameters:**
| معامل | نوع | الوصف |
| --- | --- | --- |
| قيمة | boolean | القيمة المنطقية المقابلة. |

