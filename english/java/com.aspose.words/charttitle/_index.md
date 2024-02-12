---
title: ChartTitle
linktitle: ChartTitle
second_title: Aspose.Words for Java
description: Provides access to the chart title properties in Java.
type: docs
weight: 80
url: /java/com.aspose.words/charttitle/
---

**Inheritance:**
java.lang.Object
```
public class ChartTitle
```

Provides access to the chart title properties.

To learn more, visit the [ Working with Charts ][Working with Charts] documentation article.

 **Examples:** 

Shows how to insert a chart and set a title.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a chart shape with a document builder and get its chart.
 Shape chartShape = builder.insertChart(ChartType.BAR, 400.0, 300.0);
 Chart chart = chartShape.getChart();

 // Use the "Title" property to give our chart a title, which appears at the top center of the chart area.
 ChartTitle title = chart.getTitle();
 title.setText("My Chart");
 title.getFont().setSize(15.0);
 title.getFont().setColor(Color.BLUE);

 // Set the "Show" property to "true" to make the title visible.
 title.setShow(true);

 // Set the "Overlay" property to "true" Give other chart elements more room by allowing them to overlap the title
 title.setOverlay(true);

 doc.save(getArtifactsDir() + "Charts.ChartTitle.docx");
 
```


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## Methods

| Method | Description |
| --- | --- |
| [getFont()](#getFont) | Provides access to the font formatting of the chart title. |
| [getOverlay()](#getOverlay) | Determines whether other chart elements shall be allowed to overlap title. |
| [getShow()](#getShow) | Determines whether the title shall be shown for this chart. |
| [getText()](#getText) | Gets the text of the chart title. |
| [setOverlay(boolean value)](#setOverlay-boolean) | Determines whether other chart elements shall be allowed to overlap title. |
| [setShow(boolean value)](#setShow-boolean) | Determines whether the title shall be shown for this chart. |
| [setText(String value)](#setText-java.lang.String) | Sets the text of the chart title. |
### getFont() {#getFont}
```
public Font getFont()
```


Provides access to the font formatting of the chart title.

 **Examples:** 

Shows how to insert a chart and set a title.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a chart shape with a document builder and get its chart.
 Shape chartShape = builder.insertChart(ChartType.BAR, 400.0, 300.0);
 Chart chart = chartShape.getChart();

 // Use the "Title" property to give our chart a title, which appears at the top center of the chart area.
 ChartTitle title = chart.getTitle();
 title.setText("My Chart");
 title.getFont().setSize(15.0);
 title.getFont().setColor(Color.BLUE);

 // Set the "Show" property to "true" to make the title visible.
 title.setShow(true);

 // Set the "Overlay" property to "true" Give other chart elements more room by allowing them to overlap the title
 title.setOverlay(true);

 doc.save(getArtifactsDir() + "Charts.ChartTitle.docx");
 
```

**Returns:**
[Font](../../com.aspose.words/font/) - The corresponding [Font](../../com.aspose.words/font/) value.
### getOverlay() {#getOverlay}
```
public boolean getOverlay()
```


Determines whether other chart elements shall be allowed to overlap title. By default overlay is  false .

 **Examples:** 

