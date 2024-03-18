---
title: AxisTickLabels
linktitle: AxisTickLabels
second_title: Aspose.Words for Java
description: Represents properties of axis tick mark labels in Java.
type: docs
weight: 24
url: /java/com.aspose.words/axisticklabels/
---

**Inheritance:**
java.lang.Object
```
public class AxisTickLabels
```

Represents properties of axis tick mark labels.
## Methods

| Method | Description |
| --- | --- |
| [fetchSpecialDefaultRunPropertyValue(int key)](#fetchSpecialDefaultRunPropertyValue-int) |  |
| [generateItemText()](#generateItemText) |  |
| [getAlignment()](#getAlignment) | Gets text alignment of the axis tick labels. |
| [getFont()](#getFont) | Provides access to font formatting of the tick labels. |
| [getOffset()](#getOffset) | Gets the distance of the tick labels from the axis. |
| [getPosition()](#getPosition) | Gets the position of the tick labels on the axis. |
| [getSpacing()](#getSpacing) | Gets the interval at which the tick labels are drawn. |
| [isAutoSpacing()](#isAutoSpacing) | Gets a flag indicating whether to use automatic interval for drawing the tick labels. |
| [isAutoSpacing(boolean value)](#isAutoSpacing-boolean) | Sets a flag indicating whether to use automatic interval for drawing the tick labels. |
| [setAlignment(int value)](#setAlignment-int) | Sets text alignment of the axis tick labels. |
| [setOffset(int value)](#setOffset-int) | Sets the distance of the tick labels from the axis. |
| [setPosition(int value)](#setPosition-int) | Sets the position of the tick labels on the axis. |
| [setSpacing(int value)](#setSpacing-int) | Sets the interval at which the tick labels are drawn. |
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
### getAlignment() {#getAlignment}
```
public int getAlignment()
```


Gets text alignment of the axis tick labels.

 **Remarks:** 

This property has effect only for multi-line labels.

The default value is [ParagraphAlignment.CENTER](../../com.aspose.words/paragraphalignment/\#CENTER).

.

**Returns:**
int - Text alignment of the axis tick labels. The returned value is one of [ParagraphAlignment](../../com.aspose.words/paragraphalignment/) constants.
### getFont() {#getFont}
```
public Font getFont()
```


Provides access to font formatting of the tick labels.

**Returns:**
[Font](../../com.aspose.words/font/) - The corresponding [Font](../../com.aspose.words/font/) value.
### getOffset() {#getOffset}
```
public int getOffset()
```


Gets the distance of the tick labels from the axis.

 **Remarks:** 

The property represents a percentage of the default label offset.

Valid range is from 0 to 1000 percent inclusive. The default value is 100%.

The property has effect only for category axes. It is not supported by MS Office 2016 new charts.

 **Examples:** 

Shows how to insert a chart and modify the appearance of its axes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a chart series with categories for the X-axis and respective numeric values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel", "GoogleDocs", "Note"},
         new double[]{640.0, 320.0, 280.0, 120.0, 150.0});

 // Chart axes have various options that can change their appearance,
 // such as their direction, major/minor unit ticks, and tick marks.
 ChartAxis xAxis = chart.getAxisX();
 xAxis.setCategoryType(AxisCategoryType.CATEGORY);
 xAxis.setCrosses(AxisCrosses.MINIMUM);
 xAxis.setReverseOrder(false);
 xAxis.setMajorTickMark(AxisTickMark.INSIDE);
 xAxis.setMinorTickMark(AxisTickMark.CROSS);
 xAxis.setMajorUnit(10.0d);
 xAxis.setMinorUnit(15.0d);
 xAxis.getTickLabels().setOffset(50);
 xAxis.getTickLabels().setPosition(AxisTickLabelPosition.LOW);
 xAxis.getTickLabels().isAutoSpacing(false);
 xAxis.setTickMarkSpacing(1);

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.getTickLabels().setPosition(AxisTickLabelPosition.NEXT_TO_AXIS);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Returns:**
int - The distance of the tick labels from the axis.
### getPosition() {#getPosition}
```
public int getPosition()
```


Gets the position of the tick labels on the axis.

 **Remarks:** 

The property is not supported by MS Office 2016 new charts.

 **Examples:** 

Shows how to insert a chart and modify the appearance of its axes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a chart series with categories for the X-axis and respective numeric values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel", "GoogleDocs", "Note"},
         new double[]{640.0, 320.0, 280.0, 120.0, 150.0});

 // Chart axes have various options that can change their appearance,
 // such as their direction, major/minor unit ticks, and tick marks.
 ChartAxis xAxis = chart.getAxisX();
 xAxis.setCategoryType(AxisCategoryType.CATEGORY);
 xAxis.setCrosses(AxisCrosses.MINIMUM);
 xAxis.setReverseOrder(false);
 xAxis.setMajorTickMark(AxisTickMark.INSIDE);
 xAxis.setMinorTickMark(AxisTickMark.CROSS);
 xAxis.setMajorUnit(10.0d);
 xAxis.setMinorUnit(15.0d);
 xAxis.getTickLabels().setOffset(50);
 xAxis.getTickLabels().setPosition(AxisTickLabelPosition.LOW);
 xAxis.getTickLabels().isAutoSpacing(false);
 xAxis.setTickMarkSpacing(1);

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.getTickLabels().setPosition(AxisTickLabelPosition.NEXT_TO_AXIS);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Returns:**
int - The position of the tick labels on the axis. The returned value is one of [AxisTickLabelPosition](../../com.aspose.words/axisticklabelposition/) constants.
### getSpacing() {#getSpacing}
```
public int getSpacing()
```


Gets the interval at which the tick labels are drawn.

 **Remarks:** 

The property has effect for text category and series axes. It is not supported by MS Office 2016 new charts. Valid range of a value is greater than or equal to 1.

Setting this property sets the [isAutoSpacing()](../../com.aspose.words/axisticklabels/\#isAutoSpacing) / [isAutoSpacing(boolean)](../../com.aspose.words/axisticklabels/\#isAutoSpacing-boolean) property to  false .

**Returns:**
int - The interval at which the tick labels are drawn.
### isAutoSpacing() {#isAutoSpacing}
```
public boolean isAutoSpacing()
```


Gets a flag indicating whether to use automatic interval for drawing the tick labels.

 **Remarks:** 

The default value is  true .

The property has effect for text category and series axes. It is not supported by MS Office 2016 new charts.

 **Examples:** 

Shows how to insert a chart and modify the appearance of its axes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a chart series with categories for the X-axis and respective numeric values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel", "GoogleDocs", "Note"},
         new double[]{640.0, 320.0, 280.0, 120.0, 150.0});

 // Chart axes have various options that can change their appearance,
 // such as their direction, major/minor unit ticks, and tick marks.
 ChartAxis xAxis = chart.getAxisX();
 xAxis.setCategoryType(AxisCategoryType.CATEGORY);
 xAxis.setCrosses(AxisCrosses.MINIMUM);
 xAxis.setReverseOrder(false);
 xAxis.setMajorTickMark(AxisTickMark.INSIDE);
 xAxis.setMinorTickMark(AxisTickMark.CROSS);
 xAxis.setMajorUnit(10.0d);
 xAxis.setMinorUnit(15.0d);
 xAxis.getTickLabels().setOffset(50);
 xAxis.getTickLabels().setPosition(AxisTickLabelPosition.LOW);
 xAxis.getTickLabels().isAutoSpacing(false);
 xAxis.setTickMarkSpacing(1);

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.getTickLabels().setPosition(AxisTickLabelPosition.NEXT_TO_AXIS);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Returns:**
boolean - A flag indicating whether to use automatic interval for drawing the tick labels.
### isAutoSpacing(boolean value) {#isAutoSpacing-boolean}
```
public void isAutoSpacing(boolean value)
```


Sets a flag indicating whether to use automatic interval for drawing the tick labels.

 **Remarks:** 

The default value is  true .

The property has effect for text category and series axes. It is not supported by MS Office 2016 new charts.

 **Examples:** 

Shows how to insert a chart and modify the appearance of its axes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a chart series with categories for the X-axis and respective numeric values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel", "GoogleDocs", "Note"},
         new double[]{640.0, 320.0, 280.0, 120.0, 150.0});

 // Chart axes have various options that can change their appearance,
 // such as their direction, major/minor unit ticks, and tick marks.
 ChartAxis xAxis = chart.getAxisX();
 xAxis.setCategoryType(AxisCategoryType.CATEGORY);
 xAxis.setCrosses(AxisCrosses.MINIMUM);
 xAxis.setReverseOrder(false);
 xAxis.setMajorTickMark(AxisTickMark.INSIDE);
 xAxis.setMinorTickMark(AxisTickMark.CROSS);
 xAxis.setMajorUnit(10.0d);
 xAxis.setMinorUnit(15.0d);
 xAxis.getTickLabels().setOffset(50);
 xAxis.getTickLabels().setPosition(AxisTickLabelPosition.LOW);
 xAxis.getTickLabels().isAutoSpacing(false);
 xAxis.setTickMarkSpacing(1);

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.getTickLabels().setPosition(AxisTickLabelPosition.NEXT_TO_AXIS);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether to use automatic interval for drawing the tick labels. |

### setAlignment(int value) {#setAlignment-int}
```
public void setAlignment(int value)
```


Sets text alignment of the axis tick labels.

 **Remarks:** 

This property has effect only for multi-line labels.

The default value is [ParagraphAlignment.CENTER](../../com.aspose.words/paragraphalignment/\#CENTER).

.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | Text alignment of the axis tick labels. The value must be one of [ParagraphAlignment](../../com.aspose.words/paragraphalignment/) constants. |

### setOffset(int value) {#setOffset-int}
```
public void setOffset(int value)
```


Sets the distance of the tick labels from the axis.

 **Remarks:** 

The property represents a percentage of the default label offset.

Valid range is from 0 to 1000 percent inclusive. The default value is 100%.

The property has effect only for category axes. It is not supported by MS Office 2016 new charts.

 **Examples:** 

Shows how to insert a chart and modify the appearance of its axes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a chart series with categories for the X-axis and respective numeric values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel", "GoogleDocs", "Note"},
         new double[]{640.0, 320.0, 280.0, 120.0, 150.0});

 // Chart axes have various options that can change their appearance,
 // such as their direction, major/minor unit ticks, and tick marks.
 ChartAxis xAxis = chart.getAxisX();
 xAxis.setCategoryType(AxisCategoryType.CATEGORY);
 xAxis.setCrosses(AxisCrosses.MINIMUM);
 xAxis.setReverseOrder(false);
 xAxis.setMajorTickMark(AxisTickMark.INSIDE);
 xAxis.setMinorTickMark(AxisTickMark.CROSS);
 xAxis.setMajorUnit(10.0d);
 xAxis.setMinorUnit(15.0d);
 xAxis.getTickLabels().setOffset(50);
 xAxis.getTickLabels().setPosition(AxisTickLabelPosition.LOW);
 xAxis.getTickLabels().isAutoSpacing(false);
 xAxis.setTickMarkSpacing(1);

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.getTickLabels().setPosition(AxisTickLabelPosition.NEXT_TO_AXIS);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The distance of the tick labels from the axis. |

### setPosition(int value) {#setPosition-int}
```
public void setPosition(int value)
```


Sets the position of the tick labels on the axis.

 **Remarks:** 

The property is not supported by MS Office 2016 new charts.

 **Examples:** 

Shows how to insert a chart and modify the appearance of its axes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Insert a chart series with categories for the X-axis and respective numeric values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel", "GoogleDocs", "Note"},
         new double[]{640.0, 320.0, 280.0, 120.0, 150.0});

 // Chart axes have various options that can change their appearance,
 // such as their direction, major/minor unit ticks, and tick marks.
 ChartAxis xAxis = chart.getAxisX();
 xAxis.setCategoryType(AxisCategoryType.CATEGORY);
 xAxis.setCrosses(AxisCrosses.MINIMUM);
 xAxis.setReverseOrder(false);
 xAxis.setMajorTickMark(AxisTickMark.INSIDE);
 xAxis.setMinorTickMark(AxisTickMark.CROSS);
 xAxis.setMajorUnit(10.0d);
 xAxis.setMinorUnit(15.0d);
 xAxis.getTickLabels().setOffset(50);
 xAxis.getTickLabels().setPosition(AxisTickLabelPosition.LOW);
 xAxis.getTickLabels().isAutoSpacing(false);
 xAxis.setTickMarkSpacing(1);

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.getTickLabels().setPosition(AxisTickLabelPosition.NEXT_TO_AXIS);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The position of the tick labels on the axis. The value must be one of [AxisTickLabelPosition](../../com.aspose.words/axisticklabelposition/) constants. |

### setSpacing(int value) {#setSpacing-int}
```
public void setSpacing(int value)
```


Sets the interval at which the tick labels are drawn.

 **Remarks:** 

The property has effect for text category and series axes. It is not supported by MS Office 2016 new charts. Valid range of a value is greater than or equal to 1.

Setting this property sets the [isAutoSpacing()](../../com.aspose.words/axisticklabels/\#isAutoSpacing) / [isAutoSpacing(boolean)](../../com.aspose.words/axisticklabels/\#isAutoSpacing-boolean) property to  false .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The interval at which the tick labels are drawn. |

