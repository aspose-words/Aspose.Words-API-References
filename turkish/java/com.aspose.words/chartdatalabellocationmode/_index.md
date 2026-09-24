---
title: "ChartDataLabelLocationMode"
linktitle: "ChartDataLabelLocationMode"
second_title: "Aspose.Words Java için"
description: "Veri etiketi konumunu belirten değerlerin - ChartDataLabel.getLeft / ChartDataLabel.setLeftdouble ve ChartDataLabel.getTop / ChartDataLabel.setTopdouble özelliklerinin - Java'da nasıl yorumlandığını belirtir."
type: docs
weight: 73
url: /tr/java/com.aspose.words/chartdatalabellocationmode/
---

**Inheritance:**
java.lang.Object
```
public class ChartDataLabelLocationMode
```

Veri etiketinin konumunu belirten değerlerin \\u200b\\u200b nasıl yorumlandığını belirtir - [ChartDataLabel.getLeft()](../../com.aspose.words/chartdatalabel/\#getLeft) / [ChartDataLabel.setLeft(double)](../../com.aspose.words/chartdatalabel/\#setLeft-double) ve [ChartDataLabel.getTop()](../../com.aspose.words/chartdatalabel/\#getTop) / [ChartDataLabel.setTop(double)](../../com.aspose.words/chartdatalabel/\#setTop-double) özellikleri -.

 **Examples:** 

Halka grafiğinin veri etiketlerinin halka dışına nasıl yerleştirileceğini gösterir.

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
     double labelWidth;
     if (value < 10)
         labelWidth = ONE_CHAR_LABEL_WIDTH;
     else
         labelWidth = TWO_CHAR_LABEL_WIDTH;
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
         int factor;
         if (isOnTop)
             factor = 1;
         else
             factor = -1;

         labelLeft = previousLabel.getLeft() + labelWidth * factor + LABEL_MARGIN;
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
## Alanlar

| Alan | Açıklama |
| --- | --- |
| [ABSOLUTE](#ABSOLUTE) | Bir veri etiketinin konumu, grafiğin sol üst köşesinden başlayan mutlak koordinatlar kullanılarak belirtilir. |
| [OFFSET](#OFFSET) | Bir veri etiketinin konumu, onun [ChartDataLabel.getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [ChartDataLabel.setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) özelliği tarafından tanımlanan konumdan bir offset ile belirtilir. |
| [length](#length) |  |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [fromName(String chartDataLabelLocationModeName)](#fromName-java.lang.String) |  |
| [getName(int chartDataLabelLocationMode)](#getName-int) |  |
| [getValues()](#getValues) |  |
| [toString(int chartDataLabelLocationMode)](#toString-int) |  |
### ABSOLUTE {#ABSOLUTE}
```
public static int ABSOLUTE
```


Bir veri etiketinin konumu, grafiğin sol üst köşesinden başlayan mutlak koordinatlar kullanılarak belirtilir.

### OFFSET {#OFFSET}
```
public static int OFFSET
```


Bir veri etiketinin konumu, onun [ChartDataLabel.getPosition()](../../com.aspose.words/chartdatalabel/\#getPosition) / [ChartDataLabel.setPosition(int)](../../com.aspose.words/chartdatalabel/\#setPosition-int) özelliği tarafından tanımlanan konumdan bir offset ile belirtilir.

### length {#length}
```
public static int length
```


### fromName(String chartDataLabelLocationModeName) {#fromName-java.lang.String}
```
public static int fromName(String chartDataLabelLocationModeName)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| chartDataLabelLocationModeName | java.lang.String |  |

**Returns:**
int
### getName(int chartDataLabelLocationMode) {#getName-int}
```
public static String getName(int chartDataLabelLocationMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| chartDataLabelLocationMode | int |  |

**Returns:**
java.lang.String
### getValues() {#getValues}
```
public static int[] getValues()
```




**Returns:**
int[]
### toString(int chartDataLabelLocationMode) {#toString-int}
```
public static String toString(int chartDataLabelLocationMode)
```




**Parameters:**
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| chartDataLabelLocationMode | int |  |

**Returns:**
java.lang.String
