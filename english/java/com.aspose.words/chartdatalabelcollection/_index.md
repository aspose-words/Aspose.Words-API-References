---
title: ChartDataLabelCollection
linktitle: ChartDataLabelCollection
second_title: Aspose.Words for Java
description: Represents a collection of ChartDataLabel in Java.
type: docs
weight: 61
url: /java/com.aspose.words/chartdatalabelcollection/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Iterable
```
public class ChartDataLabelCollection implements Iterable
```

Represents a collection of [ChartDataLabel](../../com.aspose.words/chartdatalabel/).

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
| [clearFormat()](#clearFormat) | Clears format of all [ChartDataLabel](../../com.aspose.words/chartdatalabel/) in this collection. |
| [get(int index)](#get-int) | Returns [ChartDataLabel](../../com.aspose.words/chartdatalabel/) for the specified index. |
| [getCount()](#getCount) | Returns the number of [ChartDataLabel](../../com.aspose.words/chartdatalabel/) in this collection. |
| [getFont()](#getFont) | Provides access to the font formatting of the data labels of the entire series. |
| [getNumberFormat()](#getNumberFormat) | Gets an [ChartNumberFormat](../../com.aspose.words/chartnumberformat/) instance allowing to set number format for the data labels of the entire series. |
| [getSeparator()](#getSeparator) | Gets string separator used for the data labels of the entire series. |
| [getShowBubbleSize()](#getShowBubbleSize) | Allows to specify whether bubble size is to be displayed for the data labels of the entire series. |
| [getShowCategoryName()](#getShowCategoryName) | Allows to specify whether category name is to be displayed for the data labels of the entire series. |
| [getShowDataLabelsRange()](#getShowDataLabelsRange) | Allows to specify whether values from data labels range to be displayed in the data labels of the entire series. |
| [getShowLeaderLines()](#getShowLeaderLines) | Allows to specify whether data label leader lines need be shown for the data labels of the entire series. |
| [getShowLegendKey()](#getShowLegendKey) | Allows to specify whether legend key is to be displayed for the data labels of the entire series. |
| [getShowPercentage()](#getShowPercentage) | Allows to specify whether percentage value is to be displayed for the data labels of the entire series. |
| [getShowSeriesName()](#getShowSeriesName) | Gets a Boolean to indicate the series name display behavior for the data labels of the entire series. |
| [getShowValue()](#getShowValue) | Allows to specify whether values are to be displayed in the data labels of the entire series. |
| [isInherited()](#isInherited) |  |
| [iterator()](#iterator) | Returns an enumerator object. |
| [setSeparator(String value)](#setSeparator-java.lang.String) | Sets string separator used for the data labels of the entire series. |
| [setShowBubbleSize(boolean value)](#setShowBubbleSize-boolean) | Allows to specify whether bubble size is to be displayed for the data labels of the entire series. |
| [setShowCategoryName(boolean value)](#setShowCategoryName-boolean) | Allows to specify whether category name is to be displayed for the data labels of the entire series. |
| [setShowDataLabelsRange(boolean value)](#setShowDataLabelsRange-boolean) | Allows to specify whether values from data labels range to be displayed in the data labels of the entire series. |
| [setShowLeaderLines(boolean value)](#setShowLeaderLines-boolean) | Allows to specify whether data label leader lines need be shown for the data labels of the entire series. |
| [setShowLegendKey(boolean value)](#setShowLegendKey-boolean) | Allows to specify whether legend key is to be displayed for the data labels of the entire series. |
| [setShowPercentage(boolean value)](#setShowPercentage-boolean) | Allows to specify whether percentage value is to be displayed for the data labels of the entire series. |
| [setShowSeriesName(boolean value)](#setShowSeriesName-boolean) | Sets a Boolean to indicate the series name display behavior for the data labels of the entire series. |
| [setShowValue(boolean value)](#setShowValue-boolean) | Allows to specify whether values are to be displayed in the data labels of the entire series. |
### clearFormat() {#clearFormat}
```
public void clearFormat()
```


Clears format of all [ChartDataLabel](../../com.aspose.words/chartdatalabel/) in this collection.

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

### get(int index) {#get-int}
```
public ChartDataLabel get(int index)
```


Returns [ChartDataLabel](../../com.aspose.words/chartdatalabel/) for the specified index.

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
| index | int |  |

**Returns:**
[ChartDataLabel](../../com.aspose.words/chartdatalabel/) - [ChartDataLabel](../../com.aspose.words/chartdatalabel/) for the specified index.
### getCount() {#getCount}
```
public int getCount()
```


Returns the number of [ChartDataLabel](../../com.aspose.words/chartdatalabel/) in this collection.

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
int - The number of [ChartDataLabel](../../com.aspose.words/chartdatalabel/) in this collection.
### getFont() {#getFont}
```
public Font getFont()
```


Provides access to the font formatting of the data labels of the entire series.

 **Remarks:** 

Value defined for this property can be overridden for an individual data label with using the [ChartDataLabel.getFont()](../../com.aspose.words/chartdatalabel/\#getFont) property.

 **Examples:** 

Shows how to enable and configure data labels for a chart series.

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
[Font](../../com.aspose.words/font/) - The corresponding [Font](../../com.aspose.words/font/) value.
### getNumberFormat() {#getNumberFormat}
```
public ChartNumberFormat getNumberFormat()
```


Gets an [ChartNumberFormat](../../com.aspose.words/chartnumberformat/) instance allowing to set number format for the data labels of the entire series.

 **Examples:** 

Shows how to enable and configure data labels for a chart series.

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
[ChartNumberFormat](../../com.aspose.words/chartnumberformat/) - An [ChartNumberFormat](../../com.aspose.words/chartnumberformat/) instance allowing to set number format for the data labels of the entire series.
### getSeparator() {#getSeparator}
```
public String getSeparator()
```


Gets string separator used for the data labels of the entire series. The default is a comma, except for pie charts showing only category name and percentage, when a line break shall be used instead.

 **Remarks:** 

Value defined for this property can be overridden for an individual data label with using the [ChartDataLabel.getSeparator()](../../com.aspose.words/chartdatalabel/\#getSeparator) / [ChartDataLabel.setSeparator(java.lang.String)](../../com.aspose.words/chartdatalabel/\#setSeparator-java.lang.String) property.

 **Examples:** 

Shows how to work with data labels of a bubble chart.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.BUBBLE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series with X/Y coordinates and diameter of each of the bubbles.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new double[]{2.9, 3.5, 1.1, 4.0, 4.0},
         new double[]{1.9, 8.5, 2.1, 6.0, 1.5},
         new double[]{9.0, 4.5, 2.5, 8.0, 5.0});

 // Enable data labels, and then modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowBubbleSize(true);
 dataLabels.setShowCategoryName(true);
 dataLabels.setShowSeriesName(true);
 dataLabels.setSeparator(" & ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsBubbleChart.docx");
 
```

Shows how to work with data labels of a pie chart.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.PIE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a custom chart series with a category name for each of the sectors, and their frequency table.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel"},
         new double[]{2.7, 3.2, 0.8});

 // Enable data labels that will display both percentage and frequency of each sector, and modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowLeaderLines(true);
 dataLabels.setShowLegendKey(true);
 dataLabels.setShowPercentage(true);
 dataLabels.setShowValue(true);
 dataLabels.setSeparator("; ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsPieChart.docx");
 
```

**Returns:**
java.lang.String - String separator used for the data labels of the entire series.
### getShowBubbleSize() {#getShowBubbleSize}
```
public boolean getShowBubbleSize()
```


Allows to specify whether bubble size is to be displayed for the data labels of the entire series. Applies only to Bubble charts. Default value is  false .

 **Remarks:** 

Value defined for this property can be overridden for an individual data label with using the [ChartDataLabel.getShowBubbleSize()](../../com.aspose.words/chartdatalabel/\#getShowBubbleSize) / [ChartDataLabel.setShowBubbleSize(boolean)](../../com.aspose.words/chartdatalabel/\#setShowBubbleSize-boolean) property.

 **Examples:** 

Shows how to work with data labels of a bubble chart.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.BUBBLE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series with X/Y coordinates and diameter of each of the bubbles.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new double[]{2.9, 3.5, 1.1, 4.0, 4.0},
         new double[]{1.9, 8.5, 2.1, 6.0, 1.5},
         new double[]{9.0, 4.5, 2.5, 8.0, 5.0});

 // Enable data labels, and then modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowBubbleSize(true);
 dataLabels.setShowCategoryName(true);
 dataLabels.setShowSeriesName(true);
 dataLabels.setSeparator(" & ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsBubbleChart.docx");
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getShowCategoryName() {#getShowCategoryName}
```
public boolean getShowCategoryName()
```


Allows to specify whether category name is to be displayed for the data labels of the entire series. Default value is  false .

 **Remarks:** 

Value defined for this property can be overridden for an individual data label with using the [ChartDataLabel.getShowCategoryName()](../../com.aspose.words/chartdatalabel/\#getShowCategoryName) / [ChartDataLabel.setShowCategoryName(boolean)](../../com.aspose.words/chartdatalabel/\#setShowCategoryName-boolean) property.

 **Examples:** 

Shows how to work with data labels of a bubble chart.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.BUBBLE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series with X/Y coordinates and diameter of each of the bubbles.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new double[]{2.9, 3.5, 1.1, 4.0, 4.0},
         new double[]{1.9, 8.5, 2.1, 6.0, 1.5},
         new double[]{9.0, 4.5, 2.5, 8.0, 5.0});

 // Enable data labels, and then modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowBubbleSize(true);
 dataLabels.setShowCategoryName(true);
 dataLabels.setShowSeriesName(true);
 dataLabels.setSeparator(" & ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsBubbleChart.docx");
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getShowDataLabelsRange() {#getShowDataLabelsRange}
```
public boolean getShowDataLabelsRange()
```


Allows to specify whether values from data labels range to be displayed in the data labels of the entire series. Default value is  false .

 **Remarks:** 

Value defined for this property can be overridden for an individual data label with using the [ChartDataLabel.getShowDataLabelsRange()](../../com.aspose.words/chartdatalabel/\#getShowDataLabelsRange) / [ChartDataLabel.setShowDataLabelsRange(boolean)](../../com.aspose.words/chartdatalabel/\#setShowDataLabelsRange-boolean) property.

**Returns:**
boolean - The corresponding  boolean  value.
### getShowLeaderLines() {#getShowLeaderLines}
```
public boolean getShowLeaderLines()
```


Allows to specify whether data label leader lines need be shown for the data labels of the entire series. Default value is  false .

 **Remarks:** 

Applies to Pie charts only. Leader lines create a visual connection between a data label and its corresponding data point.

Value defined for this property can be overridden for an individual data label with using the [ChartDataLabel.getShowLeaderLines()](../../com.aspose.words/chartdatalabel/\#getShowLeaderLines) / [ChartDataLabel.setShowLeaderLines(boolean)](../../com.aspose.words/chartdatalabel/\#setShowLeaderLines-boolean) property.

 **Examples:** 

Shows how to work with data labels of a pie chart.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.PIE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a custom chart series with a category name for each of the sectors, and their frequency table.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel"},
         new double[]{2.7, 3.2, 0.8});

 // Enable data labels that will display both percentage and frequency of each sector, and modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowLeaderLines(true);
 dataLabels.setShowLegendKey(true);
 dataLabels.setShowPercentage(true);
 dataLabels.setShowValue(true);
 dataLabels.setSeparator("; ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsPieChart.docx");
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getShowLegendKey() {#getShowLegendKey}
```
public boolean getShowLegendKey()
```


Allows to specify whether legend key is to be displayed for the data labels of the entire series. Default value is  false .

 **Remarks:** 

Value defined for this property can be overridden for an individual data label with using the [ChartDataLabel.getShowLegendKey()](../../com.aspose.words/chartdatalabel/\#getShowLegendKey) / [ChartDataLabel.setShowLegendKey(boolean)](../../com.aspose.words/chartdatalabel/\#setShowLegendKey-boolean) property.

 **Examples:** 

Shows how to work with data labels of a pie chart.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.PIE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a custom chart series with a category name for each of the sectors, and their frequency table.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel"},
         new double[]{2.7, 3.2, 0.8});

 // Enable data labels that will display both percentage and frequency of each sector, and modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowLeaderLines(true);
 dataLabels.setShowLegendKey(true);
 dataLabels.setShowPercentage(true);
 dataLabels.setShowValue(true);
 dataLabels.setSeparator("; ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsPieChart.docx");
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getShowPercentage() {#getShowPercentage}
```
public boolean getShowPercentage()
```


Allows to specify whether percentage value is to be displayed for the data labels of the entire series. Default value is  false . Applies only to Pie charts.

 **Remarks:** 

Value defined for this property can be overridden for an individual data label with using the [ChartDataLabel.getShowPercentage()](../../com.aspose.words/chartdatalabel/\#getShowPercentage) / [ChartDataLabel.setShowPercentage(boolean)](../../com.aspose.words/chartdatalabel/\#setShowPercentage-boolean) property.

 **Examples:** 

Shows how to work with data labels of a pie chart.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.PIE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a custom chart series with a category name for each of the sectors, and their frequency table.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel"},
         new double[]{2.7, 3.2, 0.8});

 // Enable data labels that will display both percentage and frequency of each sector, and modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowLeaderLines(true);
 dataLabels.setShowLegendKey(true);
 dataLabels.setShowPercentage(true);
 dataLabels.setShowValue(true);
 dataLabels.setSeparator("; ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsPieChart.docx");
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getShowSeriesName() {#getShowSeriesName}
```
public boolean getShowSeriesName()
```


Gets a Boolean to indicate the series name display behavior for the data labels of the entire series.  true  to show the series name;  false  to hide. By default  false .

 **Remarks:** 

Value defined for this property can be overridden for an individual data label with using the [ChartDataLabel.getShowSeriesName()](../../com.aspose.words/chartdatalabel/\#getShowSeriesName) / [ChartDataLabel.setShowSeriesName(boolean)](../../com.aspose.words/chartdatalabel/\#setShowSeriesName-boolean) property.

 **Examples:** 

Shows how to work with data labels of a bubble chart.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.BUBBLE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series with X/Y coordinates and diameter of each of the bubbles.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new double[]{2.9, 3.5, 1.1, 4.0, 4.0},
         new double[]{1.9, 8.5, 2.1, 6.0, 1.5},
         new double[]{9.0, 4.5, 2.5, 8.0, 5.0});

 // Enable data labels, and then modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowBubbleSize(true);
 dataLabels.setShowCategoryName(true);
 dataLabels.setShowSeriesName(true);
 dataLabels.setSeparator(" & ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsBubbleChart.docx");
 
```

**Returns:**
boolean - A Boolean to indicate the series name display behavior for the data labels of the entire series.
### getShowValue() {#getShowValue}
```
public boolean getShowValue()
```


Allows to specify whether values are to be displayed in the data labels of the entire series. Default value is  false .

 **Remarks:** 

Value defined for this property can be overridden for an individual data label with using the [ChartDataLabel.getShowValue()](../../com.aspose.words/chartdatalabel/\#getShowValue) / [ChartDataLabel.setShowValue(boolean)](../../com.aspose.words/chartdatalabel/\#setShowValue-boolean) property.

 **Examples:** 

Shows how to work with data labels of a pie chart.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.PIE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a custom chart series with a category name for each of the sectors, and their frequency table.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel"},
         new double[]{2.7, 3.2, 0.8});

 // Enable data labels that will display both percentage and frequency of each sector, and modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowLeaderLines(true);
 dataLabels.setShowLegendKey(true);
 dataLabels.setShowPercentage(true);
 dataLabels.setShowValue(true);
 dataLabels.setSeparator("; ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsPieChart.docx");
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### isInherited() {#isInherited}
```
public boolean isInherited()
```




**Returns:**
boolean
### iterator() {#iterator}
```
public Iterator iterator()
```


Returns an enumerator object.

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
java.util.Iterator
### setSeparator(String value) {#setSeparator-java.lang.String}
```
public void setSeparator(String value)
```


Sets string separator used for the data labels of the entire series. The default is a comma, except for pie charts showing only category name and percentage, when a line break shall be used instead.

 **Remarks:** 

Value defined for this property can be overridden for an individual data label with using the [ChartDataLabel.getSeparator()](../../com.aspose.words/chartdatalabel/\#getSeparator) / [ChartDataLabel.setSeparator(java.lang.String)](../../com.aspose.words/chartdatalabel/\#setSeparator-java.lang.String) property.

 **Examples:** 

Shows how to work with data labels of a bubble chart.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.BUBBLE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series with X/Y coordinates and diameter of each of the bubbles.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new double[]{2.9, 3.5, 1.1, 4.0, 4.0},
         new double[]{1.9, 8.5, 2.1, 6.0, 1.5},
         new double[]{9.0, 4.5, 2.5, 8.0, 5.0});

 // Enable data labels, and then modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowBubbleSize(true);
 dataLabels.setShowCategoryName(true);
 dataLabels.setShowSeriesName(true);
 dataLabels.setSeparator(" & ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsBubbleChart.docx");
 
```

Shows how to work with data labels of a pie chart.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.PIE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a custom chart series with a category name for each of the sectors, and their frequency table.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel"},
         new double[]{2.7, 3.2, 0.8});

 // Enable data labels that will display both percentage and frequency of each sector, and modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowLeaderLines(true);
 dataLabels.setShowLegendKey(true);
 dataLabels.setShowPercentage(true);
 dataLabels.setShowValue(true);
 dataLabels.setSeparator("; ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsPieChart.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | String separator used for the data labels of the entire series. |

### setShowBubbleSize(boolean value) {#setShowBubbleSize-boolean}
```
public void setShowBubbleSize(boolean value)
```


Allows to specify whether bubble size is to be displayed for the data labels of the entire series. Applies only to Bubble charts. Default value is  false .

 **Remarks:** 

Value defined for this property can be overridden for an individual data label with using the [ChartDataLabel.getShowBubbleSize()](../../com.aspose.words/chartdatalabel/\#getShowBubbleSize) / [ChartDataLabel.setShowBubbleSize(boolean)](../../com.aspose.words/chartdatalabel/\#setShowBubbleSize-boolean) property.

 **Examples:** 

Shows how to work with data labels of a bubble chart.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.BUBBLE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series with X/Y coordinates and diameter of each of the bubbles.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new double[]{2.9, 3.5, 1.1, 4.0, 4.0},
         new double[]{1.9, 8.5, 2.1, 6.0, 1.5},
         new double[]{9.0, 4.5, 2.5, 8.0, 5.0});

 // Enable data labels, and then modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowBubbleSize(true);
 dataLabels.setShowCategoryName(true);
 dataLabels.setShowSeriesName(true);
 dataLabels.setSeparator(" & ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsBubbleChart.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setShowCategoryName(boolean value) {#setShowCategoryName-boolean}
```
public void setShowCategoryName(boolean value)
```


Allows to specify whether category name is to be displayed for the data labels of the entire series. Default value is  false .

 **Remarks:** 

Value defined for this property can be overridden for an individual data label with using the [ChartDataLabel.getShowCategoryName()](../../com.aspose.words/chartdatalabel/\#getShowCategoryName) / [ChartDataLabel.setShowCategoryName(boolean)](../../com.aspose.words/chartdatalabel/\#setShowCategoryName-boolean) property.

 **Examples:** 

Shows how to work with data labels of a bubble chart.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.BUBBLE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series with X/Y coordinates and diameter of each of the bubbles.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new double[]{2.9, 3.5, 1.1, 4.0, 4.0},
         new double[]{1.9, 8.5, 2.1, 6.0, 1.5},
         new double[]{9.0, 4.5, 2.5, 8.0, 5.0});

 // Enable data labels, and then modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowBubbleSize(true);
 dataLabels.setShowCategoryName(true);
 dataLabels.setShowSeriesName(true);
 dataLabels.setSeparator(" & ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsBubbleChart.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setShowDataLabelsRange(boolean value) {#setShowDataLabelsRange-boolean}
```
public void setShowDataLabelsRange(boolean value)
```


Allows to specify whether values from data labels range to be displayed in the data labels of the entire series. Default value is  false .

 **Remarks:** 

Value defined for this property can be overridden for an individual data label with using the [ChartDataLabel.getShowDataLabelsRange()](../../com.aspose.words/chartdatalabel/\#getShowDataLabelsRange) / [ChartDataLabel.setShowDataLabelsRange(boolean)](../../com.aspose.words/chartdatalabel/\#setShowDataLabelsRange-boolean) property.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setShowLeaderLines(boolean value) {#setShowLeaderLines-boolean}
```
public void setShowLeaderLines(boolean value)
```


Allows to specify whether data label leader lines need be shown for the data labels of the entire series. Default value is  false .

 **Remarks:** 

Applies to Pie charts only. Leader lines create a visual connection between a data label and its corresponding data point.

Value defined for this property can be overridden for an individual data label with using the [ChartDataLabel.getShowLeaderLines()](../../com.aspose.words/chartdatalabel/\#getShowLeaderLines) / [ChartDataLabel.setShowLeaderLines(boolean)](../../com.aspose.words/chartdatalabel/\#setShowLeaderLines-boolean) property.

 **Examples:** 

Shows how to work with data labels of a pie chart.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.PIE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a custom chart series with a category name for each of the sectors, and their frequency table.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel"},
         new double[]{2.7, 3.2, 0.8});

 // Enable data labels that will display both percentage and frequency of each sector, and modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowLeaderLines(true);
 dataLabels.setShowLegendKey(true);
 dataLabels.setShowPercentage(true);
 dataLabels.setShowValue(true);
 dataLabels.setSeparator("; ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsPieChart.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setShowLegendKey(boolean value) {#setShowLegendKey-boolean}
```
public void setShowLegendKey(boolean value)
```


Allows to specify whether legend key is to be displayed for the data labels of the entire series. Default value is  false .

 **Remarks:** 

Value defined for this property can be overridden for an individual data label with using the [ChartDataLabel.getShowLegendKey()](../../com.aspose.words/chartdatalabel/\#getShowLegendKey) / [ChartDataLabel.setShowLegendKey(boolean)](../../com.aspose.words/chartdatalabel/\#setShowLegendKey-boolean) property.

 **Examples:** 

Shows how to work with data labels of a pie chart.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.PIE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a custom chart series with a category name for each of the sectors, and their frequency table.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel"},
         new double[]{2.7, 3.2, 0.8});

 // Enable data labels that will display both percentage and frequency of each sector, and modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowLeaderLines(true);
 dataLabels.setShowLegendKey(true);
 dataLabels.setShowPercentage(true);
 dataLabels.setShowValue(true);
 dataLabels.setSeparator("; ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsPieChart.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setShowPercentage(boolean value) {#setShowPercentage-boolean}
```
public void setShowPercentage(boolean value)
```


Allows to specify whether percentage value is to be displayed for the data labels of the entire series. Default value is  false . Applies only to Pie charts.

 **Remarks:** 

Value defined for this property can be overridden for an individual data label with using the [ChartDataLabel.getShowPercentage()](../../com.aspose.words/chartdatalabel/\#getShowPercentage) / [ChartDataLabel.setShowPercentage(boolean)](../../com.aspose.words/chartdatalabel/\#setShowPercentage-boolean) property.

 **Examples:** 

Shows how to work with data labels of a pie chart.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.PIE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a custom chart series with a category name for each of the sectors, and their frequency table.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel"},
         new double[]{2.7, 3.2, 0.8});

 // Enable data labels that will display both percentage and frequency of each sector, and modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowLeaderLines(true);
 dataLabels.setShowLegendKey(true);
 dataLabels.setShowPercentage(true);
 dataLabels.setShowValue(true);
 dataLabels.setSeparator("; ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsPieChart.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setShowSeriesName(boolean value) {#setShowSeriesName-boolean}
```
public void setShowSeriesName(boolean value)
```


Sets a Boolean to indicate the series name display behavior for the data labels of the entire series.  true  to show the series name;  false  to hide. By default  false .

 **Remarks:** 

Value defined for this property can be overridden for an individual data label with using the [ChartDataLabel.getShowSeriesName()](../../com.aspose.words/chartdatalabel/\#getShowSeriesName) / [ChartDataLabel.setShowSeriesName(boolean)](../../com.aspose.words/chartdatalabel/\#setShowSeriesName-boolean) property.

 **Examples:** 

Shows how to work with data labels of a bubble chart.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.BUBBLE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series with X/Y coordinates and diameter of each of the bubbles.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new double[]{2.9, 3.5, 1.1, 4.0, 4.0},
         new double[]{1.9, 8.5, 2.1, 6.0, 1.5},
         new double[]{9.0, 4.5, 2.5, 8.0, 5.0});

 // Enable data labels, and then modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowBubbleSize(true);
 dataLabels.setShowCategoryName(true);
 dataLabels.setShowSeriesName(true);
 dataLabels.setSeparator(" & ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsBubbleChart.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A Boolean to indicate the series name display behavior for the data labels of the entire series. |

### setShowValue(boolean value) {#setShowValue-boolean}
```
public void setShowValue(boolean value)
```


Allows to specify whether values are to be displayed in the data labels of the entire series. Default value is  false .

 **Remarks:** 

Value defined for this property can be overridden for an individual data label with using the [ChartDataLabel.getShowValue()](../../com.aspose.words/chartdatalabel/\#getShowValue) / [ChartDataLabel.setShowValue(boolean)](../../com.aspose.words/chartdatalabel/\#setShowValue-boolean) property.

 **Examples:** 

Shows how to work with data labels of a pie chart.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Chart chart = builder.insertChart(ChartType.PIE, 500.0, 300.0).getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a custom chart series with a category name for each of the sectors, and their frequency table.
 ChartSeries series = chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel"},
         new double[]{2.7, 3.2, 0.8});

 // Enable data labels that will display both percentage and frequency of each sector, and modify their appearance.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowLeaderLines(true);
 dataLabels.setShowLegendKey(true);
 dataLabels.setShowPercentage(true);
 dataLabels.setShowValue(true);
 dataLabels.setSeparator("; ");

 doc.save(getArtifactsDir() + "Charts.DataLabelsPieChart.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

