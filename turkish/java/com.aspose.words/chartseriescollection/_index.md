---
title: "ChartSeriesCollection"
linktitle: "ChartSeriesCollection"
second_title: "Aspose.Words Java için"
description: "Java'da bir ChartSeries koleksiyonunu temsil eder."
type: docs
weight: 86
url: /tr/java/com.aspose.words/chartseriescollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartSeriesCollection implements Iterable
```

Bir [ChartSeries](../../com.aspose.words/chartseries/) koleksiyonunu temsil eder.

Daha fazla bilgi için, [ Working with Charts ][Working with Charts] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

Bir grafikte seri verilerini ekleme ve kaldırma yöntemini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a column chart that will contain three series of demo data by default.
 Shape chartShape = builder.insertChart(ChartType.COLUMN, 400.0, 300.0);
 Chart chart = chartShape.getChart();

 // Each series has four decimal values: one for each of the four categories.
 // Four clusters of three columns will represent this data.
 ChartSeriesCollection chartData = chart.getSeries();

 Assert.assertEquals(3, chartData.getCount());

 // Print the name of every series in the chart.
 Iterator enumerator = chart.getSeries().iterator();
 while (enumerator.hasNext()) {
     System.out.println(enumerator.next().getName());
 }

 // These are the names of the categories in the chart.
 String[] categories = {"Category 1", "Category 2", "Category 3", "Category 4"};

 // We can add a series with new values for existing categories.
 // This chart will now contain four clusters of four columns.
 chart.getSeries().add("Series 4", categories, new double[]{4.4, 7.0, 3.5, 2.1});
 // A chart series can also be removed by index, like this.
 // This will remove one of the three demo series that came with the chart.
 chartData.removeAt(2);

 Assert.assertFalse(IterableUtils.matchesAny(chartData, s -> s.getName() == "Series 3"));
 // We can also clear all the chart's data at once with this method.
 // When creating a new chart, this is the way to wipe all the demo data
 // before we can begin working on a blank chart.
 chartData.clear();
 
```


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [add(String seriesName, ChartMultilevelValue[] categories, double[] values)](#add-java.lang.String-com.aspose.words.ChartMultilevelValue---double) | Bu koleksiyona yeni bir [ChartSeries](../../com.aspose.words/chartseries/) ekler. |
| [add(String seriesName, double[] xValues)](#add-java.lang.String-double) | Bu koleksiyona yeni bir [ChartSeries](../../com.aspose.words/chartseries/) ekler. |
| [add(String seriesName, double[] xValues, double[] yValues)](#add-java.lang.String-double---double) | Bu koleksiyona yeni bir [ChartSeries](../../com.aspose.words/chartseries/) ekler. |
| [add(String seriesName, double[] xValues, double[] yValues, double[] bubbleSizes)](#add-java.lang.String-double---double---double) | Bu koleksiyona yeni bir [ChartSeries](../../com.aspose.words/chartseries/) ekler. |
| [add(String seriesName, String[] categories, double[] values)](#add-java.lang.String-java.lang.String---double) | Bu koleksiyona yeni bir [ChartSeries](../../com.aspose.words/chartseries/) ekler. |
| [add(String seriesName, String[] categories, double[] values, boolean[] isSubtotal)](#add-java.lang.String-java.lang.String---double---boolean) | Bu koleksiyona yeni bir [ChartSeries](../../com.aspose.words/chartseries/) ekler. |
| [add(String seriesName, Date[] dates, double[] values)](#add-java.lang.String-java.util.Date---double) | Bu koleksiyona yeni bir [ChartSeries](../../com.aspose.words/chartseries/) ekler. |
| [clear()](#clear) | Bu koleksiyondan tüm [ChartSeries](../../com.aspose.words/chartseries/) öğelerini kaldırır. |
| [get(int index)](#get-int) | Belirtilen indeksteki bir [ChartSeries](../../com.aspose.words/chartseries/) döndürür. |
| [getCount()](#getCount) | Bu koleksiyondaki [ChartSeries](../../com.aspose.words/chartseries/) sayısını döndürür. |
| [iterator()](#iterator) | Bir enumerator nesnesi döndürür. |
| [removeAt(int index)](#removeAt-int) | Belirtilen indeksteki bir [ChartSeries](../../com.aspose.words/chartseries/) kaldırır. |
### add(String seriesName, ChartMultilevelValue[] categories, double[] values) {#add-java.lang.String-com.aspose.words.ChartMultilevelValue---double}
```
public ChartSeries add(String seriesName, ChartMultilevelValue[] categories, double[] values)
```


Bu koleksiyona yeni bir [ChartSeries](../../com.aspose.words/chartseries/) ekler. Çok seviyeli veri kategorilerine sahip serileri eklemek için bu yöntemi kullanın.

 **Examples:** 

Ağaç haritası grafiği oluşturmayı gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a Treemap chart.
 Shape shape = builder.insertChart(ChartType.TREEMAP, 450.0, 280.0);
 Chart chart = shape.getChart();
 chart.getTitle().setText("World Population");

 // Delete default generated series.
 chart.getSeries().clear();

 // Add a series.
 ChartSeries series = chart.getSeries().add(
         "Population by Region",
         new ChartMultilevelValue[]
                 {
                         new ChartMultilevelValue("Asia", "China"),
                         new ChartMultilevelValue("Asia", "India"),
                         new ChartMultilevelValue("Asia", "Indonesia"),
                         new ChartMultilevelValue("Asia", "Pakistan"),
                         new ChartMultilevelValue("Asia", "Bangladesh"),
                         new ChartMultilevelValue("Asia", "Japan"),
                         new ChartMultilevelValue("Asia", "Philippines"),
                         new ChartMultilevelValue("Asia", "Other"),
                         new ChartMultilevelValue("Africa", "Nigeria"),
                         new ChartMultilevelValue("Africa", "Ethiopia"),
                         new ChartMultilevelValue("Africa", "Egypt"),
                         new ChartMultilevelValue("Africa", "Other"),
                         new ChartMultilevelValue("Europe", "Russia"),
                         new ChartMultilevelValue("Europe", "Germany"),
                         new ChartMultilevelValue("Europe", "Other"),
                         new ChartMultilevelValue("Latin America", "Brazil"),
                         new ChartMultilevelValue("Latin America", "Mexico"),
                         new ChartMultilevelValue("Latin America", "Other"),
                         new ChartMultilevelValue("Northern America", "United States", "Other"),
                         new ChartMultilevelValue("Northern America", "Other"),
                         new ChartMultilevelValue("Oceania")
                 },
         new double[]
                 {
                         1409670000.0, 1400744000.0, 279118866.0, 241499431.0, 169828911.0, 123930000.0, 112892781.0, 764000000.0,
                         223800000.0, 107334000.0, 105914499.0, 903000000.0,
                         146150789.0, 84607016.0, 516000000.0,
                         203080756.0, 129713690.0, 310000000.0,
                         335893238.0, 35000000.0,
                         42000000.0
                 });

 // Show data labels.
 series.hasDataLabels(true);
 series.getDataLabels().setShowValue(true);
 series.getDataLabels().setShowCategoryName(true);
 DecimalFormatSymbols symbols = new DecimalFormatSymbols(Locale.getDefault());
 String thousandSeparator = Character.toString(symbols.getGroupingSeparator());
 series.getDataLabels().getNumberFormat().setFormatCode(String.format("#{0}0", thousandSeparator));

 doc.save(getArtifactsDir() + "Charts.Treemap.docx");
 
```

Sunburst (güneş patlaması) grafiği oluşturma yöntemini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a Sunburst chart.
 Shape shape = builder.insertChart(ChartType.SUNBURST, 450.0, 450.0);
 Chart chart = shape.getChart();
 chart.getTitle().setText("Sales");

 // Delete default generated series.
 chart.getSeries().clear();

 // Add a series.
 ChartSeries series = chart.getSeries().add(
         "Sales",
         new ChartMultilevelValue[]
                 {
                         new ChartMultilevelValue("Sales - Europe", "UK", "London Dep."),
                         new ChartMultilevelValue("Sales - Europe", "UK", "Liverpool Dep."),
                         new ChartMultilevelValue("Sales - Europe", "UK", "Manchester Dep."),
                         new ChartMultilevelValue("Sales - Europe", "France", "Paris Dep."),
                         new ChartMultilevelValue("Sales - Europe", "France", "Lyon Dep."),
                         new ChartMultilevelValue("Sales - NA", "USA", "Denver Dep."),
                         new ChartMultilevelValue("Sales - NA", "USA", "Seattle Dep."),
                         new ChartMultilevelValue("Sales - NA", "USA", "Detroit Dep."),
                         new ChartMultilevelValue("Sales - NA", "USA", "Houston Dep."),
                         new ChartMultilevelValue("Sales - NA", "Canada", "Toronto Dep."),
                         new ChartMultilevelValue("Sales - NA", "Canada", "Montreal Dep."),
                         new ChartMultilevelValue("Sales - Oceania", "Australia", "Sydney Dep."),
                         new ChartMultilevelValue("Sales - Oceania", "New Zealand", "Auckland Dep.")
                 },
         new double[] { 1236.0, 851.0, 536.0, 468.0, 179.0, 527.0, 799.0, 1148.0, 921.0, 457.0, 482.0, 761.0, 694.0 });

 // Show data labels.
 series.hasDataLabels(true);
 series.getDataLabels().setShowValue(false);
 series.getDataLabels().setShowCategoryName(true);

 doc.save(getArtifactsDir() + "Charts.Sunburst.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| seriesName | java.lang.String |  |
| categories | [ChartMultilevelValue\[\]](../../com.aspose.words/chartmultilevelvalue/) |  |
| değerler | double[] |  |

**Returns:**
[ChartSeries](../../com.aspose.words/chartseries/) - Recently added [ChartSeries](../../com.aspose.words/chartseries/) object.
### add(String seriesName, double[] xValues) {#add-java.lang.String-double}
```
public ChartSeries add(String seriesName, double[] xValues)
```


Bu koleksiyona yeni bir [ChartSeries](../../com.aspose.words/chartseries/) ekler. Histogram grafiklerine seri eklemek için bu yöntemi kullanın.

 **Remarks:** 

Histogram dışındaki grafik türleri için bu yöntem, boş Y değerlerine sahip bir seri ekler.

 **Examples:** 

Histogram grafiği oluşturma yöntemini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a Histogram chart.
 Shape shape = builder.insertChart(ChartType.HISTOGRAM, 450.0, 450.0);
 Chart chart = shape.getChart();
 chart.getTitle().setText("Avg Temperature since 1991");

 // Delete default generated series.
 chart.getSeries().clear();

 // Add a series.
 chart.getSeries().add(
         "Avg Temperature",
         new double[]
                 {
                         51.8, 53.6, 50.3, 54.7, 53.9, 54.3, 53.4, 52.9, 53.3, 53.7, 53.8, 52.0, 55.0, 52.1, 53.4,
                         53.8, 53.8, 51.9, 52.1, 52.7, 51.8, 56.6, 53.3, 55.6, 56.3, 56.2, 56.1, 56.2, 53.6, 55.7,
                         56.3, 55.9, 55.6
                 });

 doc.save(getArtifactsDir() + "Charts.Histogram.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| seriesName | java.lang.String |  |
| xValues | double[] |  |

**Returns:**
[ChartSeries](../../com.aspose.words/chartseries/) - Recently added [ChartSeries](../../com.aspose.words/chartseries/) object.
### add(String seriesName, double[] xValues, double[] yValues) {#add-java.lang.String-double---double}
```
public ChartSeries add(String seriesName, double[] xValues, double[] yValues)
```


Bu koleksiyona yeni bir [ChartSeries](../../com.aspose.words/chartseries/) ekler. Bu yöntemi, herhangi bir Scatter grafik türüne seri eklemek için kullanın.

 **Examples:** 

Bir grafik türü için uygun bir grafik serisi tipinin nasıl oluşturulacağını gösterir.

```

 public void chartSeriesCollection() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // There are several ways of populating a chart's series collection.
     // Different series schemas are intended for different chart types.
     // 1 -  Column chart with columns grouped and banded along the X-axis by category:
     Chart chart = appendChart(builder, ChartType.COLUMN, 500.0, 300.0);

     String[] categories = {"Category 1", "Category 2", "Category 3"};

     // Insert two series of decimal values containing a value for each respective category.
     // This column chart will have three groups, each with two columns.
     chart.getSeries().add("Series 1", categories, new double[]{76.6, 82.1, 91.6});
     chart.getSeries().add("Series 2", categories, new double[]{64.2, 79.5, 94.0});

     // Categories are distributed along the X-axis, and values are distributed along the Y-axis.
     Assert.assertEquals(ChartAxisType.CATEGORY, chart.getAxisX().getType());
     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisY().getType());

     // 2 -  Area chart with dates distributed along the X-axis:
     chart = appendChart(builder, ChartType.AREA, 500.0, 300.0);

     Date[] dates = {DocumentHelper.createDate(2014, 3, 31),
             DocumentHelper.createDate(2017, 1, 23),
             DocumentHelper.createDate(2017, 6, 18),
             DocumentHelper.createDate(2019, 11, 22),
             DocumentHelper.createDate(2020, 9, 7)
     };

     // Insert a series with a decimal value for each respective date.
     // The dates will be distributed along a linear X-axis,
     // and the values added to this series will create data points.
     chart.getSeries().add("Series 1", dates, new double[]{15.8, 21.5, 22.9, 28.7, 33.1});

     Assert.assertEquals(ChartAxisType.CATEGORY, chart.getAxisX().getType());
     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisY().getType());

     // 3 -  2D scatter plot:
     chart = appendChart(builder, ChartType.SCATTER, 500.0, 300.0);

     // Each series will need two decimal arrays of equal length.
     // The first array contains X-values, and the second contains corresponding Y-values
     // of data points on the chart's graph.
     chart.getSeries().add("Series 1",
             new double[]{3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6},
             new double[]{3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9});
     chart.getSeries().add("Series 2",
             new double[]{2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3},
             new double[]{7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6});

     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisX().getType());
     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisY().getType());

     // 4 -  Bubble chart:
     chart = appendChart(builder, ChartType.BUBBLE, 500.0, 300.0);

     // Each series will need three decimal arrays of equal length.
     // The first array contains X-values, the second contains corresponding Y-values,
     // and the third contains diameters for each of the graph's data points.
     chart.getSeries().add("Series 1",
             new double[]{1.1, 5.0, 9.8},
             new double[]{1.2, 4.9, 9.9},
             new double[]{2.0, 4.0, 8.0});

     doc.save(getArtifactsDir() + "Charts.ChartSeriesCollection.docx");
 }

 /// 
 /// Insert a chart using a document builder of a specified ChartType, width and height, and remove its demo data.
 /// 
 private static Chart appendChart(DocumentBuilder builder, int chartType, double width, double height) throws Exception {
     Shape chartShape = builder.insertChart(chartType, width, height);
     Chart chart = chartShape.getChart();
     chart.getSeries().clear();
     return chart;
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| seriesName | java.lang.String |  |
| xValues | double[] |  |
| yValues | double[] |  |

**Returns:**
[ChartSeries](../../com.aspose.words/chartseries/) - Recently added [ChartSeries](../../com.aspose.words/chartseries/) object.
### add(String seriesName, double[] xValues, double[] yValues, double[] bubbleSizes) {#add-java.lang.String-double---double---double}
```
public ChartSeries add(String seriesName, double[] xValues, double[] yValues, double[] bubbleSizes)
```


Bu koleksiyona yeni bir [ChartSeries](../../com.aspose.words/chartseries/) ekler. Bu yöntemi, herhangi bir Bubble grafik türüne seri eklemek için kullanın.

 **Examples:** 

Bir grafik türü için uygun bir grafik serisi tipinin nasıl oluşturulacağını gösterir.

```

 public void chartSeriesCollection() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // There are several ways of populating a chart's series collection.
     // Different series schemas are intended for different chart types.
     // 1 -  Column chart with columns grouped and banded along the X-axis by category:
     Chart chart = appendChart(builder, ChartType.COLUMN, 500.0, 300.0);

     String[] categories = {"Category 1", "Category 2", "Category 3"};

     // Insert two series of decimal values containing a value for each respective category.
     // This column chart will have three groups, each with two columns.
     chart.getSeries().add("Series 1", categories, new double[]{76.6, 82.1, 91.6});
     chart.getSeries().add("Series 2", categories, new double[]{64.2, 79.5, 94.0});

     // Categories are distributed along the X-axis, and values are distributed along the Y-axis.
     Assert.assertEquals(ChartAxisType.CATEGORY, chart.getAxisX().getType());
     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisY().getType());

     // 2 -  Area chart with dates distributed along the X-axis:
     chart = appendChart(builder, ChartType.AREA, 500.0, 300.0);

     Date[] dates = {DocumentHelper.createDate(2014, 3, 31),
             DocumentHelper.createDate(2017, 1, 23),
             DocumentHelper.createDate(2017, 6, 18),
             DocumentHelper.createDate(2019, 11, 22),
             DocumentHelper.createDate(2020, 9, 7)
     };

     // Insert a series with a decimal value for each respective date.
     // The dates will be distributed along a linear X-axis,
     // and the values added to this series will create data points.
     chart.getSeries().add("Series 1", dates, new double[]{15.8, 21.5, 22.9, 28.7, 33.1});

     Assert.assertEquals(ChartAxisType.CATEGORY, chart.getAxisX().getType());
     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisY().getType());

     // 3 -  2D scatter plot:
     chart = appendChart(builder, ChartType.SCATTER, 500.0, 300.0);

     // Each series will need two decimal arrays of equal length.
     // The first array contains X-values, and the second contains corresponding Y-values
     // of data points on the chart's graph.
     chart.getSeries().add("Series 1",
             new double[]{3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6},
             new double[]{3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9});
     chart.getSeries().add("Series 2",
             new double[]{2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3},
             new double[]{7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6});

     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisX().getType());
     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisY().getType());

     // 4 -  Bubble chart:
     chart = appendChart(builder, ChartType.BUBBLE, 500.0, 300.0);

     // Each series will need three decimal arrays of equal length.
     // The first array contains X-values, the second contains corresponding Y-values,
     // and the third contains diameters for each of the graph's data points.
     chart.getSeries().add("Series 1",
             new double[]{1.1, 5.0, 9.8},
             new double[]{1.2, 4.9, 9.9},
             new double[]{2.0, 4.0, 8.0});

     doc.save(getArtifactsDir() + "Charts.ChartSeriesCollection.docx");
 }

 /// 
 /// Insert a chart using a document builder of a specified ChartType, width and height, and remove its demo data.
 /// 
 private static Chart appendChart(DocumentBuilder builder, int chartType, double width, double height) throws Exception {
     Shape chartShape = builder.insertChart(chartType, width, height);
     Chart chart = chartShape.getChart();
     chart.getSeries().clear();
     return chart;
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| seriesName | java.lang.String |  |
| xValues | double[] |  |
| yValues | double[] |  |
| bubbleSizes | double[] |  |

**Returns:**
[ChartSeries](../../com.aspose.words/chartseries/) - Recently added [ChartSeries](../../com.aspose.words/chartseries/) object.
### add(String seriesName, String[] categories, double[] values) {#add-java.lang.String-java.lang.String---double}
```
public ChartSeries add(String seriesName, String[] categories, double[] values)
```


Bu koleksiyona yeni bir [ChartSeries](../../com.aspose.words/chartseries/) ekler. Bu yöntemi, Bar, Column, Line ve Surface grafiklerinin herhangi bir türüne seri eklemek için kullanın.

 **Examples:** 

Bir grafik türü için uygun bir grafik serisi tipinin nasıl oluşturulacağını gösterir.

```

 public void chartSeriesCollection() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // There are several ways of populating a chart's series collection.
     // Different series schemas are intended for different chart types.
     // 1 -  Column chart with columns grouped and banded along the X-axis by category:
     Chart chart = appendChart(builder, ChartType.COLUMN, 500.0, 300.0);

     String[] categories = {"Category 1", "Category 2", "Category 3"};

     // Insert two series of decimal values containing a value for each respective category.
     // This column chart will have three groups, each with two columns.
     chart.getSeries().add("Series 1", categories, new double[]{76.6, 82.1, 91.6});
     chart.getSeries().add("Series 2", categories, new double[]{64.2, 79.5, 94.0});

     // Categories are distributed along the X-axis, and values are distributed along the Y-axis.
     Assert.assertEquals(ChartAxisType.CATEGORY, chart.getAxisX().getType());
     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisY().getType());

     // 2 -  Area chart with dates distributed along the X-axis:
     chart = appendChart(builder, ChartType.AREA, 500.0, 300.0);

     Date[] dates = {DocumentHelper.createDate(2014, 3, 31),
             DocumentHelper.createDate(2017, 1, 23),
             DocumentHelper.createDate(2017, 6, 18),
             DocumentHelper.createDate(2019, 11, 22),
             DocumentHelper.createDate(2020, 9, 7)
     };

     // Insert a series with a decimal value for each respective date.
     // The dates will be distributed along a linear X-axis,
     // and the values added to this series will create data points.
     chart.getSeries().add("Series 1", dates, new double[]{15.8, 21.5, 22.9, 28.7, 33.1});

     Assert.assertEquals(ChartAxisType.CATEGORY, chart.getAxisX().getType());
     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisY().getType());

     // 3 -  2D scatter plot:
     chart = appendChart(builder, ChartType.SCATTER, 500.0, 300.0);

     // Each series will need two decimal arrays of equal length.
     // The first array contains X-values, and the second contains corresponding Y-values
     // of data points on the chart's graph.
     chart.getSeries().add("Series 1",
             new double[]{3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6},
             new double[]{3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9});
     chart.getSeries().add("Series 2",
             new double[]{2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3},
             new double[]{7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6});

     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisX().getType());
     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisY().getType());

     // 4 -  Bubble chart:
     chart = appendChart(builder, ChartType.BUBBLE, 500.0, 300.0);

     // Each series will need three decimal arrays of equal length.
     // The first array contains X-values, the second contains corresponding Y-values,
     // and the third contains diameters for each of the graph's data points.
     chart.getSeries().add("Series 1",
             new double[]{1.1, 5.0, 9.8},
             new double[]{1.2, 4.9, 9.9},
             new double[]{2.0, 4.0, 8.0});

     doc.save(getArtifactsDir() + "Charts.ChartSeriesCollection.docx");
 }

 /// 
 /// Insert a chart using a document builder of a specified ChartType, width and height, and remove its demo data.
 /// 
 private static Chart appendChart(DocumentBuilder builder, int chartType, double width, double height) throws Exception {
     Shape chartShape = builder.insertChart(chartType, width, height);
     Chart chart = chartShape.getChart();
     chart.getSeries().clear();
     return chart;
 }
 
```

Pareto grafiğinin nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a Pareto chart.
 Shape shape = builder.insertChart(ChartType.PARETO, 450.0, 450.0);
 Chart chart = shape.getChart();
 chart.getTitle().setText("Best-Selling Car");

 // Delete default generated series.
 chart.getSeries().clear();

 // Add a series.
 chart.getSeries().add(
         "Best-Selling Car",
         new String[] { "Tesla Model Y", "Toyota Corolla", "Toyota RAV4", "Ford F-Series", "Honda CR-V" },
         new double[] { 1.43, 0.91, 1.17, 0.98, 0.85 });

 doc.save(getArtifactsDir() + "Charts.Pareto.docx");
 
```

Kutu ve bıyık grafiğinin nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a Box & Whisker chart.
 Shape shape = builder.insertChart(ChartType.BOX_AND_WHISKER, 450.0, 450.0);
 Chart chart = shape.getChart();
 chart.getTitle().setText("Points by Years");

 // Delete default generated series.
 chart.getSeries().clear();

 // Add a series.
 ChartSeries series = chart.getSeries().add(
         "Points by Years",
         new String[]
                 {
                         "WC", "WC", "WC", "WC", "WC", "WC", "WC", "WC", "WC", "WC",
                         "NR", "NR", "NR", "NR", "NR", "NR", "NR", "NR", "NR", "NR",
                         "NA", "NA", "NA", "NA", "NA", "NA", "NA", "NA", "NA", "NA"
                 },
         new double[]
                 {
                         91.0, 80.0, 100.0, 77.0, 90.0, 104.0, 105.0, 118.0, 120.0, 101.0,
                         114.0, 107.0, 110.0, 60.0, 79.0, 78.0, 77.0, 102.0, 101.0, 113.0,
                         94.0, 93.0, 84.0, 71.0, 80.0, 103.0, 80.0, 94.0, 100.0, 101.0
                 });

 // Show data labels.
 series.hasDataLabels(true);

 doc.save(getArtifactsDir() + "Charts.BoxAndWhisker.docx");
 
```

Huni grafiğinin nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a Funnel chart.
 Shape shape = builder.insertChart(ChartType.FUNNEL, 450.0, 450.0);
 Chart chart = shape.getChart();
 chart.getTitle().setText("Population by Age Group");

 // Delete default generated series.
 chart.getSeries().clear();

 // Add a series.
 ChartSeries series = chart.getSeries().add(
         "Population by Age Group",
         new String[] { "0-9", "10-19", "20-29", "30-39", "40-49", "50-59", "60-69", "70-79", "80-89", "90-" },
         new double[] { 0.121, 0.128, 0.132, 0.146, 0.124, 0.124, 0.111, 0.075, 0.032, 0.007 });

 // Show data labels.
 series.hasDataLabels(true);
 DecimalFormatSymbols symbols = new DecimalFormatSymbols(Locale.getDefault());
 String decimalSeparator = Character.toString(symbols.getGroupingSeparator());
 series.getDataLabels().getNumberFormat().setFormatCode("0" + decimalSeparator + "0%");

 doc.save(getArtifactsDir() + "Charts.Funnel.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| seriesName | java.lang.String |  |
| categories | java.lang.String[] |  |
| değerler | double[] |  |

**Returns:**
[ChartSeries](../../com.aspose.words/chartseries/) - Recently added [ChartSeries](../../com.aspose.words/chartseries/) object.
### add(String seriesName, String[] categories, double[] values, boolean[] isSubtotal) {#add-java.lang.String-java.lang.String---double---boolean}
```
public ChartSeries add(String seriesName, String[] categories, double[] values, boolean[] isSubtotal)
```


Bu koleksiyona yeni bir [ChartSeries](../../com.aspose.words/chartseries/) ekler. Bu yöntemi, Waterfall grafiklerine seri eklemek için kullanın.

 **Remarks:** 

Waterfall dışındaki grafik türleri için,  isSubtotal  değerleri göz ardı edilir.

 **Examples:** 

Waterfall grafiğinin nasıl oluşturulacağını gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a Waterfall chart.
 Shape shape = builder.insertChart(ChartType.WATERFALL, 450.0, 450.0);
 Chart chart = shape.getChart();
 chart.getTitle().setText("New Zealand GDP");

 // Delete default generated series.
 chart.getSeries().clear();

 // Add a series.
 ChartSeries series = chart.getSeries().add(
         "New Zealand GDP",
         new String[] { "2018", "2019 growth", "2020 growth", "2020", "2021 growth", "2022 growth", "2022" },
         new double[] { 100.0, 0.57, -0.25, 100.32, 20.22, -2.92, 117.62 },
         new boolean[] { true, false, false, true, false, false, true });

 // Show data labels.
 series.hasDataLabels(true);

 doc.save(getArtifactsDir() + "Charts.Waterfall.docx");
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| seriesName | java.lang.String | Eklenecek serinin adı. |
| categories | java.lang.String[] | X ekseni için kategori adları. |
| değerler | double[] | Y ekseni değerleri. |
| isSubtotal | boolean[] | İlgili Y değerinin bir ara toplam olup olmadığını gösteren değerler. |

**Returns:**
[ChartSeries](../../com.aspose.words/chartseries/) - Recently added [ChartSeries](../../com.aspose.words/chartseries/) object.
### add(String seriesName, Date[] dates, double[] values) {#add-java.lang.String-java.util.Date---double}
```
public ChartSeries add(String seriesName, Date[] dates, double[] values)
```


Bu koleksiyona yeni bir [ChartSeries](../../com.aspose.words/chartseries/) ekler. Bu yöntemi, Area, Radar ve Stock grafiklerinin herhangi bir türüne seri eklemek için kullanın.

 **Examples:** 

Bir grafik türü için uygun bir grafik serisi tipinin nasıl oluşturulacağını gösterir.

```

 public void chartSeriesCollection() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // There are several ways of populating a chart's series collection.
     // Different series schemas are intended for different chart types.
     // 1 -  Column chart with columns grouped and banded along the X-axis by category:
     Chart chart = appendChart(builder, ChartType.COLUMN, 500.0, 300.0);

     String[] categories = {"Category 1", "Category 2", "Category 3"};

     // Insert two series of decimal values containing a value for each respective category.
     // This column chart will have three groups, each with two columns.
     chart.getSeries().add("Series 1", categories, new double[]{76.6, 82.1, 91.6});
     chart.getSeries().add("Series 2", categories, new double[]{64.2, 79.5, 94.0});

     // Categories are distributed along the X-axis, and values are distributed along the Y-axis.
     Assert.assertEquals(ChartAxisType.CATEGORY, chart.getAxisX().getType());
     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisY().getType());

     // 2 -  Area chart with dates distributed along the X-axis:
     chart = appendChart(builder, ChartType.AREA, 500.0, 300.0);

     Date[] dates = {DocumentHelper.createDate(2014, 3, 31),
             DocumentHelper.createDate(2017, 1, 23),
             DocumentHelper.createDate(2017, 6, 18),
             DocumentHelper.createDate(2019, 11, 22),
             DocumentHelper.createDate(2020, 9, 7)
     };

     // Insert a series with a decimal value for each respective date.
     // The dates will be distributed along a linear X-axis,
     // and the values added to this series will create data points.
     chart.getSeries().add("Series 1", dates, new double[]{15.8, 21.5, 22.9, 28.7, 33.1});

     Assert.assertEquals(ChartAxisType.CATEGORY, chart.getAxisX().getType());
     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisY().getType());

     // 3 -  2D scatter plot:
     chart = appendChart(builder, ChartType.SCATTER, 500.0, 300.0);

     // Each series will need two decimal arrays of equal length.
     // The first array contains X-values, and the second contains corresponding Y-values
     // of data points on the chart's graph.
     chart.getSeries().add("Series 1",
             new double[]{3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6},
             new double[]{3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9});
     chart.getSeries().add("Series 2",
             new double[]{2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3},
             new double[]{7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6});

     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisX().getType());
     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisY().getType());

     // 4 -  Bubble chart:
     chart = appendChart(builder, ChartType.BUBBLE, 500.0, 300.0);

     // Each series will need three decimal arrays of equal length.
     // The first array contains X-values, the second contains corresponding Y-values,
     // and the third contains diameters for each of the graph's data points.
     chart.getSeries().add("Series 1",
             new double[]{1.1, 5.0, 9.8},
             new double[]{1.2, 4.9, 9.9},
             new double[]{2.0, 4.0, 8.0});

     doc.save(getArtifactsDir() + "Charts.ChartSeriesCollection.docx");
 }

 /// 
 /// Insert a chart using a document builder of a specified ChartType, width and height, and remove its demo data.
 /// 
 private static Chart appendChart(DocumentBuilder builder, int chartType, double width, double height) throws Exception {
     Shape chartShape = builder.insertChart(chartType, width, height);
     Chart chart = chartShape.getChart();
     chart.getSeries().clear();
     return chart;
 }
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| seriesName | java.lang.String |  |
| dates | java.util.Date[] |  |
| değerler | double[] |  |

