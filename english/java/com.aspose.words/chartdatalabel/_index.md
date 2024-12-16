---
title: ChartDataLabel
linktitle: ChartDataLabel
second_title: Aspose.Words for Java
description: Represents data label on a chart point or trendline in Java.
type: docs
weight: 70
url: /java/com.aspose.words/chartdatalabel/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class ChartDataLabel implements Cloneable
```

Represents data label on a chart point or trendline.

To learn more, visit the [ Working with Charts ][Working with Charts] documentation article.

 **Remarks:** 

On a series, the [ChartDataLabel](../../com.aspose.words/chartdatalabel/) object is a member of the [ChartDataLabelCollection](../../com.aspose.words/chartdatalabelcollection/). The [ChartDataLabelCollection](../../com.aspose.words/chartdatalabelcollection/) contains a [ChartDataLabel](../../com.aspose.words/chartdatalabel/) object for each point.

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
| [clearFormat()](#clearFormat) | Clears format of this data label. |
| [fetchSpecialDefaultRunPropertyValue(int key)](#fetchSpecialDefaultRunPropertyValue-int) |  |
| [generateItemText()](#generateItemText) |  |
| [getFont()](#getFont) | Provides access to the font formatting of this data label. |
| [getFormat()](#getFormat) | Provides access to fill and line formatting of the data label. |
| [getIndex()](#getIndex) | Specifies the index of the containing element. |
| [getLeft()](#getLeft) | Gets the distance of the data label in points from the left edge of the chart or from the position specified by its [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) property, depending on the value of the [getLeftMode()](../../com.aspose.words/chartdatalabel/\#getLeftMode) / [setLeftMode(int)](../../com.aspose.words/chartdatalabel/\#setLeftMode-int) property. |
| [getLeftMode()](#getLeftMode) | Gets the interpretation mode of the [getLeft()](../../com.aspose.words/chartdatalabel/\#getLeft) / [setLeft(double)](../../com.aspose.words/chartdatalabel/\#setLeft-double) property value: whether it sets the location of the data label from the left edge of the chart of from the position specified by its [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) property. |
| [getNumberFormat()](#getNumberFormat) | Returns number format of the parent element. |
| [getOrientation()](#getOrientation) | Gets the orientation of the label text. |
| [getPosition()](#getPosition) | Gets the position of the data label. |
| [getRelativePropertyValue(int key, Object value)](#getRelativePropertyValue-int-java.lang.Object) |  |
| [getRotation()](#getRotation) | Gets the rotation of the label in degrees. |
| [getSeparator()](#getSeparator) | Gets string separator used for the data labels on a chart. |
| [getShapeType()](#getShapeType) |  |
| [getShowBubbleSize()](#getShowBubbleSize) | Allows to specify if bubble size is to be displayed for the data labels on a chart. |
| [getShowCategoryName()](#getShowCategoryName) | Allows to specify if category name is to be displayed for the data labels on a chart. |
| [getShowDataLabelsRange()](#getShowDataLabelsRange) | Allows to specify if values from data labels range to be displayed in the data labels. |
| [getShowLeaderLines()](#getShowLeaderLines) | Allows to specify if data label leader lines need be shown. |
| [getShowLegendKey()](#getShowLegendKey) | Allows to specify if legend key is to be displayed for the data labels on a chart. |
| [getShowPercentage()](#getShowPercentage) | Allows to specify if percentage value is to be displayed for the data labels on a chart. |
| [getShowSeriesName()](#getShowSeriesName) | Gets a Boolean to indicate the series name display behavior for the data labels on a chart. |
| [getShowValue()](#getShowValue) | Allows to specify if values are to be displayed in the data labels. |
| [getTop()](#getTop) | Gets the distance of the data label in points from the top edge of the chart or from the position specified by its [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) property, depending on the value of the [getTopMode()](../../com.aspose.words/chartdatalabel/\#getTopMode) / [setTopMode(int)](../../com.aspose.words/chartdatalabel/\#setTopMode-int) property. |
| [getTopMode()](#getTopMode) | Gets the interpretation mode of the [getTop()](../../com.aspose.words/chartdatalabel/\#getTop) / [setTop(double)](../../com.aspose.words/chartdatalabel/\#setTop-double) property value: whether it sets the location of the data label from the top edge of the chart of from the position specified by its [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) property. |
| [isFillSupported()](#isFillSupported) |  |
| [isFormatDefined()](#isFormatDefined) |  |
| [isHidden()](#isHidden) | Gets/sets a flag indicating whether this label is hidden. |
| [isHidden(boolean value)](#isHidden-boolean) | Gets/sets a flag indicating whether this label is hidden. |
| [isInherited()](#isInherited) |  |
| [isVisible()](#isVisible) | Returns  true  if this data label has something to display. |
| [materializeSpPr()](#materializeSpPr) |  |
| [setLeft(double value)](#setLeft-double) | Sets the distance of the data label in points from the left edge of the chart or from the position specified by its [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) property, depending on the value of the [getLeftMode()](../../com.aspose.words/chartdatalabel/\#getLeftMode) / [setLeftMode(int)](../../com.aspose.words/chartdatalabel/\#setLeftMode-int) property. |
| [setLeftMode(int value)](#setLeftMode-int) | Sets the interpretation mode of the [getLeft()](../../com.aspose.words/chartdatalabel/\#getLeft) / [setLeft(double)](../../com.aspose.words/chartdatalabel/\#setLeft-double) property value: whether it sets the location of the data label from the left edge of the chart of from the position specified by its [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) property. |
| [setOrientation(int value)](#setOrientation-int) | Sets the orientation of the label text. |
| [setPosition(int value)](#setPosition-int) | Sets the position of the data label. |
| [setRotation(int value)](#setRotation-int) | Sets the rotation of the label in degrees. |
| [setSeparator(String value)](#setSeparator-java.lang.String) | Sets string separator used for the data labels on a chart. |
| [setShapeType(int value)](#setShapeType-int) |  |
| [setShowBubbleSize(boolean value)](#setShowBubbleSize-boolean) | Allows to specify if bubble size is to be displayed for the data labels on a chart. |
| [setShowCategoryName(boolean value)](#setShowCategoryName-boolean) | Allows to specify if category name is to be displayed for the data labels on a chart. |
| [setShowDataLabelsRange(boolean value)](#setShowDataLabelsRange-boolean) | Allows to specify if values from data labels range to be displayed in the data labels. |
| [setShowLeaderLines(boolean value)](#setShowLeaderLines-boolean) | Allows to specify if data label leader lines need be shown. |
| [setShowLegendKey(boolean value)](#setShowLegendKey-boolean) | Allows to specify if legend key is to be displayed for the data labels on a chart. |
| [setShowPercentage(boolean value)](#setShowPercentage-boolean) | Allows to specify if percentage value is to be displayed for the data labels on a chart. |
| [setShowSeriesName(boolean value)](#setShowSeriesName-boolean) | Sets a Boolean to indicate the series name display behavior for the data labels on a chart. |
| [setShowValue(boolean value)](#setShowValue-boolean) | Allows to specify if values are to be displayed in the data labels. |
| [setTop(double value)](#setTop-double) | Sets the distance of the data label in points from the top edge of the chart or from the position specified by its [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) property, depending on the value of the [getTopMode()](../../com.aspose.words/chartdatalabel/\#getTopMode) / [setTopMode(int)](../../com.aspose.words/chartdatalabel/\#setTopMode-int) property. |
| [setTopMode(int value)](#setTopMode-int) | Sets the interpretation mode of the [getTop()](../../com.aspose.words/chartdatalabel/\#getTop) / [setTop(double)](../../com.aspose.words/chartdatalabel/\#setTop-double) property value: whether it sets the location of the data label from the top edge of the chart of from the position specified by its [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) property. |
### clearFormat() {#clearFormat}
```
public void clearFormat()
```


Clears format of this data label. The properties are set to the default values defined in the parent data label collection.

### fetchSpecialDefaultRunPropertyValue(int key) {#fetchSpecialDefaultRunPropertyValue-int}
```
public Object fetchSpecialDefaultRunPropertyValue(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### generateItemText() {#generateItemText}
```
public String generateItemText()
```




**Returns:**
java.lang.String
### getFont() {#getFont}
```
public Font getFont()
```


Provides access to the font formatting of this data label.

 **Examples:** 

Shows how to use 3D effects with bubble charts.

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
[Font](../../com.aspose.words/font/) - The corresponding [Font](../../com.aspose.words/font/) value.
### getFormat() {#getFormat}
```
public ChartFormat getFormat()
```


Provides access to fill and line formatting of the data label.

**Returns:**
[ChartFormat](../../com.aspose.words/chartformat/) - The corresponding [ChartFormat](../../com.aspose.words/chartformat/) value.
### getIndex() {#getIndex}
```
public int getIndex()
```


Specifies the index of the containing element. This index shall determine which of the parent's children collection this element applies to. Default value is 0.

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
int - The corresponding  int  value.
### getLeft() {#getLeft}
```
public double getLeft()
```


Gets the distance of the data label in points from the left edge of the chart or from the position specified by its [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) property, depending on the value of the [getLeftMode()](../../com.aspose.words/chartdatalabel/\#getLeftMode) / [setLeftMode(int)](../../com.aspose.words/chartdatalabel/\#setLeftMode-int) property.

 **Remarks:** 

The value of the property changes proportionally if the chart shape is resized.

The property cannot be set in a Word 2016 chart.

 **Examples:** 

Shows how to place data labels of doughnut chart outside doughnut.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 final int CHART_WIDTH = 432;
 final int CHART_HEIGHT = 252;
 Shape shape = builder.insertChart(ChartType.DOUGHNUT, CHART_WIDTH, CHART_HEIGHT);
 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();
 // Delete default generated series.
 seriesColl.clear();

 // Hide the legend.
 chart.getLegend().setPosition(LegendPosition.NONE);

 // Generate data.
 final int DATA_LENGTH = 20;
 double totalValue = 0.0;
 String[] categories = new String[DATA_LENGTH];
 double[] values = new double[DATA_LENGTH];
 for (int i = 0; i < DATA_LENGTH; i++)
 {
     categories[i] = MessageFormat.format("Category {0}", i);
     values[i] = DATA_LENGTH - i;
     totalValue += values[i];
 }

 ChartSeries series = seriesColl.add("Series 1", categories, values);
 series.hasDataLabels(true);

 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.setShowLeaderLines(true);

 // The Position property cannot be used for doughnut charts. Let's place data labels using the Left and Top
 // properties around a circle outside of the chart doughnut.
 // The origin is in the upper left corner of the chart.

 final double TITLE_AREA_HEIGHT = 25.5; // This can be calculated using title text and font.
 final double DOUGHNUT_CENTER_Y = TITLE_AREA_HEIGHT + (CHART_HEIGHT - TITLE_AREA_HEIGHT) / 2.0;
 final double DOUGHNUT_CENTER_X = CHART_WIDTH / 2d;
 final double LABEL_HEIGHT = 16.5; // This can be calculated using label font.
 final double ONE_CHAR_LABEL_WIDTH = 12.75; // This can be calculated for each label using its text and font.
 final double TWO_CHAR_LABEL_WIDTH = 17.25; // This can be calculated for each label using its text and font.
 final double Y_MARGIN = 0.75;
 final double LABEL_MARGIN = 1.5;
 final double LABEL_CIRCLE_RADIUS = CHART_HEIGHT - DOUGHNUT_CENTER_Y - Y_MARGIN - LABEL_HEIGHT / 2.0;

 // Because the data points start at the top, the X coordinates used in the Left and Top properties of
 // the data labels point to the right and the Y coordinates point down, the starting angle is -PI/2.
 double totalAngle = -Math.PI / 2f;
 ChartDataLabel previousLabel = null;

 for (int i = 0; i < series.getYValues().getCount(); i++)
 {
     ChartDataLabel dataLabel = dataLabels.get(i);

     double value = series.getYValues().get(i).getDoubleValue();
     double labelWidth = (value < 10) ? ONE_CHAR_LABEL_WIDTH : TWO_CHAR_LABEL_WIDTH;
     double labelSegmentAngle = value / totalValue * 2.0 * Math.PI;
     double labelAngle = labelSegmentAngle / 2.0 + totalAngle;
     double labelCenterX = LABEL_CIRCLE_RADIUS * Math.cos(labelAngle) + DOUGHNUT_CENTER_X;
     double labelCenterY = LABEL_CIRCLE_RADIUS * Math.sin(labelAngle) + DOUGHNUT_CENTER_Y;
     double labelLeft = labelCenterX - labelWidth / 2.0;
     double labelTop = labelCenterY - LABEL_HEIGHT / 2.0;

     // If the current data label overlaps other labels, move it horizontally.
     if ((previousLabel != null) &&
             (Math.abs(previousLabel.getTop() - labelTop) < LABEL_HEIGHT) &&
             (Math.abs(previousLabel.getLeft() - labelLeft) < labelWidth))
     {
         // Move right on the top, left on the bottom.
         boolean isOnTop = (totalAngle < 0) || (totalAngle >= Math.PI);
         labelLeft = previousLabel.getLeft() + labelWidth * (isOnTop ? 1 : -1) + LABEL_MARGIN;
     }

     dataLabel.setLeft(labelLeft);
     dataLabel.setLeftMode(ChartDataLabelLocationMode.ABSOLUTE);
     dataLabel.setTop(labelTop);
     dataLabel.setTopMode(ChartDataLabelLocationMode.ABSOLUTE);

     totalAngle += labelSegmentAngle;
     previousLabel = dataLabel;
 }

 doc.save(getArtifactsDir() + "Charts.DoughnutChartLabelPosition.docx");
 
```

**Returns:**
double - The distance of the data label in points from the left edge of the chart or from the position specified by its [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) property, depending on the value of the [getLeftMode()](../../com.aspose.words/chartdatalabel/\#getLeftMode) / [setLeftMode(int)](../../com.aspose.words/chartdatalabel/\#setLeftMode-int) property.
### getLeftMode() {#getLeftMode}
```
public int getLeftMode()
```


Gets the interpretation mode of the [getLeft()](../../com.aspose.words/chartdatalabel/\#getLeft) / [setLeft(double)](../../com.aspose.words/chartdatalabel/\#setLeft-double) property value: whether it sets the location of the data label from the left edge of the chart of from the position specified by its [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) property.

 **Remarks:** 

The property cannot be set in a Word 2016 chart.

 **Examples:** 

Shows how to place data labels of doughnut chart outside doughnut.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 final int CHART_WIDTH = 432;
 final int CHART_HEIGHT = 252;
 Shape shape = builder.insertChart(ChartType.DOUGHNUT, CHART_WIDTH, CHART_HEIGHT);
 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();
 // Delete default generated series.
 seriesColl.clear();

 // Hide the legend.
 chart.getLegend().setPosition(LegendPosition.NONE);

 // Generate data.
 final int DATA_LENGTH = 20;
 double totalValue = 0.0;
 String[] categories = new String[DATA_LENGTH];
 double[] values = new double[DATA_LENGTH];
 for (int i = 0; i < DATA_LENGTH; i++)
 {
     categories[i] = MessageFormat.format("Category {0}", i);
     values[i] = DATA_LENGTH - i;
     totalValue += values[i];
 }

 ChartSeries series = seriesColl.add("Series 1", categories, values);
 series.hasDataLabels(true);

 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.setShowLeaderLines(true);

 // The Position property cannot be used for doughnut charts. Let's place data labels using the Left and Top
 // properties around a circle outside of the chart doughnut.
 // The origin is in the upper left corner of the chart.

 final double TITLE_AREA_HEIGHT = 25.5; // This can be calculated using title text and font.
 final double DOUGHNUT_CENTER_Y = TITLE_AREA_HEIGHT + (CHART_HEIGHT - TITLE_AREA_HEIGHT) / 2.0;
 final double DOUGHNUT_CENTER_X = CHART_WIDTH / 2d;
 final double LABEL_HEIGHT = 16.5; // This can be calculated using label font.
 final double ONE_CHAR_LABEL_WIDTH = 12.75; // This can be calculated for each label using its text and font.
 final double TWO_CHAR_LABEL_WIDTH = 17.25; // This can be calculated for each label using its text and font.
 final double Y_MARGIN = 0.75;
 final double LABEL_MARGIN = 1.5;
 final double LABEL_CIRCLE_RADIUS = CHART_HEIGHT - DOUGHNUT_CENTER_Y - Y_MARGIN - LABEL_HEIGHT / 2.0;

 // Because the data points start at the top, the X coordinates used in the Left and Top properties of
 // the data labels point to the right and the Y coordinates point down, the starting angle is -PI/2.
 double totalAngle = -Math.PI / 2f;
 ChartDataLabel previousLabel = null;

 for (int i = 0; i < series.getYValues().getCount(); i++)
 {
     ChartDataLabel dataLabel = dataLabels.get(i);

     double value = series.getYValues().get(i).getDoubleValue();
     double labelWidth = (value < 10) ? ONE_CHAR_LABEL_WIDTH : TWO_CHAR_LABEL_WIDTH;
     double labelSegmentAngle = value / totalValue * 2.0 * Math.PI;
     double labelAngle = labelSegmentAngle / 2.0 + totalAngle;
     double labelCenterX = LABEL_CIRCLE_RADIUS * Math.cos(labelAngle) + DOUGHNUT_CENTER_X;
     double labelCenterY = LABEL_CIRCLE_RADIUS * Math.sin(labelAngle) + DOUGHNUT_CENTER_Y;
     double labelLeft = labelCenterX - labelWidth / 2.0;
     double labelTop = labelCenterY - LABEL_HEIGHT / 2.0;

     // If the current data label overlaps other labels, move it horizontally.
     if ((previousLabel != null) &&
             (Math.abs(previousLabel.getTop() - labelTop) < LABEL_HEIGHT) &&
             (Math.abs(previousLabel.getLeft() - labelLeft) < labelWidth))
     {
         // Move right on the top, left on the bottom.
         boolean isOnTop = (totalAngle < 0) || (totalAngle >= Math.PI);
         labelLeft = previousLabel.getLeft() + labelWidth * (isOnTop ? 1 : -1) + LABEL_MARGIN;
     }

     dataLabel.setLeft(labelLeft);
     dataLabel.setLeftMode(ChartDataLabelLocationMode.ABSOLUTE);
     dataLabel.setTop(labelTop);
     dataLabel.setTopMode(ChartDataLabelLocationMode.ABSOLUTE);

     totalAngle += labelSegmentAngle;
     previousLabel = dataLabel;
 }

 doc.save(getArtifactsDir() + "Charts.DoughnutChartLabelPosition.docx");
 
```

**Returns:**
int - The interpretation mode of the [getLeft()](../../com.aspose.words/chartdatalabel/\#getLeft) / [setLeft(double)](../../com.aspose.words/chartdatalabel/\#setLeft-double) property value: whether it sets the location of the data label from the left edge of the chart of from the position specified by its [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) property. The returned value is one of [ChartDataLabelLocationMode](../../com.aspose.words/chartdatalabellocationmode/) constants.
### getNumberFormat() {#getNumberFormat}
```
public ChartNumberFormat getNumberFormat()
```


Returns number format of the parent element.

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
[ChartNumberFormat](../../com.aspose.words/chartnumberformat/) - Number format of the parent element.
### getOrientation() {#getOrientation}
```
public int getOrientation()
```


Gets the orientation of the label text.

 **Remarks:** 

The default value is [ShapeTextOrientation.HORIZONTAL](../../com.aspose.words/shapetextorientation/\#HORIZONTAL).

 **Examples:** 

Shows how to change orientation and rotation for data labels.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 ChartSeries series = shape.getChart().getSeries().get(0);
 ChartDataLabelCollection dataLabels = series.getDataLabels();

 // Show data labels.
 series.hasDataLabels(true);
 dataLabels.setShowValue(true);
 dataLabels.setShowCategoryName(true);

 // Define data label shape.
 dataLabels.getFormat().setShapeType(ChartShapeType.UP_ARROW);
 dataLabels.getFormat().getStroke().getFill().solid(Color.blue);

 // Set data label orientation and rotation for the entire series.
 dataLabels.setOrientation(ShapeTextOrientation.VERTICAL_FAR_EAST);
 dataLabels.setRotation(-45);

 // Change orientation and rotation of the first data label.
 dataLabels.get(0).setOrientation(ShapeTextOrientation.HORIZONTAL);
 dataLabels.get(0).setRotation(45);

 doc.save(getArtifactsDir() + "Charts.LabelOrientationRotation.docx");
 
```

**Returns:**
int - The orientation of the label text. The returned value is one of [ShapeTextOrientation](../../com.aspose.words/shapetextorientation/) constants.
### getPosition() {#getPosition}
```
public int getPosition()
```


Gets the position of the data label.

 **Remarks:** 

The position can be set for data labels of the following chart series types:

\- [ChartSeriesType.BAR](../../com.aspose.words/chartseriestype/\#BAR), [ChartSeriesType.COLUMN](../../com.aspose.words/chartseriestype/\#COLUMN), [ChartSeriesType.HISTOGRAM](../../com.aspose.words/chartseriestype/\#HISTOGRAM), [ChartSeriesType.PARETO](../../com.aspose.words/chartseriestype/\#PARETO), [ChartSeriesType.WATERFALL](../../com.aspose.words/chartseriestype/\#WATERFALL); allowed values: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.INSIDE\_BASE](../../com.aspose.words/chartdatalabelposition/\#INSIDE-BASE), [ChartDataLabelPosition.INSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#INSIDE-END) and [ChartDataLabelPosition.OUTSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#OUTSIDE-END);

\- [ChartSeriesType.BAR\_STACKED](../../com.aspose.words/chartseriestype/\#BAR-STACKED), [ChartSeriesType.BAR\_PERCENT\_STACKED](../../com.aspose.words/chartseriestype/\#BAR-PERCENT-STACKED), [ChartSeriesType.COLUMN\_STACKED](../../com.aspose.words/chartseriestype/\#COLUMN-STACKED), [ChartSeriesType.COLUMN\_PERCENT\_STACKED](../../com.aspose.words/chartseriestype/\#COLUMN-PERCENT-STACKED); allowed values: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.INSIDE\_BASE](../../com.aspose.words/chartdatalabelposition/\#INSIDE-BASE) and [ChartDataLabelPosition.INSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#INSIDE-END);

\- [ChartSeriesType.BUBBLE](../../com.aspose.words/chartseriestype/\#BUBBLE), [ChartSeriesType.BUBBLE\_3\_D](../../com.aspose.words/chartseriestype/\#BUBBLE-3-D), [ChartSeriesType.LINE](../../com.aspose.words/chartseriestype/\#LINE), [ChartSeriesType.LINE\_STACKED](../../com.aspose.words/chartseriestype/\#LINE-STACKED), [ChartSeriesType.LINE\_PERCENT\_STACKED](../../com.aspose.words/chartseriestype/\#LINE-PERCENT-STACKED), [ChartSeriesType.SCATTER](../../com.aspose.words/chartseriestype/\#SCATTER), [ChartSeriesType.STOCK](../../com.aspose.words/chartseriestype/\#STOCK); allowed values: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.LEFT](../../com.aspose.words/chartdatalabelposition/\#LEFT), [ChartDataLabelPosition.RIGHT](../../com.aspose.words/chartdatalabelposition/\#RIGHT), [ChartDataLabelPosition.ABOVE](../../com.aspose.words/chartdatalabelposition/\#ABOVE) and [ChartDataLabelPosition.BELOW](../../com.aspose.words/chartdatalabelposition/\#BELOW);

\- [ChartSeriesType.PIE](../../com.aspose.words/chartseriestype/\#PIE), [ChartSeriesType.PIE\_3\_D](../../com.aspose.words/chartseriestype/\#PIE-3-D), [ChartSeriesType.PIE\_OF\_BAR](../../com.aspose.words/chartseriestype/\#PIE-OF-BAR), [ChartSeriesType.PIE\_OF\_PIE](../../com.aspose.words/chartseriestype/\#PIE-OF-PIE); allowed values: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.INSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#INSIDE-END), [ChartDataLabelPosition.OUTSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#OUTSIDE-END) and [ChartDataLabelPosition.BEST\_FIT](../../com.aspose.words/chartdatalabelposition/\#BEST-FIT);

\- [ChartSeriesType.BOX\_AND\_WHISKER](../../com.aspose.words/chartseriestype/\#BOX-AND-WHISKER); allowed values: [ChartDataLabelPosition.LEFT](../../com.aspose.words/chartdatalabelposition/\#LEFT), [ChartDataLabelPosition.RIGHT](../../com.aspose.words/chartdatalabelposition/\#RIGHT), [ChartDataLabelPosition.ABOVE](../../com.aspose.words/chartdatalabelposition/\#ABOVE) and [ChartDataLabelPosition.BELOW](../../com.aspose.words/chartdatalabelposition/\#BELOW).

 **Examples:** 

Shows how to set the position of the data label.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert column chart.
 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();

 // Delete default generated series.
 seriesColl.clear();

 // Add series.
 ChartSeries series = seriesColl.add(
         "Series 1",
         new String[] { "Category 1", "Category 2", "Category 3" },
         new double[] { 4.0, 5.0, 6.0 });

 // Show data labels and set font color.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.getFont().setColor(Color.WHITE);

 // Set data label position.
 dataLabels.setPosition(ChartDataLabelPosition.INSIDE_BASE);
 dataLabels.get(0).setPosition(ChartDataLabelPosition.OUTSIDE_END);
 dataLabels.get(0).getFont().setColor(Color.RED);

 doc.save(getArtifactsDir() + "Charts.LabelPosition.docx");
 
```

**Returns:**
int - The position of the data label. The returned value is one of [ChartDataLabelPosition](../../com.aspose.words/chartdatalabelposition/) constants.
### getRelativePropertyValue(int key, Object value) {#getRelativePropertyValue-int-java.lang.Object}
```
public Object getRelativePropertyValue(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

**Returns:**
java.lang.Object
### getRotation() {#getRotation}
```
public int getRotation()
```


Gets the rotation of the label in degrees.

 **Remarks:** 

The range of acceptable values is from -180 to 180 inclusive. The default value is 0.

If the [getOrientation()](../../com.aspose.words/chartdatalabel/\#getOrientation) / [setOrientation(int)](../../com.aspose.words/chartdatalabel/\#setOrientation-int) value is [ShapeTextOrientation.HORIZONTAL](../../com.aspose.words/shapetextorientation/\#HORIZONTAL), the label shape, if it exists, is rotated along with the label text. Otherwise, only the label text is rotated.

 **Examples:** 

Shows how to change orientation and rotation for data labels.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 ChartSeries series = shape.getChart().getSeries().get(0);
 ChartDataLabelCollection dataLabels = series.getDataLabels();

 // Show data labels.
 series.hasDataLabels(true);
 dataLabels.setShowValue(true);
 dataLabels.setShowCategoryName(true);

 // Define data label shape.
 dataLabels.getFormat().setShapeType(ChartShapeType.UP_ARROW);
 dataLabels.getFormat().getStroke().getFill().solid(Color.blue);

 // Set data label orientation and rotation for the entire series.
 dataLabels.setOrientation(ShapeTextOrientation.VERTICAL_FAR_EAST);
 dataLabels.setRotation(-45);

 // Change orientation and rotation of the first data label.
 dataLabels.get(0).setOrientation(ShapeTextOrientation.HORIZONTAL);
 dataLabels.get(0).setRotation(45);

 doc.save(getArtifactsDir() + "Charts.LabelOrientationRotation.docx");
 
```

**Returns:**
int - The rotation of the label in degrees.
### getSeparator() {#getSeparator}
```
public String getSeparator()
```


Gets string separator used for the data labels on a chart. The default is a comma, except for pie charts showing only category name and percentage, when a line break shall be used instead.

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
java.lang.String - String separator used for the data labels on a chart.
### getShapeType() {#getShapeType}
```
public int getShapeType()
```




**Returns:**
int
### getShowBubbleSize() {#getShowBubbleSize}
```
public boolean getShowBubbleSize()
```


Allows to specify if bubble size is to be displayed for the data labels on a chart. Applies only to Bubble charts. Default value is  false .

 **Examples:** 

Shows how to use 3D effects with bubble charts.

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
boolean - The corresponding  boolean  value.
### getShowCategoryName() {#getShowCategoryName}
```
public boolean getShowCategoryName()
```


Allows to specify if category name is to be displayed for the data labels on a chart. Default value is  false .

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
boolean - The corresponding  boolean  value.
### getShowDataLabelsRange() {#getShowDataLabelsRange}
```
public boolean getShowDataLabelsRange()
```


Allows to specify if values from data labels range to be displayed in the data labels. Default value is  false .

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
boolean - The corresponding  boolean  value.
### getShowLeaderLines() {#getShowLeaderLines}
```
public boolean getShowLeaderLines()
```


Allows to specify if data label leader lines need be shown. Default value is  false .

 **Remarks:** 

Applies to Pie charts only. Leader lines create a visual connection between a data label and its corresponding data point.

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
boolean - The corresponding  boolean  value.
### getShowLegendKey() {#getShowLegendKey}
```
public boolean getShowLegendKey()
```


Allows to specify if legend key is to be displayed for the data labels on a chart. Default value is  false .

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
boolean - The corresponding  boolean  value.
### getShowPercentage() {#getShowPercentage}
```
public boolean getShowPercentage()
```


Allows to specify if percentage value is to be displayed for the data labels on a chart. Default value is  false .

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
boolean - The corresponding  boolean  value.
### getShowSeriesName() {#getShowSeriesName}
```
public boolean getShowSeriesName()
```


Gets a Boolean to indicate the series name display behavior for the data labels on a chart.  true  to show the series name;  false  to hide. By default  false .

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
boolean - A Boolean to indicate the series name display behavior for the data labels on a chart.
### getShowValue() {#getShowValue}
```
public boolean getShowValue()
```


Allows to specify if values are to be displayed in the data labels. Default value is  false .

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
boolean - The corresponding  boolean  value.
### getTop() {#getTop}
```
public double getTop()
```


Gets the distance of the data label in points from the top edge of the chart or from the position specified by its [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) property, depending on the value of the [getTopMode()](../../com.aspose.words/chartdatalabel/\#getTopMode) / [setTopMode(int)](../../com.aspose.words/chartdatalabel/\#setTopMode-int) property.

 **Remarks:** 

The value of the property changes proportionally if the chart shape is resized.

The property cannot be set in a Word 2016 chart.

 **Examples:** 

Shows how to place data labels of doughnut chart outside doughnut.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 final int CHART_WIDTH = 432;
 final int CHART_HEIGHT = 252;
 Shape shape = builder.insertChart(ChartType.DOUGHNUT, CHART_WIDTH, CHART_HEIGHT);
 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();
 // Delete default generated series.
 seriesColl.clear();

 // Hide the legend.
 chart.getLegend().setPosition(LegendPosition.NONE);

 // Generate data.
 final int DATA_LENGTH = 20;
 double totalValue = 0.0;
 String[] categories = new String[DATA_LENGTH];
 double[] values = new double[DATA_LENGTH];
 for (int i = 0; i < DATA_LENGTH; i++)
 {
     categories[i] = MessageFormat.format("Category {0}", i);
     values[i] = DATA_LENGTH - i;
     totalValue += values[i];
 }

 ChartSeries series = seriesColl.add("Series 1", categories, values);
 series.hasDataLabels(true);

 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.setShowLeaderLines(true);

 // The Position property cannot be used for doughnut charts. Let's place data labels using the Left and Top
 // properties around a circle outside of the chart doughnut.
 // The origin is in the upper left corner of the chart.

 final double TITLE_AREA_HEIGHT = 25.5; // This can be calculated using title text and font.
 final double DOUGHNUT_CENTER_Y = TITLE_AREA_HEIGHT + (CHART_HEIGHT - TITLE_AREA_HEIGHT) / 2.0;
 final double DOUGHNUT_CENTER_X = CHART_WIDTH / 2d;
 final double LABEL_HEIGHT = 16.5; // This can be calculated using label font.
 final double ONE_CHAR_LABEL_WIDTH = 12.75; // This can be calculated for each label using its text and font.
 final double TWO_CHAR_LABEL_WIDTH = 17.25; // This can be calculated for each label using its text and font.
 final double Y_MARGIN = 0.75;
 final double LABEL_MARGIN = 1.5;
 final double LABEL_CIRCLE_RADIUS = CHART_HEIGHT - DOUGHNUT_CENTER_Y - Y_MARGIN - LABEL_HEIGHT / 2.0;

 // Because the data points start at the top, the X coordinates used in the Left and Top properties of
 // the data labels point to the right and the Y coordinates point down, the starting angle is -PI/2.
 double totalAngle = -Math.PI / 2f;
 ChartDataLabel previousLabel = null;

 for (int i = 0; i < series.getYValues().getCount(); i++)
 {
     ChartDataLabel dataLabel = dataLabels.get(i);

     double value = series.getYValues().get(i).getDoubleValue();
     double labelWidth = (value < 10) ? ONE_CHAR_LABEL_WIDTH : TWO_CHAR_LABEL_WIDTH;
     double labelSegmentAngle = value / totalValue * 2.0 * Math.PI;
     double labelAngle = labelSegmentAngle / 2.0 + totalAngle;
     double labelCenterX = LABEL_CIRCLE_RADIUS * Math.cos(labelAngle) + DOUGHNUT_CENTER_X;
     double labelCenterY = LABEL_CIRCLE_RADIUS * Math.sin(labelAngle) + DOUGHNUT_CENTER_Y;
     double labelLeft = labelCenterX - labelWidth / 2.0;
     double labelTop = labelCenterY - LABEL_HEIGHT / 2.0;

     // If the current data label overlaps other labels, move it horizontally.
     if ((previousLabel != null) &&
             (Math.abs(previousLabel.getTop() - labelTop) < LABEL_HEIGHT) &&
             (Math.abs(previousLabel.getLeft() - labelLeft) < labelWidth))
     {
         // Move right on the top, left on the bottom.
         boolean isOnTop = (totalAngle < 0) || (totalAngle >= Math.PI);
         labelLeft = previousLabel.getLeft() + labelWidth * (isOnTop ? 1 : -1) + LABEL_MARGIN;
     }

     dataLabel.setLeft(labelLeft);
     dataLabel.setLeftMode(ChartDataLabelLocationMode.ABSOLUTE);
     dataLabel.setTop(labelTop);
     dataLabel.setTopMode(ChartDataLabelLocationMode.ABSOLUTE);

     totalAngle += labelSegmentAngle;
     previousLabel = dataLabel;
 }

 doc.save(getArtifactsDir() + "Charts.DoughnutChartLabelPosition.docx");
 
```

**Returns:**
double - The distance of the data label in points from the top edge of the chart or from the position specified by its [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) property, depending on the value of the [getTopMode()](../../com.aspose.words/chartdatalabel/\#getTopMode) / [setTopMode(int)](../../com.aspose.words/chartdatalabel/\#setTopMode-int) property.
### getTopMode() {#getTopMode}
```
public int getTopMode()
```


Gets the interpretation mode of the [getTop()](../../com.aspose.words/chartdatalabel/\#getTop) / [setTop(double)](../../com.aspose.words/chartdatalabel/\#setTop-double) property value: whether it sets the location of the data label from the top edge of the chart of from the position specified by its [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) property.

 **Remarks:** 

The property cannot be set in a Word 2016 chart.

 **Examples:** 

Shows how to place data labels of doughnut chart outside doughnut.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 final int CHART_WIDTH = 432;
 final int CHART_HEIGHT = 252;
 Shape shape = builder.insertChart(ChartType.DOUGHNUT, CHART_WIDTH, CHART_HEIGHT);
 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();
 // Delete default generated series.
 seriesColl.clear();

 // Hide the legend.
 chart.getLegend().setPosition(LegendPosition.NONE);

 // Generate data.
 final int DATA_LENGTH = 20;
 double totalValue = 0.0;
 String[] categories = new String[DATA_LENGTH];
 double[] values = new double[DATA_LENGTH];
 for (int i = 0; i < DATA_LENGTH; i++)
 {
     categories[i] = MessageFormat.format("Category {0}", i);
     values[i] = DATA_LENGTH - i;
     totalValue += values[i];
 }

 ChartSeries series = seriesColl.add("Series 1", categories, values);
 series.hasDataLabels(true);

 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.setShowLeaderLines(true);

 // The Position property cannot be used for doughnut charts. Let's place data labels using the Left and Top
 // properties around a circle outside of the chart doughnut.
 // The origin is in the upper left corner of the chart.

 final double TITLE_AREA_HEIGHT = 25.5; // This can be calculated using title text and font.
 final double DOUGHNUT_CENTER_Y = TITLE_AREA_HEIGHT + (CHART_HEIGHT - TITLE_AREA_HEIGHT) / 2.0;
 final double DOUGHNUT_CENTER_X = CHART_WIDTH / 2d;
 final double LABEL_HEIGHT = 16.5; // This can be calculated using label font.
 final double ONE_CHAR_LABEL_WIDTH = 12.75; // This can be calculated for each label using its text and font.
 final double TWO_CHAR_LABEL_WIDTH = 17.25; // This can be calculated for each label using its text and font.
 final double Y_MARGIN = 0.75;
 final double LABEL_MARGIN = 1.5;
 final double LABEL_CIRCLE_RADIUS = CHART_HEIGHT - DOUGHNUT_CENTER_Y - Y_MARGIN - LABEL_HEIGHT / 2.0;

 // Because the data points start at the top, the X coordinates used in the Left and Top properties of
 // the data labels point to the right and the Y coordinates point down, the starting angle is -PI/2.
 double totalAngle = -Math.PI / 2f;
 ChartDataLabel previousLabel = null;

 for (int i = 0; i < series.getYValues().getCount(); i++)
 {
     ChartDataLabel dataLabel = dataLabels.get(i);

     double value = series.getYValues().get(i).getDoubleValue();
     double labelWidth = (value < 10) ? ONE_CHAR_LABEL_WIDTH : TWO_CHAR_LABEL_WIDTH;
     double labelSegmentAngle = value / totalValue * 2.0 * Math.PI;
     double labelAngle = labelSegmentAngle / 2.0 + totalAngle;
     double labelCenterX = LABEL_CIRCLE_RADIUS * Math.cos(labelAngle) + DOUGHNUT_CENTER_X;
     double labelCenterY = LABEL_CIRCLE_RADIUS * Math.sin(labelAngle) + DOUGHNUT_CENTER_Y;
     double labelLeft = labelCenterX - labelWidth / 2.0;
     double labelTop = labelCenterY - LABEL_HEIGHT / 2.0;

     // If the current data label overlaps other labels, move it horizontally.
     if ((previousLabel != null) &&
             (Math.abs(previousLabel.getTop() - labelTop) < LABEL_HEIGHT) &&
             (Math.abs(previousLabel.getLeft() - labelLeft) < labelWidth))
     {
         // Move right on the top, left on the bottom.
         boolean isOnTop = (totalAngle < 0) || (totalAngle >= Math.PI);
         labelLeft = previousLabel.getLeft() + labelWidth * (isOnTop ? 1 : -1) + LABEL_MARGIN;
     }

     dataLabel.setLeft(labelLeft);
     dataLabel.setLeftMode(ChartDataLabelLocationMode.ABSOLUTE);
     dataLabel.setTop(labelTop);
     dataLabel.setTopMode(ChartDataLabelLocationMode.ABSOLUTE);

     totalAngle += labelSegmentAngle;
     previousLabel = dataLabel;
 }

 doc.save(getArtifactsDir() + "Charts.DoughnutChartLabelPosition.docx");
 
```

**Returns:**
int - The interpretation mode of the [getTop()](../../com.aspose.words/chartdatalabel/\#getTop) / [setTop(double)](../../com.aspose.words/chartdatalabel/\#setTop-double) property value: whether it sets the location of the data label from the top edge of the chart of from the position specified by its [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) property. The returned value is one of [ChartDataLabelLocationMode](../../com.aspose.words/chartdatalabellocationmode/) constants.
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
### isHidden() {#isHidden}
```
public boolean isHidden()
```


Gets/sets a flag indicating whether this label is hidden. The default value is  false .

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
boolean - The corresponding  boolean  value.
### isHidden(boolean value) {#isHidden-boolean}
```
public void isHidden(boolean value)
```


Gets/sets a flag indicating whether this label is hidden. The default value is  false .

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
| value | boolean | The corresponding  boolean  value. |

### isInherited() {#isInherited}
```
public boolean isInherited()
```




**Returns:**
boolean
### isVisible() {#isVisible}
```
public boolean isVisible()
```


Returns  true  if this data label has something to display.

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
boolean -  true  if this data label has something to display.
### materializeSpPr() {#materializeSpPr}
```
public void materializeSpPr()
```




### setLeft(double value) {#setLeft-double}
```
public void setLeft(double value)
```


Sets the distance of the data label in points from the left edge of the chart or from the position specified by its [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) property, depending on the value of the [getLeftMode()](../../com.aspose.words/chartdatalabel/\#getLeftMode) / [setLeftMode(int)](../../com.aspose.words/chartdatalabel/\#setLeftMode-int) property.

 **Remarks:** 

The value of the property changes proportionally if the chart shape is resized.

The property cannot be set in a Word 2016 chart.

 **Examples:** 

Shows how to place data labels of doughnut chart outside doughnut.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 final int CHART_WIDTH = 432;
 final int CHART_HEIGHT = 252;
 Shape shape = builder.insertChart(ChartType.DOUGHNUT, CHART_WIDTH, CHART_HEIGHT);
 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();
 // Delete default generated series.
 seriesColl.clear();

 // Hide the legend.
 chart.getLegend().setPosition(LegendPosition.NONE);

 // Generate data.
 final int DATA_LENGTH = 20;
 double totalValue = 0.0;
 String[] categories = new String[DATA_LENGTH];
 double[] values = new double[DATA_LENGTH];
 for (int i = 0; i < DATA_LENGTH; i++)
 {
     categories[i] = MessageFormat.format("Category {0}", i);
     values[i] = DATA_LENGTH - i;
     totalValue += values[i];
 }

 ChartSeries series = seriesColl.add("Series 1", categories, values);
 series.hasDataLabels(true);

 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.setShowLeaderLines(true);

 // The Position property cannot be used for doughnut charts. Let's place data labels using the Left and Top
 // properties around a circle outside of the chart doughnut.
 // The origin is in the upper left corner of the chart.

 final double TITLE_AREA_HEIGHT = 25.5; // This can be calculated using title text and font.
 final double DOUGHNUT_CENTER_Y = TITLE_AREA_HEIGHT + (CHART_HEIGHT - TITLE_AREA_HEIGHT) / 2.0;
 final double DOUGHNUT_CENTER_X = CHART_WIDTH / 2d;
 final double LABEL_HEIGHT = 16.5; // This can be calculated using label font.
 final double ONE_CHAR_LABEL_WIDTH = 12.75; // This can be calculated for each label using its text and font.
 final double TWO_CHAR_LABEL_WIDTH = 17.25; // This can be calculated for each label using its text and font.
 final double Y_MARGIN = 0.75;
 final double LABEL_MARGIN = 1.5;
 final double LABEL_CIRCLE_RADIUS = CHART_HEIGHT - DOUGHNUT_CENTER_Y - Y_MARGIN - LABEL_HEIGHT / 2.0;

 // Because the data points start at the top, the X coordinates used in the Left and Top properties of
 // the data labels point to the right and the Y coordinates point down, the starting angle is -PI/2.
 double totalAngle = -Math.PI / 2f;
 ChartDataLabel previousLabel = null;

 for (int i = 0; i < series.getYValues().getCount(); i++)
 {
     ChartDataLabel dataLabel = dataLabels.get(i);

     double value = series.getYValues().get(i).getDoubleValue();
     double labelWidth = (value < 10) ? ONE_CHAR_LABEL_WIDTH : TWO_CHAR_LABEL_WIDTH;
     double labelSegmentAngle = value / totalValue * 2.0 * Math.PI;
     double labelAngle = labelSegmentAngle / 2.0 + totalAngle;
     double labelCenterX = LABEL_CIRCLE_RADIUS * Math.cos(labelAngle) + DOUGHNUT_CENTER_X;
     double labelCenterY = LABEL_CIRCLE_RADIUS * Math.sin(labelAngle) + DOUGHNUT_CENTER_Y;
     double labelLeft = labelCenterX - labelWidth / 2.0;
     double labelTop = labelCenterY - LABEL_HEIGHT / 2.0;

     // If the current data label overlaps other labels, move it horizontally.
     if ((previousLabel != null) &&
             (Math.abs(previousLabel.getTop() - labelTop) < LABEL_HEIGHT) &&
             (Math.abs(previousLabel.getLeft() - labelLeft) < labelWidth))
     {
         // Move right on the top, left on the bottom.
         boolean isOnTop = (totalAngle < 0) || (totalAngle >= Math.PI);
         labelLeft = previousLabel.getLeft() + labelWidth * (isOnTop ? 1 : -1) + LABEL_MARGIN;
     }

     dataLabel.setLeft(labelLeft);
     dataLabel.setLeftMode(ChartDataLabelLocationMode.ABSOLUTE);
     dataLabel.setTop(labelTop);
     dataLabel.setTopMode(ChartDataLabelLocationMode.ABSOLUTE);

     totalAngle += labelSegmentAngle;
     previousLabel = dataLabel;
 }

 doc.save(getArtifactsDir() + "Charts.DoughnutChartLabelPosition.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The distance of the data label in points from the left edge of the chart or from the position specified by its [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) property, depending on the value of the [getLeftMode()](../../com.aspose.words/chartdatalabel/\#getLeftMode) / [setLeftMode(int)](../../com.aspose.words/chartdatalabel/\#setLeftMode-int) property. |

### setLeftMode(int value) {#setLeftMode-int}
```
public void setLeftMode(int value)
```


Sets the interpretation mode of the [getLeft()](../../com.aspose.words/chartdatalabel/\#getLeft) / [setLeft(double)](../../com.aspose.words/chartdatalabel/\#setLeft-double) property value: whether it sets the location of the data label from the left edge of the chart of from the position specified by its [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) property.

 **Remarks:** 

The property cannot be set in a Word 2016 chart.

 **Examples:** 

Shows how to place data labels of doughnut chart outside doughnut.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 final int CHART_WIDTH = 432;
 final int CHART_HEIGHT = 252;
 Shape shape = builder.insertChart(ChartType.DOUGHNUT, CHART_WIDTH, CHART_HEIGHT);
 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();
 // Delete default generated series.
 seriesColl.clear();

 // Hide the legend.
 chart.getLegend().setPosition(LegendPosition.NONE);

 // Generate data.
 final int DATA_LENGTH = 20;
 double totalValue = 0.0;
 String[] categories = new String[DATA_LENGTH];
 double[] values = new double[DATA_LENGTH];
 for (int i = 0; i < DATA_LENGTH; i++)
 {
     categories[i] = MessageFormat.format("Category {0}", i);
     values[i] = DATA_LENGTH - i;
     totalValue += values[i];
 }

 ChartSeries series = seriesColl.add("Series 1", categories, values);
 series.hasDataLabels(true);

 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.setShowLeaderLines(true);

 // The Position property cannot be used for doughnut charts. Let's place data labels using the Left and Top
 // properties around a circle outside of the chart doughnut.
 // The origin is in the upper left corner of the chart.

 final double TITLE_AREA_HEIGHT = 25.5; // This can be calculated using title text and font.
 final double DOUGHNUT_CENTER_Y = TITLE_AREA_HEIGHT + (CHART_HEIGHT - TITLE_AREA_HEIGHT) / 2.0;
 final double DOUGHNUT_CENTER_X = CHART_WIDTH / 2d;
 final double LABEL_HEIGHT = 16.5; // This can be calculated using label font.
 final double ONE_CHAR_LABEL_WIDTH = 12.75; // This can be calculated for each label using its text and font.
 final double TWO_CHAR_LABEL_WIDTH = 17.25; // This can be calculated for each label using its text and font.
 final double Y_MARGIN = 0.75;
 final double LABEL_MARGIN = 1.5;
 final double LABEL_CIRCLE_RADIUS = CHART_HEIGHT - DOUGHNUT_CENTER_Y - Y_MARGIN - LABEL_HEIGHT / 2.0;

 // Because the data points start at the top, the X coordinates used in the Left and Top properties of
 // the data labels point to the right and the Y coordinates point down, the starting angle is -PI/2.
 double totalAngle = -Math.PI / 2f;
 ChartDataLabel previousLabel = null;

 for (int i = 0; i < series.getYValues().getCount(); i++)
 {
     ChartDataLabel dataLabel = dataLabels.get(i);

     double value = series.getYValues().get(i).getDoubleValue();
     double labelWidth = (value < 10) ? ONE_CHAR_LABEL_WIDTH : TWO_CHAR_LABEL_WIDTH;
     double labelSegmentAngle = value / totalValue * 2.0 * Math.PI;
     double labelAngle = labelSegmentAngle / 2.0 + totalAngle;
     double labelCenterX = LABEL_CIRCLE_RADIUS * Math.cos(labelAngle) + DOUGHNUT_CENTER_X;
     double labelCenterY = LABEL_CIRCLE_RADIUS * Math.sin(labelAngle) + DOUGHNUT_CENTER_Y;
     double labelLeft = labelCenterX - labelWidth / 2.0;
     double labelTop = labelCenterY - LABEL_HEIGHT / 2.0;

     // If the current data label overlaps other labels, move it horizontally.
     if ((previousLabel != null) &&
             (Math.abs(previousLabel.getTop() - labelTop) < LABEL_HEIGHT) &&
             (Math.abs(previousLabel.getLeft() - labelLeft) < labelWidth))
     {
         // Move right on the top, left on the bottom.
         boolean isOnTop = (totalAngle < 0) || (totalAngle >= Math.PI);
         labelLeft = previousLabel.getLeft() + labelWidth * (isOnTop ? 1 : -1) + LABEL_MARGIN;
     }

     dataLabel.setLeft(labelLeft);
     dataLabel.setLeftMode(ChartDataLabelLocationMode.ABSOLUTE);
     dataLabel.setTop(labelTop);
     dataLabel.setTopMode(ChartDataLabelLocationMode.ABSOLUTE);

     totalAngle += labelSegmentAngle;
     previousLabel = dataLabel;
 }

 doc.save(getArtifactsDir() + "Charts.DoughnutChartLabelPosition.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The interpretation mode of the [getLeft()](../../com.aspose.words/chartdatalabel/\#getLeft) / [setLeft(double)](../../com.aspose.words/chartdatalabel/\#setLeft-double) property value: whether it sets the location of the data label from the left edge of the chart of from the position specified by its [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) property. The value must be one of [ChartDataLabelLocationMode](../../com.aspose.words/chartdatalabellocationmode/) constants. |

### setOrientation(int value) {#setOrientation-int}
```
public void setOrientation(int value)
```


Sets the orientation of the label text.

 **Remarks:** 

The default value is [ShapeTextOrientation.HORIZONTAL](../../com.aspose.words/shapetextorientation/\#HORIZONTAL).

 **Examples:** 

Shows how to change orientation and rotation for data labels.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 ChartSeries series = shape.getChart().getSeries().get(0);
 ChartDataLabelCollection dataLabels = series.getDataLabels();

 // Show data labels.
 series.hasDataLabels(true);
 dataLabels.setShowValue(true);
 dataLabels.setShowCategoryName(true);

 // Define data label shape.
 dataLabels.getFormat().setShapeType(ChartShapeType.UP_ARROW);
 dataLabels.getFormat().getStroke().getFill().solid(Color.blue);

 // Set data label orientation and rotation for the entire series.
 dataLabels.setOrientation(ShapeTextOrientation.VERTICAL_FAR_EAST);
 dataLabels.setRotation(-45);

 // Change orientation and rotation of the first data label.
 dataLabels.get(0).setOrientation(ShapeTextOrientation.HORIZONTAL);
 dataLabels.get(0).setRotation(45);

 doc.save(getArtifactsDir() + "Charts.LabelOrientationRotation.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The orientation of the label text. The value must be one of [ShapeTextOrientation](../../com.aspose.words/shapetextorientation/) constants. |

### setPosition(int value) {#setPosition-int}
```
public void setPosition(int value)
```


Sets the position of the data label.

 **Remarks:** 

The position can be set for data labels of the following chart series types:

\- [ChartSeriesType.BAR](../../com.aspose.words/chartseriestype/\#BAR), [ChartSeriesType.COLUMN](../../com.aspose.words/chartseriestype/\#COLUMN), [ChartSeriesType.HISTOGRAM](../../com.aspose.words/chartseriestype/\#HISTOGRAM), [ChartSeriesType.PARETO](../../com.aspose.words/chartseriestype/\#PARETO), [ChartSeriesType.WATERFALL](../../com.aspose.words/chartseriestype/\#WATERFALL); allowed values: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.INSIDE\_BASE](../../com.aspose.words/chartdatalabelposition/\#INSIDE-BASE), [ChartDataLabelPosition.INSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#INSIDE-END) and [ChartDataLabelPosition.OUTSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#OUTSIDE-END);

\- [ChartSeriesType.BAR\_STACKED](../../com.aspose.words/chartseriestype/\#BAR-STACKED), [ChartSeriesType.BAR\_PERCENT\_STACKED](../../com.aspose.words/chartseriestype/\#BAR-PERCENT-STACKED), [ChartSeriesType.COLUMN\_STACKED](../../com.aspose.words/chartseriestype/\#COLUMN-STACKED), [ChartSeriesType.COLUMN\_PERCENT\_STACKED](../../com.aspose.words/chartseriestype/\#COLUMN-PERCENT-STACKED); allowed values: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.INSIDE\_BASE](../../com.aspose.words/chartdatalabelposition/\#INSIDE-BASE) and [ChartDataLabelPosition.INSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#INSIDE-END);

\- [ChartSeriesType.BUBBLE](../../com.aspose.words/chartseriestype/\#BUBBLE), [ChartSeriesType.BUBBLE\_3\_D](../../com.aspose.words/chartseriestype/\#BUBBLE-3-D), [ChartSeriesType.LINE](../../com.aspose.words/chartseriestype/\#LINE), [ChartSeriesType.LINE\_STACKED](../../com.aspose.words/chartseriestype/\#LINE-STACKED), [ChartSeriesType.LINE\_PERCENT\_STACKED](../../com.aspose.words/chartseriestype/\#LINE-PERCENT-STACKED), [ChartSeriesType.SCATTER](../../com.aspose.words/chartseriestype/\#SCATTER), [ChartSeriesType.STOCK](../../com.aspose.words/chartseriestype/\#STOCK); allowed values: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.LEFT](../../com.aspose.words/chartdatalabelposition/\#LEFT), [ChartDataLabelPosition.RIGHT](../../com.aspose.words/chartdatalabelposition/\#RIGHT), [ChartDataLabelPosition.ABOVE](../../com.aspose.words/chartdatalabelposition/\#ABOVE) and [ChartDataLabelPosition.BELOW](../../com.aspose.words/chartdatalabelposition/\#BELOW);

\- [ChartSeriesType.PIE](../../com.aspose.words/chartseriestype/\#PIE), [ChartSeriesType.PIE\_3\_D](../../com.aspose.words/chartseriestype/\#PIE-3-D), [ChartSeriesType.PIE\_OF\_BAR](../../com.aspose.words/chartseriestype/\#PIE-OF-BAR), [ChartSeriesType.PIE\_OF\_PIE](../../com.aspose.words/chartseriestype/\#PIE-OF-PIE); allowed values: [ChartDataLabelPosition.CENTER](../../com.aspose.words/chartdatalabelposition/\#CENTER), [ChartDataLabelPosition.INSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#INSIDE-END), [ChartDataLabelPosition.OUTSIDE\_END](../../com.aspose.words/chartdatalabelposition/\#OUTSIDE-END) and [ChartDataLabelPosition.BEST\_FIT](../../com.aspose.words/chartdatalabelposition/\#BEST-FIT);

\- [ChartSeriesType.BOX\_AND\_WHISKER](../../com.aspose.words/chartseriestype/\#BOX-AND-WHISKER); allowed values: [ChartDataLabelPosition.LEFT](../../com.aspose.words/chartdatalabelposition/\#LEFT), [ChartDataLabelPosition.RIGHT](../../com.aspose.words/chartdatalabelposition/\#RIGHT), [ChartDataLabelPosition.ABOVE](../../com.aspose.words/chartdatalabelposition/\#ABOVE) and [ChartDataLabelPosition.BELOW](../../com.aspose.words/chartdatalabelposition/\#BELOW).

 **Examples:** 

Shows how to set the position of the data label.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert column chart.
 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();

 // Delete default generated series.
 seriesColl.clear();

 // Add series.
 ChartSeries series = seriesColl.add(
         "Series 1",
         new String[] { "Category 1", "Category 2", "Category 3" },
         new double[] { 4.0, 5.0, 6.0 });

 // Show data labels and set font color.
 series.hasDataLabels(true);
 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.getFont().setColor(Color.WHITE);

 // Set data label position.
 dataLabels.setPosition(ChartDataLabelPosition.INSIDE_BASE);
 dataLabels.get(0).setPosition(ChartDataLabelPosition.OUTSIDE_END);
 dataLabels.get(0).getFont().setColor(Color.RED);

 doc.save(getArtifactsDir() + "Charts.LabelPosition.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The position of the data label. The value must be one of [ChartDataLabelPosition](../../com.aspose.words/chartdatalabelposition/) constants. |

### setRotation(int value) {#setRotation-int}
```
public void setRotation(int value)
```


Sets the rotation of the label in degrees.

 **Remarks:** 

The range of acceptable values is from -180 to 180 inclusive. The default value is 0.

If the [getOrientation()](../../com.aspose.words/chartdatalabel/\#getOrientation) / [setOrientation(int)](../../com.aspose.words/chartdatalabel/\#setOrientation-int) value is [ShapeTextOrientation.HORIZONTAL](../../com.aspose.words/shapetextorientation/\#HORIZONTAL), the label shape, if it exists, is rotated along with the label text. Otherwise, only the label text is rotated.

 **Examples:** 

Shows how to change orientation and rotation for data labels.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 ChartSeries series = shape.getChart().getSeries().get(0);
 ChartDataLabelCollection dataLabels = series.getDataLabels();

 // Show data labels.
 series.hasDataLabels(true);
 dataLabels.setShowValue(true);
 dataLabels.setShowCategoryName(true);

 // Define data label shape.
 dataLabels.getFormat().setShapeType(ChartShapeType.UP_ARROW);
 dataLabels.getFormat().getStroke().getFill().solid(Color.blue);

 // Set data label orientation and rotation for the entire series.
 dataLabels.setOrientation(ShapeTextOrientation.VERTICAL_FAR_EAST);
 dataLabels.setRotation(-45);

 // Change orientation and rotation of the first data label.
 dataLabels.get(0).setOrientation(ShapeTextOrientation.HORIZONTAL);
 dataLabels.get(0).setRotation(45);

 doc.save(getArtifactsDir() + "Charts.LabelOrientationRotation.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The rotation of the label in degrees. |

### setSeparator(String value) {#setSeparator-java.lang.String}
```
public void setSeparator(String value)
```


Sets string separator used for the data labels on a chart. The default is a comma, except for pie charts showing only category name and percentage, when a line break shall be used instead.

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
| value | java.lang.String | String separator used for the data labels on a chart. |

### setShapeType(int value) {#setShapeType-int}
```
public void setShapeType(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setShowBubbleSize(boolean value) {#setShowBubbleSize-boolean}
```
public void setShowBubbleSize(boolean value)
```


Allows to specify if bubble size is to be displayed for the data labels on a chart. Applies only to Bubble charts. Default value is  false .

 **Examples:** 

Shows how to use 3D effects with bubble charts.

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
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setShowCategoryName(boolean value) {#setShowCategoryName-boolean}
```
public void setShowCategoryName(boolean value)
```


Allows to specify if category name is to be displayed for the data labels on a chart. Default value is  false .

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
| value | boolean | The corresponding  boolean  value. |

### setShowDataLabelsRange(boolean value) {#setShowDataLabelsRange-boolean}
```
public void setShowDataLabelsRange(boolean value)
```


Allows to specify if values from data labels range to be displayed in the data labels. Default value is  false .

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
| value | boolean | The corresponding  boolean  value. |

### setShowLeaderLines(boolean value) {#setShowLeaderLines-boolean}
```
public void setShowLeaderLines(boolean value)
```


Allows to specify if data label leader lines need be shown. Default value is  false .

 **Remarks:** 

Applies to Pie charts only. Leader lines create a visual connection between a data label and its corresponding data point.

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
| value | boolean | The corresponding  boolean  value. |

### setShowLegendKey(boolean value) {#setShowLegendKey-boolean}
```
public void setShowLegendKey(boolean value)
```


Allows to specify if legend key is to be displayed for the data labels on a chart. Default value is  false .

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
| value | boolean | The corresponding  boolean  value. |

### setShowPercentage(boolean value) {#setShowPercentage-boolean}
```
public void setShowPercentage(boolean value)
```


Allows to specify if percentage value is to be displayed for the data labels on a chart. Default value is  false .

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
| value | boolean | The corresponding  boolean  value. |

### setShowSeriesName(boolean value) {#setShowSeriesName-boolean}
```
public void setShowSeriesName(boolean value)
```


Sets a Boolean to indicate the series name display behavior for the data labels on a chart.  true  to show the series name;  false  to hide. By default  false .

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
| value | boolean | A Boolean to indicate the series name display behavior for the data labels on a chart. |

### setShowValue(boolean value) {#setShowValue-boolean}
```
public void setShowValue(boolean value)
```


Allows to specify if values are to be displayed in the data labels. Default value is  false .

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
| value | boolean | The corresponding  boolean  value. |

### setTop(double value) {#setTop-double}
```
public void setTop(double value)
```


Sets the distance of the data label in points from the top edge of the chart or from the position specified by its [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) property, depending on the value of the [getTopMode()](../../com.aspose.words/chartdatalabel/\#getTopMode) / [setTopMode(int)](../../com.aspose.words/chartdatalabel/\#setTopMode-int) property.

 **Remarks:** 

The value of the property changes proportionally if the chart shape is resized.

The property cannot be set in a Word 2016 chart.

 **Examples:** 

Shows how to place data labels of doughnut chart outside doughnut.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 final int CHART_WIDTH = 432;
 final int CHART_HEIGHT = 252;
 Shape shape = builder.insertChart(ChartType.DOUGHNUT, CHART_WIDTH, CHART_HEIGHT);
 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();
 // Delete default generated series.
 seriesColl.clear();

 // Hide the legend.
 chart.getLegend().setPosition(LegendPosition.NONE);

 // Generate data.
 final int DATA_LENGTH = 20;
 double totalValue = 0.0;
 String[] categories = new String[DATA_LENGTH];
 double[] values = new double[DATA_LENGTH];
 for (int i = 0; i < DATA_LENGTH; i++)
 {
     categories[i] = MessageFormat.format("Category {0}", i);
     values[i] = DATA_LENGTH - i;
     totalValue += values[i];
 }

 ChartSeries series = seriesColl.add("Series 1", categories, values);
 series.hasDataLabels(true);

 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.setShowLeaderLines(true);

 // The Position property cannot be used for doughnut charts. Let's place data labels using the Left and Top
 // properties around a circle outside of the chart doughnut.
 // The origin is in the upper left corner of the chart.

 final double TITLE_AREA_HEIGHT = 25.5; // This can be calculated using title text and font.
 final double DOUGHNUT_CENTER_Y = TITLE_AREA_HEIGHT + (CHART_HEIGHT - TITLE_AREA_HEIGHT) / 2.0;
 final double DOUGHNUT_CENTER_X = CHART_WIDTH / 2d;
 final double LABEL_HEIGHT = 16.5; // This can be calculated using label font.
 final double ONE_CHAR_LABEL_WIDTH = 12.75; // This can be calculated for each label using its text and font.
 final double TWO_CHAR_LABEL_WIDTH = 17.25; // This can be calculated for each label using its text and font.
 final double Y_MARGIN = 0.75;
 final double LABEL_MARGIN = 1.5;
 final double LABEL_CIRCLE_RADIUS = CHART_HEIGHT - DOUGHNUT_CENTER_Y - Y_MARGIN - LABEL_HEIGHT / 2.0;

 // Because the data points start at the top, the X coordinates used in the Left and Top properties of
 // the data labels point to the right and the Y coordinates point down, the starting angle is -PI/2.
 double totalAngle = -Math.PI / 2f;
 ChartDataLabel previousLabel = null;

 for (int i = 0; i < series.getYValues().getCount(); i++)
 {
     ChartDataLabel dataLabel = dataLabels.get(i);

     double value = series.getYValues().get(i).getDoubleValue();
     double labelWidth = (value < 10) ? ONE_CHAR_LABEL_WIDTH : TWO_CHAR_LABEL_WIDTH;
     double labelSegmentAngle = value / totalValue * 2.0 * Math.PI;
     double labelAngle = labelSegmentAngle / 2.0 + totalAngle;
     double labelCenterX = LABEL_CIRCLE_RADIUS * Math.cos(labelAngle) + DOUGHNUT_CENTER_X;
     double labelCenterY = LABEL_CIRCLE_RADIUS * Math.sin(labelAngle) + DOUGHNUT_CENTER_Y;
     double labelLeft = labelCenterX - labelWidth / 2.0;
     double labelTop = labelCenterY - LABEL_HEIGHT / 2.0;

     // If the current data label overlaps other labels, move it horizontally.
     if ((previousLabel != null) &&
             (Math.abs(previousLabel.getTop() - labelTop) < LABEL_HEIGHT) &&
             (Math.abs(previousLabel.getLeft() - labelLeft) < labelWidth))
     {
         // Move right on the top, left on the bottom.
         boolean isOnTop = (totalAngle < 0) || (totalAngle >= Math.PI);
         labelLeft = previousLabel.getLeft() + labelWidth * (isOnTop ? 1 : -1) + LABEL_MARGIN;
     }

     dataLabel.setLeft(labelLeft);
     dataLabel.setLeftMode(ChartDataLabelLocationMode.ABSOLUTE);
     dataLabel.setTop(labelTop);
     dataLabel.setTopMode(ChartDataLabelLocationMode.ABSOLUTE);

     totalAngle += labelSegmentAngle;
     previousLabel = dataLabel;
 }

 doc.save(getArtifactsDir() + "Charts.DoughnutChartLabelPosition.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The distance of the data label in points from the top edge of the chart or from the position specified by its [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) property, depending on the value of the [getTopMode()](../../com.aspose.words/chartdatalabel/\#getTopMode) / [setTopMode(int)](../../com.aspose.words/chartdatalabel/\#setTopMode-int) property. |

### setTopMode(int value) {#setTopMode-int}
```
public void setTopMode(int value)
```


Sets the interpretation mode of the [getTop()](../../com.aspose.words/chartdatalabel/\#getTop) / [setTop(double)](../../com.aspose.words/chartdatalabel/\#setTop-double) property value: whether it sets the location of the data label from the top edge of the chart of from the position specified by its [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) property.

 **Remarks:** 

The property cannot be set in a Word 2016 chart.

 **Examples:** 

Shows how to place data labels of doughnut chart outside doughnut.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 final int CHART_WIDTH = 432;
 final int CHART_HEIGHT = 252;
 Shape shape = builder.insertChart(ChartType.DOUGHNUT, CHART_WIDTH, CHART_HEIGHT);
 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();
 // Delete default generated series.
 seriesColl.clear();

 // Hide the legend.
 chart.getLegend().setPosition(LegendPosition.NONE);

 // Generate data.
 final int DATA_LENGTH = 20;
 double totalValue = 0.0;
 String[] categories = new String[DATA_LENGTH];
 double[] values = new double[DATA_LENGTH];
 for (int i = 0; i < DATA_LENGTH; i++)
 {
     categories[i] = MessageFormat.format("Category {0}", i);
     values[i] = DATA_LENGTH - i;
     totalValue += values[i];
 }

 ChartSeries series = seriesColl.add("Series 1", categories, values);
 series.hasDataLabels(true);

 ChartDataLabelCollection dataLabels = series.getDataLabels();
 dataLabels.setShowValue(true);
 dataLabels.setShowLeaderLines(true);

 // The Position property cannot be used for doughnut charts. Let's place data labels using the Left and Top
 // properties around a circle outside of the chart doughnut.
 // The origin is in the upper left corner of the chart.

 final double TITLE_AREA_HEIGHT = 25.5; // This can be calculated using title text and font.
 final double DOUGHNUT_CENTER_Y = TITLE_AREA_HEIGHT + (CHART_HEIGHT - TITLE_AREA_HEIGHT) / 2.0;
 final double DOUGHNUT_CENTER_X = CHART_WIDTH / 2d;
 final double LABEL_HEIGHT = 16.5; // This can be calculated using label font.
 final double ONE_CHAR_LABEL_WIDTH = 12.75; // This can be calculated for each label using its text and font.
 final double TWO_CHAR_LABEL_WIDTH = 17.25; // This can be calculated for each label using its text and font.
 final double Y_MARGIN = 0.75;
 final double LABEL_MARGIN = 1.5;
 final double LABEL_CIRCLE_RADIUS = CHART_HEIGHT - DOUGHNUT_CENTER_Y - Y_MARGIN - LABEL_HEIGHT / 2.0;

 // Because the data points start at the top, the X coordinates used in the Left and Top properties of
 // the data labels point to the right and the Y coordinates point down, the starting angle is -PI/2.
 double totalAngle = -Math.PI / 2f;
 ChartDataLabel previousLabel = null;

 for (int i = 0; i < series.getYValues().getCount(); i++)
 {
     ChartDataLabel dataLabel = dataLabels.get(i);

     double value = series.getYValues().get(i).getDoubleValue();
     double labelWidth = (value < 10) ? ONE_CHAR_LABEL_WIDTH : TWO_CHAR_LABEL_WIDTH;
     double labelSegmentAngle = value / totalValue * 2.0 * Math.PI;
     double labelAngle = labelSegmentAngle / 2.0 + totalAngle;
     double labelCenterX = LABEL_CIRCLE_RADIUS * Math.cos(labelAngle) + DOUGHNUT_CENTER_X;
     double labelCenterY = LABEL_CIRCLE_RADIUS * Math.sin(labelAngle) + DOUGHNUT_CENTER_Y;
     double labelLeft = labelCenterX - labelWidth / 2.0;
     double labelTop = labelCenterY - LABEL_HEIGHT / 2.0;

     // If the current data label overlaps other labels, move it horizontally.
     if ((previousLabel != null) &&
             (Math.abs(previousLabel.getTop() - labelTop) < LABEL_HEIGHT) &&
             (Math.abs(previousLabel.getLeft() - labelLeft) < labelWidth))
     {
         // Move right on the top, left on the bottom.
         boolean isOnTop = (totalAngle < 0) || (totalAngle >= Math.PI);
         labelLeft = previousLabel.getLeft() + labelWidth * (isOnTop ? 1 : -1) + LABEL_MARGIN;
     }

     dataLabel.setLeft(labelLeft);
     dataLabel.setLeftMode(ChartDataLabelLocationMode.ABSOLUTE);
     dataLabel.setTop(labelTop);
     dataLabel.setTopMode(ChartDataLabelLocationMode.ABSOLUTE);

     totalAngle += labelSegmentAngle;
     previousLabel = dataLabel;
 }

 doc.save(getArtifactsDir() + "Charts.DoughnutChartLabelPosition.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The interpretation mode of the [getTop()](../../com.aspose.words/chartdatalabel/\#getTop) / [setTop(double)](../../com.aspose.words/chartdatalabel/\#setTop-double) property value: whether it sets the location of the data label from the top edge of the chart of from the position specified by its [getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) property. The value must be one of [ChartDataLabelLocationMode](../../com.aspose.words/chartdatalabellocationmode/) constants. |

