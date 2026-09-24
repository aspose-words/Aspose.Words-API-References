---
title: "ChartSeriesGroup"
linktitle: "ChartSeriesGroup"
second_title: "Aspose.Words Java için"
description: "Java'da aynı eksenlere bağlı aynı türdeki grafik serilerinin özelliklerini temsil eden bir grafik serisi grubunun özelliklerini temsil eder."
type: docs
weight: 87
url: /tr/java/com.aspose.words/chartseriesgroup/
---

**Inheritance:**
java.lang.Object
```
public class ChartSeriesGroup
```

Bir grafik serisi grubunun özelliklerini, yani aynı eksenlere bağlı aynı tipteki grafik serilerinin özelliklerini temsil eder.

 **Remarks:** 

Kombinasyon grafikleri, her seri türü için ayrı bir grup olmak üzere birden fazla grafik serisi grubu içerir.

Ayrıca, bir veya daha fazla grafik serisine ikincil eksen atamak için bir grafik serisi grubu oluşturabilirsiniz.

Daha fazla bilgi için, [ Working with Charts ][Working with Charts] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Grafiğin ikincil ekseniyle nasıl çalışılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 450.0, 250.0);
 Chart chart = shape.getChart();
 ChartSeriesCollection series = chart.getSeries();

 // Delete default generated series.
 series.clear();

 String[] categories = new String[] { "Category 1", "Category 2", "Category 3" };
 series.add("Series 1 of primary series group", categories, new double[] { 2.0, 3.0, 4.0 });
 series.add("Series 2 of primary series group", categories, new double[] { 5.0, 2.0, 3.0 });

 // Create an additional series group, also of the line type.
 ChartSeriesGroup newSeriesGroup = chart.getSeriesGroups().add(ChartSeriesType.LINE);
 // Specify the use of secondary axes for the new series group.
 newSeriesGroup.setAxisGroup(AxisGroup.SECONDARY);
 // Hide the secondary X axis.
 newSeriesGroup.getAxisX().setHidden(true);
 // Define title of the secondary Y axis.
 newSeriesGroup.getAxisY().getTitle().setShow(true);
 newSeriesGroup.getAxisY().getTitle().setText("Secondary Y axis");

 Assert.assertEquals(ChartSeriesType.LINE, newSeriesGroup.getSeriesType());

 // Add a series to the new series group.
 ChartSeries series3 =
         newSeriesGroup.getSeries().add("Series of secondary series group", categories, new double[] { 13.0, 11.0, 16.0 });
 series3.getFormat().getStroke().setWeight(3.5);

 doc.save(getArtifactsDir() + "Charts.SecondaryAxis.docx");
 
