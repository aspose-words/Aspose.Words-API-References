---
title: "ChartDataPointCollection"
linktitle: "ChartDataPointCollection"
second_title: "Aspose.Words per Java"
description: "Rappresenta una collezione di un ChartDataPoint in Java."
type: docs
weight: 76
url: /it/java/com.aspose.words/chartdatapointcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartDataPointCollection implements Iterable
```

Rappresenta una collezione di un [ChartDataPoint](../../com.aspose.words/chartdatapoint/).

Per saperne di più, visita l'articolo di documentazione [ Working with Charts ][Working with Charts].

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


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## Metodi

| Metodo | Descrizione |
| --- | --- |
| [clearFormat()](#clearFormat) | Cancella il formato di tutti i [ChartDataPoint](../../com.aspose.words/chartdatapoint/) in questa collezione. |
| [copyFormat(int sourceIndex, int destinationIndex)](#copyFormat-int-int) | Copia il formato dal punto dati di origine al punto dati di destinazione. |
| [get(int index)](#get-int) | Restituisce [ChartDataPoint](../../com.aspose.words/chartdatapoint/) per l'indice specificato. |
| [getCount()](#getCount) | Restituisce il numero di [ChartDataPoint](../../com.aspose.words/chartdatapoint/) in questa collezione. |
| [hasDefaultFormat(int dataPointIndex)](#hasDefaultFormat-int) | Ottiene un flag che indica se il punto dati all'indice specificato ha il formato predefinito. |
| [iterator()](#iterator) | Restituisce un oggetto enumeratore. |
### clearFormat() {#clearFormat}
```
public void clearFormat()
```


Cancella il formato di tutti i [ChartDataPoint](../../com.aspose.words/chartdatapoint/) in questa collezione.

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

### copyFormat(int sourceIndex, int destinationIndex) {#copyFormat-int-int}
```
public void copyFormat(int sourceIndex, int destinationIndex)
```


Copia il formato dal punto dati di origine al punto dati di destinazione.

 **Examples:** 

Mostra come copiare il formato del punto dati.

```

 Document doc = new Document(getMyDir() + "DataPoint format.docx");

 // Get the chart and series to update format.
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ChartSeries series = shape.getChart().getSeries().get(0);
 ChartDataPointCollection dataPoints = series.getDataPoints();

 Assert.assertTrue(dataPoints.hasDefaultFormat(0));
 Assert.assertFalse(dataPoints.hasDefaultFormat(1));

 // Copy format of the data point with index 1 to the data point with index 2
 // so that the data point 2 looks the same as the data point 1.
 dataPoints.copyFormat(0, 1);

 Assert.assertTrue(dataPoints.hasDefaultFormat(0));
 Assert.assertTrue(dataPoints.hasDefaultFormat(1));

 // Copy format of the data point with index 0 to the series defaults so that all data points
 // in the series that have the default format look the same as the data point 0.
 series.copyFormatFrom(1);

 Assert.assertTrue(dataPoints.hasDefaultFormat(0));
 Assert.assertTrue(dataPoints.hasDefaultFormat(1));

 doc.save(getArtifactsDir() + "Charts.CopyDataPointFormat.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| sourceIndex | int |  |
| destinationIndex | int |  |

### get(int index) {#get-int}
```
public ChartDataPoint get(int index)
```


Restituisce [ChartDataPoint](../../com.aspose.words/chartdatapoint/) per l'indice specificato.

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

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| indice | int |  |

**Returns:**
[ChartDataPoint](../../com.aspose.words/chartdatapoint/) - [ChartDataPoint](../../com.aspose.words/chartdatapoint/) for the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Restituisce il numero di [ChartDataPoint](../../com.aspose.words/chartdatapoint/) in questa collezione.

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

**Returns:**
int - Il numero di [ChartDataPoint](../../com.aspose.words/chartdatapoint/) in questa collezione.
### hasDefaultFormat(int dataPointIndex) {#hasDefaultFormat-int}
```
public boolean hasDefaultFormat(int dataPointIndex)
```


Ottiene un flag che indica se il punto dati all'indice specificato ha il formato predefinito.

 **Examples:** 

Mostra come copiare il formato del punto dati.

```

 Document doc = new Document(getMyDir() + "DataPoint format.docx");

 // Get the chart and series to update format.
 Shape shape = (Shape)doc.getChild(NodeType.SHAPE, 0, true);
 ChartSeries series = shape.getChart().getSeries().get(0);
 ChartDataPointCollection dataPoints = series.getDataPoints();

 Assert.assertTrue(dataPoints.hasDefaultFormat(0));
 Assert.assertFalse(dataPoints.hasDefaultFormat(1));

 // Copy format of the data point with index 1 to the data point with index 2
 // so that the data point 2 looks the same as the data point 1.
 dataPoints.copyFormat(0, 1);

 Assert.assertTrue(dataPoints.hasDefaultFormat(0));
 Assert.assertTrue(dataPoints.hasDefaultFormat(1));

 // Copy format of the data point with index 0 to the series defaults so that all data points
 // in the series that have the default format look the same as the data point 0.
 series.copyFormatFrom(1);

 Assert.assertTrue(dataPoints.hasDefaultFormat(0));
 Assert.assertTrue(dataPoints.hasDefaultFormat(1));

 doc.save(getArtifactsDir() + "Charts.CopyDataPointFormat.docx");
 
```

**Parameters:**
| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| dataPointIndex | int |  |

**Returns:**
boolean
### iterator() {#iterator}
```
public Iterator iterator()
```


Restituisce un oggetto enumeratore.

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

**Returns:**
java.util.Iterator
