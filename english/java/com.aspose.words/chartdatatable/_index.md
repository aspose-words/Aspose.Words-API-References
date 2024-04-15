---
title: ChartDataTable
linktitle: ChartDataTable
second_title: Aspose.Words for Java
description: Allows to specify properties of a chart data table in Java.
type: docs
weight: 68
url: /java/com.aspose.words/chartdatatable/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class ChartDataTable implements Cloneable
```

Allows to specify properties of a chart data table.

 **Examples:** 

Shows how to show data table with chart series data.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 ChartSeriesCollection series = chart.getSeries();
 series.clear();
 double[] xValues = new double[] { 2020.0, 2021.0, 2022.0, 2023.0 };
 series.add("Series1", xValues, new double[] { 5.0, 11.0, 2.0, 7.0 });
 series.add("Series2", xValues, new double[] { 6.0, 5.5, 7.0, 7.8 });
 series.add("Series3", xValues, new double[] { 10.0, 8.0, 7.0, 9.0 });

 ChartDataTable dataTable = chart.getDataTable();
 dataTable.setShow(true);

 dataTable.hasLegendKeys(false);
 dataTable.hasHorizontalBorder(false);
 dataTable.hasVerticalBorder(false);

 dataTable.getFont().setItalic(true);
 dataTable.getFormat().getStroke().setWeight(1.0);
 dataTable.getFormat().getStroke().setDashStyle(DashStyle.SHORT_DOT);
 dataTable.getFormat().getStroke().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.DataTable.docx");
 
```
## Methods

