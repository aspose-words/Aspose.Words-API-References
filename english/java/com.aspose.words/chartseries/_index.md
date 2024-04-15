---
title: ChartSeries
linktitle: ChartSeries
second_title: Aspose.Words for Java
description: Represents chart series properties in Java.
type: docs
weight: 76
url: /java/com.aspose.words/chartseries/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
[com.aspose.words.IChartDataPoint](../../com.aspose.words/ichartdatapoint/), java.lang.Cloneable
```
public class ChartSeries implements IChartDataPoint, Cloneable
```

Represents chart series properties.

To learn more, visit the [ Working with Charts ][Working with Charts] documentation article.

 **Examples:** 

Shows how to apply labels to data points in a line chart.

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

     // For a cleaner looking graph, we can remove data labels individually.
     chart.getSeries().get(1).getDataLabels().get(2).clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     for (int i = 0; i < labelsCount; i++) {
         series.hasDataLabels(true);

         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         series.getDataLabels().get(i).isHidden(false);
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
## Methods

| Method | Description |
| --- | --- |
| [add(ChartXValue xValue)](#add-com.aspose.words.ChartXValue) | Adds the specified X value to the chart series. |
| [add(ChartXValue xValue, ChartYValue yValue)](#add-com.aspose.words.ChartXValue-com.aspose.words.ChartYValue) | Adds the specified X and Y values to the chart series. |
| [add(ChartXValue xValue, ChartYValue yValue, double bubbleSize)](#add-com.aspose.words.ChartXValue-com.aspose.words.ChartYValue-double) | Adds the specified X value, Y value and bubble size to the chart series. |
| [clear()](#clear) | Removes all data values from the chart series. |
| [clearValues()](#clearValues) | Removes all data values from the chart series with preserving the format of the data points and data labels. |
| [copyFormatFrom(int dataPointIndex)](#copyFormatFrom-int) | Copies default data point format from the data point with the specified index. |
| [getBubble3D()](#getBubble3D) | Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them. |
| [getBubbleSizes()](#getBubbleSizes) | Gets a collection of bubble sizes for this chart series. |
| [getDataLabels()](#getDataLabels) | Specifies the settings for the data labels for the entire series. |
| [getDataPoints()](#getDataPoints) | Returns a collection of formatting objects for all data points in this series. |
| [getExplosion()](#getExplosion) | Specifies the amount the data point shall be moved from the center of the pie. |
| [getFormat()](#getFormat) | Provides access to fill and line formatting of the series. |
| [getInvertIfNegative()](#getInvertIfNegative) | Specifies whether the parent element shall inverts its colors if the value is negative. |
| [getLegendEntry()](#getLegendEntry) | Gets a legend entry for this chart series. |
| [getMarker()](#getMarker) | Specifies a data marker. |
| [getName()](#getName) | Gets the name of the series, if name is not set explicitly it is generated using index. |
| [getSeriesType()](#getSeriesType) | Gets the type of this chart series. |
| [getSmooth()](#getSmooth) | Allows to specify whether the line connecting the points on the chart shall be smoothed using Catmull-Rom splines. |
| [getXValues()](#getXValues) | Gets a collection of X values for this chart series. |
| [getYValues()](#getYValues) | Gets a collection of Y values for this chart series. |
| [hasDataLabels()](#hasDataLabels) | Gets a flag indicating whether data labels are displayed for the series. |
| [hasDataLabels(boolean value)](#hasDataLabels-boolean) | Sets a flag indicating whether data labels are displayed for the series. |
| [insert(int index, ChartXValue xValue)](#insert-int-com.aspose.words.ChartXValue) | Inserts the specified X value into the chart series at the specified index. |
| [insert(int index, ChartXValue xValue, ChartYValue yValue)](#insert-int-com.aspose.words.ChartXValue-com.aspose.words.ChartYValue) | Inserts the specified X and Y values into the chart series at the specified index. |
| [insert(int index, ChartXValue xValue, ChartYValue yValue, double bubbleSize)](#insert-int-com.aspose.words.ChartXValue-com.aspose.words.ChartYValue-double) | Inserts the specified X value, Y value and bubble size into the chart series at the specified index. |
| [remove(int index)](#remove-int) | Removes the X value, Y value, and bubble size, if supported, from the chart series at the specified index. |
| [setBubble3D(boolean value)](#setBubble3D-boolean) | Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them. |
| [setExplosion(int value)](#setExplosion-int) | Specifies the amount the data point shall be moved from the center of the pie. |
| [setInvertIfNegative(boolean value)](#setInvertIfNegative-boolean) | Specifies whether the parent element shall inverts its colors if the value is negative. |
| [setName(String value)](#setName-java.lang.String) | Sets the name of the series, if name is not set explicitly it is generated using index. |
| [setSmooth(boolean value)](#setSmooth-boolean) | Allows to specify whether the line connecting the points on the chart shall be smoothed using Catmull-Rom splines. |
### add(ChartXValue xValue) {#add-com.aspose.words.ChartXValue}
```
public void add(ChartXValue xValue)
```


Adds the specified X value to the chart series. If the series supports Y values and bubble sizes, they will be empty for the X value.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| xValue | [ChartXValue](../../com.aspose.words/chartxvalue/) |  |

### add(ChartXValue xValue, ChartYValue yValue) {#add-com.aspose.words.ChartXValue-com.aspose.words.ChartYValue}
```
public void add(ChartXValue xValue, ChartYValue yValue)
```


Adds the specified X and Y values to the chart series.

 **Examples:** 

Shows how to add/remove chart data values.

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

Shows how to populate chart series with data.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder();

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeries series1 = chart.getSeries().get(0);

 // Clear X and Y values of the first series.
 series1.clearValues();

 // Populate the series with data.
 series1.add(ChartXValue.fromDouble(3.0), ChartYValue.fromDouble(10.0));
 series1.add(ChartXValue.fromDouble(5.0), ChartYValue.fromDouble(5.0));
 series1.add(ChartXValue.fromDouble(7.0), ChartYValue.fromDouble(11.0));
 series1.add(ChartXValue.fromDouble(9.0), ChartYValue.fromDouble(17.0));

 ChartSeries series2 = chart.getSeries().get(1);

 // Clear X and Y values of the second series.
 series2.clearValues();

 // Populate the series with data.
 series2.add(ChartXValue.fromDouble(2.0), ChartYValue.fromDouble(4.0));
 series2.add(ChartXValue.fromDouble(4.0), ChartYValue.fromDouble(7.0));
 series2.add(ChartXValue.fromDouble(6.0), ChartYValue.fromDouble(14.0));
 series2.add(ChartXValue.fromDouble(8.0), ChartYValue.fromDouble(7.0));

 doc.save(getArtifactsDir() + "Charts.PopulateChartWithData.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| xValue | [ChartXValue](../../com.aspose.words/chartxvalue/) |  |
| yValue | [ChartYValue](../../com.aspose.words/chartyvalue/) |  |

### add(ChartXValue xValue, ChartYValue yValue, double bubbleSize) {#add-com.aspose.words.ChartXValue-com.aspose.words.ChartYValue-double}
```
public void add(ChartXValue xValue, ChartYValue yValue, double bubbleSize)
```


Adds the specified X value, Y value and bubble size to the chart series.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| xValue | [ChartXValue](../../com.aspose.words/chartxvalue/) |  |
| yValue | [ChartYValue](../../com.aspose.words/chartyvalue/) |  |
| bubbleSize | double |  |

### clear() {#clear}
```
public void clear()
```


Removes all data values from the chart series. Format of all individual data points and data labels is cleared.

### clearValues() {#clearValues}
```
public void clearValues()
```


Removes all data values from the chart series with preserving the format of the data points and data labels.

### copyFormatFrom(int dataPointIndex) {#copyFormatFrom-int}
```
public void copyFormatFrom(int dataPointIndex)
```


Copies default data point format from the data point with the specified index.

 **Examples:** 

Shows how to copy data point format.

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
| Parameter | Type | Description |
| --- | --- | --- |
| dataPointIndex | int |  |

### getBubble3D() {#getBubble3D}
```
public boolean getBubble3D()
```


Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them.

**Returns:**
boolean - The corresponding  boolean  value.
### getBubbleSizes() {#getBubbleSizes}
```
public BubbleSizeCollection getBubbleSizes()
```


Gets a collection of bubble sizes for this chart series.

**Returns:**
[BubbleSizeCollection](../../com.aspose.words/bubblesizecollection/) - A collection of bubble sizes for this chart series.
### getDataLabels() {#getDataLabels}
```
public ChartDataLabelCollection getDataLabels()
```


Specifies the settings for the data labels for the entire series.

 **Examples:** 

Shows how to apply labels to data points in a line chart.

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

     // For a cleaner looking graph, we can remove data labels individually.
     chart.getSeries().get(1).getDataLabels().get(2).clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     for (int i = 0; i < labelsCount; i++) {
         series.hasDataLabels(true);

         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         series.getDataLabels().get(i).isHidden(false);
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


Returns a collection of formatting objects for all data points in this series.

 **Examples:** 

Shows how to apply labels to data points in a line chart.

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

     // For a cleaner looking graph, we can remove data labels individually.
     chart.getSeries().get(1).getDataLabels().get(2).clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     for (int i = 0; i < labelsCount; i++) {
         series.hasDataLabels(true);

         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         series.getDataLabels().get(i).isHidden(false);
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


Specifies the amount the data point shall be moved from the center of the pie. Can be negative, negative means that property is not set and no explosion should be applied. Applies only to Pie charts.

**Returns:**
int - The corresponding  int  value.
### getFormat() {#getFormat}
```
public ChartFormat getFormat()
```


Provides access to fill and line formatting of the series.

 **Examples:** 

Sows how to set series color.

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


Specifies whether the parent element shall inverts its colors if the value is negative.

**Returns:**
boolean - The corresponding  boolean  value.
### getLegendEntry() {#getLegendEntry}
```
public ChartLegendEntry getLegendEntry()
```


Gets a legend entry for this chart series.

**Returns:**
[ChartLegendEntry](../../com.aspose.words/chartlegendentry/) - A legend entry for this chart series.
### getMarker() {#getMarker}
```
public ChartMarker getMarker()
```


Specifies a data marker. Marker is automatically created when requested.

**Returns:**
[ChartMarker](../../com.aspose.words/chartmarker/) - The corresponding [ChartMarker](../../com.aspose.words/chartmarker/) value.
### getName() {#getName}
```
public String getName()
```


Gets the name of the series, if name is not set explicitly it is generated using index. By default returns Series plus one based index.

 **Examples:** 

Shows how to apply labels to data points in a line chart.

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

     // For a cleaner looking graph, we can remove data labels individually.
     chart.getSeries().get(1).getDataLabels().get(2).clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     for (int i = 0; i < labelsCount; i++) {
         series.hasDataLabels(true);

         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         series.getDataLabels().get(i).isHidden(false);
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
java.lang.String - The name of the series, if name is not set explicitly it is generated using index.
### getSeriesType() {#getSeriesType}
```
public int getSeriesType()
```


Gets the type of this chart series.

 **Examples:** 

Shows how to remove specific chart serie.

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
int - The type of this chart series. The returned value is one of [ChartSeriesType](../../com.aspose.words/chartseriestype/) constants.
### getSmooth() {#getSmooth}
```
public boolean getSmooth()
```


Allows to specify whether the line connecting the points on the chart shall be smoothed using Catmull-Rom splines.

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
boolean - The corresponding  boolean  value.
### getXValues() {#getXValues}
```
public ChartXValueCollection getXValues()
```


Gets a collection of X values for this chart series.

**Returns:**
[ChartXValueCollection](../../com.aspose.words/chartxvaluecollection/) - A collection of X values for this chart series.
### getYValues() {#getYValues}
```
public ChartYValueCollection getYValues()
```


Gets a collection of Y values for this chart series.

**Returns:**
[ChartYValueCollection](../../com.aspose.words/chartyvaluecollection/) - A collection of Y values for this chart series.
### hasDataLabels() {#hasDataLabels}
```
public boolean hasDataLabels()
```


Gets a flag indicating whether data labels are displayed for the series.

**Returns:**
boolean - A flag indicating whether data labels are displayed for the series.
### hasDataLabels(boolean value) {#hasDataLabels-boolean}
```
public void hasDataLabels(boolean value)
```


Sets a flag indicating whether data labels are displayed for the series.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether data labels are displayed for the series. |

### insert(int index, ChartXValue xValue) {#insert-int-com.aspose.words.ChartXValue}
```
public void insert(int index, ChartXValue xValue)
```


Inserts the specified X value into the chart series at the specified index. If the series supports Y values and bubble sizes, they will be empty for the X value.

 **Remarks:** 

The corresponding data point with default formatting will be inserted into the data point collection. And, if data labels are displayed, the corresponding data label with default formatting will be inserted too.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |
| xValue | [ChartXValue](../../com.aspose.words/chartxvalue/) |  |

### insert(int index, ChartXValue xValue, ChartYValue yValue) {#insert-int-com.aspose.words.ChartXValue-com.aspose.words.ChartYValue}
```
public void insert(int index, ChartXValue xValue, ChartYValue yValue)
```


Inserts the specified X and Y values into the chart series at the specified index.

 **Remarks:** 

The corresponding data point with default formatting will be inserted into the data point collection. And, if data labels are displayed, the corresponding data label with default formatting will be inserted too.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |
| xValue | [ChartXValue](../../com.aspose.words/chartxvalue/) |  |
| yValue | [ChartYValue](../../com.aspose.words/chartyvalue/) |  |

### insert(int index, ChartXValue xValue, ChartYValue yValue, double bubbleSize) {#insert-int-com.aspose.words.ChartXValue-com.aspose.words.ChartYValue-double}
```
public void insert(int index, ChartXValue xValue, ChartYValue yValue, double bubbleSize)
```


Inserts the specified X value, Y value and bubble size into the chart series at the specified index.

 **Remarks:** 

The corresponding data point with default formatting will be inserted into the data point collection. And, if data labels are displayed, the corresponding data label with default formatting will be inserted too.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |
| xValue | [ChartXValue](../../com.aspose.words/chartxvalue/) |  |
| yValue | [ChartYValue](../../com.aspose.words/chartyvalue/) |  |
| bubbleSize | double |  |

### remove(int index) {#remove-int}
```
public void remove(int index)
```


Removes the X value, Y value, and bubble size, if supported, from the chart series at the specified index. The corresponding data point and data label are also removed.

 **Examples:** 

Shows how to add/remove chart data values.

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
| Parameter | Type | Description |
| --- | --- | --- |
| index | int |  |

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

### setName(String value) {#setName-java.lang.String}
```
public void setName(String value)
```


Sets the name of the series, if name is not set explicitly it is generated using index. By default returns Series plus one based index.

 **Examples:** 

Shows how to apply labels to data points in a line chart.

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

     // For a cleaner looking graph, we can remove data labels individually.
     chart.getSeries().get(1).getDataLabels().get(2).clearFormat();

     // We can also strip an entire series of its data labels at once.
     chart.getSeries().get(2).getDataLabels().clearFormat();

     doc.save(getArtifactsDir() + "Charts.DataLabels.docx");
 }

 /// 
 /// Apply data labels with custom number format and separator to several data points in a series.
 /// 
 private static void applyDataLabels(ChartSeries series, int labelsCount, String numberFormat, String separator) {
     for (int i = 0; i < labelsCount; i++) {
         series.hasDataLabels(true);

         Assert.assertFalse(series.getDataLabels().get(i).isVisible());

         series.getDataLabels().get(i).setShowCategoryName(true);
         series.getDataLabels().get(i).setShowSeriesName(true);
         series.getDataLabels().get(i).setShowValue(true);
         series.getDataLabels().get(i).setShowLeaderLines(true);
         series.getDataLabels().get(i).setShowLegendKey(true);
         series.getDataLabels().get(i).setShowPercentage(false);
         series.getDataLabels().get(i).isHidden(false);
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
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of the series, if name is not set explicitly it is generated using index. |

### setSmooth(boolean value) {#setSmooth-boolean}
```
public void setSmooth(boolean value)
```


Allows to specify whether the line connecting the points on the chart shall be smoothed using Catmull-Rom splines.

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

