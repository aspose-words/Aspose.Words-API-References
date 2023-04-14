---
title: ChartLegendEntry
linktitle: ChartLegendEntry
second_title: Aspose.Words for Java API Reference
description: Represents a chart legend entry in Java.
type: docs
weight: 65
url: /java/com.aspose.words/chartlegendentry/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class ChartLegendEntry implements Cloneable
```

Represents a chart legend entry.

To learn more, visit the [ Working with Charts ][Working with Charts] documentation article.

 **Remarks:** 

A legend entry corresponds to a specific chart series or trendline.

The text of the entry is the name of the series or trendline. The text cannot be changed.


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [generateItemText()](#generateItemText) |  |
| [getClass()](#getClass) |  |
| [getFont()](#getFont) | Provides access to the font formatting of this legend entry. |
| [hashCode()](#hashCode) |  |
| [isHidden()](#isHidden) | Gets a value indicating whether this entry is hidden in the chart legend. |
| [isHidden(boolean value)](#isHidden-boolean) | Sets a value indicating whether this entry is hidden in the chart legend. |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### equals(Object arg0) {#equals-java.lang.Object}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### generateItemText() {#generateItemText}
```
public String generateItemText()
```




**Returns:**
java.lang.String
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getFont() {#getFont}
```
public Font getFont()
```


Provides access to the font formatting of this legend entry.

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
[Font](../../com.aspose.words/font/) - The corresponding [Font](../../com.aspose.words/font/) value.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### isHidden() {#isHidden}
```
public boolean isHidden()
```


Gets a value indicating whether this entry is hidden in the chart legend. The default value is **false**.

 **Remarks:** 

When a chart legend entry is hidden, it does not affect the corresponding chart series or trendline that is still displayed on the chart.

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
boolean - A value indicating whether this entry is hidden in the chart legend.
### isHidden(boolean value) {#isHidden-boolean}
```
public void isHidden(boolean value)
```


Sets a value indicating whether this entry is hidden in the chart legend. The default value is **false**.

 **Remarks:** 

When a chart legend entry is hidden, it does not affect the corresponding chart series or trendline that is still displayed on the chart.

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

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A value indicating whether this entry is hidden in the chart legend. |

### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### toString() {#toString}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait}
```
public final void wait()
```




### wait(long arg0) {#wait-long}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