```


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getAxisGroup()](#getAxisGroup) | Bu seri grubunun ait olduğu eksen grubunu alır. |
| [getAxisX()](#getAxisX) | Bu seri grubunun X ekseninin özelliklerine erişim sağlar. |
| [getAxisY()](#getAxisY) | Bu seri grubunun Y ekseninin özelliklerine erişim sağlar. |
| [getBubbleScale()](#getBubbleScale) | Kabarcıkların boyutunu varsayılan boyutlarının yüzdesi olarak alır. |
| [getDoughnutHoleSize()](#getDoughnutHoleSize) | Üst döner grafiğin delik boyutunu yüzde olarak alır. |
| [getFirstSliceAngle()](#getFirstSliceAngle) | Üst pasta grafiğinin ilk diliminin açısını derece cinsinden alır. |
| [getGapWidth()](#getGapWidth) | Grafik öğeleri arasındaki boşluk genişliğinin yüzdesini alır. |
| [getOverlap()](#getOverlap) | Seri çubukları veya sütunlarının ne kadar üst üste bindiğinin yüzdesini alır. |
| [getSecondSectionSize()](#getSecondSectionSize) | Pasta grafiğinin ikincil bölümünün boyutunu yüzde olarak alır. |
| [getSeries()](#getSeries) | Bu seri grubuna ait serilerin bir koleksiyonunu alır. |
| [getSeriesType()](#getSeriesType) | Bu grupta bulunan grafik serisi tipini alır. |
| [setAxisGroup(int value)](#setAxisGroup-int) | Bu seri grubunun ait olduğu eksen grubunu ayarlar. |
| [setBubbleScale(int value)](#setBubbleScale-int) | Kabarcıkların boyutunu varsayılan boyutlarının yüzdesi olarak ayarlar. |
| [setDoughnutHoleSize(int value)](#setDoughnutHoleSize-int) | Üst döner grafiğin delik boyutunu yüzde olarak ayarlar. |
| [setFirstSliceAngle(int value)](#setFirstSliceAngle-int) | Üst pasta grafiğinin ilk diliminin açısını derece cinsinden ayarlar. |
| [setGapWidth(int value)](#setGapWidth-int) | Grafik öğeleri arasındaki boşluk genişliğinin yüzdesini ayarlar. |
| [setOverlap(int value)](#setOverlap-int) | Seri çubukları veya sütunlarının ne kadar üst üste bindiğinin yüzdesini ayarlar. |
| [setSecondSectionSize(int value)](#setSecondSectionSize-int) | Pasta grafiğinin ikincil bölümünün boyutunu yüzde olarak ayarlar. |
### getAxisGroup() {#getAxisGroup}
```
public int getAxisGroup()
```


Bu seri grubunun ait olduğu eksen grubunu alır.

 **Examples:** 

Grafiğin ikincil ekseniyle nasıl çalışılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 450.0, 250.0);
 Chart chart = shape.getChart();
 ChartSeriesCollection series = chart.getSeries();

 // Delete default generated series.
 series.clear();

 String[] categories = new String[] { "Category 1", "Category 2", "Category 3" };
 series.add("Series 1 of primary series group", categories, new double[] { 2.0, 3.0, 4.0 });
 series.add("Series 2 of primary series group", categories, new double[] { 5.0, 2.0, 3.0 });

 // Create an additional series group, also of the line type.
 ChartSeriesGroup newSeriesGroup = chart.getSeriesGroups().add(ChartSeriesType.LINE);
 // Specify the use of secondary axes for the new series group.
 newSeriesGroup.setAxisGroup(AxisGroup.SECONDARY);
 // Hide the secondary X axis.
 newSeriesGroup.getAxisX().setHidden(true);
 // Define title of the secondary Y axis.
 newSeriesGroup.getAxisY().getTitle().setShow(true);
 newSeriesGroup.getAxisY().getTitle().setText("Secondary Y axis");

 Assert.assertEquals(ChartSeriesType.LINE, newSeriesGroup.getSeriesType());

 // Add a series to the new series group.
 ChartSeries series3 =
         newSeriesGroup.getSeries().add("Series of secondary series group", categories, new double[] { 13.0, 11.0, 16.0 });
 series3.getFormat().getStroke().setWeight(3.5);

 doc.save(getArtifactsDir() + "Charts.SecondaryAxis.docx");
 
```

**Returns:**
int - Bu seri grubunun ait olduğu eksen grubu. Döndürülen değer, [AxisGroup](../../com.aspose.words/axisgroup/) sabitlerinden biridir.
### getAxisX() {#getAxisX}
```
public ChartAxis getAxisX()
```


Bu seri grubunun X ekseninin özelliklerine erişim sağlar.

 **Examples:** 

Grafiğin ikincil ekseniyle nasıl çalışılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 450.0, 250.0);
 Chart chart = shape.getChart();
 ChartSeriesCollection series = chart.getSeries();

 // Delete default generated series.
 series.clear();

 String[] categories = new String[] { "Category 1", "Category 2", "Category 3" };
 series.add("Series 1 of primary series group", categories, new double[] { 2.0, 3.0, 4.0 });
 series.add("Series 2 of primary series group", categories, new double[] { 5.0, 2.0, 3.0 });

 // Create an additional series group, also of the line type.
 ChartSeriesGroup newSeriesGroup = chart.getSeriesGroups().add(ChartSeriesType.LINE);
 // Specify the use of secondary axes for the new series group.
 newSeriesGroup.setAxisGroup(AxisGroup.SECONDARY);
 // Hide the secondary X axis.
 newSeriesGroup.getAxisX().setHidden(true);
 // Define title of the secondary Y axis.
 newSeriesGroup.getAxisY().getTitle().setShow(true);
 newSeriesGroup.getAxisY().getTitle().setText("Secondary Y axis");

 Assert.assertEquals(ChartSeriesType.LINE, newSeriesGroup.getSeriesType());

 // Add a series to the new series group.
 ChartSeries series3 =
         newSeriesGroup.getSeries().add("Series of secondary series group", categories, new double[] { 13.0, 11.0, 16.0 });
 series3.getFormat().getStroke().setWeight(3.5);

 doc.save(getArtifactsDir() + "Charts.SecondaryAxis.docx");
 
