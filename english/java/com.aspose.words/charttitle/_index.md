---
title: ChartTitle
linktitle: ChartTitle
second_title: Aspose.Words for Java
description: Provides access to the chart title properties in Java.
type: docs
weight: 74
url: /java/com.aspose.words/charttitle/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class ChartTitle implements Cloneable
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
| [clearRunAttrs()](#clearRunAttrs) |  |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [fetchInheritedRunAttr(int key)](#fetchInheritedRunAttr-int) |  |
| [getClass()](#getClass) |  |
| [getDirectRunAttr(int key)](#getDirectRunAttr-int) |  |
| [getDirectRunAttr(int key, int revisionsView)](#getDirectRunAttr-int-int) |  |
| [getOverlay()](#getOverlay) | Determines whether other chart elements shall be allowed to overlap title. |
| [getShow()](#getShow) | Determines whether the title shall be shown for this chart. |
| [getText()](#getText) | Gets the text of the chart title. |
| [hashCode()](#hashCode) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [removeRunAttr(int key)](#removeRunAttr-int) |  |
| [setOverlay(boolean value)](#setOverlay-boolean) | Determines whether other chart elements shall be allowed to overlap title. |
| [setRunAttr(int key, Object value)](#setRunAttr-int-java.lang.Object) |  |
| [setShow(boolean value)](#setShow-boolean) | Determines whether the title shall be shown for this chart. |
| [setText(String value)](#setText-java.lang.String) | Sets the text of the chart title. |
| [toString()](#toString) |  |
| [wait()](#wait) |  |
| [wait(long arg0)](#wait-long) |  |
| [wait(long arg0, int arg1)](#wait-long-int) |  |
### clearRunAttrs() {#clearRunAttrs}
```
public void clearRunAttrs()
```




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
### fetchInheritedRunAttr(int key) {#fetchInheritedRunAttr-int}
```
public Object fetchInheritedRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getDirectRunAttr(int key) {#getDirectRunAttr-int}
```
public Object getDirectRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

**Returns:**
java.lang.Object
### getDirectRunAttr(int key, int revisionsView) {#getDirectRunAttr-int-int}
```
public Object getDirectRunAttr(int key, int revisionsView)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| revisionsView | int |  |

**Returns:**
java.lang.Object
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

 // Set the "Show" property to "true" to make the title visible.
 title.setShow(true);

 // Set the "Overlay" property to "true" Give other chart elements more room by allowing them to overlap the title
 title.setOverlay(true);

 doc.save(getArtifactsDir() + "Charts.ChartTitle.docx");
 
```

**Returns:**
java.lang.String - The text of the chart title.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### removeRunAttr(int key) {#removeRunAttr-int}
```
public void removeRunAttr(int key)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |

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

### setRunAttr(int key, Object value) {#setRunAttr-int-java.lang.Object}
```
public void setRunAttr(int key, Object value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| key | int |  |
| value | java.lang.Object |  |

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

