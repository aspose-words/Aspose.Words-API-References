---
title: ChartAxisTitle
linktitle: ChartAxisTitle
second_title: Aspose.Words for Java
description: Provides access to the axis title properties in Java.
type: docs
weight: 62
url: /java/com.aspose.words/chartaxistitle/
---

**Inheritance:**
java.lang.Object
```
public class ChartAxisTitle
```

Provides access to the axis title properties.

To learn more, visit the [ Working with Charts ][Working with Charts] documentation article.

 **Examples:** 

Shows how to set chart axis title.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);

 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();
 // Delete default generated series.
 seriesColl.clear();

 seriesColl.add("AW Series 1", new String[] { "AW Category 1", "AW Category 2" }, new double[] { 1.0, 2.0 });

 // Set axis title.
 ChartAxisTitle chartAxisXTitle = chart.getAxisX().getTitle();
 chartAxisXTitle.setText("Categories");
 chartAxisXTitle.setShow(true);
 ChartAxisTitle chartAxisYTitle = chart.getAxisY().getTitle();
 chartAxisYTitle.setText("Values");
 chartAxisYTitle.setShow(true);
 chartAxisYTitle.setOverlay(true);
 chartAxisYTitle.getFont().setSize(12.0);
 chartAxisYTitle.getFont().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.ChartAxisTitle.docx");
 
```


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## Methods

| Method | Description |
| --- | --- |
| [getFont()](#getFont) | Provides access to the font formatting of the axis title. |
| [getOverlay()](#getOverlay) | Determines whether other chart elements shall be allowed to overlap the title. |
| [getShow()](#getShow) | Determines whether the title shall be shown for the axis. |
| [getText()](#getText) | Gets the text of the axis title. |
| [setOverlay(boolean value)](#setOverlay-boolean) | Determines whether other chart elements shall be allowed to overlap the title. |
| [setShow(boolean value)](#setShow-boolean) | Determines whether the title shall be shown for the axis. |
| [setText(String value)](#setText-java.lang.String) | Sets the text of the axis title. |
### getFont() {#getFont}
```
public Font getFont()
```


Provides access to the font formatting of the axis title.

 **Examples:** 

Shows how to set chart axis title.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);

 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();
 // Delete default generated series.
 seriesColl.clear();

 seriesColl.add("AW Series 1", new String[] { "AW Category 1", "AW Category 2" }, new double[] { 1.0, 2.0 });

 // Set axis title.
 ChartAxisTitle chartAxisXTitle = chart.getAxisX().getTitle();
 chartAxisXTitle.setText("Categories");
 chartAxisXTitle.setShow(true);
 ChartAxisTitle chartAxisYTitle = chart.getAxisY().getTitle();
 chartAxisYTitle.setText("Values");
 chartAxisYTitle.setShow(true);
 chartAxisYTitle.setOverlay(true);
 chartAxisYTitle.getFont().setSize(12.0);
 chartAxisYTitle.getFont().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.ChartAxisTitle.docx");
 
```

**Returns:**
[Font](../../com.aspose.words/font/) - The corresponding [Font](../../com.aspose.words/font/) value.
### getOverlay() {#getOverlay}
```
public boolean getOverlay()
```


Determines whether other chart elements shall be allowed to overlap the title. The default value is  false .

 **Examples:** 

