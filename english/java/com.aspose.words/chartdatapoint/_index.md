---
title: ChartDataPoint
linktitle: ChartDataPoint
second_title: Aspose.Words for Java
description: Allows to specify formatting of a single data point on the chart in Java.
type: docs
weight: 62
url: /java/com.aspose.words/chartdatapoint/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
[com.aspose.words.IChartDataPoint](../../com.aspose.words/ichartdatapoint/), java.lang.Cloneable
```
public class ChartDataPoint implements IChartDataPoint, Cloneable
```

Allows to specify formatting of a single data point on the chart.

To learn more, visit the [ Working with Charts ][Working with Charts] documentation article.

 **Remarks:** 

On a series, the [ChartDataPoint](../../com.aspose.words/chartdatapoint/) object is a member of the [ChartDataPointCollection](../../com.aspose.words/chartdatapointcollection/). The [ChartDataPointCollection](../../com.aspose.words/chartdatapointcollection/) contains a [ChartDataPoint](../../com.aspose.words/chartdatapoint/) object for each point.

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


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## Methods

| Method | Description |
| --- | --- |
| [clearFormat()](#clearFormat) | Clears format of this data point. |
| [getBubble3D()](#getBubble3D) | Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them. |
| [getExplosion()](#getExplosion) | Specifies the amount the data point shall be moved from the center of the pie. |
| [getFormat()](#getFormat) | Provides access to fill and line formatting of this data point. |
| [getIndex()](#getIndex) | Index of the data point this object applies formatting to. |
| [getInvertIfNegative()](#getInvertIfNegative) | Specifies whether the parent element shall inverts its colors if the value is negative. |
| [getMarker()](#getMarker) | Specifies chart data marker. |
| [getShapeType()](#getShapeType) |  |
| [materializeSpPr()](#materializeSpPr) |  |
| [setBubble3D(boolean value)](#setBubble3D-boolean) | Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them. |
| [setExplosion(int value)](#setExplosion-int) | Specifies the amount the data point shall be moved from the center of the pie. |
| [setInvertIfNegative(boolean value)](#setInvertIfNegative-boolean) | Specifies whether the parent element shall inverts its colors if the value is negative. |
| [setShapeType(int value)](#setShapeType-int) |  |
### clearFormat() {#clearFormat}
```
public void clearFormat()
```


Clears format of this data point. The properties are set to the default values defined in the parent series.

### getBubble3D() {#getBubble3D}
```
public boolean getBubble3D()
```


Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them.

**Returns:**
boolean - The corresponding  boolean  value.
### getExplosion() {#getExplosion}
```
public int getExplosion()
```


Specifies the amount the data point shall be moved from the center of the pie. Can be negative, negative means that property is not set and no explosion should be applied. Applies only to Pie charts.

**Returns:**
int - The corresponding  int  value.
### getFormat() {#getFormat}
```
public ChartFormat getFormat()
```


Provides access to fill and line formatting of this data point.

 **Examples:** 

Shows how to set individual formatting for categories of a column chart.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 // Delete default generated series.
 chart.getSeries().clear();

 // Adding new series.
 ChartSeries series = chart.getSeries().add("Series 1",
         new String[] { "Category 1", "Category 2", "Category 3", "Category 4" },
         new double[] { 1.0, 2.0, 3.0, 4.0 });

 // Set column formatting.
 ChartDataPointCollection dataPoints = series.getDataPoints();
 dataPoints.get(0).getFormat().getFill().presetTextured(PresetTexture.DENIM);
 dataPoints.get(1).getFormat().getFill().setForeColor(Color.RED);
 dataPoints.get(2).getFormat().getFill().setForeColor(Color.YELLOW);
 dataPoints.get(3).getFormat().getFill().setForeColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.DataPointsFormatting.docx");
 
```

**Returns:**
[ChartFormat](../../com.aspose.words/chartformat/) - The corresponding [ChartFormat](../../com.aspose.words/chartformat/) value.
### getIndex() {#getIndex}
```
public int getIndex()
```


Index of the data point this object applies formatting to.

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

**Returns:**
int - The corresponding  int  value.
### getInvertIfNegative() {#getInvertIfNegative}
```
public boolean getInvertIfNegative()
```


Specifies whether the parent element shall inverts its colors if the value is negative.

**Returns:**
boolean - The corresponding  boolean  value.
### getMarker() {#getMarker}
```
public ChartMarker getMarker()
```


Specifies chart data marker.

**Returns:**
[ChartMarker](../../com.aspose.words/chartmarker/) - The corresponding [ChartMarker](../../com.aspose.words/chartmarker/) value.
### getShapeType() {#getShapeType}
```
public int getShapeType()
```




**Returns:**
int
### materializeSpPr() {#materializeSpPr}
```
public void materializeSpPr()
```




### setBubble3D(boolean value) {#setBubble3D-boolean}
```
public void setBubble3D(boolean value)
```


Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setExplosion(int value) {#setExplosion-int}
```
public void setExplosion(int value)
```


Specifies the amount the data point shall be moved from the center of the pie. Can be negative, negative means that property is not set and no explosion should be applied. Applies only to Pie charts.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setInvertIfNegative(boolean value) {#setInvertIfNegative-boolean}
```
public void setInvertIfNegative(boolean value)
```


Specifies whether the parent element shall inverts its colors if the value is negative.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setShapeType(int value) {#setShapeType-int}
```
public void setShapeType(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