```

**Returns:**
[ChartAxis](../../com.aspose.words/chartaxis/) - The corresponding [ChartAxis](../../com.aspose.words/chartaxis/) value.
### getAxisY() {#getAxisY}
```
public ChartAxis getAxisY()
```


Bu seri grubunun Y ekseninin özelliklerine erişim sağlar.

 **Examples:** 

Grafiğin ikincil ekseniyle nasıl çalışılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 450.0, 250.0);
 Chart chart = shape.getChart();
 ChartSeriesCollection series = chart.getSeries();

 // Delete default generated series.
 series.clear();

 String[] categories = new String[] { "Category 1", "Category 2", "Category 3" };
 series.add("Series 1 of primary series group", categories, new double[] { 2.0, 3.0, 4.0 });
 series.add("Series 2 of primary series group", categories, new double[] { 5.0, 2.0, 3.0 });

 // Create an additional series group, also of the line type.
 ChartSeriesGroup newSeriesGroup = chart.getSeriesGroups().add(ChartSeriesType.LINE);
 // Specify the use of secondary axes for the new series group.
 newSeriesGroup.setAxisGroup(AxisGroup.SECONDARY);
 // Hide the secondary X axis.
 newSeriesGroup.getAxisX().setHidden(true);
 // Define title of the secondary Y axis.
 newSeriesGroup.getAxisY().getTitle().setShow(true);
 newSeriesGroup.getAxisY().getTitle().setText("Secondary Y axis");

 Assert.assertEquals(ChartSeriesType.LINE, newSeriesGroup.getSeriesType());

 // Add a series to the new series group.
 ChartSeries series3 =
         newSeriesGroup.getSeries().add("Series of secondary series group", categories, new double[] { 13.0, 11.0, 16.0 });
 series3.getFormat().getStroke().setWeight(3.5);

 doc.save(getArtifactsDir() + "Charts.SecondaryAxis.docx");
 
```

**Returns:**
[ChartAxis](../../com.aspose.words/chartaxis/) - The corresponding [ChartAxis](../../com.aspose.words/chartaxis/) value.
### getBubbleScale() {#getBubbleScale}
```
public int getBubbleScale()
```


Kabarcıkların boyutunu varsayılan boyutlarının yüzdesi olarak alır.

 **Remarks:** 

