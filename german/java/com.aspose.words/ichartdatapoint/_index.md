---
title: "IChartDataPoint"
linktitle: "IChartDataPoint"
second_title: "Aspose.Words für Java"
description: "Enthält Eigenschaften eines einzelnen Datenpunkts im Diagramm in Java."
type: docs
weight: 754
url: /de/java/com.aspose.words/ichartdatapoint/
---
```
public interface IChartDataPoint
```

Enthält Eigenschaften eines einzelnen Datenpunkts im Diagramm.

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
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getBubble3D()](#getBubble3D) | Gibt an, ob die Blasen im Blasendiagramm einen 3‑D‑Effekt erhalten sollen. |
| [getExplosion()](#getExplosion) | Gibt an, um welchen Betrag der Datenpunkt vom Mittelpunkt des Kuchendiagramms verschoben werden soll. |
| [getInvertIfNegative()](#getInvertIfNegative) | Gibt an, ob das übergeordnete Element seine Farben invertiert, wenn der Wert negativ ist. |
| [getMarker()](#getMarker) | Gibt einen Datenmarker an. |
| [setBubble3D(boolean value)](#setBubble3D-boolean) | Gibt an, ob die Blasen im Blasendiagramm einen 3‑D‑Effekt erhalten sollen. |
| [setExplosion(int value)](#setExplosion-int) | Gibt an, um welchen Betrag der Datenpunkt vom Mittelpunkt des Kuchendiagramms verschoben werden soll. |
| [setInvertIfNegative(boolean value)](#setInvertIfNegative-boolean) | Gibt an, ob das übergeordnete Element seine Farben invertiert, wenn der Wert negativ ist. |
### getBubble3D() {#getBubble3D}
```
public abstract boolean getBubble3D()
```


Gibt an, ob die Blasen im Blasendiagramm einen 3‑D‑Effekt erhalten sollen.

 **Examples:** 

Zeigt, wie man 3D‑Effekte mit Blasendiagrammen verwendet.

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
boolean - Der entsprechende  boolean  Wert.
### getExplosion() {#getExplosion}
```
public abstract int getExplosion()
```


Gibt an, um welchen Betrag der Datenpunkt vom Mittelpunkt des Kuchendiagramms verschoben werden soll. Kann negativ sein; ein negativer Wert bedeutet, dass die Eigenschaft nicht gesetzt ist und keine Explosion angewendet wird. Gilt nur für Kuchendiagramme.

 **Examples:** 

Zeigt, wie man die Segmente eines Kreisdiagramms vom Mittelpunkt entfernt.

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
int - Der entsprechende int-Wert.
### getInvertIfNegative() {#getInvertIfNegative}
```
public abstract boolean getInvertIfNegative()
```


Gibt an, ob das übergeordnete Element seine Farben invertiert, wenn der Wert negativ ist.

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
boolean - Der entsprechende  boolean  Wert.
### getMarker() {#getMarker}
```
public abstract ChartMarker getMarker()
```


Gibt einen Datenmarker an. Der Marker wird bei Bedarf automatisch erstellt.

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
[ChartMarker](../../com.aspose.words/chartmarker/) - The corresponding [ChartMarker](../../com.aspose.words/chartmarker/) value.
### setBubble3D(boolean value) {#setBubble3D-boolean}
```
public abstract void setBubble3D(boolean value)
```


Gibt an, ob die Blasen im Blasendiagramm einen 3‑D‑Effekt erhalten sollen.

 **Examples:** 

Zeigt, wie man 3D‑Effekte mit Blasendiagrammen verwendet.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Der entsprechende  boolean  Wert. |

### setExplosion(int value) {#setExplosion-int}
```
public abstract void setExplosion(int value)
```


Gibt an, um welchen Betrag der Datenpunkt vom Mittelpunkt des Kuchendiagramms verschoben werden soll. Kann negativ sein; ein negativer Wert bedeutet, dass die Eigenschaft nicht gesetzt ist und keine Explosion angewendet wird. Gilt nur für Kuchendiagramme.

 **Examples:** 

Zeigt, wie man die Segmente eines Kreisdiagramms vom Mittelpunkt entfernt.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Der entsprechende  int  Wert. |

### setInvertIfNegative(boolean value) {#setInvertIfNegative-boolean}
```
public abstract void setInvertIfNegative(boolean value)
```


Gibt an, ob das übergeordnete Element seine Farben invertiert, wenn der Wert negativ ist.

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
| Wert | boolean | Der entsprechende  boolean  Wert. |