| Method | Description |
| --- | --- |
| [fetchSpecialDefaultRunPropertyValue(int key)](#fetchSpecialDefaultRunPropertyValue-int) |  |
| [generateItemText()](#generateItemText) |  |
| [getFont()](#getFont) | Provides access to font formatting of the data table. |
| [getFormat()](#getFormat) | Provides access to fill of text background and border formatting of the data table. |
| [getRelativePropertyValue(int key, Object value)](#getRelativePropertyValue-int-java.lang.Object) |  |
| [getShapeType()](#getShapeType) |  |
| [getShow()](#getShow) | Gets a flag indicating whether the data table will be shown for the chart. |
| [hasHorizontalBorder()](#hasHorizontalBorder) | Gets a flag indicating whether a horizontal border of the data table is displayed. |
| [hasHorizontalBorder(boolean value)](#hasHorizontalBorder-boolean) | Sets a flag indicating whether a horizontal border of the data table is displayed. |
| [hasLegendKeys()](#hasLegendKeys) | Gets a flag indicating whether legend keys are displayed in the data table. |
| [hasLegendKeys(boolean value)](#hasLegendKeys-boolean) | Sets a flag indicating whether legend keys are displayed in the data table. |
| [hasOutlineBorder()](#hasOutlineBorder) | Gets a flag indicating whether an outline border, that is, a border around series and category names, is displayed. |
| [hasOutlineBorder(boolean value)](#hasOutlineBorder-boolean) | Sets a flag indicating whether an outline border, that is, a border around series and category names, is displayed. |
| [hasVerticalBorder()](#hasVerticalBorder) | Gets a flag indicating whether a vertical border of the data table is displayed. |
| [hasVerticalBorder(boolean value)](#hasVerticalBorder-boolean) | Sets a flag indicating whether a vertical border of the data table is displayed. |
| [isFillSupported()](#isFillSupported) |  |
| [isFormatDefined()](#isFormatDefined) |  |
| [materializeSpPr()](#materializeSpPr) |  |
| [setShapeType(int value)](#setShapeType-int) |  |
| [setShow(boolean value)](#setShow-boolean) | Sets a flag indicating whether the data table will be shown for the chart. |
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


Provides access to font formatting of the data table.

**Returns:**
[Font](../../com.aspose.words/font/) - The corresponding [Font](../../com.aspose.words/font/) value.
### getFormat() {#getFormat}
```
public ChartFormat getFormat()
```


Provides access to fill of text background and border formatting of the data table.

**Returns:**
[ChartFormat](../../com.aspose.words/chartformat/) - The corresponding [ChartFormat](../../com.aspose.words/chartformat/) value.
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
### getShapeType() {#getShapeType}
```
public int getShapeType()
```




**Returns:**
int
### getShow() {#getShow}
```
public boolean getShow()
```


Gets a flag indicating whether the data table will be shown for the chart. Default value is  false .

 **Remarks:** 

The following chart types do not support data tables: Scatter, Pie, Doughnut, Surface, Radar, Treemap, Sunburst, Histogram, Pareto, Box and Whisker, Waterfall, Funnel, Combo charts that include series of these types. Showing a data table for the chart types throws a java.lang.IllegalStateException exception.

 **Examples:** 

Shows how to show data table with chart series data.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 ChartSeriesCollection series = chart.getSeries();
 series.clear();
 double[] xValues = new double[] { 2020.0, 2021.0, 2022.0, 2023.0 };
 series.add("Series1", xValues, new double[] { 5.0, 11.0, 2.0, 7.0 });
 series.add("Series2", xValues, new double[] { 6.0, 5.5, 7.0, 7.8 });
 series.add("Series3", xValues, new double[] { 10.0, 8.0, 7.0, 9.0 });

 ChartDataTable dataTable = chart.getDataTable();
 dataTable.setShow(true);

 dataTable.hasLegendKeys(false);
 dataTable.hasHorizontalBorder(false);
 dataTable.hasVerticalBorder(false);

 dataTable.getFont().setItalic(true);
 dataTable.getFormat().getStroke().setWeight(1.0);
 dataTable.getFormat().getStroke().setDashStyle(DashStyle.SHORT_DOT);
 dataTable.getFormat().getStroke().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.DataTable.docx");
 
```

**Returns:**
boolean - A flag indicating whether the data table will be shown for the chart.
### hasHorizontalBorder() {#hasHorizontalBorder}
```
public boolean hasHorizontalBorder()
```


Gets a flag indicating whether a horizontal border of the data table is displayed. The default value is  true .

**Returns:**
boolean - A flag indicating whether a horizontal border of the data table is displayed.
### hasHorizontalBorder(boolean value) {#hasHorizontalBorder-boolean}
```
public void hasHorizontalBorder(boolean value)
```


Sets a flag indicating whether a horizontal border of the data table is displayed. The default value is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether a horizontal border of the data table is displayed. |

### hasLegendKeys() {#hasLegendKeys}
```
public boolean hasLegendKeys()
```


Gets a flag indicating whether legend keys are displayed in the data table. The default value is  true .

**Returns:**
boolean - A flag indicating whether legend keys are displayed in the data table.
### hasLegendKeys(boolean value) {#hasLegendKeys-boolean}
```
public void hasLegendKeys(boolean value)
```


Sets a flag indicating whether legend keys are displayed in the data table. The default value is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether legend keys are displayed in the data table. |

### hasOutlineBorder() {#hasOutlineBorder}
```
public boolean hasOutlineBorder()
```


Gets a flag indicating whether an outline border, that is, a border around series and category names, is displayed. The default value is  true .

**Returns:**
boolean - A flag indicating whether an outline border, that is, a border around series and category names, is displayed.
### hasOutlineBorder(boolean value) {#hasOutlineBorder-boolean}
```
public void hasOutlineBorder(boolean value)
```


Sets a flag indicating whether an outline border, that is, a border around series and category names, is displayed. The default value is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether an outline border, that is, a border around series and category names, is displayed. |

### hasVerticalBorder() {#hasVerticalBorder}
```
public boolean hasVerticalBorder()
```


Gets a flag indicating whether a vertical border of the data table is displayed. The default value is  true .

**Returns:**
boolean - A flag indicating whether a vertical border of the data table is displayed.
### hasVerticalBorder(boolean value) {#hasVerticalBorder-boolean}
```
public void hasVerticalBorder(boolean value)
```


Sets a flag indicating whether a vertical border of the data table is displayed. The default value is  true .

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether a vertical border of the data table is displayed. |

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

### setShow(boolean value) {#setShow-boolean}
```
public void setShow(boolean value)
```


Sets a flag indicating whether the data table will be shown for the chart. Default value is  false .

 **Remarks:** 

The following chart types do not support data tables: Scatter, Pie, Doughnut, Surface, Radar, Treemap, Sunburst, Histogram, Pareto, Box and Whisker, Waterfall, Funnel, Combo charts that include series of these types. Showing a data table for the chart types throws a java.lang.IllegalStateException exception.

 **Examples:** 

Shows how to show data table with chart series data.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);
 Chart chart = shape.getChart();

 ChartSeriesCollection series = chart.getSeries();
 series.clear();
 double[] xValues = new double[] { 2020.0, 2021.0, 2022.0, 2023.0 };
 series.add("Series1", xValues, new double[] { 5.0, 11.0, 2.0, 7.0 });
 series.add("Series2", xValues, new double[] { 6.0, 5.5, 7.0, 7.8 });
 series.add("Series3", xValues, new double[] { 10.0, 8.0, 7.0, 9.0 });

 ChartDataTable dataTable = chart.getDataTable();
 dataTable.setShow(true);

 dataTable.hasLegendKeys(false);
 dataTable.hasHorizontalBorder(false);
 dataTable.hasVerticalBorder(false);

 dataTable.getFont().setItalic(true);
 dataTable.getFormat().getStroke().setWeight(1.0);
 dataTable.getFormat().getStroke().setDashStyle(DashStyle.SHORT_DOT);
 dataTable.getFormat().getStroke().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.DataTable.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether the data table will be shown for the chart. |

