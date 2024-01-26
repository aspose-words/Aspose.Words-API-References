---
title: ChartAxis
linktitle: ChartAxis
second_title: Aspose.Words for Java
description: Represents the axis options of the chart in Java.
type: docs
weight: 59
url: /java/com.aspose.words/chartaxis/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class ChartAxis implements Cloneable
```

Represents the axis options of the chart.

To learn more, visit the [ Working with Charts ][Working with Charts] documentation article.

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
 xAxis.setTickLabelOffset(50);
 xAxis.setTickLabelPosition(AxisTickLabelPosition.LOW);
 xAxis.setTickLabelSpacingIsAuto(false);
 xAxis.setTickMarkSpacing(1);

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.setTickLabelPosition(AxisTickLabelPosition.NEXT_TO_AXIS);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```


[Working with Charts]: https://docs.aspose.com/words/java/working-with-charts/
## Methods

| Method | Description |
| --- | --- |
| [getAxisBetweenCategories()](#getAxisBetweenCategories) | Gets a flag indicating whether the value axis crosses the category axis between categories. |
| [getBaseTimeUnit()](#getBaseTimeUnit) | Gets the smallest time unit that is represented on the time category axis. |
| [getCategoryType()](#getCategoryType) | Gets type of the category axis. |
| [getCrosses()](#getCrosses) | Specifies how this axis crosses the perpendicular axis. |
| [getCrossesAt()](#getCrossesAt) | Specifies where on the perpendicular axis the axis crosses. |
| [getDefaultFontSize()](#getDefaultFontSize) |  |
| [getDefaultTitleText()](#getDefaultTitleText) |  |
| [getDisplayUnit()](#getDisplayUnit) | Specifies the scaling value of the display units for the value axis. |
| [getDocument()](#getDocument) | Returns the Document the title holder belongs. |
| [getHidden()](#getHidden) | Gets a flag indicating whether this axis is hidden or not. |
| [getMajorTickMark()](#getMajorTickMark) | Gets the major tick marks. |
| [getMajorUnit()](#getMajorUnit) | Gets the distance between major tick marks. |
| [getMajorUnitIsAuto()](#getMajorUnitIsAuto) | Gets a flag indicating whether default distance between major tick marks shall be used. |
| [getMajorUnitScale()](#getMajorUnitScale) | Gets the scale value for major tick marks on the time category axis. |
| [getMinorTickMark()](#getMinorTickMark) | Gets the minor tick marks for the axis. |
| [getMinorUnit()](#getMinorUnit) | Gets the distance between minor tick marks. |
| [getMinorUnitIsAuto()](#getMinorUnitIsAuto) | Gets a flag indicating whether default distance between minor tick marks shall be used. |
| [getMinorUnitScale()](#getMinorUnitScale) | Gets the scale value for minor tick marks on the time category axis. |
| [getNumberFormat()](#getNumberFormat) | Returns a [ChartNumberFormat](../../com.aspose.words/chartnumberformat/) object that allows defining number formats for the axis. |
| [getReverseOrder()](#getReverseOrder) | Gets a flag indicating whether values of axis should be displayed in reverse order, i.e. |
| [getScaling()](#getScaling) | Provides access to the scaling options of the axis. |
| [getTickLabelAlignment()](#getTickLabelAlignment) | Gets text alignment of axis tick labels. |
| [getTickLabelOffset()](#getTickLabelOffset) | Gets the distance of labels from the axis. |
| [getTickLabelPosition()](#getTickLabelPosition) | Gets the position of the tick labels on the axis. |
| [getTickLabelSpacing()](#getTickLabelSpacing) | Gets the interval, at which tick labels are drawn. |
| [getTickLabelSpacingIsAuto()](#getTickLabelSpacingIsAuto) | Gets a flag indicating whether automatic interval of drawing tick labels shall be used. |
| [getTickMarkSpacing()](#getTickMarkSpacing) | Gets the interval, at which tick marks are drawn. |
| [getTitle()](#getTitle) | Provides access to the axis title properties. |
| [getTitleDeleted()](#getTitleDeleted) |  |
| [getTitlePosition()](#getTitlePosition) |  |
| [getType()](#getType) | Returns type of the axis. |
| [hasMajorGridlines()](#hasMajorGridlines) | Gets a flag indicating whether the axis has major gridlines. |
| [hasMajorGridlines(boolean value)](#hasMajorGridlines-boolean) | Sets a flag indicating whether the axis has major gridlines. |
| [hasMinorGridlines()](#hasMinorGridlines) | Gets a flag indicating whether the axis has minor gridlines. |
| [hasMinorGridlines(boolean value)](#hasMinorGridlines-boolean) | Sets a flag indicating whether the axis has minor gridlines. |
| [isInherited()](#isInherited) |  |
| [isVisible()](#isVisible) |  |
| [setAxisBetweenCategories(boolean value)](#setAxisBetweenCategories-boolean) | Sets a flag indicating whether the value axis crosses the category axis between categories. |
| [setBaseTimeUnit(int value)](#setBaseTimeUnit-int) | Sets the smallest time unit that is represented on the time category axis. |
| [setCategoryType(int value)](#setCategoryType-int) | Sets type of the category axis. |
| [setCrosses(int value)](#setCrosses-int) | Specifies how this axis crosses the perpendicular axis. |
| [setCrossesAt(double value)](#setCrossesAt-double) | Specifies where on the perpendicular axis the axis crosses. |
| [setHidden(boolean value)](#setHidden-boolean) | Sets a flag indicating whether this axis is hidden or not. |
| [setMajorTickMark(int value)](#setMajorTickMark-int) | Sets the major tick marks. |
| [setMajorUnit(double value)](#setMajorUnit-double) | Sets the distance between major tick marks. |
| [setMajorUnitIsAuto(boolean value)](#setMajorUnitIsAuto-boolean) | Sets a flag indicating whether default distance between major tick marks shall be used. |
| [setMajorUnitScale(int value)](#setMajorUnitScale-int) | Sets the scale value for major tick marks on the time category axis. |
| [setMinorTickMark(int value)](#setMinorTickMark-int) | Sets the minor tick marks for the axis. |
| [setMinorUnit(double value)](#setMinorUnit-double) | Sets the distance between minor tick marks. |
| [setMinorUnitIsAuto(boolean value)](#setMinorUnitIsAuto-boolean) | Sets a flag indicating whether default distance between minor tick marks shall be used. |
| [setMinorUnitScale(int value)](#setMinorUnitScale-int) | Sets the scale value for minor tick marks on the time category axis. |
| [setReverseOrder(boolean value)](#setReverseOrder-boolean) | Sets a flag indicating whether values of axis should be displayed in reverse order, i.e. |
| [setTickLabelAlignment(int value)](#setTickLabelAlignment-int) | Sets text alignment of axis tick labels. |
| [setTickLabelOffset(int value)](#setTickLabelOffset-int) | Sets the distance of labels from the axis. |
| [setTickLabelPosition(int value)](#setTickLabelPosition-int) | Sets the position of the tick labels on the axis. |
| [setTickLabelSpacing(int value)](#setTickLabelSpacing-int) | Sets the interval, at which tick labels are drawn. |
| [setTickLabelSpacingIsAuto(boolean value)](#setTickLabelSpacingIsAuto-boolean) | Sets a flag indicating whether automatic interval of drawing tick labels shall be used. |
| [setTickMarkSpacing(int value)](#setTickMarkSpacing-int) | Sets the interval, at which tick marks are drawn. |
| [setTitleDeleted(boolean value)](#setTitleDeleted-boolean) |  |
### getAxisBetweenCategories() {#getAxisBetweenCategories}
```
public boolean getAxisBetweenCategories()
```


Gets a flag indicating whether the value axis crosses the category axis between categories.

 **Remarks:** 

The property has effect only for value axes. It is not supported by MS Office 2016 new charts.

 **Examples:** 

Shows how to get a graph axis to cross at a custom location.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 450.0, 250.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(3, chart.getSeries().getCount());
 Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
 Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
 Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

 // For column charts, the Y-axis crosses at zero by default,
 // which means that columns for all values below zero point down to represent negative values.
 // We can set a different value for the Y-axis crossing. In this case, we will set it to 3.
 ChartAxis axis = chart.getAxisX();
 axis.setCrosses(AxisCrosses.CUSTOM);
 axis.setCrossesAt(3.0);
 axis.setAxisBetweenCategories(true);

 doc.save(getArtifactsDir() + "Charts.AxisCross.docx");
 
```

**Returns:**
boolean - A flag indicating whether the value axis crosses the category axis between categories.
### getBaseTimeUnit() {#getBaseTimeUnit}
```
public int getBaseTimeUnit()
```


Gets the smallest time unit that is represented on the time category axis.

 **Remarks:** 

The property has effect only for time category axes.

 **Examples:** 

Shows how to insert chart with date/time values.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series containing date/time values for the X-axis, and respective decimal values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new Date[]
                 {
                         DocumentHelper.createDate(2017, 11, 6), DocumentHelper.createDate(2017, 11, 9), DocumentHelper.createDate(2017, 11, 15),
                         DocumentHelper.createDate(2017, 11, 21), DocumentHelper.createDate(2017, 11, 25), DocumentHelper.createDate(2017, 11, 29)
                 },
         new double[]{1.2, 0.3, 2.1, 2.9, 4.2, 5.3});

 // Set lower and upper bounds for the X-axis.
 ChartAxis xAxis = chart.getAxisX();
 xAxis.getScaling().setMinimum(new AxisBound(DocumentHelper.createDate(2017, 11, 5)));
 xAxis.getScaling().setMaximum(new AxisBound(DocumentHelper.createDate(2017, 12, 3)));

 // Set the major units of the X-axis to a week, and the minor units to a day.
 xAxis.setBaseTimeUnit(AxisTimeUnit.DAYS);
 xAxis.setMajorUnit(7.0d);
 xAxis.setMajorTickMark(AxisTickMark.CROSS);
 xAxis.setMinorUnit(1.0d);
 xAxis.setMinorTickMark(AxisTickMark.OUTSIDE);
 xAxis.hasMajorGridlines(true);
 xAxis.hasMinorGridlines(true);

 // Define Y-axis properties for decimal values.
 ChartAxis yAxis = chart.getAxisY();
 yAxis.setTickLabelPosition(AxisTickLabelPosition.HIGH);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(50.0d);
 yAxis.getDisplayUnit().setUnit(AxisBuiltInUnit.HUNDREDS);
 yAxis.getScaling().setMinimum(new AxisBound(100.0));
 yAxis.getScaling().setMaximum(new AxisBound(700.0));
 yAxis.hasMajorGridlines(true);
 yAxis.hasMinorGridlines(true);

 doc.save(getArtifactsDir() + "Charts.DateTimeValues.docx");
 
```

**Returns:**
int - The smallest time unit that is represented on the time category axis. The returned value is one of [AxisTimeUnit](../../com.aspose.words/axistimeunit/) constants.
### getCategoryType() {#getCategoryType}
```
public int getCategoryType()
```


Gets type of the category axis.

 **Remarks:** 

Only text categories ( [AxisCategoryType.CATEGORY](../../com.aspose.words/axiscategorytype/\#CATEGORY)) are allowed in MS Office 2016 new charts.

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
 xAxis.setTickLabelOffset(50);
 xAxis.setTickLabelPosition(AxisTickLabelPosition.LOW);
 xAxis.setTickLabelSpacingIsAuto(false);
 xAxis.setTickMarkSpacing(1);

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.setTickLabelPosition(AxisTickLabelPosition.NEXT_TO_AXIS);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Returns:**
int - Type of the category axis. The returned value is one of [AxisCategoryType](../../com.aspose.words/axiscategorytype/) constants.
### getCrosses() {#getCrosses}
```
public int getCrosses()
```


Specifies how this axis crosses the perpendicular axis.

 **Remarks:** 

Default value is [AxisCrosses.AUTOMATIC](../../com.aspose.words/axiscrosses/\#AUTOMATIC).

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
 xAxis.setTickLabelOffset(50);
 xAxis.setTickLabelPosition(AxisTickLabelPosition.LOW);
 xAxis.setTickLabelSpacingIsAuto(false);
 xAxis.setTickMarkSpacing(1);

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.setTickLabelPosition(AxisTickLabelPosition.NEXT_TO_AXIS);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Returns:**
int - The corresponding  int  value. The returned value is one of [AxisCrosses](../../com.aspose.words/axiscrosses/) constants.
### getCrossesAt() {#getCrossesAt}
```
public double getCrossesAt()
```


Specifies where on the perpendicular axis the axis crosses.

 **Remarks:** 

The property has effect only if [getCrosses()](../../com.aspose.words/chartaxis/\#getCrosses) / [setCrosses(int)](../../com.aspose.words/chartaxis/\#setCrosses-int) are set to [AxisCrosses.CUSTOM](../../com.aspose.words/axiscrosses/\#CUSTOM). It is not supported by MS Office 2016 new charts.

The units are determined by the type of axis. When the axis is a value axis, the value of the property is a decimal number on the value axis. When the axis is a time category axis, the value is defined as an integer number of days relative to the base date (30/12/1899). For a text category axis, the value is an integer category number, starting with 1 as the first category.

 **Examples:** 

Shows how to get a graph axis to cross at a custom location.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 450.0, 250.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(3, chart.getSeries().getCount());
 Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
 Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
 Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

 // For column charts, the Y-axis crosses at zero by default,
 // which means that columns for all values below zero point down to represent negative values.
 // We can set a different value for the Y-axis crossing. In this case, we will set it to 3.
 ChartAxis axis = chart.getAxisX();
 axis.setCrosses(AxisCrosses.CUSTOM);
 axis.setCrossesAt(3.0);
 axis.setAxisBetweenCategories(true);

 doc.save(getArtifactsDir() + "Charts.AxisCross.docx");
 
```

**Returns:**
double - The corresponding  double  value.
### getDefaultFontSize() {#getDefaultFontSize}
```
public double getDefaultFontSize()
```




**Returns:**
double
### getDefaultTitleText() {#getDefaultTitleText}
```
public String getDefaultTitleText()
```




**Returns:**
java.lang.String
### getDisplayUnit() {#getDisplayUnit}
```
public AxisDisplayUnit getDisplayUnit()
```


Specifies the scaling value of the display units for the value axis.

 **Remarks:** 

The property has effect only for value axes.

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
[AxisDisplayUnit](../../com.aspose.words/axisdisplayunit/) - The corresponding [AxisDisplayUnit](../../com.aspose.words/axisdisplayunit/) value.
### getDocument() {#getDocument}
```
public DocumentBase getDocument()
```


Returns the Document the title holder belongs.

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase/) - The Document the title holder belongs.
### getHidden() {#getHidden}
```
public boolean getHidden()
```


Gets a flag indicating whether this axis is hidden or not.

 **Remarks:** 

Default value is  false .

 **Examples:** 

Shows how to hide chart axes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series with categories for the X-axis, and respective decimal values for the Y-axis.
 chart.getSeries().add("AW Series 1",
         new String[]{"Item 1", "Item 2", "Item 3", "Item 4", "Item 5"},
         new double[]{1.2, 0.3, 2.1, 2.9, 4.2});

 // Hide the chart axes to simplify the appearance of the chart.
 chart.getAxisX().setHidden(true);
 chart.getAxisY().setHidden(true);

 doc.save(getArtifactsDir() + "Charts.HideChartAxis.docx");
 
```

**Returns:**
boolean - A flag indicating whether this axis is hidden or not.
### getMajorTickMark() {#getMajorTickMark}
```
public int getMajorTickMark()
```


Gets the major tick marks.

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
 xAxis.setTickLabelOffset(50);
 xAxis.setTickLabelPosition(AxisTickLabelPosition.LOW);
 xAxis.setTickLabelSpacingIsAuto(false);
 xAxis.setTickMarkSpacing(1);

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.setTickLabelPosition(AxisTickLabelPosition.NEXT_TO_AXIS);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Returns:**
int - The major tick marks. The returned value is one of [AxisTickMark](../../com.aspose.words/axistickmark/) constants.
### getMajorUnit() {#getMajorUnit}
```
public double getMajorUnit()
```


Gets the distance between major tick marks.

 **Remarks:** 

Valid range of a value is greater than zero. The property has effect for time category and value axes.

Setting this property sets the [getMajorUnitIsAuto()](../../com.aspose.words/chartaxis/\#getMajorUnitIsAuto) / [setMajorUnitIsAuto(boolean)](../../com.aspose.words/chartaxis/\#setMajorUnitIsAuto-boolean) property to  false .

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
 xAxis.setTickLabelOffset(50);
 xAxis.setTickLabelPosition(AxisTickLabelPosition.LOW);
 xAxis.setTickLabelSpacingIsAuto(false);
 xAxis.setTickMarkSpacing(1);

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.setTickLabelPosition(AxisTickLabelPosition.NEXT_TO_AXIS);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Returns:**
double - The distance between major tick marks.
### getMajorUnitIsAuto() {#getMajorUnitIsAuto}
```
public boolean getMajorUnitIsAuto()
```


Gets a flag indicating whether default distance between major tick marks shall be used.

 **Remarks:** 

The property has effect for time category and value axes.

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
boolean - A flag indicating whether default distance between major tick marks shall be used.
### getMajorUnitScale() {#getMajorUnitScale}
```
public int getMajorUnitScale()
```


Gets the scale value for major tick marks on the time category axis.

 **Remarks:** 

The property has effect only for time category axes.

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
int - The scale value for major tick marks on the time category axis. The returned value is one of [AxisTimeUnit](../../com.aspose.words/axistimeunit/) constants.
### getMinorTickMark() {#getMinorTickMark}
```
public int getMinorTickMark()
```


Gets the minor tick marks for the axis.

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
 xAxis.setTickLabelOffset(50);
 xAxis.setTickLabelPosition(AxisTickLabelPosition.LOW);
 xAxis.setTickLabelSpacingIsAuto(false);
 xAxis.setTickMarkSpacing(1);

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.setTickLabelPosition(AxisTickLabelPosition.NEXT_TO_AXIS);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Returns:**
int - The minor tick marks for the axis. The returned value is one of [AxisTickMark](../../com.aspose.words/axistickmark/) constants.
### getMinorUnit() {#getMinorUnit}
```
public double getMinorUnit()
```


Gets the distance between minor tick marks.

 **Remarks:** 

Valid range of a value is greater than zero. The property has effect for time category and value axes.

Setting this property sets the [getMinorUnitIsAuto()](../../com.aspose.words/chartaxis/\#getMinorUnitIsAuto) / [setMinorUnitIsAuto(boolean)](../../com.aspose.words/chartaxis/\#setMinorUnitIsAuto-boolean) property to  false .

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
 xAxis.setTickLabelOffset(50);
 xAxis.setTickLabelPosition(AxisTickLabelPosition.LOW);
 xAxis.setTickLabelSpacingIsAuto(false);
 xAxis.setTickMarkSpacing(1);

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.setTickLabelPosition(AxisTickLabelPosition.NEXT_TO_AXIS);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Returns:**
double - The distance between minor tick marks.
### getMinorUnitIsAuto() {#getMinorUnitIsAuto}
```
public boolean getMinorUnitIsAuto()
```


Gets a flag indicating whether default distance between minor tick marks shall be used.

 **Remarks:** 

The property has effect for time category and value axes.

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
boolean - A flag indicating whether default distance between minor tick marks shall be used.
### getMinorUnitScale() {#getMinorUnitScale}
```
public int getMinorUnitScale()
```


Gets the scale value for minor tick marks on the time category axis.

 **Remarks:** 

The property has effect only for time category axes.

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
int - The scale value for minor tick marks on the time category axis. The returned value is one of [AxisTimeUnit](../../com.aspose.words/axistimeunit/) constants.
### getNumberFormat() {#getNumberFormat}
```
public ChartNumberFormat getNumberFormat()
```


Returns a [ChartNumberFormat](../../com.aspose.words/chartnumberformat/) object that allows defining number formats for the axis.

 **Examples:** 

Shows how to set formatting for chart values.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series to the chart with categories for the X-axis,
 // and large respective numeric values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new String[]{"Word", "PDF", "Excel", "GoogleDocs", "Note"},
         new double[]{1900000.0, 850000.0, 2100000.0, 600000.0, 1500000.0});

 // Set the number format of the Y-axis tick labels to not group digits with commas.
 chart.getAxisY().getNumberFormat().setFormatCode("#,##0");

 // This flag can override the above value and draw the number format from the source cell.
 Assert.assertFalse(chart.getAxisY().getNumberFormat().isLinkedToSource());

 doc.save(getArtifactsDir() + "Charts.SetNumberFormatToChartAxis.docx");
 
```

**Returns:**
[ChartNumberFormat](../../com.aspose.words/chartnumberformat/) - A [ChartNumberFormat](../../com.aspose.words/chartnumberformat/) object that allows defining number formats for the axis.
### getReverseOrder() {#getReverseOrder}
```
public boolean getReverseOrder()
```


Gets a flag indicating whether values of axis should be displayed in reverse order, i.e. from max to min.

 **Remarks:** 

The property is not supported by MS Office 2016 new charts. Default value is  false .

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
 xAxis.setTickLabelOffset(50);
 xAxis.setTickLabelPosition(AxisTickLabelPosition.LOW);
 xAxis.setTickLabelSpacingIsAuto(false);
 xAxis.setTickMarkSpacing(1);

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.setTickLabelPosition(AxisTickLabelPosition.NEXT_TO_AXIS);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Returns:**
boolean - A flag indicating whether values of axis should be displayed in reverse order, i.e.
### getScaling() {#getScaling}
```
public AxisScaling getScaling()
```


Provides access to the scaling options of the axis.

 **Examples:** 

Shows how to insert chart with date/time values.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series containing date/time values for the X-axis, and respective decimal values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new Date[]
                 {
                         DocumentHelper.createDate(2017, 11, 6), DocumentHelper.createDate(2017, 11, 9), DocumentHelper.createDate(2017, 11, 15),
                         DocumentHelper.createDate(2017, 11, 21), DocumentHelper.createDate(2017, 11, 25), DocumentHelper.createDate(2017, 11, 29)
                 },
         new double[]{1.2, 0.3, 2.1, 2.9, 4.2, 5.3});

 // Set lower and upper bounds for the X-axis.
 ChartAxis xAxis = chart.getAxisX();
 xAxis.getScaling().setMinimum(new AxisBound(DocumentHelper.createDate(2017, 11, 5)));
 xAxis.getScaling().setMaximum(new AxisBound(DocumentHelper.createDate(2017, 12, 3)));

 // Set the major units of the X-axis to a week, and the minor units to a day.
 xAxis.setBaseTimeUnit(AxisTimeUnit.DAYS);
 xAxis.setMajorUnit(7.0d);
 xAxis.setMajorTickMark(AxisTickMark.CROSS);
 xAxis.setMinorUnit(1.0d);
 xAxis.setMinorTickMark(AxisTickMark.OUTSIDE);
 xAxis.hasMajorGridlines(true);
 xAxis.hasMinorGridlines(true);

 // Define Y-axis properties for decimal values.
 ChartAxis yAxis = chart.getAxisY();
 yAxis.setTickLabelPosition(AxisTickLabelPosition.HIGH);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(50.0d);
 yAxis.getDisplayUnit().setUnit(AxisBuiltInUnit.HUNDREDS);
 yAxis.getScaling().setMinimum(new AxisBound(100.0));
 yAxis.getScaling().setMaximum(new AxisBound(700.0));
 yAxis.hasMajorGridlines(true);
 yAxis.hasMinorGridlines(true);

 doc.save(getArtifactsDir() + "Charts.DateTimeValues.docx");
 
```

**Returns:**
[AxisScaling](../../com.aspose.words/axisscaling/) - The corresponding [AxisScaling](../../com.aspose.words/axisscaling/) value.
### getTickLabelAlignment() {#getTickLabelAlignment}
```
public int getTickLabelAlignment()
```


Gets text alignment of axis tick labels.

 **Remarks:** 

This property has effect only for multi-line labels.

Default value is [ParagraphAlignment.CENTER](../../com.aspose.words/paragraphalignment/\#CENTER).

.

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
int - Text alignment of axis tick labels. The returned value is one of [ParagraphAlignment](../../com.aspose.words/paragraphalignment/) constants.
### getTickLabelOffset() {#getTickLabelOffset}
```
public int getTickLabelOffset()
```


Gets the distance of labels from the axis.

 **Remarks:** 

The property represents a percentage of the default label offset.

Valid range is from 0 to 1000 percent inclusive. Default value is 100%.

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
 xAxis.setTickLabelOffset(50);
 xAxis.setTickLabelPosition(AxisTickLabelPosition.LOW);
 xAxis.setTickLabelSpacingIsAuto(false);
 xAxis.setTickMarkSpacing(1);

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.setTickLabelPosition(AxisTickLabelPosition.NEXT_TO_AXIS);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Returns:**
int - The distance of labels from the axis.
### getTickLabelPosition() {#getTickLabelPosition}
```
public int getTickLabelPosition()
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
 xAxis.setTickLabelOffset(50);
 xAxis.setTickLabelPosition(AxisTickLabelPosition.LOW);
 xAxis.setTickLabelSpacingIsAuto(false);
 xAxis.setTickMarkSpacing(1);

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.setTickLabelPosition(AxisTickLabelPosition.NEXT_TO_AXIS);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Returns:**
int - The position of the tick labels on the axis. The returned value is one of [AxisTickLabelPosition](../../com.aspose.words/axisticklabelposition/) constants.
### getTickLabelSpacing() {#getTickLabelSpacing}
```
public int getTickLabelSpacing()
```


Gets the interval, at which tick labels are drawn.

 **Remarks:** 

The property has effect for text category and series axes. It is not supported by MS Office 2016 new charts. Valid range of a value is greater than or equal to 1.

Setting this property sets the [getTickLabelSpacingIsAuto()](../../com.aspose.words/chartaxis/\#getTickLabelSpacingIsAuto) / [setTickLabelSpacingIsAuto(boolean)](../../com.aspose.words/chartaxis/\#setTickLabelSpacingIsAuto-boolean) property to  false .

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
int - The interval, at which tick labels are drawn.
### getTickLabelSpacingIsAuto() {#getTickLabelSpacingIsAuto}
```
public boolean getTickLabelSpacingIsAuto()
```


Gets a flag indicating whether automatic interval of drawing tick labels shall be used.

 **Remarks:** 

Default value is  true .

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
 xAxis.setTickLabelOffset(50);
 xAxis.setTickLabelPosition(AxisTickLabelPosition.LOW);
 xAxis.setTickLabelSpacingIsAuto(false);
 xAxis.setTickMarkSpacing(1);

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.setTickLabelPosition(AxisTickLabelPosition.NEXT_TO_AXIS);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Returns:**
boolean - A flag indicating whether automatic interval of drawing tick labels shall be used.
### getTickMarkSpacing() {#getTickMarkSpacing}
```
public int getTickMarkSpacing()
```


Gets the interval, at which tick marks are drawn.

 **Remarks:** 

The property has effect for text category and series axes. It is not supported by MS Office 2016 new charts.

Valid range of a value is greater than or equal to 1.

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
 xAxis.setTickLabelOffset(50);
 xAxis.setTickLabelPosition(AxisTickLabelPosition.LOW);
 xAxis.setTickLabelSpacingIsAuto(false);
 xAxis.setTickMarkSpacing(1);

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.setTickLabelPosition(AxisTickLabelPosition.NEXT_TO_AXIS);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Returns:**
int - The interval, at which tick marks are drawn.
### getTitle() {#getTitle}
```
public ChartAxisTitle getTitle()
```


Provides access to the axis title properties.

**Returns:**
[ChartAxisTitle](../../com.aspose.words/chartaxistitle/) - The corresponding [ChartAxisTitle](../../com.aspose.words/chartaxistitle/) value.
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
### getType() {#getType}
```
public int getType()
```


Returns type of the axis.

 **Examples:** 

Shows how to create an appropriate type of chart series for a graph type.

```

 public void chartSeriesCollection() throws Exception {
     Document doc = new Document();
     DocumentBuilder builder = new DocumentBuilder(doc);

     // There are several ways of populating a chart's series collection.
     // Different series schemas are intended for different chart types.
     // 1 -  Column chart with columns grouped and banded along the X-axis by category:
     Chart chart = appendChart(builder, ChartType.COLUMN, 500.0, 300.0);

     String[] categories = {"Category 1", "Category 2", "Category 3"};

     // Insert two series of decimal values containing a value for each respective category.
     // This column chart will have three groups, each with two columns.
     chart.getSeries().add("Series 1", categories, new double[]{76.6, 82.1, 91.6});
     chart.getSeries().add("Series 2", categories, new double[]{64.2, 79.5, 94.0});

     // Categories are distributed along the X-axis, and values are distributed along the Y-axis.
     Assert.assertEquals(ChartAxisType.CATEGORY, chart.getAxisX().getType());
     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisY().getType());

     // 2 -  Area chart with dates distributed along the X-axis:
     chart = appendChart(builder, ChartType.AREA, 500.0, 300.0);

     Date[] dates = {DocumentHelper.createDate(2014, 3, 31),
             DocumentHelper.createDate(2017, 1, 23),
             DocumentHelper.createDate(2017, 6, 18),
             DocumentHelper.createDate(2019, 11, 22),
             DocumentHelper.createDate(2020, 9, 7)
     };

     // Insert a series with a decimal value for each respective date.
     // The dates will be distributed along a linear X-axis,
     // and the values added to this series will create data points.
     chart.getSeries().add("Series 1", dates, new double[]{15.8, 21.5, 22.9, 28.7, 33.1});

     Assert.assertEquals(ChartAxisType.CATEGORY, chart.getAxisX().getType());
     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisY().getType());

     // 3 -  2D scatter plot:
     chart = appendChart(builder, ChartType.SCATTER, 500.0, 300.0);

     // Each series will need two decimal arrays of equal length.
     // The first array contains X-values, and the second contains corresponding Y-values
     // of data points on the chart's graph.
     chart.getSeries().add("Series 1",
             new double[]{3.1, 3.5, 6.3, 4.1, 2.2, 8.3, 1.2, 3.6},
             new double[]{3.1, 6.3, 4.6, 0.9, 8.5, 4.2, 2.3, 9.9});
     chart.getSeries().add("Series 2",
             new double[]{2.6, 7.3, 4.5, 6.6, 2.1, 9.3, 0.7, 3.3},
             new double[]{7.1, 6.6, 3.5, 7.8, 7.7, 9.5, 1.3, 4.6});

     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisX().getType());
     Assert.assertEquals(ChartAxisType.VALUE, chart.getAxisY().getType());

     // 4 -  Bubble chart:
     chart = appendChart(builder, ChartType.BUBBLE, 500.0, 300.0);

     // Each series will need three decimal arrays of equal length.
     // The first array contains X-values, the second contains corresponding Y-values,
     // and the third contains diameters for each of the graph's data points.
     chart.getSeries().add("Series 1",
             new double[]{1.1, 5.0, 9.8},
             new double[]{1.2, 4.9, 9.9},
             new double[]{2.0, 4.0, 8.0});

     doc.save(getArtifactsDir() + "Charts.ChartSeriesCollection.docx");
 }

 /// 
 /// Insert a chart using a document builder of a specified ChartType, width and height, and remove its demo data.
 /// 
 private static Chart appendChart(DocumentBuilder builder, int chartType, double width, double height) throws Exception {
     Shape chartShape = builder.insertChart(chartType, width, height);
     Chart chart = chartShape.getChart();
     chart.getSeries().clear();
     return chart;
 }
 
```

**Returns:**
int - Type of the axis. The returned value is one of [ChartAxisType](../../com.aspose.words/chartaxistype/) constants.
### hasMajorGridlines() {#hasMajorGridlines}
```
public boolean hasMajorGridlines()
```


Gets a flag indicating whether the axis has major gridlines.

 **Examples:** 

Shows how to insert chart with date/time values.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series containing date/time values for the X-axis, and respective decimal values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new Date[]
                 {
                         DocumentHelper.createDate(2017, 11, 6), DocumentHelper.createDate(2017, 11, 9), DocumentHelper.createDate(2017, 11, 15),
                         DocumentHelper.createDate(2017, 11, 21), DocumentHelper.createDate(2017, 11, 25), DocumentHelper.createDate(2017, 11, 29)
                 },
         new double[]{1.2, 0.3, 2.1, 2.9, 4.2, 5.3});

 // Set lower and upper bounds for the X-axis.
 ChartAxis xAxis = chart.getAxisX();
 xAxis.getScaling().setMinimum(new AxisBound(DocumentHelper.createDate(2017, 11, 5)));
 xAxis.getScaling().setMaximum(new AxisBound(DocumentHelper.createDate(2017, 12, 3)));

 // Set the major units of the X-axis to a week, and the minor units to a day.
 xAxis.setBaseTimeUnit(AxisTimeUnit.DAYS);
 xAxis.setMajorUnit(7.0d);
 xAxis.setMajorTickMark(AxisTickMark.CROSS);
 xAxis.setMinorUnit(1.0d);
 xAxis.setMinorTickMark(AxisTickMark.OUTSIDE);
 xAxis.hasMajorGridlines(true);
 xAxis.hasMinorGridlines(true);

 // Define Y-axis properties for decimal values.
 ChartAxis yAxis = chart.getAxisY();
 yAxis.setTickLabelPosition(AxisTickLabelPosition.HIGH);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(50.0d);
 yAxis.getDisplayUnit().setUnit(AxisBuiltInUnit.HUNDREDS);
 yAxis.getScaling().setMinimum(new AxisBound(100.0));
 yAxis.getScaling().setMaximum(new AxisBound(700.0));
 yAxis.hasMajorGridlines(true);
 yAxis.hasMinorGridlines(true);

 doc.save(getArtifactsDir() + "Charts.DateTimeValues.docx");
 
```

**Returns:**
boolean - A flag indicating whether the axis has major gridlines.
### hasMajorGridlines(boolean value) {#hasMajorGridlines-boolean}
```
public void hasMajorGridlines(boolean value)
```


Sets a flag indicating whether the axis has major gridlines.

 **Examples:** 

Shows how to insert chart with date/time values.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series containing date/time values for the X-axis, and respective decimal values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new Date[]
                 {
                         DocumentHelper.createDate(2017, 11, 6), DocumentHelper.createDate(2017, 11, 9), DocumentHelper.createDate(2017, 11, 15),
                         DocumentHelper.createDate(2017, 11, 21), DocumentHelper.createDate(2017, 11, 25), DocumentHelper.createDate(2017, 11, 29)
                 },
         new double[]{1.2, 0.3, 2.1, 2.9, 4.2, 5.3});

 // Set lower and upper bounds for the X-axis.
 ChartAxis xAxis = chart.getAxisX();
 xAxis.getScaling().setMinimum(new AxisBound(DocumentHelper.createDate(2017, 11, 5)));
 xAxis.getScaling().setMaximum(new AxisBound(DocumentHelper.createDate(2017, 12, 3)));

 // Set the major units of the X-axis to a week, and the minor units to a day.
 xAxis.setBaseTimeUnit(AxisTimeUnit.DAYS);
 xAxis.setMajorUnit(7.0d);
 xAxis.setMajorTickMark(AxisTickMark.CROSS);
 xAxis.setMinorUnit(1.0d);
 xAxis.setMinorTickMark(AxisTickMark.OUTSIDE);
 xAxis.hasMajorGridlines(true);
 xAxis.hasMinorGridlines(true);

 // Define Y-axis properties for decimal values.
 ChartAxis yAxis = chart.getAxisY();
 yAxis.setTickLabelPosition(AxisTickLabelPosition.HIGH);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(50.0d);
 yAxis.getDisplayUnit().setUnit(AxisBuiltInUnit.HUNDREDS);
 yAxis.getScaling().setMinimum(new AxisBound(100.0));
 yAxis.getScaling().setMaximum(new AxisBound(700.0));
 yAxis.hasMajorGridlines(true);
 yAxis.hasMinorGridlines(true);

 doc.save(getArtifactsDir() + "Charts.DateTimeValues.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether the axis has major gridlines. |

### hasMinorGridlines() {#hasMinorGridlines}
```
public boolean hasMinorGridlines()
```


Gets a flag indicating whether the axis has minor gridlines.

 **Examples:** 

Shows how to insert chart with date/time values.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series containing date/time values for the X-axis, and respective decimal values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new Date[]
                 {
                         DocumentHelper.createDate(2017, 11, 6), DocumentHelper.createDate(2017, 11, 9), DocumentHelper.createDate(2017, 11, 15),
                         DocumentHelper.createDate(2017, 11, 21), DocumentHelper.createDate(2017, 11, 25), DocumentHelper.createDate(2017, 11, 29)
                 },
         new double[]{1.2, 0.3, 2.1, 2.9, 4.2, 5.3});

 // Set lower and upper bounds for the X-axis.
 ChartAxis xAxis = chart.getAxisX();
 xAxis.getScaling().setMinimum(new AxisBound(DocumentHelper.createDate(2017, 11, 5)));
 xAxis.getScaling().setMaximum(new AxisBound(DocumentHelper.createDate(2017, 12, 3)));

 // Set the major units of the X-axis to a week, and the minor units to a day.
 xAxis.setBaseTimeUnit(AxisTimeUnit.DAYS);
 xAxis.setMajorUnit(7.0d);
 xAxis.setMajorTickMark(AxisTickMark.CROSS);
 xAxis.setMinorUnit(1.0d);
 xAxis.setMinorTickMark(AxisTickMark.OUTSIDE);
 xAxis.hasMajorGridlines(true);
 xAxis.hasMinorGridlines(true);

 // Define Y-axis properties for decimal values.
 ChartAxis yAxis = chart.getAxisY();
 yAxis.setTickLabelPosition(AxisTickLabelPosition.HIGH);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(50.0d);
 yAxis.getDisplayUnit().setUnit(AxisBuiltInUnit.HUNDREDS);
 yAxis.getScaling().setMinimum(new AxisBound(100.0));
 yAxis.getScaling().setMaximum(new AxisBound(700.0));
 yAxis.hasMajorGridlines(true);
 yAxis.hasMinorGridlines(true);

 doc.save(getArtifactsDir() + "Charts.DateTimeValues.docx");
 
```

**Returns:**
boolean - A flag indicating whether the axis has minor gridlines.
### hasMinorGridlines(boolean value) {#hasMinorGridlines-boolean}
```
public void hasMinorGridlines(boolean value)
```


Sets a flag indicating whether the axis has minor gridlines.

 **Examples:** 

Shows how to insert chart with date/time values.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series containing date/time values for the X-axis, and respective decimal values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new Date[]
                 {
                         DocumentHelper.createDate(2017, 11, 6), DocumentHelper.createDate(2017, 11, 9), DocumentHelper.createDate(2017, 11, 15),
                         DocumentHelper.createDate(2017, 11, 21), DocumentHelper.createDate(2017, 11, 25), DocumentHelper.createDate(2017, 11, 29)
                 },
         new double[]{1.2, 0.3, 2.1, 2.9, 4.2, 5.3});

 // Set lower and upper bounds for the X-axis.
 ChartAxis xAxis = chart.getAxisX();
 xAxis.getScaling().setMinimum(new AxisBound(DocumentHelper.createDate(2017, 11, 5)));
 xAxis.getScaling().setMaximum(new AxisBound(DocumentHelper.createDate(2017, 12, 3)));

 // Set the major units of the X-axis to a week, and the minor units to a day.
 xAxis.setBaseTimeUnit(AxisTimeUnit.DAYS);
 xAxis.setMajorUnit(7.0d);
 xAxis.setMajorTickMark(AxisTickMark.CROSS);
 xAxis.setMinorUnit(1.0d);
 xAxis.setMinorTickMark(AxisTickMark.OUTSIDE);
 xAxis.hasMajorGridlines(true);
 xAxis.hasMinorGridlines(true);

 // Define Y-axis properties for decimal values.
 ChartAxis yAxis = chart.getAxisY();
 yAxis.setTickLabelPosition(AxisTickLabelPosition.HIGH);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(50.0d);
 yAxis.getDisplayUnit().setUnit(AxisBuiltInUnit.HUNDREDS);
 yAxis.getScaling().setMinimum(new AxisBound(100.0));
 yAxis.getScaling().setMaximum(new AxisBound(700.0));
 yAxis.hasMajorGridlines(true);
 yAxis.hasMinorGridlines(true);

 doc.save(getArtifactsDir() + "Charts.DateTimeValues.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether the axis has minor gridlines. |

### isInherited() {#isInherited}
```
public boolean isInherited()
```




**Returns:**
boolean
### isVisible() {#isVisible}
```
public boolean isVisible()
```




**Returns:**
boolean
### setAxisBetweenCategories(boolean value) {#setAxisBetweenCategories-boolean}
```
public void setAxisBetweenCategories(boolean value)
```


Sets a flag indicating whether the value axis crosses the category axis between categories.

 **Remarks:** 

The property has effect only for value axes. It is not supported by MS Office 2016 new charts.

 **Examples:** 

Shows how to get a graph axis to cross at a custom location.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 450.0, 250.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(3, chart.getSeries().getCount());
 Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
 Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
 Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

 // For column charts, the Y-axis crosses at zero by default,
 // which means that columns for all values below zero point down to represent negative values.
 // We can set a different value for the Y-axis crossing. In this case, we will set it to 3.
 ChartAxis axis = chart.getAxisX();
 axis.setCrosses(AxisCrosses.CUSTOM);
 axis.setCrossesAt(3.0);
 axis.setAxisBetweenCategories(true);

 doc.save(getArtifactsDir() + "Charts.AxisCross.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether the value axis crosses the category axis between categories. |

### setBaseTimeUnit(int value) {#setBaseTimeUnit-int}
```
public void setBaseTimeUnit(int value)
```


Sets the smallest time unit that is represented on the time category axis.

 **Remarks:** 

The property has effect only for time category axes.

 **Examples:** 

Shows how to insert chart with date/time values.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series containing date/time values for the X-axis, and respective decimal values for the Y-axis.
 chart.getSeries().add("Aspose Test Series",
         new Date[]
                 {
                         DocumentHelper.createDate(2017, 11, 6), DocumentHelper.createDate(2017, 11, 9), DocumentHelper.createDate(2017, 11, 15),
                         DocumentHelper.createDate(2017, 11, 21), DocumentHelper.createDate(2017, 11, 25), DocumentHelper.createDate(2017, 11, 29)
                 },
         new double[]{1.2, 0.3, 2.1, 2.9, 4.2, 5.3});

 // Set lower and upper bounds for the X-axis.
 ChartAxis xAxis = chart.getAxisX();
 xAxis.getScaling().setMinimum(new AxisBound(DocumentHelper.createDate(2017, 11, 5)));
 xAxis.getScaling().setMaximum(new AxisBound(DocumentHelper.createDate(2017, 12, 3)));

 // Set the major units of the X-axis to a week, and the minor units to a day.
 xAxis.setBaseTimeUnit(AxisTimeUnit.DAYS);
 xAxis.setMajorUnit(7.0d);
 xAxis.setMajorTickMark(AxisTickMark.CROSS);
 xAxis.setMinorUnit(1.0d);
 xAxis.setMinorTickMark(AxisTickMark.OUTSIDE);
 xAxis.hasMajorGridlines(true);
 xAxis.hasMinorGridlines(true);

 // Define Y-axis properties for decimal values.
 ChartAxis yAxis = chart.getAxisY();
 yAxis.setTickLabelPosition(AxisTickLabelPosition.HIGH);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(50.0d);
 yAxis.getDisplayUnit().setUnit(AxisBuiltInUnit.HUNDREDS);
 yAxis.getScaling().setMinimum(new AxisBound(100.0));
 yAxis.getScaling().setMaximum(new AxisBound(700.0));
 yAxis.hasMajorGridlines(true);
 yAxis.hasMinorGridlines(true);

 doc.save(getArtifactsDir() + "Charts.DateTimeValues.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The smallest time unit that is represented on the time category axis. The value must be one of [AxisTimeUnit](../../com.aspose.words/axistimeunit/) constants. |

### setCategoryType(int value) {#setCategoryType-int}
```
public void setCategoryType(int value)
```


Sets type of the category axis.

 **Remarks:** 

Only text categories ( [AxisCategoryType.CATEGORY](../../com.aspose.words/axiscategorytype/\#CATEGORY)) are allowed in MS Office 2016 new charts.

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
 xAxis.setTickLabelOffset(50);
 xAxis.setTickLabelPosition(AxisTickLabelPosition.LOW);
 xAxis.setTickLabelSpacingIsAuto(false);
 xAxis.setTickMarkSpacing(1);

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.setTickLabelPosition(AxisTickLabelPosition.NEXT_TO_AXIS);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | Type of the category axis. The value must be one of [AxisCategoryType](../../com.aspose.words/axiscategorytype/) constants. |

### setCrosses(int value) {#setCrosses-int}
```
public void setCrosses(int value)
```


Specifies how this axis crosses the perpendicular axis.

 **Remarks:** 

Default value is [AxisCrosses.AUTOMATIC](../../com.aspose.words/axiscrosses/\#AUTOMATIC).

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
 xAxis.setTickLabelOffset(50);
 xAxis.setTickLabelPosition(AxisTickLabelPosition.LOW);
 xAxis.setTickLabelSpacingIsAuto(false);
 xAxis.setTickMarkSpacing(1);

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.setTickLabelPosition(AxisTickLabelPosition.NEXT_TO_AXIS);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [AxisCrosses](../../com.aspose.words/axiscrosses/) constants. |

### setCrossesAt(double value) {#setCrossesAt-double}
```
public void setCrossesAt(double value)
```


Specifies where on the perpendicular axis the axis crosses.

 **Remarks:** 

The property has effect only if [getCrosses()](../../com.aspose.words/chartaxis/\#getCrosses) / [setCrosses(int)](../../com.aspose.words/chartaxis/\#setCrosses-int) are set to [AxisCrosses.CUSTOM](../../com.aspose.words/axiscrosses/\#CUSTOM). It is not supported by MS Office 2016 new charts.

The units are determined by the type of axis. When the axis is a value axis, the value of the property is a decimal number on the value axis. When the axis is a time category axis, the value is defined as an integer number of days relative to the base date (30/12/1899). For a text category axis, the value is an integer category number, starting with 1 as the first category.

 **Examples:** 

Shows how to get a graph axis to cross at a custom location.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.COLUMN, 450.0, 250.0);
 Chart chart = shape.getChart();

 Assert.assertEquals(3, chart.getSeries().getCount());
 Assert.assertEquals("Series 1", chart.getSeries().get(0).getName());
 Assert.assertEquals("Series 2", chart.getSeries().get(1).getName());
 Assert.assertEquals("Series 3", chart.getSeries().get(2).getName());

 // For column charts, the Y-axis crosses at zero by default,
 // which means that columns for all values below zero point down to represent negative values.
 // We can set a different value for the Y-axis crossing. In this case, we will set it to 3.
 ChartAxis axis = chart.getAxisX();
 axis.setCrosses(AxisCrosses.CUSTOM);
 axis.setCrossesAt(3.0);
 axis.setAxisBetweenCategories(true);

 doc.save(getArtifactsDir() + "Charts.AxisCross.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The corresponding  double  value. |

### setHidden(boolean value) {#setHidden-boolean}
```
public void setHidden(boolean value)
```


Sets a flag indicating whether this axis is hidden or not.

 **Remarks:** 

Default value is  false .

 **Examples:** 

Shows how to hide chart axes.

```

 Document doc = new Document();
 DocumentBuilder builder = new DocumentBuilder(doc);

 Shape shape = builder.insertChart(ChartType.LINE, 500.0, 300.0);
 Chart chart = shape.getChart();

 // Clear the chart's demo data series to start with a clean chart.
 chart.getSeries().clear();

 // Add a custom series with categories for the X-axis, and respective decimal values for the Y-axis.
 chart.getSeries().add("AW Series 1",
         new String[]{"Item 1", "Item 2", "Item 3", "Item 4", "Item 5"},
         new double[]{1.2, 0.3, 2.1, 2.9, 4.2});

 // Hide the chart axes to simplify the appearance of the chart.
 chart.getAxisX().setHidden(true);
 chart.getAxisY().setHidden(true);

 doc.save(getArtifactsDir() + "Charts.HideChartAxis.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether this axis is hidden or not. |

### setMajorTickMark(int value) {#setMajorTickMark-int}
```
public void setMajorTickMark(int value)
```


Sets the major tick marks.

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
 xAxis.setTickLabelOffset(50);
 xAxis.setTickLabelPosition(AxisTickLabelPosition.LOW);
 xAxis.setTickLabelSpacingIsAuto(false);
 xAxis.setTickMarkSpacing(1);

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.setTickLabelPosition(AxisTickLabelPosition.NEXT_TO_AXIS);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The major tick marks. The value must be one of [AxisTickMark](../../com.aspose.words/axistickmark/) constants. |

### setMajorUnit(double value) {#setMajorUnit-double}
```
public void setMajorUnit(double value)
```


Sets the distance between major tick marks.

 **Remarks:** 

Valid range of a value is greater than zero. The property has effect for time category and value axes.

Setting this property sets the [getMajorUnitIsAuto()](../../com.aspose.words/chartaxis/\#getMajorUnitIsAuto) / [setMajorUnitIsAuto(boolean)](../../com.aspose.words/chartaxis/\#setMajorUnitIsAuto-boolean) property to  false .

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
 xAxis.setTickLabelOffset(50);
 xAxis.setTickLabelPosition(AxisTickLabelPosition.LOW);
 xAxis.setTickLabelSpacingIsAuto(false);
 xAxis.setTickMarkSpacing(1);

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.setTickLabelPosition(AxisTickLabelPosition.NEXT_TO_AXIS);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The distance between major tick marks. |

### setMajorUnitIsAuto(boolean value) {#setMajorUnitIsAuto-boolean}
```
public void setMajorUnitIsAuto(boolean value)
```


Sets a flag indicating whether default distance between major tick marks shall be used.

 **Remarks:** 

The property has effect for time category and value axes.

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
| value | boolean | A flag indicating whether default distance between major tick marks shall be used. |

### setMajorUnitScale(int value) {#setMajorUnitScale-int}
```
public void setMajorUnitScale(int value)
```


Sets the scale value for major tick marks on the time category axis.

 **Remarks:** 

The property has effect only for time category axes.

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
| value | int | The scale value for major tick marks on the time category axis. The value must be one of [AxisTimeUnit](../../com.aspose.words/axistimeunit/) constants. |

### setMinorTickMark(int value) {#setMinorTickMark-int}
```
public void setMinorTickMark(int value)
```


Sets the minor tick marks for the axis.

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
 xAxis.setTickLabelOffset(50);
 xAxis.setTickLabelPosition(AxisTickLabelPosition.LOW);
 xAxis.setTickLabelSpacingIsAuto(false);
 xAxis.setTickMarkSpacing(1);

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.setTickLabelPosition(AxisTickLabelPosition.NEXT_TO_AXIS);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The minor tick marks for the axis. The value must be one of [AxisTickMark](../../com.aspose.words/axistickmark/) constants. |

### setMinorUnit(double value) {#setMinorUnit-double}
```
public void setMinorUnit(double value)
```


Sets the distance between minor tick marks.

 **Remarks:** 

Valid range of a value is greater than zero. The property has effect for time category and value axes.

Setting this property sets the [getMinorUnitIsAuto()](../../com.aspose.words/chartaxis/\#getMinorUnitIsAuto) / [setMinorUnitIsAuto(boolean)](../../com.aspose.words/chartaxis/\#setMinorUnitIsAuto-boolean) property to  false .

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
 xAxis.setTickLabelOffset(50);
 xAxis.setTickLabelPosition(AxisTickLabelPosition.LOW);
 xAxis.setTickLabelSpacingIsAuto(false);
 xAxis.setTickMarkSpacing(1);

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.setTickLabelPosition(AxisTickLabelPosition.NEXT_TO_AXIS);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The distance between minor tick marks. |

### setMinorUnitIsAuto(boolean value) {#setMinorUnitIsAuto-boolean}
```
public void setMinorUnitIsAuto(boolean value)
```


Sets a flag indicating whether default distance between minor tick marks shall be used.

 **Remarks:** 

The property has effect for time category and value axes.

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
| value | boolean | A flag indicating whether default distance between minor tick marks shall be used. |

### setMinorUnitScale(int value) {#setMinorUnitScale-int}
```
public void setMinorUnitScale(int value)
```


Sets the scale value for minor tick marks on the time category axis.

 **Remarks:** 

The property has effect only for time category axes.

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
| value | int | The scale value for minor tick marks on the time category axis. The value must be one of [AxisTimeUnit](../../com.aspose.words/axistimeunit/) constants. |

### setReverseOrder(boolean value) {#setReverseOrder-boolean}
```
public void setReverseOrder(boolean value)
```


Sets a flag indicating whether values of axis should be displayed in reverse order, i.e. from max to min.

 **Remarks:** 

The property is not supported by MS Office 2016 new charts. Default value is  false .

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
 xAxis.setTickLabelOffset(50);
 xAxis.setTickLabelPosition(AxisTickLabelPosition.LOW);
 xAxis.setTickLabelSpacingIsAuto(false);
 xAxis.setTickMarkSpacing(1);

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.setTickLabelPosition(AxisTickLabelPosition.NEXT_TO_AXIS);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether values of axis should be displayed in reverse order, i.e. |

### setTickLabelAlignment(int value) {#setTickLabelAlignment-int}
```
public void setTickLabelAlignment(int value)
```


Sets text alignment of axis tick labels.

 **Remarks:** 

This property has effect only for multi-line labels.

Default value is [ParagraphAlignment.CENTER](../../com.aspose.words/paragraphalignment/\#CENTER).

.

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
| value | int | Text alignment of axis tick labels. The value must be one of [ParagraphAlignment](../../com.aspose.words/paragraphalignment/) constants. |

### setTickLabelOffset(int value) {#setTickLabelOffset-int}
```
public void setTickLabelOffset(int value)
```


Sets the distance of labels from the axis.

 **Remarks:** 

The property represents a percentage of the default label offset.

Valid range is from 0 to 1000 percent inclusive. Default value is 100%.

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
 xAxis.setTickLabelOffset(50);
 xAxis.setTickLabelPosition(AxisTickLabelPosition.LOW);
 xAxis.setTickLabelSpacingIsAuto(false);
 xAxis.setTickMarkSpacing(1);

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.setTickLabelPosition(AxisTickLabelPosition.NEXT_TO_AXIS);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The distance of labels from the axis. |

### setTickLabelPosition(int value) {#setTickLabelPosition-int}
```
public void setTickLabelPosition(int value)
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
 xAxis.setTickLabelOffset(50);
 xAxis.setTickLabelPosition(AxisTickLabelPosition.LOW);
 xAxis.setTickLabelSpacingIsAuto(false);
 xAxis.setTickMarkSpacing(1);

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.setTickLabelPosition(AxisTickLabelPosition.NEXT_TO_AXIS);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The position of the tick labels on the axis. The value must be one of [AxisTickLabelPosition](../../com.aspose.words/axisticklabelposition/) constants. |

### setTickLabelSpacing(int value) {#setTickLabelSpacing-int}
```
public void setTickLabelSpacing(int value)
```


Sets the interval, at which tick labels are drawn.

 **Remarks:** 

The property has effect for text category and series axes. It is not supported by MS Office 2016 new charts. Valid range of a value is greater than or equal to 1.

Setting this property sets the [getTickLabelSpacingIsAuto()](../../com.aspose.words/chartaxis/\#getTickLabelSpacingIsAuto) / [setTickLabelSpacingIsAuto(boolean)](../../com.aspose.words/chartaxis/\#setTickLabelSpacingIsAuto-boolean) property to  false .

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
| value | int | The interval, at which tick labels are drawn. |

### setTickLabelSpacingIsAuto(boolean value) {#setTickLabelSpacingIsAuto-boolean}
```
public void setTickLabelSpacingIsAuto(boolean value)
```


Sets a flag indicating whether automatic interval of drawing tick labels shall be used.

 **Remarks:** 

Default value is  true .

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
 xAxis.setTickLabelOffset(50);
 xAxis.setTickLabelPosition(AxisTickLabelPosition.LOW);
 xAxis.setTickLabelSpacingIsAuto(false);
 xAxis.setTickMarkSpacing(1);

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.setTickLabelPosition(AxisTickLabelPosition.NEXT_TO_AXIS);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether automatic interval of drawing tick labels shall be used. |

### setTickMarkSpacing(int value) {#setTickMarkSpacing-int}
```
public void setTickMarkSpacing(int value)
```


Sets the interval, at which tick marks are drawn.

 **Remarks:** 

The property has effect for text category and series axes. It is not supported by MS Office 2016 new charts.

Valid range of a value is greater than or equal to 1.

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
 xAxis.setTickLabelOffset(50);
 xAxis.setTickLabelPosition(AxisTickLabelPosition.LOW);
 xAxis.setTickLabelSpacingIsAuto(false);
 xAxis.setTickMarkSpacing(1);

 ChartAxis yAxis = chart.getAxisY();
 yAxis.setCategoryType(AxisCategoryType.AUTOMATIC);
 yAxis.setCrosses(AxisCrosses.MAXIMUM);
 yAxis.setReverseOrder(true);
 yAxis.setMajorTickMark(AxisTickMark.INSIDE);
 yAxis.setMinorTickMark(AxisTickMark.CROSS);
 yAxis.setMajorUnit(100.0d);
 yAxis.setMinorUnit(20.0d);
 yAxis.setTickLabelPosition(AxisTickLabelPosition.NEXT_TO_AXIS);

 // Column charts do not have a Z-axis.
 Assert.assertNull(chart.getAxisZ());

 doc.save(getArtifactsDir() + "Charts.AxisProperties.docx");
 
```

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The interval, at which tick marks are drawn. |

### setTitleDeleted(boolean value) {#setTitleDeleted-boolean}
```
public void setTitleDeleted(boolean value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean |  |