**Returns:**
[ChartSeries](../../com.aspose.words/chartseries/)
### clear() {#clear}
```
public void clear()
```


Bu koleksiyondan tüm [ChartSeries](../../com.aspose.words/chartseries/) öğelerini kaldırır.

 **Examples:** 

Bir grafikte seri verilerini ekleme ve kaldırma yöntemini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a column chart that will contain three series of demo data by default.
 Shape chartShape = builder.insertChart(ChartType.COLUMN, 400.0, 300.0);
 Chart chart = chartShape.getChart();

 // Each series has four decimal values: one for each of the four categories.
 // Four clusters of three columns will represent this data.
 ChartSeriesCollection chartData = chart.getSeries();

 Assert.assertEquals(3, chartData.getCount());

 // Print the name of every series in the chart.
 Iterator enumerator = chart.getSeries().iterator();
 while (enumerator.hasNext()) {
     System.out.println(enumerator.next().getName());
 }

 // These are the names of the categories in the chart.
 String[] categories = {"Category 1", "Category 2", "Category 3", "Category 4"};

 // We can add a series with new values for existing categories.
 // This chart will now contain four clusters of four columns.
 chart.getSeries().add("Series 4", categories, new double[]{4.4, 7.0, 3.5, 2.1});
 // A chart series can also be removed by index, like this.
 // This will remove one of the three demo series that came with the chart.
 chartData.removeAt(2);

 Assert.assertFalse(IterableUtils.matchesAny(chartData, s -> s.getName() == "Series 3"));
 // We can also clear all the chart's data at once with this method.
 // When creating a new chart, this is the way to wipe all the demo data
 // before we can begin working on a blank chart.
 chartData.clear();
 