Yalnızca [ChartSeriesType.BUBBLE](../../com.aspose.words/chartseriestype/\#BUBBLE) ve [ChartSeriesType.BUBBLE\_3\_D](../../com.aspose.words/chartseriestype/\#BUBBLE-3-D) tipindeki seri gruplarına uygulanır.

Kabul edilebilir değer aralığı 0 ile 300 arasındadır (her iki uç dahil). Varsayılan değer 100'dür.

 **Examples:** 

Kabarcıkların boyutunun nasıl ayarlanacağını göster.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a bubble 3D chart.
 Shape shape = builder.insertChart(ChartType.BUBBLE_3_D, 450.0, 250.0);
 ChartSeriesGroup seriesGroup = shape.getChart().getSeriesGroups().get(0);

 // Set bubble scale to 200%.
 seriesGroup.setBubbleScale(200);

 doc.save(getArtifactsDir() + "Charts.BubbleScale.docx");
 
```

**Returns:**
int - Kabarcıkların boyutunu varsayılan boyutlarının yüzdesi olarak.
### getDoughnutHoleSize() {#getDoughnutHoleSize}
```
public int getDoughnutHoleSize()
```


Üst döner grafiğin delik boyutunu yüzde olarak alır.

 **Remarks:** 

Yalnızca [ChartSeriesType.DOUGHNUT](../../com.aspose.words/chartseriestype/\#DOUGHNUT) tipindeki seri gruplarına uygulanır.

Kabul edilebilir değer aralığı 0 ile 90 arasındadır (her iki uç dahil). Varsayılan değer 75'tir.

 **Examples:** 

Doughnut grafiğinin nasıl oluşturulacağını ve biçimlendirileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.DOUGHNUT, 400.0, 400.0);
 Chart chart = shape.getChart();
 // Delete the default generated series.
 chart.getSeries().clear();

 String[] categories = new String[] { "Category 1", "Category 2", "Category 3" };
 chart.getSeries().add("Series 1", categories, new double[] { 4.0, 2.0, 5.0 });

 // Format the Doughnut chart.
 ChartSeriesGroup seriesGroup = chart.getSeriesGroups().get(0);
 seriesGroup.setDoughnutHoleSize(10);
 seriesGroup.setFirstSliceAngle(270);

 doc.save(getArtifactsDir() + "Charts.DoughnutChart.docx");
 
```

**Returns:**
int - Üst doughnut grafiğinin delik boyutu yüzde olarak.
### getFirstSliceAngle() {#getFirstSliceAngle}
```
public int getFirstSliceAngle()
```


Üst pasta grafiğinin ilk diliminin açısını derece cinsinden alır.

 **Remarks:** 

Şu tiplerin [ChartSeriesType.PIE](../../com.aspose.words/chartseriestype/\#PIE), [ChartSeriesType.PIE\_3\_D](../../com.aspose.words/chartseriestype/\#PIE-3-D) ve [ChartSeriesType.DOUGHNUT](../../com.aspose.words/chartseriestype/\#DOUGHNUT) serileri gruplarına uygulanır.

Kabul edilebilir değer aralığı 0 ile 360 arasındadır (her iki uç dahil). Varsayılan değer 0'dır.

 **Examples:** 

Doughnut grafiğinin nasıl oluşturulacağını ve biçimlendirileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.DOUGHNUT, 400.0, 400.0);
 Chart chart = shape.getChart();
 // Delete the default generated series.
 chart.getSeries().clear();

 String[] categories = new String[] { "Category 1", "Category 2", "Category 3" };
 chart.getSeries().add("Series 1", categories, new double[] { 4.0, 2.0, 5.0 });

 // Format the Doughnut chart.
 ChartSeriesGroup seriesGroup = chart.getSeriesGroups().get(0);
 seriesGroup.setDoughnutHoleSize(10);
 seriesGroup.setFirstSliceAngle(270);

 doc.save(getArtifactsDir() + "Charts.DoughnutChart.docx");
 
```

**Returns:**
int - Üst pie grafiğinin ilk diliminin açısı, derece cinsinden.
### getGapWidth() {#getGapWidth}
```
public int getGapWidth()
```


Grafik öğeleri arasındaki boşluk genişliğinin yüzdesini alır.

 **Remarks:** 

Yalnızca bar, sütun, pie-of-bar, pie-of-pie, histogram, box&whisker, waterfall ve funnel tiplerinin serileri gruplarına uygulanır.

Kabul edilebilir değer aralığı 0 ile 500 arasındadır (her iki uç dahil). Bar/sütun tabanlı serileri grupları için, özellik çubuk kümeleri arasındaki boşluğu genişliklerinin yüzde olarak temsil eder. Pie-of-pie ve bar-of-pie grafiklerinde ise bu, birincil ve ikincil bölümler arasındaki boşluktur.

 **Examples:** 

Boşluk genişliği ve üst üste binmeyi nasıl yapılandıracağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 450.0, 250.0);
 ChartSeriesGroup seriesGroup = shape.getChart().getSeriesGroups().get(0);

 // Set column gap width and overlap.
 seriesGroup.setGapWidth(450);
 seriesGroup.setOverlap(-75);

 doc.save(getArtifactsDir() + "Charts.ConfigureGapOverlap.docx");
 
```

**Returns:**
int - Grafik öğeleri arasındaki boşluk genişliğinin yüzdesi.
### getOverlap() {#getOverlap}
```
public int getOverlap()
```


Seri çubukları veya sütunlarının ne kadar üst üste bindiğinin yüzdesini alır.

 **Remarks:** 

Tüm bar ve sütun tiplerinin serileri gruplarına uygulanır.

Kabul edilebilir değer aralığı -100 ile 100 arasındadır (her iki uç dahil). 0 değeri, çubuklar/sütunlar arasında boşluk olmadığını gösterir. Değer -100 ise, çubuklar/sütunlar arasındaki mesafe genişliklerine eşittir. 100 değeri, çubukların/sütunların tamamen üst üste bindiğini ifade eder.

 **Examples:** 

Boşluk genişliği ve üst üste binmeyi nasıl yapılandıracağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 450.0, 250.0);
 ChartSeriesGroup seriesGroup = shape.getChart().getSeriesGroups().get(0);

 // Set column gap width and overlap.
 seriesGroup.setGapWidth(450);
 seriesGroup.setOverlap(-75);

 doc.save(getArtifactsDir() + "Charts.ConfigureGapOverlap.docx");
 
