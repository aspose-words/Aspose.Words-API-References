---
title: "ChartSeries"
linktitle: "ChartSeries"
second_title: "Aspose.Words für Java"
description: "Stellt Diagrammserien-Eigenschaften in Java dar."
type: docs
weight: 85
url: /de/java/com.aspose.words/chartseries/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
[com.aspose.words.IChartDataPoint](../../com.aspose.words/ichartdatapoint/), java.lang.Cloneable
```
public class ChartSeries implements IChartDataPoint, Cloneable
```

Stellt die Eigenschaften von Diagrammserien dar.

Weitere Informationen finden Sie im Dokumentationsartikel zu [ Working with Charts ][Working with Charts].

 **Examples:** 

Zeigt, wie Beschriftungen auf Datenpunkte in einem Liniendiagramm angewendet werden.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [add(ChartXValue xValue)](#add-com.aspose.words.ChartXValue) | Fügt den angegebenen X-Wert zur Diagrammserie hinzu. |
| [add(ChartXValue xValue, ChartYValue yValue)](#add-com.aspose.words.ChartXValue-com.aspose.words.ChartYValue) | Fügt die angegebenen X- und Y-Werte zur Diagrammreihe hinzu. |
| [add(ChartXValue xValue, ChartYValue yValue, double bubbleSize)](#add-com.aspose.words.ChartXValue-com.aspose.words.ChartYValue-double) | Fügt den angegebenen X-Wert, Y-Wert und die Blasengröße zur Diagrammreihe hinzu. |
| [clear()](#clear) | Entfernt alle Datenwerte aus der Diagrammreihe. |
| [clearValues()](#clearValues) | Entfernt alle Datenwerte aus der Diagrammreihe und bewahrt dabei das Format der Datenpunkte und Datenbeschriftungen. |
| [copyFormatFrom(int dataPointIndex)](#copyFormatFrom-int) | Kopiert das Standardformat des Datenpunkts vom Datenpunkt mit dem angegebenen Index. |
| [getBubble3D()](#getBubble3D) | Gibt an, ob die Blasen im Blasendiagramm einen 3‑D‑Effekt erhalten sollen. |
| [getBubbleSizes()](#getBubbleSizes) | Ruft eine Sammlung von Blasengrößen für diese Diagrammreihe ab. |
| [getDataLabels()](#getDataLabels) | Gibt die Einstellungen für die Datenbeschriftungen der gesamten Reihe an. |
| [getDataPoints()](#getDataPoints) | Gibt eine Sammlung von Formatierungsobjekten für alle Datenpunkte in dieser Reihe zurück. |
| [getExplosion()](#getExplosion) | Gibt an, um welchen Betrag der Datenpunkt vom Mittelpunkt des Kuchendiagramms verschoben werden soll. |
| [getFormat()](#getFormat) | Stellt Zugriff auf Füll‑ und Linienformatierung der Reihe bereit. |
| [getInvertIfNegative()](#getInvertIfNegative) | Gibt an, ob das übergeordnete Element seine Farben invertiert, wenn der Wert negativ ist. |
| [getLegendEntry()](#getLegendEntry) | Ruft einen Legendeeintrag für diese Diagrammreihe ab. |
| [getMarker()](#getMarker) | Gibt einen Datenmarker an. |
| [getName()](#getName) | Ruft den Namen der Reihe ab; wenn der Name nicht explizit festgelegt ist, wird er anhand des Index generiert. |
| [getSeriesType()](#getSeriesType) | Ruft den Typ dieser Diagrammreihe ab. |
| [getSmooth()](#getSmooth) | Ermöglicht die Angabe, ob die Linie, die die Punkte im Diagramm verbindet, mithilfe von Catmull‑Rom‑Splines geglättet werden soll. |
| [getXValues()](#getXValues) | Ruft eine Sammlung von X-Werten für diese Diagrammreihe ab. |
| [getYValues()](#getYValues) | Ruft eine Sammlung von Y-Werten für diese Diagrammreihe ab. |
| [hasDataLabels()](#hasDataLabels) | Ruft ein Flag ab, das angibt, ob Datenbeschriftungen für die Reihe angezeigt werden. |
| [hasDataLabels(boolean value)](#hasDataLabels-boolean) | Setzt ein Flag, das angibt, ob Datenbeschriftungen für die Reihe angezeigt werden. |
| [insert(int index, ChartXValue xValue)](#insert-int-com.aspose.words.ChartXValue) | Fügt den angegebenen X-Wert an der angegebenen Position in die Diagrammreihe ein. |
| [insert(int index, ChartXValue xValue, ChartYValue yValue)](#insert-int-com.aspose.words.ChartXValue-com.aspose.words.ChartYValue) | Fügt die angegebenen X- und Y-Werte an der angegebenen Position in die Diagrammreihe ein. |
| [insert(int index, ChartXValue xValue, ChartYValue yValue, double bubbleSize)](#insert-int-com.aspose.words.ChartXValue-com.aspose.words.ChartYValue-double) | Fügt den angegebenen X-Wert, Y-Wert und die Blasengröße an der angegebenen Position in die Diagrammreihe ein. |
| [remove(int index)](#remove-int) | Entfernt den X-Wert, Y-Wert und die Blasengröße, falls unterstützt, aus der Diagrammreihe an der angegebenen Position. |
| [setBubble3D(boolean value)](#setBubble3D-boolean) | Gibt an, ob die Blasen im Blasendiagramm einen 3‑D‑Effekt erhalten sollen. |
| [setExplosion(int value)](#setExplosion-int) | Gibt an, um welchen Betrag der Datenpunkt vom Mittelpunkt des Kuchendiagramms verschoben werden soll. |
| [setInvertIfNegative(boolean value)](#setInvertIfNegative-boolean) | Gibt an, ob das übergeordnete Element seine Farben invertiert, wenn der Wert negativ ist. |
| [setName(String value)](#setName-java.lang.String) | Legt den Namen der Serie fest, wenn der Name nicht explizit gesetzt wird, wird er anhand des Index generiert. |
| [setSmooth(boolean value)](#setSmooth-boolean) | Ermöglicht die Angabe, ob die Linie, die die Punkte im Diagramm verbindet, mithilfe von Catmull‑Rom‑Splines geglättet werden soll. |
### add(ChartXValue xValue) {#add-com.aspose.words.ChartXValue}
```
public void add(ChartXValue xValue)
```


Fügt den angegebenen X‑Wert zur Diagrammserie hinzu. Unterstützt die Serie Y‑Werte und Blasengrößen, bleiben diese für den X‑Wert leer.

 **Examples:** 

Zeigt, wie man Diagrammserien mit Daten füllt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeries series1 = chart.getSeries().get(0);

 // Clear X and Y values of the first series.
 series1.clearValues();

 // Populate the series with data.
 series1.add(ChartXValue.fromDouble(3.0), ChartYValue.fromDouble(10.0), 10.0);
 series1.add(ChartXValue.fromDouble(5.0), ChartYValue.fromDouble(5.0));
 series1.add(ChartXValue.fromDouble(7.0), ChartYValue.fromDouble(11.0));
 series1.add(ChartXValue.fromDouble(9.0));

 ChartSeries series2 = chart.getSeries().get(1);

 // Clear X and Y values of the second series.
 series2.clear();

 // Populate the series with data.
 series2.add(ChartXValue.fromDouble(2.0), ChartYValue.fromDouble(4.0));
 series2.add(ChartXValue.fromDouble(4.0), ChartYValue.fromDouble(7.0));
 series2.add(ChartXValue.fromDouble(6.0), ChartYValue.fromDouble(14.0));
 series2.add(ChartXValue.fromDouble(8.0), ChartYValue.fromDouble(7.0));

 doc.save(getArtifactsDir() + "Charts.PopulateChartWithData.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xValue | [ChartXValue](../../com.aspose.words/chartxvalue/) |  |

### add(ChartXValue xValue, ChartYValue yValue) {#add-com.aspose.words.ChartXValue-com.aspose.words.ChartYValue}
```
public void add(ChartXValue xValue, ChartYValue yValue)
```


Fügt die angegebenen X- und Y-Werte zur Diagrammreihe hinzu.

 **Examples:** 

Zeigt, wie man Diagrammserien mit Daten füllt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeries series1 = chart.getSeries().get(0);

 // Clear X and Y values of the first series.
 series1.clearValues();

 // Populate the series with data.
 series1.add(ChartXValue.fromDouble(3.0), ChartYValue.fromDouble(10.0), 10.0);
 series1.add(ChartXValue.fromDouble(5.0), ChartYValue.fromDouble(5.0));
 series1.add(ChartXValue.fromDouble(7.0), ChartYValue.fromDouble(11.0));
 series1.add(ChartXValue.fromDouble(9.0));

 ChartSeries series2 = chart.getSeries().get(1);

 // Clear X and Y values of the second series.
 series2.clear();

 // Populate the series with data.
 series2.add(ChartXValue.fromDouble(2.0), ChartYValue.fromDouble(4.0));
 series2.add(ChartXValue.fromDouble(4.0), ChartYValue.fromDouble(7.0));
 series2.add(ChartXValue.fromDouble(6.0), ChartYValue.fromDouble(14.0));
 series2.add(ChartXValue.fromDouble(8.0), ChartYValue.fromDouble(7.0));

 doc.save(getArtifactsDir() + "Charts.PopulateChartWithData.docx");
 
```

Zeigt, wie man Diagrammdatenwerte hinzufügt/entfernt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder();

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeries department1Series = chart.getSeries().get(0);
 ChartSeries department2Series = chart.getSeries().get(1);

 // Remove the first value in the both series.
 department1Series.remove(0);
 department2Series.remove(0);

 // Add new values to the both series.
 ChartXValue newXCategory = ChartXValue.fromString("Q1, 2023");
 department1Series.add(newXCategory, ChartYValue.fromDouble(10.3));
 department2Series.add(newXCategory, ChartYValue.fromDouble(5.7));

 doc.save(getArtifactsDir() + "Charts.ChartDataValues.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xValue | [ChartXValue](../../com.aspose.words/chartxvalue/) |  |
| yValue | [ChartYValue](../../com.aspose.words/chartyvalue/) |  |

### add(ChartXValue xValue, ChartYValue yValue, double bubbleSize) {#add-com.aspose.words.ChartXValue-com.aspose.words.ChartYValue-double}
```
public void add(ChartXValue xValue, ChartYValue yValue, double bubbleSize)
```


Fügt den angegebenen X-Wert, Y-Wert und die Blasengröße zur Diagrammreihe hinzu.

 **Examples:** 

Zeigt, wie man Diagrammserien mit Daten füllt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeries series1 = chart.getSeries().get(0);

 // Clear X and Y values of the first series.
 series1.clearValues();

 // Populate the series with data.
 series1.add(ChartXValue.fromDouble(3.0), ChartYValue.fromDouble(10.0), 10.0);
 series1.add(ChartXValue.fromDouble(5.0), ChartYValue.fromDouble(5.0));
 series1.add(ChartXValue.fromDouble(7.0), ChartYValue.fromDouble(11.0));
 series1.add(ChartXValue.fromDouble(9.0));

 ChartSeries series2 = chart.getSeries().get(1);

 // Clear X and Y values of the second series.
 series2.clear();

 // Populate the series with data.
 series2.add(ChartXValue.fromDouble(2.0), ChartYValue.fromDouble(4.0));
 series2.add(ChartXValue.fromDouble(4.0), ChartYValue.fromDouble(7.0));
 series2.add(ChartXValue.fromDouble(6.0), ChartYValue.fromDouble(14.0));
 series2.add(ChartXValue.fromDouble(8.0), ChartYValue.fromDouble(7.0));

 doc.save(getArtifactsDir() + "Charts.PopulateChartWithData.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| xValue | [ChartXValue](../../com.aspose.words/chartxvalue/) |  |
| yValue | [ChartYValue](../../com.aspose.words/chartyvalue/) |  |
| bubbleSize | double |  |

### clear() {#clear}
```
public void clear()
```


Entfernt alle Datenwerte aus der Diagrammserie. Das Format aller einzelnen Datenpunkte und Datenbeschriftungen wird zurückgesetzt.

 **Examples:** 

Zeigt, wie man Diagrammserien mit Daten füllt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeries series1 = chart.getSeries().get(0);

 // Clear X and Y values of the first series.
 series1.clearValues();

 // Populate the series with data.
 series1.add(ChartXValue.fromDouble(3.0), ChartYValue.fromDouble(10.0), 10.0);
 series1.add(ChartXValue.fromDouble(5.0), ChartYValue.fromDouble(5.0));
 series1.add(ChartXValue.fromDouble(7.0), ChartYValue.fromDouble(11.0));
 series1.add(ChartXValue.fromDouble(9.0));

 ChartSeries series2 = chart.getSeries().get(1);

 // Clear X and Y values of the second series.
 series2.clear();

 // Populate the series with data.
 series2.add(ChartXValue.fromDouble(2.0), ChartYValue.fromDouble(4.0));
 series2.add(ChartXValue.fromDouble(4.0), ChartYValue.fromDouble(7.0));
 series2.add(ChartXValue.fromDouble(6.0), ChartYValue.fromDouble(14.0));
 series2.add(ChartXValue.fromDouble(8.0), ChartYValue.fromDouble(7.0));

 doc.save(getArtifactsDir() + "Charts.PopulateChartWithData.docx");
 
```

### clearValues() {#clearValues}
```
public void clearValues()
```


Entfernt alle Datenwerte aus der Diagrammreihe und bewahrt dabei das Format der Datenpunkte und Datenbeschriftungen.

 **Examples:** 

Zeigt, wie man Diagrammserien mit Daten füllt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeries series1 = chart.getSeries().get(0);

 // Clear X and Y values of the first series.
 series1.clearValues();

 // Populate the series with data.
 series1.add(ChartXValue.fromDouble(3.0), ChartYValue.fromDouble(10.0), 10.0);
 series1.add(ChartXValue.fromDouble(5.0), ChartYValue.fromDouble(5.0));
 series1.add(ChartXValue.fromDouble(7.0), ChartYValue.fromDouble(11.0));
 series1.add(ChartXValue.fromDouble(9.0));

 ChartSeries series2 = chart.getSeries().get(1);

 // Clear X and Y values of the second series.
 series2.clear();

 // Populate the series with data.
 series2.add(ChartXValue.fromDouble(2.0), ChartYValue.fromDouble(4.0));
 series2.add(ChartXValue.fromDouble(4.0), ChartYValue.fromDouble(7.0));
 series2.add(ChartXValue.fromDouble(6.0), ChartYValue.fromDouble(14.0));
 series2.add(ChartXValue.fromDouble(8.0), ChartYValue.fromDouble(7.0));

 doc.save(getArtifactsDir() + "Charts.PopulateChartWithData.docx");
 
```

### copyFormatFrom(int dataPointIndex) {#copyFormatFrom-int}
```
public void copyFormatFrom(int dataPointIndex)
```


Kopiert das Standardformat des Datenpunkts vom Datenpunkt mit dem angegebenen Index.

 **Examples:** 

Zeigt, wie man das Format von Datenpunkten kopiert.

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
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| dataPointIndex | int |  |

### getBubble3D() {#getBubble3D}
```
public boolean getBubble3D()
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
### getBubbleSizes() {#getBubbleSizes}
```
public BubbleSizeCollection getBubbleSizes()
```


Ruft eine Sammlung von Blasengrößen für diese Diagrammreihe ab.

 **Examples:** 

Zeigt, wie man mit dem Formatcode der Diagrammdaten arbeitet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a Bubble chart.
 Shape shape = builder.insertChart(ChartType.BUBBLE, 432.0, 252.0);
 Chart chart = shape.getChart();

 // Delete default generated series.
 chart.getSeries().clear();

 ChartSeries series = chart.getSeries().add(
         "Series1",
         new double[] { 1.0, 1.9, 2.45, 3.0 },
         new double[] { 1.0, -0.9, 1.82, 0.0 },
         new double[] { 2.0, 1.1, 2.95, 2.0 });

 // Show data labels.
 series.hasDataLabels(true);
 series.getDataLabels().setShowCategoryName(true);
 series.getDataLabels().setShowValue(true);
 series.getDataLabels().setShowBubbleSize(true);

 // Set data format codes.
 series.getXValues().setFormatCode("#,##0.0#");
 series.getYValues().setFormatCode("#,##0.0#;[Red]\\-#,##0.0#");
 series.getBubbleSizes().setFormatCode("#,##0.0#");

 doc.save(getArtifactsDir() + "Charts.FormatCode.docx");
 
```

**Returns:**
[BubbleSizeCollection](../../com.aspose.words/bubblesizecollection/) - A collection of bubble sizes for this chart series.
### getDataLabels() {#getDataLabels}
```
public ChartDataLabelCollection getDataLabels()
```


Gibt die Einstellungen für die Datenbeschriftungen der gesamten Reihe an.

 **Examples:** 

Zeigt, wie Beschriftungen auf Datenpunkte in einem Liniendiagramm angewendet werden.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```

**Returns:**
[ChartDataLabelCollection](../../com.aspose.words/chartdatalabelcollection/) - The corresponding [ChartDataLabelCollection](../../com.aspose.words/chartdatalabelcollection/) value.
### getDataPoints() {#getDataPoints}
```
public ChartDataPointCollection getDataPoints()
```


Gibt eine Sammlung von Formatierungsobjekten für alle Datenpunkte in dieser Reihe zurück.

 **Examples:** 

Zeigt, wie Beschriftungen auf Datenpunkte in einem Liniendiagramm angewendet werden.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```

**Returns:**
[ChartDataPointCollection](../../com.aspose.words/chartdatapointcollection/) - A collection of formatting objects for all data points in this series.
### getExplosion() {#getExplosion}
```
public int getExplosion()
```


Gibt an, um welchen Betrag der Datenpunkt vom Mittelpunkt des Kuchendiagramms verschoben werden soll. Kann negativ sein; ein negativer Wert bedeutet, dass die Eigenschaft nicht gesetzt ist und keine Explosion angewendet wird. Gilt nur für Kuchendiagramme.

 **Examples:** 

Zeigt, wie Beschriftungen auf Datenpunkte in einem Liniendiagramm angewendet werden.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```

**Returns:**
int - Der entsprechende int-Wert.
### getFormat() {#getFormat}
```
public ChartFormat getFormat()
```


Stellt Zugriff auf Füll‑ und Linienformatierung der Reihe bereit.

 **Examples:** 

Zeigt, wie man die Serienfarbe festlegt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);

 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();

 // Delete default generated series.
 seriesColl.clear();

 // Create category names array.
 String[] categories = new String[] { "Category 1", "Category 2" };

 // Adding new series. Value and category arrays must be the same size.
 ChartSeries series1 = seriesColl.add("Series 1", categories, new double[] { 1.0, 2.0 });
 ChartSeries series2 = seriesColl.add("Series 2", categories, new double[] { 3.0, 4.0 });
 ChartSeries series3 = seriesColl.add("Series 3", categories, new double[] { 5.0, 6.0 });

 // Set series color.
 series1.getFormat().getFill().setForeColor(Color.RED);
 series2.getFormat().getFill().setForeColor(Color.YELLOW);
 series3.getFormat().getFill().setForeColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.SeriesColor.docx");
 
```

**Returns:**
[ChartFormat](../../com.aspose.words/chartformat/) - The corresponding [ChartFormat](../../com.aspose.words/chartformat/) value.
### getInvertIfNegative() {#getInvertIfNegative}
```
public boolean getInvertIfNegative()
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
### getLegendEntry() {#getLegendEntry}
```
public ChartLegendEntry getLegendEntry()
```


Ruft einen Legendeeintrag für diese Diagrammreihe ab.

 **Examples:** 

Zeigt, wie man mit einer Legenden‑Schriftart arbeitet.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - Chart series (Java).docx");
 Chart chart = ((Shape)doc.getChild(NodeType.SHAPE, 0, true)).getChart();

 ChartLegend chartLegend = chart.getLegend();
 // Set default font size all legend entries.
 chartLegend.getFont().setSize(14.0);
 // Change font for specific legend entry.
 chartLegend.getLegendEntries().get(1).getFont().setItalic(true);
 chartLegend.getLegendEntries().get(1).getFont().setSize(12.0);
 // Get legend entry for chart series.
 ChartLegendEntry legendEntry = chart.getSeries().get(0).getLegendEntry();

 doc.save(getArtifactsDir() + "Charts.LegendFont.docx");
 
```

**Returns:**
[ChartLegendEntry](../../com.aspose.words/chartlegendentry/) - A legend entry for this chart series.
### getMarker() {#getMarker}
```
public ChartMarker getMarker()
```


Gibt einen Datenmarker an. Der Marker wird bei Bedarf automatisch erstellt.

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
[ChartMarker](../../com.aspose.words/chartmarker/) - The corresponding [ChartMarker](../../com.aspose.words/chartmarker/) value.
### getName() {#getName}
```
public String getName()
```


Liefert den Namen der Serie, wenn der Name nicht explizit gesetzt wird, wird er anhand des Index generiert. Standardmäßig wird 'Series' plus ein eins‑basierter Index zurückgegeben.

 **Examples:** 

Zeigt, wie Beschriftungen auf Datenpunkte in einem Liniendiagramm angewendet werden.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```

**Returns:**
java.lang.String – Der Name der Serie, wenn der Name nicht explizit gesetzt wird, wird er anhand des Index generiert.
### getSeriesType() {#getSeriesType}
```
public int getSeriesType()
```


Ruft den Typ dieser Diagrammreihe ab.

 **Examples:** 

Zeigt, wie man eine bestimmte Diagrammserie entfernt.

```

 Document doc = new Document(getMyDir() + "Reporting engine template - Chart series (Java).docx");
 Chart chart = ((Shape)doc.getChild(NodeType.SHAPE, 0, true)).getChart();

 // Remove all series of the Column type.
 for (int i = chart.getSeries().getCount() - 1; i >= 0; i--)
 {
     if (chart.getSeries().get(i).getSeriesType() == ChartSeriesType.COLUMN)
         chart.getSeries().removeAt(i);
 }

 chart.getSeries().add(
         "Aspose Series",
         new String[] { "Category 1", "Category 2", "Category 3", "Category 4" },
         new double[] { 5.6, 7.1, 2.9, 8.9 });

 doc.save(getArtifactsDir() + "Charts.RemoveSpecificChartSeries.docx");
 
```

**Returns:**
int – Der Typ dieser Diagrammserie. Der zurückgegebene Wert ist einer der [ChartSeriesType](../../com.aspose.words/chartseriestype/) Konstanten.
### getSmooth() {#getSmooth}
```
public boolean getSmooth()
```


Ermöglicht die Angabe, ob die Linie, die die Punkte im Diagramm verbindet, mithilfe von Catmull‑Rom‑Splines geglättet werden soll.

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
### getXValues() {#getXValues}
```
public ChartXValueCollection getXValues()
```


Ruft eine Sammlung von X-Werten für diese Diagrammreihe ab.

 **Examples:** 

Zeigt, wie man mit dem Formatcode der Diagrammdaten arbeitet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a Bubble chart.
 Shape shape = builder.insertChart(ChartType.BUBBLE, 432.0, 252.0);
 Chart chart = shape.getChart();

 // Delete default generated series.
 chart.getSeries().clear();

 ChartSeries series = chart.getSeries().add(
         "Series1",
         new double[] { 1.0, 1.9, 2.45, 3.0 },
         new double[] { 1.0, -0.9, 1.82, 0.0 },
         new double[] { 2.0, 1.1, 2.95, 2.0 });

 // Show data labels.
 series.hasDataLabels(true);
 series.getDataLabels().setShowCategoryName(true);
 series.getDataLabels().setShowValue(true);
 series.getDataLabels().setShowBubbleSize(true);

 // Set data format codes.
 series.getXValues().setFormatCode("#,##0.0#");
 series.getYValues().setFormatCode("#,##0.0#;[Red]\\-#,##0.0#");
 series.getBubbleSizes().setFormatCode("#,##0.0#");

 doc.save(getArtifactsDir() + "Charts.FormatCode.docx");
 
```

**Returns:**
[ChartXValueCollection](../../com.aspose.words/chartxvaluecollection/) - A collection of X values for this chart series.
### getYValues() {#getYValues}
```
public ChartYValueCollection getYValues()
```


Ruft eine Sammlung von Y-Werten für diese Diagrammreihe ab.

 **Examples:** 

Zeigt, wie man mit dem Formatcode der Diagrammdaten arbeitet.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a Bubble chart.
 Shape shape = builder.insertChart(ChartType.BUBBLE, 432.0, 252.0);
 Chart chart = shape.getChart();

 // Delete default generated series.
 chart.getSeries().clear();

 ChartSeries series = chart.getSeries().add(
         "Series1",
         new double[] { 1.0, 1.9, 2.45, 3.0 },
         new double[] { 1.0, -0.9, 1.82, 0.0 },
         new double[] { 2.0, 1.1, 2.95, 2.0 });

 // Show data labels.
 series.hasDataLabels(true);
 series.getDataLabels().setShowCategoryName(true);
 series.getDataLabels().setShowValue(true);
 series.getDataLabels().setShowBubbleSize(true);

 // Set data format codes.
 series.getXValues().setFormatCode("#,##0.0#");
 series.getYValues().setFormatCode("#,##0.0#;[Red]\\-#,##0.0#");
 series.getBubbleSizes().setFormatCode("#,##0.0#");

 doc.save(getArtifactsDir() + "Charts.FormatCode.docx");
 
```

**Returns:**
[ChartYValueCollection](../../com.aspose.words/chartyvaluecollection/) - A collection of Y values for this chart series.
### hasDataLabels() {#hasDataLabels}
```
public boolean hasDataLabels()
```


Ruft ein Flag ab, das angibt, ob Datenbeschriftungen für die Reihe angezeigt werden.

 **Examples:** 

Zeigt, wie man Datenbeschriftungen für eine Diagrammserie aktiviert und konfiguriert.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add a line chart, then clear its demo data series to start with a clean chart,
 // and then set a title.
 Shape shape = builder.insertChart(ChartType.LINE, 500.0, 300.0);
 Chart chart = shape.getChart();
 chart.getSeries().clear();
 chart.getTitle().setText("Monthly sales report");

 // Insert a custom chart series with months as categories for the X-axis,
 // and respective decimal amounts for the Y-axis.
 ChartSeries series = chart.getSeries().add("Revenue",
         new String[]{"January", "February", "March"},
         new double[]{25.611d, 21.439d, 33.750d});

 // Enable data labels, and then apply a custom number format for values displayed in the data labels.
 // This format will treat displayed decimal values as millions of US Dollars.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.getNumberFormat().setFormatCode("\"US$\" #,##0.000\"M\"");
 dataLabels.getFont().setSize(12.0);

 doc.save(getArtifactsDir() + "Charts.DataLabelNumberFormat.docx");
 
```

**Returns:**
boolean – Ein Flag, das angibt, ob Datenbeschriftungen für die Serie angezeigt werden.
### hasDataLabels(boolean value) {#hasDataLabels-boolean}
```
public void hasDataLabels(boolean value)
```


Setzt ein Flag, das angibt, ob Datenbeschriftungen für die Reihe angezeigt werden.

 **Examples:** 

Zeigt, wie man Datenbeschriftungen für eine Diagrammserie aktiviert und konfiguriert.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Add a line chart, then clear its demo data series to start with a clean chart,
 // and then set a title.
 Shape shape = builder.insertChart(ChartType.LINE, 500.0, 300.0);
 Chart chart = shape.getChart();
 chart.getSeries().clear();
 chart.getTitle().setText("Monthly sales report");

 // Insert a custom chart series with months as categories for the X-axis,
 // and respective decimal amounts for the Y-axis.
 ChartSeries series = chart.getSeries().add("Revenue",
         new String[]{"January", "February", "March"},
         new double[]{25.611d, 21.439d, 33.750d});

 // Enable data labels, and then apply a custom number format for values displayed in the data labels.
 // This format will treat displayed decimal values as millions of US Dollars.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.getNumberFormat().setFormatCode("\"US$\" #,##0.000\"M\"");
 dataLabels.getFont().setSize(12.0);

 doc.save(getArtifactsDir() + "Charts.DataLabelNumberFormat.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | boolean | Ein Flag, das angibt, ob Datenbeschriftungen für die Serie angezeigt werden. |

### insert(int index, ChartXValue xValue) {#insert-int-com.aspose.words.ChartXValue}
```
public void insert(int index, ChartXValue xValue)
```


Fügt den angegebenen X‑Wert an der angegebenen Position in die Diagrammserie ein. Unterstützt die Serie Y‑Werte und Blasengrößen, bleiben diese für den X‑Wert leer.

 **Remarks:** 

Der entsprechende Datenpunkt mit Standardformatierung wird in die Datenpunktsammlung eingefügt. Und wenn Datenbeschriftungen angezeigt werden, wird auch die entsprechende Datenbeschriftung mit Standardformatierung eingefügt.

 **Examples:** 

Zeigt, wie man Daten in eine Diagrammserie einfügt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeries series1 = chart.getSeries().get(0);

 // Clear X and Y values of the first series.
 series1.clearValues();
 // Populate the series with data.
 series1.insert(0, ChartXValue.fromDouble(3.0));
 series1.insert(1, ChartXValue.fromDouble(3.0), ChartYValue.fromDouble(10.0));
 series1.insert(2, ChartXValue.fromDouble(3.0), ChartYValue.fromDouble(10.0));
 series1.insert(3, ChartXValue.fromDouble(3.0), ChartYValue.fromDouble(10.0), 10.0);

 doc.save(getArtifactsDir() + "Charts.PopulateChartWithData.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int |  |
| xValue | [ChartXValue](../../com.aspose.words/chartxvalue/) |  |

### insert(int index, ChartXValue xValue, ChartYValue yValue) {#insert-int-com.aspose.words.ChartXValue-com.aspose.words.ChartYValue}
```
public void insert(int index, ChartXValue xValue, ChartYValue yValue)
```


Fügt die angegebenen X- und Y-Werte an der angegebenen Position in die Diagrammreihe ein.

 **Remarks:** 

Der entsprechende Datenpunkt mit Standardformatierung wird in die Datenpunktsammlung eingefügt. Und wenn Datenbeschriftungen angezeigt werden, wird auch die entsprechende Datenbeschriftung mit Standardformatierung eingefügt.

 **Examples:** 

Zeigt, wie man Daten in eine Diagrammserie einfügt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeries series1 = chart.getSeries().get(0);

 // Clear X and Y values of the first series.
 series1.clearValues();
 // Populate the series with data.
 series1.insert(0, ChartXValue.fromDouble(3.0));
 series1.insert(1, ChartXValue.fromDouble(3.0), ChartYValue.fromDouble(10.0));
 series1.insert(2, ChartXValue.fromDouble(3.0), ChartYValue.fromDouble(10.0));
 series1.insert(3, ChartXValue.fromDouble(3.0), ChartYValue.fromDouble(10.0), 10.0);

 doc.save(getArtifactsDir() + "Charts.PopulateChartWithData.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int |  |
| xValue | [ChartXValue](../../com.aspose.words/chartxvalue/) |  |
| yValue | [ChartYValue](../../com.aspose.words/chartyvalue/) |  |

### insert(int index, ChartXValue xValue, ChartYValue yValue, double bubbleSize) {#insert-int-com.aspose.words.ChartXValue-com.aspose.words.ChartYValue-double}
```
public void insert(int index, ChartXValue xValue, ChartYValue yValue, double bubbleSize)
```


Fügt den angegebenen X-Wert, Y-Wert und die Blasengröße an der angegebenen Position in die Diagrammreihe ein.

 **Remarks:** 

Der entsprechende Datenpunkt mit Standardformatierung wird in die Datenpunktsammlung eingefügt. Und wenn Datenbeschriftungen angezeigt werden, wird auch die entsprechende Datenbeschriftung mit Standardformatierung eingefügt.

 **Examples:** 

Zeigt, wie man Daten in eine Diagrammserie einfügt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeries series1 = chart.getSeries().get(0);

 // Clear X and Y values of the first series.
 series1.clearValues();
 // Populate the series with data.
 series1.insert(0, ChartXValue.fromDouble(3.0));
 series1.insert(1, ChartXValue.fromDouble(3.0), ChartYValue.fromDouble(10.0));
 series1.insert(2, ChartXValue.fromDouble(3.0), ChartYValue.fromDouble(10.0));
 series1.insert(3, ChartXValue.fromDouble(3.0), ChartYValue.fromDouble(10.0), 10.0);

 doc.save(getArtifactsDir() + "Charts.PopulateChartWithData.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int |  |
| xValue | [ChartXValue](../../com.aspose.words/chartxvalue/) |  |
| yValue | [ChartYValue](../../com.aspose.words/chartyvalue/) |  |
| bubbleSize | double |  |

### remove(int index) {#remove-int}
```
public void remove(int index)
```


Entfernt den X‑Wert, den Y‑Wert und die Blasengröße, falls unterstützt, aus der Diagrammserie am angegebenen Index. Der entsprechende Datenpunkt und das Datenetikett werden ebenfalls entfernt.

 **Examples:** 

Zeigt, wie man Diagrammdatenwerte hinzufügt/entfernt.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder();

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeries department1Series = chart.getSeries().get(0);
 ChartSeries department2Series = chart.getSeries().get(1);

 // Remove the first value in the both series.
 department1Series.remove(0);
 department2Series.remove(0);

 // Add new values to the both series.
 ChartXValue newXCategory = ChartXValue.fromString("Q1, 2023");
 department1Series.add(newXCategory, ChartYValue.fromDouble(10.3));
 department2Series.add(newXCategory, ChartYValue.fromDouble(5.7));

 doc.save(getArtifactsDir() + "Charts.ChartDataValues.docx");
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Index | int |  |

### setBubble3D(boolean value) {#setBubble3D-boolean}
```
public void setBubble3D(boolean value)
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
public void setExplosion(int value)
```


Gibt an, um welchen Betrag der Datenpunkt vom Mittelpunkt des Kuchendiagramms verschoben werden soll. Kann negativ sein; ein negativer Wert bedeutet, dass die Eigenschaft nicht gesetzt ist und keine Explosion angewendet wird. Gilt nur für Kuchendiagramme.

 **Examples:** 

Zeigt, wie Beschriftungen auf Datenpunkte in einem Liniendiagramm angewendet werden.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | int | Der entsprechende  int  Wert. |

### setInvertIfNegative(boolean value) {#setInvertIfNegative-boolean}
```
public void setInvertIfNegative(boolean value)
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

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Setzt den Namen der Serie; wenn der Name nicht explizit festgelegt ist, wird er anhand des Index generiert. Standardmäßig wird Serie plus eins basierend auf dem Index zurückgegeben.

 **Examples:** 

Zeigt, wie Beschriftungen auf Datenpunkte in einem Liniendiagramm angewendet werden.

```

 public void dataLabels() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     Shape chartShape = builder.insertChart(ChartType.LINE, 400.0, 300.0);
     Chart chart = chartShape.getChart();

     Assert.assertEquals(3, chart.getSeries().getCount());
     Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
     Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
     Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

     // Apply data labels to every series in the chart.
     // These labels will appear next to each data point in the graph and display its value.
     for (ChartSeries series : chart.getSeries()) {
         applyDataLabels(series, 4, "000.0", ", ");
         Assert.assertEquals(series.getDataLabels().getCount(), 4);
     }

     // Change the separator string for every data label in a series.
     Iterator enumerator = chart.getSeries().get(0).getDataLabels().iterator();
     while (enumerator.hasNext()) {
         Assert.assertEquals(enumerator.next().getSeparator(), ", ");
         enumerator.next().setSeparator(" & ");
     }

     ChartDataLabel dataLabel = chart.getSeries().get(1).getDataLabels().get(2);
     dataLabel.getFormat().getFill().setColor(Color.RED);

     // For a cleaner looking graph, we can remove data labels individually.
     dataLabel.clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     series.hasDataLabels(true);
     series.setExplosion(40);

     for (int i = 0; i < labelsCount; i++) {
         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());

         series.getDataLabels().get(i).getNumberFormat().setFormatCode(numberFormat);
         series.getDataLabels().get(i).setSeparator(separator);

         Assert.assertFalse(series.getDataLabels().get(i).getShowDataLabelsRange());
         Assert.assertTrue(series.getDataLabels().get(i).isVisible());
         Assert.assertFalse(series.getDataLabels().get(i).isHidden());
     }
 }
 
```

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Wert | java.lang.String | Der Name der Serie; wenn der Name nicht explizit festgelegt ist, wird er anhand des Index generiert. |

### setSmooth(boolean value) {#setSmooth-boolean}
```
public void setSmooth(boolean value)
```


Ermöglicht die Angabe, ob die Linie, die die Punkte im Diagramm verbindet, mithilfe von Catmull‑Rom‑Splines geglättet werden soll.

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

