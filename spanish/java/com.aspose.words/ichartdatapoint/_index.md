---
title: "IChartDataPoint"
linktitle: "IChartDataPoint"
second_title: "Aspose.Words para Java"
description: "Contiene propiedades de un único punto de datos en el gráfico en Java."
type: docs
weight: 754
url: /es/java/com.aspose.words/ichartdatapoint/
---
```
public interface IChartDataPoint
```

Contiene propiedades de un único punto de datos en el gráfico.

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
## Métodos

| Método | Descripción |
| --- | --- |
| [getBubble3D()](#getBubble3D) | Especifica si las burbujas en el gráfico de burbujas deben tener un efecto 3D aplicado. |
| [getExplosion()](#getExplosion) | Especifica la cantidad que el punto de datos debe desplazarse desde el centro del pastel. |
| [getInvertIfNegative()](#getInvertIfNegative) | Especifica si el elemento padre debe invertir sus colores cuando el valor es negativo. |
| [getMarker()](#getMarker) | Especifica un marcador de datos. |
| [setBubble3D(boolean value)](#setBubble3D-boolean) | Especifica si las burbujas en el gráfico de burbujas deben tener un efecto 3D aplicado. |
| [setExplosion(int value)](#setExplosion-int) | Especifica la cantidad que el punto de datos debe desplazarse desde el centro del pastel. |
| [setInvertIfNegative(boolean value)](#setInvertIfNegative-boolean) | Especifica si el elemento padre debe invertir sus colores cuando el valor es negativo. |
### getBubble3D() {#getBubble3D}
```
public abstract boolean getBubble3D()
```


Especifica si las burbujas en el gráfico de burbujas deben tener un efecto 3D aplicado.

 **Examples:** 

Muestra cómo usar efectos 3D con gráficos de burbujas.

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
boolean - El valor  boolean  correspondiente.
### getExplosion() {#getExplosion}
```
public abstract int getExplosion()
```


Especifica la cantidad que el punto de datos debe moverse desde el centro del pastel. Puede ser negativo; un valor negativo indica que la propiedad no está establecida y no se debe aplicar explosión. Se aplica solo a gráficos de pastel.

 **Examples:** 

Muestra cómo mover las porciones de un gráfico circular alejándolas del centro.

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
int - El valor  int  correspondiente.
### getInvertIfNegative() {#getInvertIfNegative}
```
public abstract boolean getInvertIfNegative()
```


Especifica si el elemento padre debe invertir sus colores cuando el valor es negativo.

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

**Returns:**
boolean - El valor  boolean  correspondiente.
### getMarker() {#getMarker}
```
public abstract ChartMarker getMarker()
```


Especifica un marcador de datos. El marcador se crea automáticamente cuando se solicita.

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

**Returns:**
[ChartMarker](../../com.aspose.words/chartmarker/) - The corresponding [ChartMarker](../../com.aspose.words/chartmarker/) value.
### setBubble3D(boolean value) {#setBubble3D-boolean}
```
public abstract void setBubble3D(boolean value)
```


Especifica si las burbujas en el gráfico de burbujas deben tener un efecto 3D aplicado.

 **Examples:** 

Muestra cómo usar efectos 3D con gráficos de burbujas.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

### setExplosion(int value) {#setExplosion-int}
```
public abstract void setExplosion(int value)
```


Especifica la cantidad que el punto de datos debe moverse desde el centro del pastel. Puede ser negativo; un valor negativo indica que la propiedad no está establecida y no se debe aplicar explosión. Se aplica solo a gráficos de pastel.

 **Examples:** 

Muestra cómo mover las porciones de un gráfico circular alejándolas del centro.

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
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | int | El valor  int  correspondiente. |

### setInvertIfNegative(boolean value) {#setInvertIfNegative-boolean}
```
public abstract void setInvertIfNegative(boolean value)
```


Especifica si el elemento padre debe invertir sus colores cuando el valor es negativo.

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

**Parameters:**
| Parámetro | Tipo | Descripción |
| --- | --- | --- |
| valor | boolean | El valor  boolean  correspondiente. |