```

**Returns:**
int - Serilerin çubukları veya sütunlarının ne kadar üst üste bindiğinin yüzdesi.
### getSecondSectionSize() {#getSecondSectionSize}
```
public int getSecondSectionSize()
```


Pasta grafiğinin ikincil bölümünün boyutunu yüzde olarak alır.

 **Remarks:** 

Şu tiplerin [ChartSeriesType.PIE\_OF\_PIE](../../com.aspose.words/chartseriestype/\#PIE-OF-PIE) ve [ChartSeriesType.PIE\_OF\_BAR](../../com.aspose.words/chartseriestype/\#PIE-OF-BAR) serileri gruplarına uygulanır.

Kabul edilebilir değer aralığı 5 ile 200 arasındadır (her iki uç dahil). Varsayılan değer 75'tir.

 **Examples:** 

pie of Pie grafiğinin nasıl oluşturulacağını ve biçimlendirileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.PIE_OF_PIE, 440.0, 300.0);
 Chart chart = shape.getChart();
 // Delete the default generated series.
 chart.getSeries().clear();

 String[] categories = new String[] { "Category 1", "Category 2", "Category 3", "Category 4" };
 chart.getSeries().add("Series 1", categories, new double[] { 11.0, 8.0, 4.0, 3.0 });

 // Format the Pie of Pie chart.
 ChartSeriesGroup seriesGroup = chart.getSeriesGroups().get(0);
 seriesGroup.setGapWidth(10);
 seriesGroup.setSecondSectionSize(77);

 doc.save(getArtifactsDir() + "Charts.PieOfPieChart.docx");
 
```

**Returns:**
int - Pie grafiğinin ikincil bölümünün yüzde olarak boyutu.
### getSeries() {#getSeries}
```
public ChartSeriesCollection getSeries()
```


Bu seri grubuna ait serilerin bir koleksiyonunu alır.

 **Examples:** 

Grafiğin ikincil ekseniyle nasıl çalışılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 450.0, 250.0);
 Chart chart = shape.getChart();
 ChartSeriesCollection series = chart.getSeries();

 // Delete default generated series.
 series.clear();

 String[] categories = new String[] { "Category 1", "Category 2", "Category 3" };
 series.add("Series 1 of primary series group", categories, new double[] { 2.0, 3.0, 4.0 });
 series.add("Series 2 of primary series group", categories, new double[] { 5.0, 2.0, 3.0 });

 // Create an additional series group, also of the line type.
 ChartSeriesGroup newSeriesGroup = chart.getSeriesGroups().add(ChartSeriesType.LINE);
 // Specify the use of secondary axes for the new series group.
 newSeriesGroup.setAxisGroup(AxisGroup.SECONDARY);
 // Hide the secondary X axis.
 newSeriesGroup.getAxisX().setHidden(true);
 // Define title of the secondary Y axis.
 newSeriesGroup.getAxisY().getTitle().setShow(true);
 newSeriesGroup.getAxisY().getTitle().setText("Secondary Y axis");

 Assert.assertEquals(ChartSeriesType.LINE, newSeriesGroup.getSeriesType());

 // Add a series to the new series group.
 ChartSeries series3 =
         newSeriesGroup.getSeries().add("Series of secondary series group", categories, new double[] { 13.0, 11.0, 16.0 });
 series3.getFormat().getStroke().setWeight(3.5);

 doc.save(getArtifactsDir() + "Charts.SecondaryAxis.docx");
 
