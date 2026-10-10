---
title: "ChartMarker"
linktitle: "ChartMarker"
second_title: "Aspose.Words für Java"
description: "Stellt einen Diagrammdatenmarker in Java dar."
type: docs
weight: 82
url: /de/java/com.aspose.words/chartmarker/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class ChartMarker implements Cloneable
```

Stellt einen Diagrammdatenmarker dar.

Weitere Informationen finden Sie im Dokumentationsartikel zu [ Working with Charts ][Working with Charts].

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


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getFormat()](#getFormat) | Bietet Zugriff auf die Füll- und Linienformatierung dieses Markers. |
| [getShapeType()](#getShapeType) |  |
| [getSize()](#getSize) | Liefert die Größe des Diagrammmarkers. |
| [getSymbol()](#getSymbol) | Liefert das Symbol des Diagrammmarkers. |
| [isFillSupported()](#isFillSupported) |  |
| [isFormatDefined()](#isFormatDefined) |  |
| [materializeSpPr()](#materializeSpPr) |  |
| [setShapeType(int value)](#setShapeType-int) |  |
| [setSize(int value)](#setSize-int) | Legt die Größe des Diagrammmarkers fest. |
| [setSymbol(int value)](#setSymbol-int) | Legt das Symbol des Diagrammmarkers fest. |
### getFormat() {#getFormat}
```
public ChartFormat getFormat()
```


Bietet Zugriff auf die Füll- und Linienformatierung dieses Markers.

 **Examples:** 

Zeigt, wie man das Marker‑Format festlegt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.SCATTER, 432.0, 252.0);
 Chart chart = shape.getChart();

 // Delete default generated series.
 chart.getSeries().clear();
 ChartSeries series = chart.getSeries().add("AW Series 1", new double[] { 0.7, 1.8, 2.6, 3.9 },
         new double[] { 2.7, 3.2, 0.8, 1.7 });

 // Set marker formatting.
 series.getMarker().setSize(40);
 series.getMarker().setSymbol(MarkerSymbol.SQUARE);
 ChartDataPointCollection dataPoints = series.getDataPoints();
 dataPoints.get(0).getMarker().getFormat().getFill().presetTextured(PresetTexture.DENIM);
 dataPoints.get(0).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(0).getMarker().getFormat().getStroke().setBackColor(Color.RED);
 dataPoints.get(1).getMarker().getFormat().getFill().presetTextured(PresetTexture.WATER_DROPLETS);
 dataPoints.get(1).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(1).getMarker().getFormat().getStroke().setVisible(false);
 dataPoints.get(2).getMarker().getFormat().getFill().presetTextured(PresetTexture.GREEN_MARBLE);
 dataPoints.get(2).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(3).getMarker().getFormat().getFill().presetTextured(PresetTexture.OAK);
 dataPoints.get(3).getMarker().getFormat().getStroke().setForeColor(Color.YELLOW);
 dataPoints.get(3).getMarker().getFormat().getStroke().setTransparency(0.5);

 doc.save(getArtifactsDir() + "Charts.MarkerFormatting.docx");
 
```

**Returns:**
[ChartFormat](../../com.aspose.words/chartformat/) - The corresponding [ChartFormat](../../com.aspose.words/chartformat/) value.
### getShapeType() {#getShapeType}
```
public int getShapeType()
```




**Returns:**
int
### getSize() {#getSize}
```
public int getSize()
```


Liefert die Größe des Diagrammmarkers. Standardwert ist 7.

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

**Returns:**
int - Größe des Diagrammmarkers.
### getSymbol() {#getSymbol}
```
public int getSymbol()
```


Liefert das Symbol des Diagrammmarkers.

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

**Returns:**
int - Diagrammmarker-Symbol. Der zurückgegebene Wert ist einer der [MarkerSymbol](../../com.aspose.words/markersymbol/) Konstanten.
### isFillSupported() {#isFillSupported}
```
public boolean isFillSupported()
```




**Returns:**
boolean
### isFormatDefined() {#isFormatDefined}
```
public boolean isFormatDefined()
```




**Returns:**
boolean
### materializeSpPr() {#materializeSpPr}
```
public void materializeSpPr()
```




### setShapeType(int value) {#setShapeType-int}
```
public void setShapeType(int value)
```




**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int |  |

### setSize(int value) {#setSize-int}
```
public void setSize(int value)
```


Legt die Größe des Diagrammmarkers fest. Standardwert ist 7.

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

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Diagramm-Markergröße. |

### setSymbol(int value) {#setSymbol-int}
```
public void setSymbol(int value)
```


Legt das Symbol des Diagrammmarkers fest.

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

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| value | int | Diagramm-Markersymbol. Der Wert muss einer der [MarkerSymbol](../../com.aspose.words/markersymbol/) Konstanten sein. |

