---
title: ChartLegend
linktitle: ChartLegend
second_title: Aspose.Words for Java
description: Represents chart legend properties in Java.
type: docs
weight: 65
url: /java/com.aspose.words/chartlegend/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class ChartLegend implements Cloneable
```

Represents chart legend properties.

To learn more, visit the [ Working with Charts ][Working with Charts] documentation article.

 **Examples:** 

Shows how to edit the appearance of a chart's legend.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 450.0, 300.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(3, chart.getSeries().getCount());
 Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
 Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
 Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

 // Move the chart's legend to the top right corner.
 ChartLegend legend = chart.getLegend();
 legend.setPosition(LegendPosition.TOP_RIGHT);

 // Give other chart elements, such as the graph, more room by allowing them to overlap the legend.
 legend.setOverlay(true);

 doc.save(getArtifactsDir() + "Charts.ChartLegend.docx");
 
```


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## Methods

| Method | Description |
| --- | --- |
| [getLegendEntries()](#getLegendEntries) | Returns a collection of legend entries for all series and trendlines of the parent chart. |
| [getOverlay()](#getOverlay) | Determines whether other chart elements shall be allowed to overlap legend. |
| [getPosition()](#getPosition) | Specifies the position of the legend on a chart. |
| [setOverlay(boolean value)](#setOverlay-boolean) | Determines whether other chart elements shall be allowed to overlap legend. |
| [setPosition(int value)](#setPosition-int) | Specifies the position of the legend on a chart. |
### getLegendEntries() {#getLegendEntries}
```
public ChartLegendEntryCollection getLegendEntries()
```


Returns a collection of legend entries for all series and trendlines of the parent chart.

 **Examples:** 

Shows how to work with a legend entry for chart series.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);

 Chart chart = shape.getChart();
 ChartSeriesCollection series = chart.getSeries();
 series.clear();

 String[] categories = new String[] { "AW Category 1", "AW Category 2" };

 ChartSeries series1 = series.add("Series 1", categories, new double[] { 1.0, 2.0 });
 series.add("Series 2", categories, new double[] { 3.0, 4.0 });
 series.add("Series 3", categories, new double[] { 5.0, 6.0 });
 series.add("Series 4", categories, new double[] { 0.0, 0.0 });

 ChartLegendEntryCollection legendEntries = chart.getLegend().getLegendEntries();
 legendEntries.get(3).isHidden(true);

 for (ChartLegendEntry legendEntry : legendEntries)
     legendEntry.getFont().setSize(12.0);

 series1.getLegendEntry().getFont().setItalic(true);

 doc.save(getArtifactsDir() + "Charts.LegendEntries.docx");
 
```

**Returns:**
[ChartLegendEntryCollection](../../com.aspose.words/chartlegendentrycollection/) - A collection of legend entries for all series and trendlines of the parent chart.
### getOverlay() {#getOverlay}
```
public boolean getOverlay()
```


Determines whether other chart elements shall be allowed to overlap legend. Default value is  false .

 **Examples:** 

Shows how to edit the appearance of a chart's legend.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 450.0, 300.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(3, chart.getSeries().getCount());
 Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
 Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
 Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

 // Move the chart's legend to the top right corner.
 ChartLegend legend = chart.getLegend();
 legend.setPosition(LegendPosition.TOP_RIGHT);

 // Give other chart elements, such as the graph, more room by allowing them to overlap the legend.
 legend.setOverlay(true);

 doc.save(getArtifactsDir() + "Charts.ChartLegend.docx");
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getPosition() {#getPosition}
```
public int getPosition()
```


Specifies the position of the legend on a chart. Default value is [LegendPosition.RIGHT](../../com.aspose.words/legendposition/\#RIGHT).

 **Examples:** 

Shows how to edit the appearance of a chart's legend.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 450.0, 300.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(3, chart.getSeries().getCount());
 Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
 Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
 Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

 // Move the chart's legend to the top right corner.
 ChartLegend legend = chart.getLegend();
 legend.setPosition(LegendPosition.TOP_RIGHT);

 // Give other chart elements, such as the graph, more room by allowing them to overlap the legend.
 legend.setOverlay(true);

 doc.save(getArtifactsDir() + "Charts.ChartLegend.docx");
 
```

**Returns:**
int - The corresponding  int  value. The returned value is one of [LegendPosition](../../com.aspose.words/legendposition/) constants.
### setOverlay(boolean value) {#setOverlay-boolean}
```
public void setOverlay(boolean value)
```


Determines whether other chart elements shall be allowed to overlap legend. Default value is  false .

 **Examples:** 

Shows how to edit the appearance of a chart's legend.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 450.0, 300.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(3, chart.getSeries().getCount());
 Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
 Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
 Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

 // Move the chart's legend to the top right corner.
 ChartLegend legend = chart.getLegend();
 legend.setPosition(LegendPosition.TOP_RIGHT);

 // Give other chart elements, such as the graph, more room by allowing them to overlap the legend.
 legend.setOverlay(true);

 doc.save(getArtifactsDir() + "Charts.ChartLegend.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setPosition(int value) {#setPosition-int}
```
public void setPosition(int value)
```


Specifies the position of the legend on a chart. Default value is [LegendPosition.RIGHT](../../com.aspose.words/legendposition/\#RIGHT).

 **Examples:** 

Shows how to edit the appearance of a chart's legend.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 450.0, 300.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(3, chart.getSeries().getCount());
 Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
 Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
 Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

 // Move the chart's legend to the top right corner.
 ChartLegend legend = chart.getLegend();
 legend.setPosition(LegendPosition.TOP_RIGHT);

 // Give other chart elements, such as the graph, more room by allowing them to overlap the legend.
 legend.setOverlay(true);

 doc.save(getArtifactsDir() + "Charts.ChartLegend.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [LegendPosition](../../com.aspose.words/legendposition/) constants. |