```

**Returns:**
[ChartSeriesCollection](../../com.aspose.words/chartseriescollection/) - A collection of series that belong to this series group.
### getSeriesType() {#getSeriesType}
```
public int getSeriesType()
```


Bu grupta bulunan grafik serisi tipini alır.

 **Examples:** 

Grafiğin ikincil ekseniyle nasıl çalışılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 450.0, 250.0);
 Chart chart = shape.getChart();
 ChartSeriesCollection series = chart.getSeries();

 // Delete default generated series.
 series.clear();

 String[] categories = new String[] { "Category 1", "Category 2", "Category 3" };
 series.add("Series 1 of primary series group", categories, new double[] { 2.0, 3.0, 4.0 });
 series.add("Series 2 of primary series group", categories, new double[] { 5.0, 2.0, 3.0 });

 // Create an additional series group, also of the line type.
 ChartSeriesGroup newSeriesGroup = chart.getSeriesGroups().add(ChartSeriesType.LINE);
 // Specify the use of secondary axes for the new series group.
 newSeriesGroup.setAxisGroup(AxisGroup.SECONDARY);
 // Hide the secondary X axis.
 newSeriesGroup.getAxisX().setHidden(true);
 // Define title of the secondary Y axis.
 newSeriesGroup.getAxisY().getTitle().setShow(true);
 newSeriesGroup.getAxisY().getTitle().setText("Secondary Y axis");

 Assert.assertEquals(ChartSeriesType.LINE, newSeriesGroup.getSeriesType());

 // Add a series to the new series group.
 ChartSeries series3 =
         newSeriesGroup.getSeries().add("Series of secondary series group", categories, new double[] { 13.0, 11.0, 16.0 });
 series3.getFormat().getStroke().setWeight(3.5);

 doc.save(getArtifactsDir() + "Charts.SecondaryAxis.docx");
 
```

**Returns:**
int - Bu grupta bulunan grafik serisi türü. Döndürülen değer, [ChartSeriesType](../../com.aspose.words/chartseriestype/) sabitlerinden biridir.
### setAxisGroup(int value) {#setAxisGroup-int}
```
public void setAxisGroup(int value)
```


Bu seri grubunun ait olduğu eksen grubunu ayarlar.

 **Examples:** 

