---
title: AxisDisplayUnit
linktitle: AxisDisplayUnit
second_title: Aspose.Words for Java API Reference
description: Provides access to the scaling options of the display units for the value axis in Java.
type: docs
weight: 20
url: /java/com.aspose.words/axisdisplayunit/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class AxisDisplayUnit implements Cloneable
```

Provides access to the scaling options of the display units for the value axis.

To learn more, visit the [ Working with Charts ][Working with Charts] documentation article.

 **Examples:** 

Shows how to manipulate the tick marks and displayed values of a chart axis.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.SCATTER, 450.0, 250.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(1, chart.getSeries().getCount());
 Assert.assertEquals("Y-Values", chart.getSeries().get(0).getName());

 // Set the minor tick marks of the Y-axis to point away from the plot area,
 // and the major tick marks to cross the axis.
 ChartAxis axis = chart.getAxisY();
 axis.setMajorTickMark(AxisTickMark.CROSS);
 axis.setMinorTickMark(AxisTickMark.OUTSIDE);

 // Set they Y-axis to show a major tick every 10 units, and a minor tick every 1 unit.
 axis.setMajorUnit(10.0);
 axis.setMinorUnit(1.0);

 // Set the Y-axis bounds to -10 and 20.
 // This Y-axis will now display 4 major tick marks and 27 minor tick marks.
 axis.getScaling().setMinimum(new AxisBound(-10));
 axis.getScaling().setMaximum(new AxisBound(20.0));

 // For the X-axis, set the major tick marks at every 10 units,
 // every minor tick mark at 2.5 units.
 axis = chart.getAxisX();
 axis.setMajorUnit(10.0);
 axis.setMinorUnit(2.5);

 // Configure both types of tick marks to appear inside the graph plot area.
 axis.setMajorTickMark(AxisTickMark.INSIDE);
 axis.setMinorTickMark(AxisTickMark.INSIDE);

 // Set the X-axis bounds so that the X-axis spans 5 major tick marks and 12 minor tick marks.
 axis.getScaling().setMinimum(new AxisBound(-10));
 axis.getScaling().setMaximum(new AxisBound(30.0));
 axis.setTickLabelAlignment(ParagraphAlignment.RIGHT);

 Assert.assertEquals(1, axis.getTickLabelSpacing());

 // Set the tick labels to display their value in millions.
 axis.getDisplayUnit().setUnit(AxisBuiltInUnit.MILLIONS);

 // We can set a more specific value by which tick labels will display their values.
 // This statement is equivalent to the one above.
 axis.getDisplayUnit().setCustomUnit(1000000.0);
 doc.save(getArtifactsDir() + "Charts.AxisDisplayUnit.docx");
 
```


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object) |  |
| [getClass()](#getClass) |  |
| [getCustomUnit()](#getCustomUnit) | Gets a user-defined divisor to scale display units on the value axis. |
| [getDocument()](#getDocument) | Returns the Document the title holder belongs. |
| [getTitle()](#getTitle) |  |
| [getTitleDeleted()](#getTitleDeleted) |  |
| [getTitlePosition()](#getTitlePosition) |  |
| [getUnit()](#getUnit) | Gets the scaling value of the display units as one of the predefined values. |
| [hashCode()](#hashCode) |  |
| [isVisible()](#isVisible) |  |
| [notify()](#notify) |  |
| [notifyAll()](#notifyAll) |  |
| [setCustomUnit(double value)](#setCustomUnit-double) | Sets a user-defined divisor to scale display units on the value axis. |
| [setTitle(ChartTitle value)](#setTitle-com.aspose.words.ChartTitle) |  |
| [setTitleDeleted(boolean value)](#setTitleDeleted-boolean) |  |
| [setUnit(int value)](#setUnit-int) | Sets the scaling value of the display units as one of the predefined values. |
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
### getClass() {#getClass}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getCustomUnit() {#getCustomUnit}
```
public double getCustomUnit()
```


Gets a user-defined divisor to scale display units on the value axis.

 **Remarks:** 

The property is not supported by MS Office 2016 new charts. Default value is 1.

Setting this property sets the [getUnit()](../../com.aspose.words/axisdisplayunit/\#getUnit) / [setUnit(int)](../../com.aspose.words/axisdisplayunit/\#setUnit-int) property to [AxisBuiltInUnit.CUSTOM](../../com.aspose.words/axisbuiltinunit/\#CUSTOM).

 **Examples:** 

Shows how to manipulate the tick marks and displayed values of a chart axis.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.SCATTER, 450.0, 250.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(1, chart.getSeries().getCount());
 Assert.assertEquals("Y-Values", chart.getSeries().get(0).getName());

 // Set the minor tick marks of the Y-axis to point away from the plot area,
 // and the major tick marks to cross the axis.
 ChartAxis axis = chart.getAxisY();
 axis.setMajorTickMark(AxisTickMark.CROSS);
 axis.setMinorTickMark(AxisTickMark.OUTSIDE);

 // Set they Y-axis to show a major tick every 10 units, and a minor tick every 1 unit.
 axis.setMajorUnit(10.0);
 axis.setMinorUnit(1.0);

 // Set the Y-axis bounds to -10 and 20.
 // This Y-axis will now display 4 major tick marks and 27 minor tick marks.
 axis.getScaling().setMinimum(new AxisBound(-10));
 axis.getScaling().setMaximum(new AxisBound(20.0));

 // For the X-axis, set the major tick marks at every 10 units,
 // every minor tick mark at 2.5 units.
 axis = chart.getAxisX();
 axis.setMajorUnit(10.0);
 axis.setMinorUnit(2.5);

 // Configure both types of tick marks to appear inside the graph plot area.
 axis.setMajorTickMark(AxisTickMark.INSIDE);
 axis.setMinorTickMark(AxisTickMark.INSIDE);

 // Set the X-axis bounds so that the X-axis spans 5 major tick marks and 12 minor tick marks.
 axis.getScaling().setMinimum(new AxisBound(-10));
 axis.getScaling().setMaximum(new AxisBound(30.0));
 axis.setTickLabelAlignment(ParagraphAlignment.RIGHT);

 Assert.assertEquals(1, axis.getTickLabelSpacing());

 // Set the tick labels to display their value in millions.
 axis.getDisplayUnit().setUnit(AxisBuiltInUnit.MILLIONS);

 // We can set a more specific value by which tick labels will display their values.
 // This statement is equivalent to the one above.
 axis.getDisplayUnit().setCustomUnit(1000000.0);
 doc.save(getArtifactsDir() + "Charts.AxisDisplayUnit.docx");
 
```

**Returns:**
double - A user-defined divisor to scale display units on the value axis.
### getDocument() {#getDocument}
```
public DocumentBase getDocument()
```


Returns the Document the title holder belongs.

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase/) - The Document the title holder belongs.
### getTitle() {#getTitle}
```
public ChartTitle getTitle()
```




**Returns:**
[ChartTitle](../../com.aspose.words/charttitle/)
### getTitleDeleted() {#getTitleDeleted}
```
public boolean getTitleDeleted()
```




**Returns:**
boolean
### getTitlePosition() {#getTitlePosition}
```
public int getTitlePosition()
```




**Returns:**
int
### getUnit() {#getUnit}
```
public int getUnit()
```


Gets the scaling value of the display units as one of the predefined values.

 **Remarks:** 

Default value is [AxisBuiltInUnit.NONE](../../com.aspose.words/axisbuiltinunit/\#NONE). The [AxisBuiltInUnit.CUSTOM](../../com.aspose.words/axisbuiltinunit/\#CUSTOM) and [AxisBuiltInUnit.PERCENTAGE](../../com.aspose.words/axisbuiltinunit/\#PERCENTAGE) values are not available in some chart types; see [AxisBuiltInUnit](../../com.aspose.words/axisbuiltinunit/) for more information.

 **Examples:** 

Shows how to manipulate the tick marks and displayed values of a chart axis.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.SCATTER, 450.0, 250.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(1, chart.getSeries().getCount());
 Assert.assertEquals("Y-Values", chart.getSeries().get(0).getName());

 // Set the minor tick marks of the Y-axis to point away from the plot area,
 // and the major tick marks to cross the axis.
 ChartAxis axis = chart.getAxisY();
 axis.setMajorTickMark(AxisTickMark.CROSS);
 axis.setMinorTickMark(AxisTickMark.OUTSIDE);

 // Set they Y-axis to show a major tick every 10 units, and a minor tick every 1 unit.
 axis.setMajorUnit(10.0);
 axis.setMinorUnit(1.0);

 // Set the Y-axis bounds to -10 and 20.
 // This Y-axis will now display 4 major tick marks and 27 minor tick marks.
 axis.getScaling().setMinimum(new AxisBound(-10));
 axis.getScaling().setMaximum(new AxisBound(20.0));

 // For the X-axis, set the major tick marks at every 10 units,
 // every minor tick mark at 2.5 units.
 axis = chart.getAxisX();
 axis.setMajorUnit(10.0);
 axis.setMinorUnit(2.5);

 // Configure both types of tick marks to appear inside the graph plot area.
 axis.setMajorTickMark(AxisTickMark.INSIDE);
 axis.setMinorTickMark(AxisTickMark.INSIDE);

 // Set the X-axis bounds so that the X-axis spans 5 major tick marks and 12 minor tick marks.
 axis.getScaling().setMinimum(new AxisBound(-10));
 axis.getScaling().setMaximum(new AxisBound(30.0));
 axis.setTickLabelAlignment(ParagraphAlignment.RIGHT);

 Assert.assertEquals(1, axis.getTickLabelSpacing());

 // Set the tick labels to display their value in millions.
 axis.getDisplayUnit().setUnit(AxisBuiltInUnit.MILLIONS);

 // We can set a more specific value by which tick labels will display their values.
 // This statement is equivalent to the one above.
 axis.getDisplayUnit().setCustomUnit(1000000.0);
 doc.save(getArtifactsDir() + "Charts.AxisDisplayUnit.docx");
 
```

**Returns:**
int - The scaling value of the display units as one of the predefined values. The returned value is one of [AxisBuiltInUnit](../../com.aspose.words/axisbuiltinunit/) constants.
### hashCode() {#hashCode}
```
public native int hashCode()
```




**Returns:**
int
### isVisible() {#isVisible}
```
public boolean isVisible()
```




**Returns:**
boolean
### notify() {#notify}
```
public final native void notify()
```




### notifyAll() {#notifyAll}
```
public final native void notifyAll()
```




### setCustomUnit(double value) {#setCustomUnit-double}
```
public void setCustomUnit(double value)
```


Sets a user-defined divisor to scale display units on the value axis.

 **Remarks:** 

The property is not supported by MS Office 2016 new charts. Default value is 1.

Setting this property sets the [getUnit()](../../com.aspose.words/axisdisplayunit/\#getUnit) / [setUnit(int)](../../com.aspose.words/axisdisplayunit/\#setUnit-int) property to [AxisBuiltInUnit.CUSTOM](../../com.aspose.words/axisbuiltinunit/\#CUSTOM).

 **Examples:** 

Shows how to manipulate the tick marks and displayed values of a chart axis.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.SCATTER, 450.0, 250.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(1, chart.getSeries().getCount());
 Assert.assertEquals("Y-Values", chart.getSeries().get(0).getName());

 // Set the minor tick marks of the Y-axis to point away from the plot area,
 // and the major tick marks to cross the axis.
 ChartAxis axis = chart.getAxisY();
 axis.setMajorTickMark(AxisTickMark.CROSS);
 axis.setMinorTickMark(AxisTickMark.OUTSIDE);

 // Set they Y-axis to show a major tick every 10 units, and a minor tick every 1 unit.
 axis.setMajorUnit(10.0);
 axis.setMinorUnit(1.0);

 // Set the Y-axis bounds to -10 and 20.
 // This Y-axis will now display 4 major tick marks and 27 minor tick marks.
 axis.getScaling().setMinimum(new AxisBound(-10));
 axis.getScaling().setMaximum(new AxisBound(20.0));

 // For the X-axis, set the major tick marks at every 10 units,
 // every minor tick mark at 2.5 units.
 axis = chart.getAxisX();
 axis.setMajorUnit(10.0);
 axis.setMinorUnit(2.5);

 // Configure both types of tick marks to appear inside the graph plot area.
 axis.setMajorTickMark(AxisTickMark.INSIDE);
 axis.setMinorTickMark(AxisTickMark.INSIDE);

 // Set the X-axis bounds so that the X-axis spans 5 major tick marks and 12 minor tick marks.
 axis.getScaling().setMinimum(new AxisBound(-10));
 axis.getScaling().setMaximum(new AxisBound(30.0));
 axis.setTickLabelAlignment(ParagraphAlignment.RIGHT);

 Assert.assertEquals(1, axis.getTickLabelSpacing());

 // Set the tick labels to display their value in millions.
 axis.getDisplayUnit().setUnit(AxisBuiltInUnit.MILLIONS);

 // We can set a more specific value by which tick labels will display their values.
 // This statement is equivalent to the one above.
 axis.getDisplayUnit().setCustomUnit(1000000.0);
 doc.save(getArtifactsDir() + "Charts.AxisDisplayUnit.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | A user-defined divisor to scale display units on the value axis. |

### setTitle(ChartTitle value) {#setTitle-com.aspose.words.ChartTitle}
```
public void setTitle(ChartTitle value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [ChartTitle](../../com.aspose.words/charttitle/) |  |

### setTitleDeleted(boolean value) {#setTitleDeleted-boolean}
```
public void setTitleDeleted(boolean value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean |  |

### setUnit(int value) {#setUnit-int}
```
public void setUnit(int value)
```


Sets the scaling value of the display units as one of the predefined values.

 **Remarks:** 

Default value is [AxisBuiltInUnit.NONE](../../com.aspose.words/axisbuiltinunit/\#NONE). The [AxisBuiltInUnit.CUSTOM](../../com.aspose.words/axisbuiltinunit/\#CUSTOM) and [AxisBuiltInUnit.PERCENTAGE](../../com.aspose.words/axisbuiltinunit/\#PERCENTAGE) values are not available in some chart types; see [AxisBuiltInUnit](../../com.aspose.words/axisbuiltinunit/) for more information.

 **Examples:** 

Shows how to manipulate the tick marks and displayed values of a chart axis.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.SCATTER, 450.0, 250.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(1, chart.getSeries().getCount());
 Assert.assertEquals("Y-Values", chart.getSeries().get(0).getName());

 // Set the minor tick marks of the Y-axis to point away from the plot area,
 // and the major tick marks to cross the axis.
 ChartAxis axis = chart.getAxisY();
 axis.setMajorTickMark(AxisTickMark.CROSS);
 axis.setMinorTickMark(AxisTickMark.OUTSIDE);

 // Set they Y-axis to show a major tick every 10 units, and a minor tick every 1 unit.
 axis.setMajorUnit(10.0);
 axis.setMinorUnit(1.0);

 // Set the Y-axis bounds to -10 and 20.
 // This Y-axis will now display 4 major tick marks and 27 minor tick marks.
 axis.getScaling().setMinimum(new AxisBound(-10));
 axis.getScaling().setMaximum(new AxisBound(20.0));

 // For the X-axis, set the major tick marks at every 10 units,
 // every minor tick mark at 2.5 units.
 axis = chart.getAxisX();
 axis.setMajorUnit(10.0);
 axis.setMinorUnit(2.5);

 // Configure both types of tick marks to appear inside the graph plot area.
 axis.setMajorTickMark(AxisTickMark.INSIDE);
 axis.setMinorTickMark(AxisTickMark.INSIDE);

 // Set the X-axis bounds so that the X-axis spans 5 major tick marks and 12 minor tick marks.
 axis.getScaling().setMinimum(new AxisBound(-10));
 axis.getScaling().setMaximum(new AxisBound(30.0));
 axis.setTickLabelAlignment(ParagraphAlignment.RIGHT);

 Assert.assertEquals(1, axis.getTickLabelSpacing());

 // Set the tick labels to display their value in millions.
 axis.getDisplayUnit().setUnit(AxisBuiltInUnit.MILLIONS);

 // We can set a more specific value by which tick labels will display their values.
 // This statement is equivalent to the one above.
 axis.getDisplayUnit().setCustomUnit(1000000.0);
 doc.save(getArtifactsDir() + "Charts.AxisDisplayUnit.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The scaling value of the display units as one of the predefined values. The value must be one of [AxisBuiltInUnit](../../com.aspose.words/axisbuiltinunit/) constants. |

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