Shows how to insert a chart and set a title.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a chart shape with a document builder and get its chart.
 Shape chartShape = builder.insertChart(ChartType.BAR, 400.0, 300.0);
 Chart chart = chartShape.getChart();

 // Use the "Title" property to give our chart a title, which appears at the top center of the chart area.
 ChartTitle title = chart.getTitle();
 title.setText("My Chart");
 title.getFont().setSize(15.0);
 title.getFont().setColor(Color.BLUE);

 // Set the "Show" property to "true" to make the title visible.
 title.setShow(true);

 // Set the "Overlay" property to "true" Give other chart elements more room by allowing them to overlap the title
 title.setOverlay(true);

 doc.save(getArtifactsDir() + "Charts.ChartTitle.docx");
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getShow() {#getShow}
```
public boolean getShow()
```


Determines whether the title shall be shown for this chart. Default value is  true .

 **Examples:** 

Shows how to insert a chart and set a title.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a chart shape with a document builder and get its chart.
 Shape chartShape = builder.insertChart(ChartType.BAR, 400.0, 300.0);
 Chart chart = chartShape.getChart();

 // Use the "Title" property to give our chart a title, which appears at the top center of the chart area.
 ChartTitle title = chart.getTitle();
 title.setText("My Chart");
 title.getFont().setSize(15.0);
 title.getFont().setColor(Color.BLUE);

 // Set the "Show" property to "true" to make the title visible.
 title.setShow(true);

 // Set the "Overlay" property to "true" Give other chart elements more room by allowing them to overlap the title
 title.setOverlay(true);

 doc.save(getArtifactsDir() + "Charts.ChartTitle.docx");
 
```

**Returns:**
boolean - The corresponding  boolean  value.
### getText() {#getText}
```
public String getText()
```


Gets the text of the chart title. If  null  or empty value is specified, auto generated title will be shown.

 **Remarks:** 

Use [getShow()](../../com.aspose.words/charttitle/\#getShow) / [setShow(boolean)](../../com.aspose.words/charttitle/\#setShow-boolean) option if you need to hide the Title.

 **Examples:** 

Shows how to insert a chart and set a title.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a chart shape with a document builder and get its chart.
 Shape chartShape = builder.insertChart(ChartType.BAR, 400.0, 300.0);
 Chart chart = chartShape.getChart();

 // Use the "Title" property to give our chart a title, which appears at the top center of the chart area.
 ChartTitle title = chart.getTitle();
 title.setText("My Chart");
 title.getFont().setSize(15.0);
 title.getFont().setColor(Color.BLUE);

 // Set the "Show" property to "true" to make the title visible.
 title.setShow(true);

 // Set the "Overlay" property to "true" Give other chart elements more room by allowing them to overlap the title
 title.setOverlay(true);

 doc.save(getArtifactsDir() + "Charts.ChartTitle.docx");
 
```

**Returns:**
java.lang.String - The text of the chart title.
### setOverlay(boolean value) {#setOverlay-boolean}
```
public void setOverlay(boolean value)
```


Determines whether other chart elements shall be allowed to overlap title. By default overlay is  false .

 **Examples:** 

Shows how to insert a chart and set a title.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a chart shape with a document builder and get its chart.
 Shape chartShape = builder.insertChart(ChartType.BAR, 400.0, 300.0);
 Chart chart = chartShape.getChart();

 // Use the "Title" property to give our chart a title, which appears at the top center of the chart area.
 ChartTitle title = chart.getTitle();
 title.setText("My Chart");
 title.getFont().setSize(15.0);
 title.getFont().setColor(Color.BLUE);

 // Set the "Show" property to "true" to make the title visible.
 title.setShow(true);

 // Set the "Overlay" property to "true" Give other chart elements more room by allowing them to overlap the title
 title.setOverlay(true);

 doc.save(getArtifactsDir() + "Charts.ChartTitle.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setShow(boolean value) {#setShow-boolean}
```
public void setShow(boolean value)
```


Determines whether the title shall be shown for this chart. Default value is  true .

 **Examples:** 

Shows how to insert a chart and set a title.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a chart shape with a document builder and get its chart.
 Shape chartShape = builder.insertChart(ChartType.BAR, 400.0, 300.0);
 Chart chart = chartShape.getChart();

 // Use the "Title" property to give our chart a title, which appears at the top center of the chart area.
 ChartTitle title = chart.getTitle();
 title.setText("My Chart");
 title.getFont().setSize(15.0);
 title.getFont().setColor(Color.BLUE);

 // Set the "Show" property to "true" to make the title visible.
 title.setShow(true);

 // Set the "Overlay" property to "true" Give other chart elements more room by allowing them to overlap the title
 title.setOverlay(true);

 doc.save(getArtifactsDir() + "Charts.ChartTitle.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setText(String value) {#setText-java.lang.String}
```
public void setText(String value)
```


Sets the text of the chart title. If  null  or empty value is specified, auto generated title will be shown.

 **Remarks:** 

Use [getShow()](../../com.aspose.words/charttitle/\#getShow) / [setShow(boolean)](../../com.aspose.words/charttitle/\#setShow-boolean) option if you need to hide the Title.

 **Examples:** 

Shows how to insert a chart and set a title.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 // Insert a chart shape with a document builder and get its chart.
 Shape chartShape = builder.insertChart(ChartType.BAR, 400.0, 300.0);
 Chart chart = chartShape.getChart();

 // Use the "Title" property to give our chart a title, which appears at the top center of the chart area.
 ChartTitle title = chart.getTitle();
 title.setText("My Chart");
 title.getFont().setSize(15.0);
 title.getFont().setColor(Color.BLUE);

 // Set the "Show" property to "true" to make the title visible.
 title.setShow(true);

 // Set the "Overlay" property to "true" Give other chart elements more room by allowing them to overlap the title
 title.setOverlay(true);

 doc.save(getArtifactsDir() + "Charts.ChartTitle.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The text of the chart title. |