```

### get(int index) {#get-int}
```
public ChartSeries get(int index)
```


Belirtilen indeksteki bir [ChartSeries](../../com.aspose.words/chartseries/) döndürür.

 **Remarks:** 

Dizin sıfır tabanlıdır.

Negatif dizinlere izin verilir ve koleksiyonun sonundan erişimi gösterir. Örneğin -1 son öğeyi, -2 sondan bir önceki öğeyi ve böyle devam eder.

Eğer dizin listedeki öğe sayısına eşit veya daha büyükse, bu null referans döndürür.

Eğer dizin negatifse ve mutlak değeri listedeki öğe sayısından büyükse, bu null referans döndürür.

 **Examples:** 

Bir grafikte seri verilerini ekleme ve kaldırma yöntemini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a column chart that will contain three series of demo data by default.
 Shape chartShape = builder.insertChart(ChartType.COLUMN, 400.0, 300.0);
 Chart chart = chartShape.getChart();

 // Each series has four decimal values: one for each of the four categories.
 // Four clusters of three columns will represent this data.
 ChartSeriesCollection chartData = chart.getSeries();

 Assert.assertEquals(3, chartData.getCount());

 // Print the name of every series in the chart.
 Iterator enumerator = chart.getSeries().iterator();
 while (enumerator.hasNext()) {
     System.out.println(enumerator.next().getName());
 }

 // These are the names of the categories in the chart.
 String[] categories = {"Category 1", "Category 2", "Category 3", "Category 4"};

 // We can add a series with new values for existing categories.
 // This chart will now contain four clusters of four columns.
 chart.getSeries().add("Series 4", categories, new double[]{4.4, 7.0, 3.5, 2.1});
 // A chart series can also be removed by index, like this.
 // This will remove one of the three demo series that came with the chart.
 chartData.removeAt(2);

 Assert.assertFalse(IterableUtils.matchesAny(chartData, s -> s.getName() == "Series 3"));
 // We can also clear all the chart's data at once with this method.
 // When creating a new chart, this is the way to wipe all the demo data
 // before we can begin working on a blank chart.
 chartData.clear();
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| indeks | int | Koleksiyona ait bir indeks. |

**Returns:**
[ChartSeries](../../com.aspose.words/chartseries/) - A [ChartSeries](../../com.aspose.words/chartseries/) at the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Bu koleksiyondaki [ChartSeries](../../com.aspose.words/chartseries/) sayısını döndürür.

 **Examples:** 

Bir grafikte seri verilerini ekleme ve kaldırma yöntemini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a column chart that will contain three series of demo data by default.
 Shape chartShape = builder.insertChart(ChartType.COLUMN, 400.0, 300.0);
 Chart chart = chartShape.getChart();

 // Each series has four decimal values: one for each of the four categories.
 // Four clusters of three columns will represent this data.
 ChartSeriesCollection chartData = chart.getSeries();

 Assert.assertEquals(3, chartData.getCount());

 // Print the name of every series in the chart.
 Iterator enumerator = chart.getSeries().iterator();
 while (enumerator.hasNext()) {
     System.out.println(enumerator.next().getName());
 }

 // These are the names of the categories in the chart.
 String[] categories = {"Category 1", "Category 2", "Category 3", "Category 4"};

 // We can add a series with new values for existing categories.
 // This chart will now contain four clusters of four columns.
 chart.getSeries().add("Series 4", categories, new double[]{4.4, 7.0, 3.5, 2.1});
 // A chart series can also be removed by index, like this.
 // This will remove one of the three demo series that came with the chart.
 chartData.removeAt(2);

 Assert.assertFalse(IterableUtils.matchesAny(chartData, s -> s.getName() == "Series 3"));
 // We can also clear all the chart's data at once with this method.
 // When creating a new chart, this is the way to wipe all the demo data
 // before we can begin working on a blank chart.
 chartData.clear();
 
```