Shows how to set chart axis title.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);

 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();
 // Delete default generated series.
 seriesColl.clear();

 seriesColl.add("AW Series 1", new String[] { "AW Category 1", "AW Category 2" }, new double[] { 1.0, 2.0 });

 // Set axis title.
 ChartAxisTitle chartAxisXTitle = chart.getAxisX().getTitle();
 chartAxisXTitle.setText("Categories");
 chartAxisXTitle.setShow(true);
 ChartAxisTitle chartAxisYTitle = chart.getAxisY().getTitle();
 chartAxisYTitle.setText("Values");
 chartAxisYTitle.setShow(true);
 chartAxisYTitle.setOverlay(true);
 chartAxisYTitle.getFont().setSize(12.0);
 chartAxisYTitle.getFont().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.ChartAxisTitle.docx");
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getShow() {#getShow}
```
public boolean getShow()
```


Determines whether the title shall be shown for the axis. The default value is  false .

 **Examples:** 

Shows how to set chart axis title.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);

 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();
 // Delete default generated series.
 seriesColl.clear();

 seriesColl.add("AW Series 1", new String[] { "AW Category 1", "AW Category 2" }, new double[] { 1.0, 2.0 });

 // Set axis title.
 ChartAxisTitle chartAxisXTitle = chart.getAxisX().getTitle();
 chartAxisXTitle.setText("Categories");
 chartAxisXTitle.setShow(true);
 ChartAxisTitle chartAxisYTitle = chart.getAxisY().getTitle();
 chartAxisYTitle.setText("Values");
 chartAxisYTitle.setShow(true);
 chartAxisYTitle.setOverlay(true);
 chartAxisYTitle.getFont().setSize(12.0);
 chartAxisYTitle.getFont().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.ChartAxisTitle.docx");
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getText() {#getText}
```
public String getText()
```


Gets the text of the axis title. If  null  or empty value is specified, auto generated title will be shown.

 **Remarks:** 

Use [getShow()](../../com.aspose.words/chartaxistitle/\#getShow) / [setShow(boolean)](../../com.aspose.words/chartaxistitle/\#setShow-boolean) option if you need to show the title.

 **Examples:** 

Shows how to set chart axis title.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);

 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();
 // Delete default generated series.
 seriesColl.clear();

 seriesColl.add("AW Series 1", new String[] { "AW Category 1", "AW Category 2" }, new double[] { 1.0, 2.0 });

 // Set axis title.
 ChartAxisTitle chartAxisXTitle = chart.getAxisX().getTitle();
 chartAxisXTitle.setText("Categories");
 chartAxisXTitle.setShow(true);
 ChartAxisTitle chartAxisYTitle = chart.getAxisY().getTitle();
 chartAxisYTitle.setText("Values");
 chartAxisYTitle.setShow(true);
 chartAxisYTitle.setOverlay(true);
 chartAxisYTitle.getFont().setSize(12.0);
 chartAxisYTitle.getFont().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.ChartAxisTitle.docx");
 
```

**Returns:**
java.lang.String - The text of the axis title.
### setOverlay(boolean value) {#setOverlay-boolean}
```
public void setOverlay(boolean value)
```


Determines whether other chart elements shall be allowed to overlap the title. The default value is  false .

 **Examples:** 

Shows how to set chart axis title.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);

 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();
 // Delete default generated series.
 seriesColl.clear();

 seriesColl.add("AW Series 1", new String[] { "AW Category 1", "AW Category 2" }, new double[] { 1.0, 2.0 });

 // Set axis title.
 ChartAxisTitle chartAxisXTitle = chart.getAxisX().getTitle();
 chartAxisXTitle.setText("Categories");
 chartAxisXTitle.setShow(true);
 ChartAxisTitle chartAxisYTitle = chart.getAxisY().getTitle();
 chartAxisYTitle.setText("Values");
 chartAxisYTitle.setShow(true);
 chartAxisYTitle.setOverlay(true);
 chartAxisYTitle.getFont().setSize(12.0);
 chartAxisYTitle.getFont().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.ChartAxisTitle.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setShow(boolean value) {#setShow-boolean}
```
public void setShow(boolean value)
```


Determines whether the title shall be shown for the axis. The default value is  false .

 **Examples:** 

Shows how to set chart axis title.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);

 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();
 // Delete default generated series.
 seriesColl.clear();

 seriesColl.add("AW Series 1", new String[] { "AW Category 1", "AW Category 2" }, new double[] { 1.0, 2.0 });

 // Set axis title.
 ChartAxisTitle chartAxisXTitle = chart.getAxisX().getTitle();
 chartAxisXTitle.setText("Categories");
 chartAxisXTitle.setShow(true);
 ChartAxisTitle chartAxisYTitle = chart.getAxisY().getTitle();
 chartAxisYTitle.setText("Values");
 chartAxisYTitle.setShow(true);
 chartAxisYTitle.setOverlay(true);
 chartAxisYTitle.getFont().setSize(12.0);
 chartAxisYTitle.getFont().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.ChartAxisTitle.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setText(String value) {#setText-java.lang.String}
```
public void setText(String value)
```


Sets the text of the axis title. If  null  or empty value is specified, auto generated title will be shown.

 **Remarks:** 

Use [getShow()](../../com.aspose.words/chartaxistitle/\#getShow) / [setShow(boolean)](../../com.aspose.words/chartaxistitle/\#setShow-boolean) option if you need to show the title.

 **Examples:** 

Shows how to set chart axis title.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 432.0, 252.0);

 Chart chart = shape.getChart();
 ChartSeriesCollection seriesColl = chart.getSeries();
 // Delete default generated series.
 seriesColl.clear();

 seriesColl.add("AW Series 1", new String[] { "AW Category 1", "AW Category 2" }, new double[] { 1.0, 2.0 });

 // Set axis title.
 ChartAxisTitle chartAxisXTitle = chart.getAxisX().getTitle();
 chartAxisXTitle.setText("Categories");
 chartAxisXTitle.setShow(true);
 ChartAxisTitle chartAxisYTitle = chart.getAxisY().getTitle();
 chartAxisYTitle.setText("Values");
 chartAxisYTitle.setShow(true);
 chartAxisYTitle.setOverlay(true);
 chartAxisYTitle.getFont().setSize(12.0);
 chartAxisYTitle.getFont().setColor(Color.BLUE);

 doc.save(getArtifactsDir() + "Charts.ChartAxisTitle.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The text of the axis title. |

