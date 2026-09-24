---
title: "ChartSeries"
linktitle: "ChartSeries"
second_title: "Aspose.Words Java için"
description: "Java'da grafik serisi özelliklerini temsil eder."
type: docs
weight: 85
url: /tr/java/com.aspose.words/chartseries/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
[com.aspose.words.IChartDataPoint](../../com.aspose.words/ichartdatapoint/), java.lang.Cloneable
```
public class ChartSeries implements IChartDataPoint, Cloneable
```

Grafik serisi özelliklerini temsil eder.

Daha fazla bilgi için, [ Working with Charts ][Working with Charts] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Bir çizgi grafiğindeki veri noktalarına etiketlerin nasıl uygulanacağını gösterir.

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
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [add(ChartXValue xValue)](#add-com.aspose.words.ChartXValue) | Belirtilen X değerini grafik serisine ekler. |
| [add(ChartXValue xValue, ChartYValue yValue)](#add-com.aspose.words.ChartXValue-com.aspose.words.ChartYValue) | Belirtilen X ve Y değerlerini grafik serisine ekler. |
| [add(ChartXValue xValue, ChartYValue yValue, double bubbleSize)](#add-com.aspose.words.ChartXValue-com.aspose.words.ChartYValue-double) | Belirtilen X değerini, Y değerini ve balon boyutunu grafik serisine ekler. |
| [clear()](#clear) | Grafik serisinden tüm veri değerlerini kaldırır. |
| [clearValues()](#clearValues) | Veri noktalarının ve veri etiketlerinin biçimini koruyarak grafik serisinden tüm veri değerlerini kaldırır. |
| [copyFormatFrom(int dataPointIndex)](#copyFormatFrom-int) | Belirtilen dizine sahip veri noktasından varsayılan veri noktası biçimini kopyalar. |
| [getBubble3D()](#getBubble3D) | Balon grafiğindeki balonların 3B etkisi uygulanıp uygulanmayacağını belirtir. |
| [getBubbleSizes()](#getBubbleSizes) | Bu grafik serisi için balon boyutlarının bir koleksiyonunu alır. |
| [getDataLabels()](#getDataLabels) | Tüm seri için veri etiketlerinin ayarlarını belirtir. |
| [getDataPoints()](#getDataPoints) | Bu serideki tüm veri noktaları için biçimlendirme nesnelerinin bir koleksiyonunu döndürür. |
| [getExplosion()](#getExplosion) | Veri noktasının pasta grafiğinin merkezinden ne kadar taşınacağını belirtir. |
| [getFormat()](#getFormat) | Serinin dolgu ve çizgi biçimlendirmesine erişim sağlar. |
| [getInvertIfNegative()](#getInvertIfNegative) | Ebeveyn öğenin değeri negatifse renklerini tersine çevirip çevirmeyeceğini belirtir. |
| [getLegendEntry()](#getLegendEntry) | Bu grafik serisi için bir lejand (legend) girişi alır. |
| [getMarker()](#getMarker) | Bir veri işaretçisi belirtir. |
| [getName()](#getName) | Serinin adını alır; ad açıkça ayarlanmamışsa dizin kullanılarak oluşturulur. |
| [getSeriesType()](#getSeriesType) | Bu grafik serisinin tipini alır. |
| [getSmooth()](#getSmooth) | Grafikteki noktaları bağlayan çizginin Catmull-Rom spline'ları kullanılarak yumuşatılıp yumuşatılmayacağını belirtmeye izin verir. |
| [getXValues()](#getXValues) | Bu grafik serisi için X değerlerinin bir koleksiyonunu alır. |
| [getYValues()](#getYValues) | Bu grafik serisi için Y değerlerinin bir koleksiyonunu alır. |
| [hasDataLabels()](#hasDataLabels) | Seri için veri etiketlerinin gösterilip gösterilmeyeceğini belirten bir bayrak alır. |
| [hasDataLabels(boolean value)](#hasDataLabels-boolean) | Seri için veri etiketlerinin gösterilip gösterilmeyeceğini belirten bir bayrağı ayarlar. |
| [insert(int index, ChartXValue xValue)](#insert-int-com.aspose.words.ChartXValue) | Belirtilen X değerini belirtilen dizinde grafik serisine ekler. |
| [insert(int index, ChartXValue xValue, ChartYValue yValue)](#insert-int-com.aspose.words.ChartXValue-com.aspose.words.ChartYValue) | Belirtilen X ve Y değerlerini belirtilen dizinde grafik serisine ekler. |
| [insert(int index, ChartXValue xValue, ChartYValue yValue, double bubbleSize)](#insert-int-com.aspose.words.ChartXValue-com.aspose.words.ChartYValue-double) | Belirtilen X değeri, Y değeri ve balon boyutunu belirtilen dizinde grafik serisine ekler. |
| [remove(int index)](#remove-int) | Destekleniyorsa, belirtilen dizindeki grafik serisinden X değeri, Y değeri ve balon boyutunu kaldırır. |
| [setBubble3D(boolean value)](#setBubble3D-boolean) | Balon grafiğindeki balonların 3B etkisi uygulanıp uygulanmayacağını belirtir. |
| [setExplosion(int value)](#setExplosion-int) | Veri noktasının pasta grafiğinin merkezinden ne kadar taşınacağını belirtir. |
| [setInvertIfNegative(boolean value)](#setInvertIfNegative-boolean) | Ebeveyn öğenin değeri negatifse renklerini tersine çevirip çevirmeyeceğini belirtir. |
| [setName(String value)](#setName-java.lang.String) | Serinin adını ayarlar; ad açıkça ayarlanmamışsa dizin kullanılarak oluşturulur. |
| [setSmooth(boolean value)](#setSmooth-boolean) | Grafikteki noktaları bağlayan çizginin Catmull-Rom spline'ları kullanılarak yumuşatılıp yumuşatılmayacağını belirtmeye izin verir. |
### add(ChartXValue xValue) {#add-com.aspose.words.ChartXValue}
```
public void add(ChartXValue xValue)
```


Belirtilen X değerini grafik serisine ekler. Seri Y değerlerini ve balon boyutlarını destekliyorsa, X değeri için bunlar boş olur.

 **Examples:** 

Grafik serisini veriyle nasıl doldurulacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| xValue | [ChartXValue](../../com.aspose.words/chartxvalue/) |  |

### add(ChartXValue xValue, ChartYValue yValue) {#add-com.aspose.words.ChartXValue-com.aspose.words.ChartYValue}
```
public void add(ChartXValue xValue, ChartYValue yValue)
```


Belirtilen X ve Y değerlerini grafik serisine ekler.

 **Examples:** 

Grafik serisini veriyle nasıl doldurulacağını gösterir.

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

Grafik veri değerlerini ekleme/kaldırma işlemlerinin nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| xValue | [ChartXValue](../../com.aspose.words/chartxvalue/) |  |
| yValue | [ChartYValue](../../com.aspose.words/chartyvalue/) |  |

### add(ChartXValue xValue, ChartYValue yValue, double bubbleSize) {#add-com.aspose.words.ChartXValue-com.aspose.words.ChartYValue-double}
```
public void add(ChartXValue xValue, ChartYValue yValue, double bubbleSize)
```


Belirtilen X değerini, Y değerini ve balon boyutunu grafik serisine ekler.

 **Examples:** 

Grafik serisini veriyle nasıl doldurulacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| xValue | [ChartXValue](../../com.aspose.words/chartxvalue/) |  |
| yValue | [ChartYValue](../../com.aspose.words/chartyvalue/) |  |
| bubbleSize | double |  |

### clear() {#clear}
```
public void clear()
```


Grafik serisindeki tüm veri değerlerini kaldırır. Tüm bireysel veri noktalarının ve veri etiketlerinin biçimi temizlenir.

 **Examples:** 

Grafik serisini veriyle nasıl doldurulacağını gösterir.

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


Veri noktalarının ve veri etiketlerinin biçimini koruyarak grafik serisinden tüm veri değerlerini kaldırır.

 **Examples:** 

Grafik serisini veriyle nasıl doldurulacağını gösterir.

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


Belirtilen dizine sahip veri noktasından varsayılan veri noktası biçimini kopyalar.

 **Examples:** 

Veri noktası biçiminin nasıl kopyalanacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| dataPointIndex | int |  |

### getBubble3D() {#getBubble3D}
```
public boolean getBubble3D()
```


Balon grafiğindeki balonların 3B etkisi uygulanıp uygulanmayacağını belirtir.

 **Examples:** 

Balon grafiklerinde 3B efektlerin nasıl kullanılacağını gösterir.

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
boolean - İlgili  boolean  değeri.
### getBubbleSizes() {#getBubbleSizes}
```
public BubbleSizeCollection getBubbleSizes()
```


Bu grafik serisi için balon boyutlarının bir koleksiyonunu alır.

 **Examples:** 

Grafik verisinin biçim kodu ile nasıl çalışılacağını gösterir.

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


Tüm seri için veri etiketlerinin ayarlarını belirtir.

 **Examples:** 

Bir çizgi grafiğindeki veri noktalarına etiketlerin nasıl uygulanacağını gösterir.

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


Bu serideki tüm veri noktaları için biçimlendirme nesnelerinin bir koleksiyonunu döndürür.

 **Examples:** 

Bir çizgi grafiğindeki veri noktalarına etiketlerin nasıl uygulanacağını gösterir.

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


Veri noktasının pasta grafiğinin merkezinden ne kadar kaydırılacağını belirtir. Negatif olabilir; negatif değer, özelliğin ayarlanmadığını ve patlama uygulanmayacağını gösterir. Yalnızca Pasta grafiklerinde geçerlidir.

 **Examples:** 

Bir çizgi grafiğindeki veri noktalarına etiketlerin nasıl uygulanacağını gösterir.

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
int - İlgili  int  değeri.
### getFormat() {#getFormat}
```
public ChartFormat getFormat()
```


Serinin dolgu ve çizgi biçimlendirmesine erişim sağlar.

 **Examples:** 

Seri renginin nasıl ayarlanacağını gösterir.

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


Ebeveyn öğenin değeri negatifse renklerini tersine çevirip çevirmeyeceğini belirtir.

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

**Returns:**
boolean - İlgili  boolean  değeri.
### getLegendEntry() {#getLegendEntry}
```
public ChartLegendEntry getLegendEntry()
```


Bu grafik serisi için bir lejand (legend) girişi alır.

 **Examples:** 

Lejant yazı tipiyle nasıl çalışılacağını gösterir.

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


Bir veri işaretleyicisi belirtir. İşaretleyici, talep edildiğinde otomatik olarak oluşturulur.

 **Examples:** 

İşaretleyici biçimlendirmesinin nasıl ayarlanacağını gösterir.

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


Serinin adını alır; ad açıkça ayarlanmamışsa indeks kullanılarak oluşturulur. Varsayılan olarak, Series ve bir indeks döndürür.

 **Examples:** 

Bir çizgi grafiğindeki veri noktalarına etiketlerin nasıl uygulanacağını gösterir.

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
java.lang.String - Serinin adı, ad açıkça ayarlanmamışsa indeks kullanılarak oluşturulur.
### getSeriesType() {#getSeriesType}
```
public int getSeriesType()
```


Bu grafik serisinin tipini alır.

 **Examples:** 

Belirli bir grafik serisinin nasıl kaldırılacağını gösterir.

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
int - Bu grafik serisinin türü. Döndürülen değer, [ChartSeriesType](../../com.aspose.words/chartseriestype/) sabitlerinden biridir.
### getSmooth() {#getSmooth}
```
public boolean getSmooth()
```


Grafikteki noktaları bağlayan çizginin Catmull-Rom spline'ları kullanılarak yumuşatılıp yumuşatılmayacağını belirtmeye izin verir.

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

**Returns:**
boolean - İlgili  boolean  değeri.
### getXValues() {#getXValues}
```
public ChartXValueCollection getXValues()
```


Bu grafik serisi için X değerlerinin bir koleksiyonunu alır.

 **Examples:** 

Grafik verisinin biçim kodu ile nasıl çalışılacağını gösterir.

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


Bu grafik serisi için Y değerlerinin bir koleksiyonunu alır.

 **Examples:** 

Grafik verisinin biçim kodu ile nasıl çalışılacağını gösterir.

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


Seri için veri etiketlerinin gösterilip gösterilmeyeceğini belirten bir bayrak alır.

 **Examples:** 

Grafik serisi için veri etiketlerini etkinleştirme ve yapılandırma yöntemlerini gösterir.

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
boolean - Seride veri etiketlerinin gösterilip gösterilmediğini belirten bir işaret.
### hasDataLabels(boolean value) {#hasDataLabels-boolean}
```
public void hasDataLabels(boolean value)
```


Seri için veri etiketlerinin gösterilip gösterilmeyeceğini belirten bir bayrağı ayarlar.

 **Examples:** 

Grafik serisi için veri etiketlerini etkinleştirme ve yapılandırma yöntemlerini gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | Seride veri etiketlerinin gösterilip gösterilmediğini belirten bir işaret. |

### insert(int index, ChartXValue xValue) {#insert-int-com.aspose.words.ChartXValue}
```
public void insert(int index, ChartXValue xValue)
```


Belirtilen X değerini, belirtilen indekste grafik serisine ekler. Seri Y değerlerini ve balon boyutlarını destekliyorsa, X değeri için bunlar boş olur.

 **Remarks:** 

Varsayılan biçimlendirmeye sahip ilgili veri noktası veri noktası koleksiyonuna eklenecektir. Ayrıca, veri etiketleri gösteriliyorsa, ilgili veri etiketi de varsayılan biçimlendirme ile eklenecektir.

 **Examples:** 

Grafik serisine veri eklemenin nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int |  |
| xValue | [ChartXValue](../../com.aspose.words/chartxvalue/) |  |

### insert(int index, ChartXValue xValue, ChartYValue yValue) {#insert-int-com.aspose.words.ChartXValue-com.aspose.words.ChartYValue}
```
public void insert(int index, ChartXValue xValue, ChartYValue yValue)
```


Belirtilen X ve Y değerlerini belirtilen dizinde grafik serisine ekler.

 **Remarks:** 

Varsayılan biçimlendirmeye sahip ilgili veri noktası veri noktası koleksiyonuna eklenecektir. Ayrıca, veri etiketleri gösteriliyorsa, ilgili veri etiketi de varsayılan biçimlendirme ile eklenecektir.

 **Examples:** 

Grafik serisine veri eklemenin nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int |  |
| xValue | [ChartXValue](../../com.aspose.words/chartxvalue/) |  |
| yValue | [ChartYValue](../../com.aspose.words/chartyvalue/) |  |

### insert(int index, ChartXValue xValue, ChartYValue yValue, double bubbleSize) {#insert-int-com.aspose.words.ChartXValue-com.aspose.words.ChartYValue-double}
```
public void insert(int index, ChartXValue xValue, ChartYValue yValue, double bubbleSize)
```


Belirtilen X değeri, Y değeri ve balon boyutunu belirtilen dizinde grafik serisine ekler.

 **Remarks:** 

Varsayılan biçimlendirmeye sahip ilgili veri noktası veri noktası koleksiyonuna eklenecektir. Ayrıca, veri etiketleri gösteriliyorsa, ilgili veri etiketi de varsayılan biçimlendirme ile eklenecektir.

 **Examples:** 

Grafik serisine veri eklemenin nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int |  |
| xValue | [ChartXValue](../../com.aspose.words/chartxvalue/) |  |
| yValue | [ChartYValue](../../com.aspose.words/chartyvalue/) |  |
| bubbleSize | double |  |

### remove(int index) {#remove-int}
```
public void remove(int index)
```


Belirtilen indeksdeki grafik serisinden, destekleniyorsa X değeri, Y değeri ve balon boyutunu kaldırır. İlgili veri noktası ve veri etiketi de kaldırılır.

 **Examples:** 

Grafik veri değerlerini ekleme/kaldırma işlemlerinin nasıl yapılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int |  |

### setBubble3D(boolean value) {#setBubble3D-boolean}
```
public void setBubble3D(boolean value)
```


Balon grafiğindeki balonların 3B etkisi uygulanıp uygulanmayacağını belirtir.

 **Examples:** 

Balon grafiklerinde 3B efektlerin nasıl kullanılacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setExplosion(int value) {#setExplosion-int}
```
public void setExplosion(int value)
```


Veri noktasının pasta grafiğinin merkezinden ne kadar kaydırılacağını belirtir. Negatif olabilir; negatif değer, özelliğin ayarlanmadığını ve patlama uygulanmayacağını gösterir. Yalnızca Pasta grafiklerinde geçerlidir.

 **Examples:** 

Bir çizgi grafiğindeki veri noktalarına etiketlerin nasıl uygulanacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | İlgili  int  değeri. |

### setInvertIfNegative(boolean value) {#setInvertIfNegative-boolean}
```
public void setInvertIfNegative(boolean value)
```


Ebeveyn öğenin değeri negatifse renklerini tersine çevirip çevirmeyeceğini belirtir.

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

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Serinin adını ayarlar, ad açıkça ayarlanmamışsa indeks kullanılarak oluşturulur. Varsayılan olarak, Series artı bir tabanlı indeks döndürür.

 **Examples:** 

Bir çizgi grafiğindeki veri noktalarına etiketlerin nasıl uygulanacağını gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | java.lang.String | Serinin adı, ad açıkça ayarlanmamışsa indeks kullanılarak oluşturulur. |

### setSmooth(boolean value) {#setSmooth-boolean}
```
public void setSmooth(boolean value)
```


Grafikteki noktaları bağlayan çizginin Catmull-Rom spline'ları kullanılarak yumuşatılıp yumuşatılmayacağını belirtmeye izin verir.

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

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | boolean | İlgili  boolean  değeri. |

