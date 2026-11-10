---
title: ChartPlotArea
linktitle: ChartPlotArea
second_title: Aspose.Words for Java
description: Provides access to the plot area properties of a chart in Java.
type: docs
weight: 86
url: /java/com.aspose.words/chartplotarea/
---

**Inheritance:**
java.lang.Object
```
public class ChartPlotArea
```

Provides access to the plot area properties of a chart.

To learn more, visit the [ Working with Charts ][Working with Charts] documentation article.

 **Examples:** 

Shows how to set fill and line formatting for the plot area of a chart.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 // Delete default generated series and add our own.
 ChartSeriesCollection seriesColl = chart.getSeries();
 seriesColl.clear();
 String[] categories = new String[] { "Category 1", "Category 2" };
 seriesColl.add("Series 1", categories, new double[] { 1.0, 2.0 });
 seriesColl.add("Series 2", categories, new double[] { 3.0, 4.0 });

 // Fill the plot area with a gradient and outline it with a thin blue line.
 ChartPlotArea plotArea = chart.getPlotArea();
 plotArea.getFormat().getFill().oneColorGradient(Color.blue, GradientStyle.DIAGONAL_UP, GradientVariant.VARIANT_2, 1.0);
 plotArea.getFormat().getStroke().setForeColor(Color.BLUE);
 plotArea.getFormat().getStroke().setWeight(0.25);

 doc.save(getArtifactsDir() + "Charts.PlotAreaFormat.docx");
 
```


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## Methods

| Method | Description |
| --- | --- |
| [getFormat()](#getFormat) | Provides access to fill and line formatting of the plot area. |
| [getShapeType()](#getShapeType) |  |
| [isFillSupported()](#isFillSupported) |  |
| [isFormatDefined()](#isFormatDefined) |  |
| [materializeSpPr()](#materializeSpPr) |  |
| [setShapeType(int value)](#setShapeType-int) |  |
### getFormat() {#getFormat}
```
public ChartFormat getFormat()
```


Provides access to fill and line formatting of the plot area.

 **Examples:** 

Shows how to set fill and line formatting for the plot area of a chart.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 // Delete default generated series and add our own.
 ChartSeriesCollection seriesColl = chart.getSeries();
 seriesColl.clear();
 String[] categories = new String[] { "Category 1", "Category 2" };
 seriesColl.add("Series 1", categories, new double[] { 1.0, 2.0 });
 seriesColl.add("Series 2", categories, new double[] { 3.0, 4.0 });

 // Fill the plot area with a gradient and outline it with a thin blue line.
 ChartPlotArea plotArea = chart.getPlotArea();
 plotArea.getFormat().getFill().oneColorGradient(Color.blue, GradientStyle.DIAGONAL_UP, GradientVariant.VARIANT_2, 1.0);
 plotArea.getFormat().getStroke().setForeColor(Color.BLUE);
 plotArea.getFormat().getStroke().setWeight(0.25);

 doc.save(getArtifactsDir() + "Charts.PlotAreaFormat.docx");
 
```

**Returns:**
[ChartFormat](../../com.aspose.words/chartformat/) - The corresponding [ChartFormat](../../com.aspose.words/chartformat/) value.
### getShapeType() {#getShapeType}
```
public int getShapeType()
```




**Returns:**
int
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
### materializeSpPr() {#materializeSpPr}
```
public void materializeSpPr()
```




### setShapeType(int value) {#setShapeType-int}
```
public void setShapeType(int value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