Grafiğin ikincil ekseniyle nasıl çalışılacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 450.0, 250.0);
 Chart chart = shape.getChart();
 ChartSeriesCollection series = chart.getSeries();

 // Delete default generated series.
 series.clear();

 String[] categories = new String[] { "Category 1", "Category 2", "Category 3" };
 series.add("Series 1 of primary series group", categories, new double[] { 2.0, 3.0, 4.0 });
 series.add("Series 2 of primary series group", categories, new double[] { 5.0, 2.0, 3.0 });

 // Create an additional series group, also of the line type.
 ChartSeriesGroup newSeriesGroup = chart.getSeriesGroups().add(ChartSeriesType.LINE);
 // Specify the use of secondary axes for the new series group.
 newSeriesGroup.setAxisGroup(AxisGroup.SECONDARY);
 // Hide the secondary X axis.
 newSeriesGroup.getAxisX().setHidden(true);
 // Define title of the secondary Y axis.
 newSeriesGroup.getAxisY().getTitle().setShow(true);
 newSeriesGroup.getAxisY().getTitle().setText("Secondary Y axis");

 Assert.assertEquals(ChartSeriesType.LINE, newSeriesGroup.getSeriesType());

 // Add a series to the new series group.
 ChartSeries series3 =
         newSeriesGroup.getSeries().add("Series of secondary series group", categories, new double[] { 13.0, 11.0, 16.0 });
 series3.getFormat().getStroke().setWeight(3.5);

 doc.save(getArtifactsDir() + "Charts.SecondaryAxis.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| value | int | Bu seriler grubunun ait olduğu eksen grubu. Değer, [AxisGroup](../../com.aspose.words/axisgroup/) sabitlerinden biri olmalıdır. |

### setBubbleScale(int value) {#setBubbleScale-int}
```
public void setBubbleScale(int value)
```


Kabarcıkların boyutunu varsayılan boyutlarının yüzdesi olarak ayarlar.

 **Remarks:** 

Yalnızca [ChartSeriesType.BUBBLE](../../com.aspose.words/chartseriestype/\#BUBBLE) ve [ChartSeriesType.BUBBLE\_3\_D](../../com.aspose.words/chartseriestype/\#BUBBLE-3-D) tipindeki seri gruplarına uygulanır.

Kabul edilebilir değer aralığı 0 ile 300 arasındadır (her iki uç dahil). Varsayılan değer 100'dür.

 **Examples:** 

Kabarcıkların boyutunun nasıl ayarlanacağını göster.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a bubble 3D chart.
 Shape shape = builder.insertChart(ChartType.BUBBLE_3_D, 450.0, 250.0);
 ChartSeriesGroup seriesGroup = shape.getChart().getSeriesGroups().get(0);

 // Set bubble scale to 200%.
 seriesGroup.setBubbleScale(200);

 doc.save(getArtifactsDir() + "Charts.BubbleScale.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Baloncukların varsayılan boyutlarına göre yüzde olarak boyutu. |

### setDoughnutHoleSize(int value) {#setDoughnutHoleSize-int}
```
public void setDoughnutHoleSize(int value)
```


Üst döner grafiğin delik boyutunu yüzde olarak ayarlar.

 **Remarks:** 

Yalnızca [ChartSeriesType.DOUGHNUT](../../com.aspose.words/chartseriestype/\#DOUGHNUT) tipindeki seri gruplarına uygulanır.

Kabul edilebilir değer aralığı 0 ile 90 arasındadır (her iki uç dahil). Varsayılan değer 75'tir.

 **Examples:** 

Doughnut grafiğinin nasıl oluşturulacağını ve biçimlendirileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.DOUGHNUT, 400.0, 400.0);
 Chart chart = shape.getChart();
 // Delete the default generated series.
 chart.getSeries().clear();

 String[] categories = new String[] { "Category 1", "Category 2", "Category 3" };
 chart.getSeries().add("Series 1", categories, new double[] { 4.0, 2.0, 5.0 });

 // Format the Doughnut chart.
 ChartSeriesGroup seriesGroup = chart.getSeriesGroups().get(0);
 seriesGroup.setDoughnutHoleSize(10);
 seriesGroup.setFirstSliceAngle(270);

 doc.save(getArtifactsDir() + "Charts.DoughnutChart.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Üst doughnut grafiğinin delik boyutu yüzde olarak. |

### setFirstSliceAngle(int value) {#setFirstSliceAngle-int}
```
public void setFirstSliceAngle(int value)
```


Üst pasta grafiğinin ilk diliminin açısını derece cinsinden ayarlar.

 **Remarks:** 

Şu tiplerin [ChartSeriesType.PIE](../../com.aspose.words/chartseriestype/\#PIE), [ChartSeriesType.PIE\_3\_D](../../com.aspose.words/chartseriestype/\#PIE-3-D) ve [ChartSeriesType.DOUGHNUT](../../com.aspose.words/chartseriestype/\#DOUGHNUT) serileri gruplarına uygulanır.

Kabul edilebilir değer aralığı 0 ile 360 arasındadır (her iki uç dahil). Varsayılan değer 0'dır.

 **Examples:** 

Doughnut grafiğinin nasıl oluşturulacağını ve biçimlendirileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.DOUGHNUT, 400.0, 400.0);
 Chart chart = shape.getChart();
 // Delete the default generated series.
 chart.getSeries().clear();

 String[] categories = new String[] { "Category 1", "Category 2", "Category 3" };
 chart.getSeries().add("Series 1", categories, new double[] { 4.0, 2.0, 5.0 });

 // Format the Doughnut chart.
 ChartSeriesGroup seriesGroup = chart.getSeriesGroups().get(0);
 seriesGroup.setDoughnutHoleSize(10);
 seriesGroup.setFirstSliceAngle(270);

 doc.save(getArtifactsDir() + "Charts.DoughnutChart.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Üst pie grafiğinin ilk diliminin açısı, derece cinsinden. |

### setGapWidth(int value) {#setGapWidth-int}
```
public void setGapWidth(int value)
```


Grafik öğeleri arasındaki boşluk genişliğinin yüzdesini ayarlar.

 **Remarks:** 

Yalnızca bar, sütun, pie-of-bar, pie-of-pie, histogram, box&whisker, waterfall ve funnel tiplerinin serileri gruplarına uygulanır.

Kabul edilebilir değer aralığı 0 ile 500 arasındadır (her iki uç dahil). Bar/sütun tabanlı serileri grupları için, özellik çubuk kümeleri arasındaki boşluğu genişliklerinin yüzde olarak temsil eder. Pie-of-pie ve bar-of-pie grafiklerinde ise bu, birincil ve ikincil bölümler arasındaki boşluktur.

 **Examples:** 

Boşluk genişliği ve üst üste binmeyi nasıl yapılandıracağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 450.0, 250.0);
 ChartSeriesGroup seriesGroup = shape.getChart().getSeriesGroups().get(0);

 // Set column gap width and overlap.
 seriesGroup.setGapWidth(450);
 seriesGroup.setOverlap(-75);

 doc.save(getArtifactsDir() + "Charts.ConfigureGapOverlap.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Grafik öğeleri arasındaki boşluk genişliğinin yüzdesi. |

### setOverlap(int value) {#setOverlap-int}
```
public void setOverlap(int value)
```


Seri çubukları veya sütunlarının ne kadar üst üste bindiğinin yüzdesini ayarlar.

 **Remarks:** 

Tüm bar ve sütun tiplerinin serileri gruplarına uygulanır.

Kabul edilebilir değer aralığı -100 ile 100 arasındadır (her iki uç dahil). 0 değeri, çubuklar/sütunlar arasında boşluk olmadığını gösterir. Değer -100 ise, çubuklar/sütunlar arasındaki mesafe genişliklerine eşittir. 100 değeri, çubukların/sütunların tamamen üst üste bindiğini ifade eder.

 **Examples:** 

Boşluk genişliği ve üst üste binmeyi nasıl yapılandıracağınızı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 450.0, 250.0);
 ChartSeriesGroup seriesGroup = shape.getChart().getSeriesGroups().get(0);

 // Set column gap width and overlap.
 seriesGroup.setGapWidth(450);
 seriesGroup.setOverlap(-75);

 doc.save(getArtifactsDir() + "Charts.ConfigureGapOverlap.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Serilerin çubukları veya sütunlarının ne kadar üst üste bindiğinin yüzdesi. |

### setSecondSectionSize(int value) {#setSecondSectionSize-int}
```
public void setSecondSectionSize(int value)
```


Pasta grafiğinin ikincil bölümünün boyutunu yüzde olarak ayarlar.

 **Remarks:** 

Şu tiplerin [ChartSeriesType.PIE\_OF\_PIE](../../com.aspose.words/chartseriestype/\#PIE-OF-PIE) ve [ChartSeriesType.PIE\_OF\_BAR](../../com.aspose.words/chartseriestype/\#PIE-OF-BAR) serileri gruplarına uygulanır.

Kabul edilebilir değer aralığı 5 ile 200 arasındadır (her iki uç dahil). Varsayılan değer 75'tir.

 **Examples:** 

pie of Pie grafiğinin nasıl oluşturulacağını ve biçimlendirileceğini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.PIE_OF_PIE, 440.0, 300.0);
 Chart chart = shape.getChart();
 // Delete the default generated series.
 chart.getSeries().clear();

 String[] categories = new String[] { "Category 1", "Category 2", "Category 3", "Category 4" };
 chart.getSeries().add("Series 1", categories, new double[] { 11.0, 8.0, 4.0, 3.0 });

 // Format the Pie of Pie chart.
 ChartSeriesGroup seriesGroup = chart.getSeriesGroups().get(0);
 seriesGroup.setGapWidth(10);
 seriesGroup.setSecondSectionSize(77);

 doc.save(getArtifactsDir() + "Charts.PieOfPieChart.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| değer | int | Pie grafiğinin ikincil bölümünün yüzde olarak boyutu. |