**Returns:**
int - Bu koleksiyondaki [ChartSeries](../../com.aspose.words/chartseries/) sayısı.
### iterator() {#iterator}
```
public Iterator iterator()
```


Bir enumerator nesnesi döndürür.

 **Examples:** 

Bir grafikte seri verilerini ekleme ve kaldırma yöntemini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a column chart that will contain three series of demo data by default.
 Shape chartShape = builder.insertChart(ChartType.COLUMN, 400.0, 300.0);
 Chart chart = chartShape.getChart();

 // Each series has four decimal values: one for each of the four categories.
 // Four clusters of three columns will represent this data.
 ChartSeriesCollection chartData = chart.getSeries();

 Assert.assertEquals(3, chartData.getCount());

 // Print the name of every series in the chart.
 Iterator enumerator = chart.getSeries().iterator();
 while (enumerator.hasNext()) {
     System.out.println(enumerator.next().getName());
 }

 // These are the names of the categories in the chart.
 String[] categories = {"Category 1", "Category 2", "Category 3", "Category 4"};

 // We can add a series with new values for existing categories.
 // This chart will now contain four clusters of four columns.
 chart.getSeries().add("Series 4", categories, new double[]{4.4, 7.0, 3.5, 2.1});
 // A chart series can also be removed by index, like this.
 // This will remove one of the three demo series that came with the chart.
 chartData.removeAt(2);

 Assert.assertFalse(IterableUtils.matchesAny(chartData, s -> s.getName() == "Series 3"));
 // We can also clear all the chart's data at once with this method.
 // When creating a new chart, this is the way to wipe all the demo data
 // before we can begin working on a blank chart.
 chartData.clear();
 
```

**Returns:**
java.util.Iterator
### removeAt(int index) {#removeAt-int}
```
public void removeAt(int index)
```


Belirtilen indeksteki bir [ChartSeries](../../com.aspose.words/chartseries/) kaldırır.

 **Examples:** 

Bir grafikte seri verilerini ekleme ve kaldırma yöntemini gösterir.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a column chart that will contain three series of demo data by default.
 Shape chartShape = builder.insertChart(ChartType.COLUMN, 400.0, 300.0);
 Chart chart = chartShape.getChart();

 // Each series has four decimal values: one for each of the four categories.
 // Four clusters of three columns will represent this data.
 ChartSeriesCollection chartData = chart.getSeries();

 Assert.assertEquals(3, chartData.getCount());

 // Print the name of every series in the chart.
 Iterator enumerator = chart.getSeries().iterator();
 while (enumerator.hasNext()) {
     System.out.println(enumerator.next().getName());
 }

 // These are the names of the categories in the chart.
 String[] categories = {"Category 1", "Category 2", "Category 3", "Category 4"};

 // We can add a series with new values for existing categories.
 // This chart will now contain four clusters of four columns.
 chart.getSeries().add("Series 4", categories, new double[]{4.4, 7.0, 3.5, 2.1});
 // A chart series can also be removed by index, like this.
 // This will remove one of the three demo series that came with the chart.
 chartData.removeAt(2);

 Assert.assertFalse(IterableUtils.matchesAny(chartData, s -> s.getName() == "Series 3"));
 // We can also clear all the chart's data at once with this method.
 // When creating a new chart, this is the way to wipe all the demo data
 // before we can begin working on a blank chart.
 chartData.clear();
 
```

**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| index | int | Kaldırılacak [ChartSeries](../../com.aspose.words/chartseries/) öğesinin sıfır tabanlı indeksi. |

