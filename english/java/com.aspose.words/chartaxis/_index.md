---
title: ChartAxis
second_title: Aspose.Words for Java API Reference
description: Represents the axis options of the chart.
type: docs
weight: 56
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

To learn more, visit the **Working with Charts** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getType()](#getType--) | Returns type of the axis. |
| [getCategoryType()](#getCategoryType--) | Gets type of the category axis. |
| [setCategoryType(int value)](#setCategoryType-int-) | Sets type of the category axis. |
| [getCrosses()](#getCrosses--) | Specifies how this axis crosses the perpendicular axis. |
| [setCrosses(int value)](#setCrosses-int-) | Specifies how this axis crosses the perpendicular axis. |
| [getCrossesAt()](#getCrossesAt--) | Specifies where on the perpendicular axis the axis crosses. |
| [setCrossesAt(double value)](#setCrossesAt-double-) | Specifies where on the perpendicular axis the axis crosses. |
| [getReverseOrder()](#getReverseOrder--) | Gets a flag indicating whether values of axis should be displayed in reverse order, i.e. |
| [setReverseOrder(boolean value)](#setReverseOrder-boolean-) | Sets a flag indicating whether values of axis should be displayed in reverse order, i.e. |
| [getMajorTickMark()](#getMajorTickMark--) | Gets the major tick marks. |
| [setMajorTickMark(int value)](#setMajorTickMark-int-) | Sets the major tick marks. |
| [getMinorTickMark()](#getMinorTickMark--) | Gets the minor tick marks for the axis. |
| [setMinorTickMark(int value)](#setMinorTickMark-int-) | Sets the minor tick marks for the axis. |
| [getTickLabelPosition()](#getTickLabelPosition--) | Gets the position of the tick labels on the axis. |
| [setTickLabelPosition(int value)](#setTickLabelPosition-int-) | Sets the position of the tick labels on the axis. |
| [getMajorUnit()](#getMajorUnit--) | Gets the distance between major tick marks. |
| [setMajorUnit(double value)](#setMajorUnit-double-) | Sets the distance between major tick marks. |
| [getMajorUnitIsAuto()](#getMajorUnitIsAuto--) | Gets a flag indicating whether default distance between major tick marks shall be used. |
| [setMajorUnitIsAuto(boolean value)](#setMajorUnitIsAuto-boolean-) | Sets a flag indicating whether default distance between major tick marks shall be used. |
| [getMajorUnitScale()](#getMajorUnitScale--) | Gets the scale value for major tick marks on the time category axis. |
| [setMajorUnitScale(int value)](#setMajorUnitScale-int-) | Sets the scale value for major tick marks on the time category axis. |
| [getMinorUnit()](#getMinorUnit--) | Gets the distance between minor tick marks. |
| [setMinorUnit(double value)](#setMinorUnit-double-) | Sets the distance between minor tick marks. |
| [getMinorUnitIsAuto()](#getMinorUnitIsAuto--) | Gets a flag indicating whether default distance between minor tick marks shall be used. |
| [setMinorUnitIsAuto(boolean value)](#setMinorUnitIsAuto-boolean-) | Sets a flag indicating whether default distance between minor tick marks shall be used. |
| [getMinorUnitScale()](#getMinorUnitScale--) | Gets the scale value for minor tick marks on the time category axis. |
| [setMinorUnitScale(int value)](#setMinorUnitScale-int-) | Sets the scale value for minor tick marks on the time category axis. |
| [getBaseTimeUnit()](#getBaseTimeUnit--) | Gets the smallest time unit that is represented on the time category axis. |
| [setBaseTimeUnit(int value)](#setBaseTimeUnit-int-) | Sets the smallest time unit that is represented on the time category axis. |
| [getNumberFormat()](#getNumberFormat--) | Returns a [ChartNumberFormat](../../com.aspose.words/chartnumberformat) object that allows defining number formats for the axis. |
| [getTickLabelOffset()](#getTickLabelOffset--) | Gets the distance of labels from the axis. |
| [setTickLabelOffset(int value)](#setTickLabelOffset-int-) | Sets the distance of labels from the axis. |
| [getDisplayUnit()](#getDisplayUnit--) | Specifies the scaling value of the display units for the value axis. |
| [getAxisBetweenCategories()](#getAxisBetweenCategories--) | Gets a flag indicating whether the value axis crosses the category axis between categories. |
| [setAxisBetweenCategories(boolean value)](#setAxisBetweenCategories-boolean-) | Sets a flag indicating whether the value axis crosses the category axis between categories. |
| [getScaling()](#getScaling--) | Provides access to the scaling options of the axis. |
| [getTickLabelSpacing()](#getTickLabelSpacing--) | Gets the interval, at which tick labels are drawn. |
| [setTickLabelSpacing(int value)](#setTickLabelSpacing-int-) | Sets the interval, at which tick labels are drawn. |
| [getTickLabelSpacingIsAuto()](#getTickLabelSpacingIsAuto--) | Gets a flag indicating whether automatic interval of drawing tick labels shall be used. |
| [setTickLabelSpacingIsAuto(boolean value)](#setTickLabelSpacingIsAuto-boolean-) | Sets a flag indicating whether automatic interval of drawing tick labels shall be used. |
| [getTickLabelAlignment()](#getTickLabelAlignment--) | Gets text alignment of axis tick labels. |
| [setTickLabelAlignment(int value)](#setTickLabelAlignment-int-) | Sets text alignment of axis tick labels. |
| [getTickMarkSpacing()](#getTickMarkSpacing--) | Gets the interval, at which tick marks are drawn. |
| [setTickMarkSpacing(int value)](#setTickMarkSpacing-int-) | Sets the interval, at which tick marks are drawn. |
| [getHidden()](#getHidden--) | Gets a flag indicating whether this axis is hidden or not. |
| [setHidden(boolean value)](#setHidden-boolean-) | Sets a flag indicating whether this axis is hidden or not. |
| [getTitle()](#getTitle--) |  |
| [setTitle(ChartTitle value)](#setTitle-com.aspose.words.ChartTitle-) |  |
| [getTitlePosition()](#getTitlePosition--) |  |
| [getDocument()](#getDocument--) | Returns the Document the title holder belongs. |
| [getTitleDeleted()](#getTitleDeleted--) |  |
| [setTitleDeleted(boolean value)](#setTitleDeleted-boolean-) |  |
| [isVisible()](#isVisible--) |  |
| [isInherited()](#isInherited--) |  |
### getType() {#getType--}
```
public int getType()
```


Returns type of the axis.

**Returns:**
int - Type of the axis. The returned value is one of [ChartAxisType](../../com.aspose.words/chartaxistype) constants.
### getCategoryType() {#getCategoryType--}
```
public int getCategoryType()
```


Gets type of the category axis. Only text categories ( [AxisCategoryType.CATEGORY](../../com.aspose.words/axiscategorytype\#CATEGORY)) are allowed in MS Office 2016 new charts.

**Returns:**
int - Type of the category axis. The returned value is one of [AxisCategoryType](../../com.aspose.words/axiscategorytype) constants.
### setCategoryType(int value) {#setCategoryType-int-}
```
public void setCategoryType(int value)
```


Sets type of the category axis. Only text categories ( [AxisCategoryType.CATEGORY](../../com.aspose.words/axiscategorytype\#CATEGORY)) are allowed in MS Office 2016 new charts.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | Type of the category axis. The value must be one of [AxisCategoryType](../../com.aspose.words/axiscategorytype) constants. |

### getCrosses() {#getCrosses--}
```
public int getCrosses()
```


Specifies how this axis crosses the perpendicular axis.

Default value is [AxisCrosses.AUTOMATIC](../../com.aspose.words/axiscrosses\#AUTOMATIC).

The property is not supported by MS Office 2016 new charts.

**Returns:**
int - The corresponding  int  value. The returned value is one of [AxisCrosses](../../com.aspose.words/axiscrosses) constants.
### setCrosses(int value) {#setCrosses-int-}
```
public void setCrosses(int value)
```


Specifies how this axis crosses the perpendicular axis.

Default value is [AxisCrosses.AUTOMATIC](../../com.aspose.words/axiscrosses\#AUTOMATIC).

The property is not supported by MS Office 2016 new charts.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. The value must be one of [AxisCrosses](../../com.aspose.words/axiscrosses) constants. |

### getCrossesAt() {#getCrossesAt--}
```
public double getCrossesAt()
```


Specifies where on the perpendicular axis the axis crosses.

The property has effect only if [getCrosses()](../../com.aspose.words/chartaxis\#getCrosses--) / [setCrosses(int)](../../com.aspose.words/chartaxis\#setCrosses-int-) are set to [AxisCrosses.CUSTOM](../../com.aspose.words/axiscrosses\#CUSTOM). It is not supported by MS Office 2016 new charts.

The units are determined by the type of axis. When the axis is a value axis, the value of the property is a decimal number on the value axis. When the axis is a time category axis, the value is defined as an integer number of days relative to the base date (30/12/1899). For a text category axis, the value is an integer category number, starting with 1 as the first category.

**Returns:**
double - The corresponding  double  value.
### setCrossesAt(double value) {#setCrossesAt-double-}
```
public void setCrossesAt(double value)
```


Specifies where on the perpendicular axis the axis crosses.

The property has effect only if [getCrosses()](../../com.aspose.words/chartaxis\#getCrosses--) / [setCrosses(int)](../../com.aspose.words/chartaxis\#setCrosses-int-) are set to [AxisCrosses.CUSTOM](../../com.aspose.words/axiscrosses\#CUSTOM). It is not supported by MS Office 2016 new charts.

The units are determined by the type of axis. When the axis is a value axis, the value of the property is a decimal number on the value axis. When the axis is a time category axis, the value is defined as an integer number of days relative to the base date (30/12/1899). For a text category axis, the value is an integer category number, starting with 1 as the first category.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The corresponding  double  value. |

### getReverseOrder() {#getReverseOrder--}
```
public boolean getReverseOrder()
```


Gets a flag indicating whether values of axis should be displayed in reverse order, i.e. from max to min. The property is not supported by MS Office 2016 new charts. Default value is **false**.

**Returns:**
boolean - A flag indicating whether values of axis should be displayed in reverse order, i.e.
### setReverseOrder(boolean value) {#setReverseOrder-boolean-}
```
public void setReverseOrder(boolean value)
```


Sets a flag indicating whether values of axis should be displayed in reverse order, i.e. from max to min. The property is not supported by MS Office 2016 new charts. Default value is **false**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether values of axis should be displayed in reverse order, i.e. |

### getMajorTickMark() {#getMajorTickMark--}
```
public int getMajorTickMark()
```


Gets the major tick marks.

**Returns:**
int - The major tick marks. The returned value is one of [AxisTickMark](../../com.aspose.words/axistickmark) constants.
### setMajorTickMark(int value) {#setMajorTickMark-int-}
```
public void setMajorTickMark(int value)
```


Sets the major tick marks.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The major tick marks. The value must be one of [AxisTickMark](../../com.aspose.words/axistickmark) constants. |

### getMinorTickMark() {#getMinorTickMark--}
```
public int getMinorTickMark()
```


Gets the minor tick marks for the axis.

**Returns:**
int - The minor tick marks for the axis. The returned value is one of [AxisTickMark](../../com.aspose.words/axistickmark) constants.
### setMinorTickMark(int value) {#setMinorTickMark-int-}
```
public void setMinorTickMark(int value)
```


Sets the minor tick marks for the axis.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The minor tick marks for the axis. The value must be one of [AxisTickMark](../../com.aspose.words/axistickmark) constants. |

### getTickLabelPosition() {#getTickLabelPosition--}
```
public int getTickLabelPosition()
```


Gets the position of the tick labels on the axis. The property is not supported by MS Office 2016 new charts.

**Returns:**
int - The position of the tick labels on the axis. The returned value is one of [AxisTickLabelPosition](../../com.aspose.words/axisticklabelposition) constants.
### setTickLabelPosition(int value) {#setTickLabelPosition-int-}
```
public void setTickLabelPosition(int value)
```


Sets the position of the tick labels on the axis. The property is not supported by MS Office 2016 new charts.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The position of the tick labels on the axis. The value must be one of [AxisTickLabelPosition](../../com.aspose.words/axisticklabelposition) constants. |

### getMajorUnit() {#getMajorUnit--}
```
public double getMajorUnit()
```


Gets the distance between major tick marks.

Valid range of a value is greater than zero. The property has effect for time category and value axes.

Setting this property sets the [getMajorUnitIsAuto()](../../com.aspose.words/chartaxis\#getMajorUnitIsAuto--) / [setMajorUnitIsAuto(boolean)](../../com.aspose.words/chartaxis\#setMajorUnitIsAuto-boolean-) property to **false**.

**Returns:**
double - The distance between major tick marks.
### setMajorUnit(double value) {#setMajorUnit-double-}
```
public void setMajorUnit(double value)
```


Sets the distance between major tick marks.

Valid range of a value is greater than zero. The property has effect for time category and value axes.

Setting this property sets the [getMajorUnitIsAuto()](../../com.aspose.words/chartaxis\#getMajorUnitIsAuto--) / [setMajorUnitIsAuto(boolean)](../../com.aspose.words/chartaxis\#setMajorUnitIsAuto-boolean-) property to **false**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The distance between major tick marks. |

### getMajorUnitIsAuto() {#getMajorUnitIsAuto--}
```
public boolean getMajorUnitIsAuto()
```


Gets a flag indicating whether default distance between major tick marks shall be used. The property has effect for time category and value axes.

**Returns:**
boolean - A flag indicating whether default distance between major tick marks shall be used.
### setMajorUnitIsAuto(boolean value) {#setMajorUnitIsAuto-boolean-}
```
public void setMajorUnitIsAuto(boolean value)
```


Sets a flag indicating whether default distance between major tick marks shall be used. The property has effect for time category and value axes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether default distance between major tick marks shall be used. |

### getMajorUnitScale() {#getMajorUnitScale--}
```
public int getMajorUnitScale()
```


Gets the scale value for major tick marks on the time category axis. The property has effect only for time category axes.

**Returns:**
int - The scale value for major tick marks on the time category axis. The returned value is one of [AxisTimeUnit](../../com.aspose.words/axistimeunit) constants.
### setMajorUnitScale(int value) {#setMajorUnitScale-int-}
```
public void setMajorUnitScale(int value)
```


Sets the scale value for major tick marks on the time category axis. The property has effect only for time category axes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The scale value for major tick marks on the time category axis. The value must be one of [AxisTimeUnit](../../com.aspose.words/axistimeunit) constants. |

### getMinorUnit() {#getMinorUnit--}
```
public double getMinorUnit()
```


Gets the distance between minor tick marks.

Valid range of a value is greater than zero. The property has effect for time category and value axes.

Setting this property sets the [getMinorUnitIsAuto()](../../com.aspose.words/chartaxis\#getMinorUnitIsAuto--) / [setMinorUnitIsAuto(boolean)](../../com.aspose.words/chartaxis\#setMinorUnitIsAuto-boolean-) property to **false**.

**Returns:**
double - The distance between minor tick marks.
### setMinorUnit(double value) {#setMinorUnit-double-}
```
public void setMinorUnit(double value)
```


Sets the distance between minor tick marks.

Valid range of a value is greater than zero. The property has effect for time category and value axes.

Setting this property sets the [getMinorUnitIsAuto()](../../com.aspose.words/chartaxis\#getMinorUnitIsAuto--) / [setMinorUnitIsAuto(boolean)](../../com.aspose.words/chartaxis\#setMinorUnitIsAuto-boolean-) property to **false**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The distance between minor tick marks. |

### getMinorUnitIsAuto() {#getMinorUnitIsAuto--}
```
public boolean getMinorUnitIsAuto()
```


Gets a flag indicating whether default distance between minor tick marks shall be used. The property has effect for time category and value axes.

**Returns:**
boolean - A flag indicating whether default distance between minor tick marks shall be used.
### setMinorUnitIsAuto(boolean value) {#setMinorUnitIsAuto-boolean-}
```
public void setMinorUnitIsAuto(boolean value)
```


Sets a flag indicating whether default distance between minor tick marks shall be used. The property has effect for time category and value axes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether default distance between minor tick marks shall be used. |

### getMinorUnitScale() {#getMinorUnitScale--}
```
public int getMinorUnitScale()
```


Gets the scale value for minor tick marks on the time category axis. The property has effect only for time category axes.

**Returns:**
int - The scale value for minor tick marks on the time category axis. The returned value is one of [AxisTimeUnit](../../com.aspose.words/axistimeunit) constants.
### setMinorUnitScale(int value) {#setMinorUnitScale-int-}
```
public void setMinorUnitScale(int value)
```


Sets the scale value for minor tick marks on the time category axis. The property has effect only for time category axes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The scale value for minor tick marks on the time category axis. The value must be one of [AxisTimeUnit](../../com.aspose.words/axistimeunit) constants. |

### getBaseTimeUnit() {#getBaseTimeUnit--}
```
public int getBaseTimeUnit()
```


Gets the smallest time unit that is represented on the time category axis. The property has effect only for time category axes.

**Returns:**
int - The smallest time unit that is represented on the time category axis. The returned value is one of [AxisTimeUnit](../../com.aspose.words/axistimeunit) constants.
### setBaseTimeUnit(int value) {#setBaseTimeUnit-int-}
```
public void setBaseTimeUnit(int value)
```


Sets the smallest time unit that is represented on the time category axis. The property has effect only for time category axes.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The smallest time unit that is represented on the time category axis. The value must be one of [AxisTimeUnit](../../com.aspose.words/axistimeunit) constants. |

### getNumberFormat() {#getNumberFormat--}
```
public ChartNumberFormat getNumberFormat()
```


Returns a [ChartNumberFormat](../../com.aspose.words/chartnumberformat) object that allows defining number formats for the axis.

**Returns:**
[ChartNumberFormat](../../com.aspose.words/chartnumberformat) - A [ChartNumberFormat](../../com.aspose.words/chartnumberformat) object that allows defining number formats for the axis.
### getTickLabelOffset() {#getTickLabelOffset--}
```
public int getTickLabelOffset()
```


Gets the distance of labels from the axis.

The property represents a percentage of the default label offset.

Valid range is from 0 to 1000 percent inclusive. Default value is 100%.

The property has effect only for category axes. It is not supported by MS Office 2016 new charts.

**Returns:**
int - The distance of labels from the axis.
### setTickLabelOffset(int value) {#setTickLabelOffset-int-}
```
public void setTickLabelOffset(int value)
```


Sets the distance of labels from the axis.

The property represents a percentage of the default label offset.

Valid range is from 0 to 1000 percent inclusive. Default value is 100%.

The property has effect only for category axes. It is not supported by MS Office 2016 new charts.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The distance of labels from the axis. |

### getDisplayUnit() {#getDisplayUnit--}
```
public AxisDisplayUnit getDisplayUnit()
```


Specifies the scaling value of the display units for the value axis. The property has effect only for value axes.

**Returns:**
[AxisDisplayUnit](../../com.aspose.words/axisdisplayunit) - The corresponding [AxisDisplayUnit](../../com.aspose.words/axisdisplayunit) value.
### getAxisBetweenCategories() {#getAxisBetweenCategories--}
```
public boolean getAxisBetweenCategories()
```


Gets a flag indicating whether the value axis crosses the category axis between categories. The property has effect only for value axes. It is not supported by MS Office 2016 new charts.

**Returns:**
boolean - A flag indicating whether the value axis crosses the category axis between categories.
### setAxisBetweenCategories(boolean value) {#setAxisBetweenCategories-boolean-}
```
public void setAxisBetweenCategories(boolean value)
```


Sets a flag indicating whether the value axis crosses the category axis between categories. The property has effect only for value axes. It is not supported by MS Office 2016 new charts.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether the value axis crosses the category axis between categories. |

### getScaling() {#getScaling--}
```
public AxisScaling getScaling()
```


Provides access to the scaling options of the axis.

**Returns:**
[AxisScaling](../../com.aspose.words/axisscaling) - The corresponding [AxisScaling](../../com.aspose.words/axisscaling) value.
### getTickLabelSpacing() {#getTickLabelSpacing--}
```
public int getTickLabelSpacing()
```


Gets the interval, at which tick labels are drawn.

The property has effect for text category and series axes. It is not supported by MS Office 2016 new charts. Valid range of a value is greater than or equal to 1.

Setting this property sets the [getTickLabelSpacingIsAuto()](../../com.aspose.words/chartaxis\#getTickLabelSpacingIsAuto--) / [setTickLabelSpacingIsAuto(boolean)](../../com.aspose.words/chartaxis\#setTickLabelSpacingIsAuto-boolean-) property to **false**.

**Returns:**
int - The interval, at which tick labels are drawn.
### setTickLabelSpacing(int value) {#setTickLabelSpacing-int-}
```
public void setTickLabelSpacing(int value)
```


Sets the interval, at which tick labels are drawn.

The property has effect for text category and series axes. It is not supported by MS Office 2016 new charts. Valid range of a value is greater than or equal to 1.

Setting this property sets the [getTickLabelSpacingIsAuto()](../../com.aspose.words/chartaxis\#getTickLabelSpacingIsAuto--) / [setTickLabelSpacingIsAuto(boolean)](../../com.aspose.words/chartaxis\#setTickLabelSpacingIsAuto-boolean-) property to **false**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The interval, at which tick labels are drawn. |

### getTickLabelSpacingIsAuto() {#getTickLabelSpacingIsAuto--}
```
public boolean getTickLabelSpacingIsAuto()
```


Gets a flag indicating whether automatic interval of drawing tick labels shall be used.

Default value is **true**.

The property has effect for text category and series axes. It is not supported by MS Office 2016 new charts.

**Returns:**
boolean - A flag indicating whether automatic interval of drawing tick labels shall be used.
### setTickLabelSpacingIsAuto(boolean value) {#setTickLabelSpacingIsAuto-boolean-}
```
public void setTickLabelSpacingIsAuto(boolean value)
```


Sets a flag indicating whether automatic interval of drawing tick labels shall be used.

Default value is **true**.

The property has effect for text category and series axes. It is not supported by MS Office 2016 new charts.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether automatic interval of drawing tick labels shall be used. |

### getTickLabelAlignment() {#getTickLabelAlignment--}
```
public int getTickLabelAlignment()
```


Gets text alignment of axis tick labels.

This property has effect only for multi-line labels.

Default value is [ParagraphAlignment.CENTER](../../com.aspose.words/paragraphalignment\#CENTER).

.

**Returns:**
int - Text alignment of axis tick labels. The returned value is one of [ParagraphAlignment](../../com.aspose.words/paragraphalignment) constants.
### setTickLabelAlignment(int value) {#setTickLabelAlignment-int-}
```
public void setTickLabelAlignment(int value)
```


Sets text alignment of axis tick labels.

This property has effect only for multi-line labels.

Default value is [ParagraphAlignment.CENTER](../../com.aspose.words/paragraphalignment\#CENTER).

.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | Text alignment of axis tick labels. The value must be one of [ParagraphAlignment](../../com.aspose.words/paragraphalignment) constants. |

### getTickMarkSpacing() {#getTickMarkSpacing--}
```
public int getTickMarkSpacing()
```


Gets the interval, at which tick marks are drawn.

The property has effect for text category and series axes. It is not supported by MS Office 2016 new charts.

Valid range of a value is greater than or equal to 1.

**Returns:**
int - The interval, at which tick marks are drawn.
### setTickMarkSpacing(int value) {#setTickMarkSpacing-int-}
```
public void setTickMarkSpacing(int value)
```


Sets the interval, at which tick marks are drawn.

The property has effect for text category and series axes. It is not supported by MS Office 2016 new charts.

Valid range of a value is greater than or equal to 1.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The interval, at which tick marks are drawn. |

### getHidden() {#getHidden--}
```
public boolean getHidden()
```


Gets a flag indicating whether this axis is hidden or not. Default value is **false**.

**Returns:**
boolean - A flag indicating whether this axis is hidden or not.
### setHidden(boolean value) {#setHidden-boolean-}
```
public void setHidden(boolean value)
```


Sets a flag indicating whether this axis is hidden or not. Default value is **false**.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether this axis is hidden or not. |

### getTitle() {#getTitle--}
```
public ChartTitle getTitle()
```




**Returns:**
[ChartTitle](../../com.aspose.words/charttitle)
### setTitle(ChartTitle value) {#setTitle-com.aspose.words.ChartTitle-}
```
public void setTitle(ChartTitle value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [ChartTitle](../../com.aspose.words/charttitle) |  |

### getTitlePosition() {#getTitlePosition--}
```
public int getTitlePosition()
```




**Returns:**
int
### getDocument() {#getDocument--}
```
public DocumentBase getDocument()
```


Returns the Document the title holder belongs.

**Returns:**
[DocumentBase](../../com.aspose.words/documentbase) - The Document the title holder belongs.
### getTitleDeleted() {#getTitleDeleted--}
```
public boolean getTitleDeleted()
```




**Returns:**
boolean
### setTitleDeleted(boolean value) {#setTitleDeleted-boolean-}
```
public void setTitleDeleted(boolean value)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean |  |

### isVisible() {#isVisible--}
```
public boolean isVisible()
```




**Returns:**
boolean
### isInherited() {#isInherited--}
```
public boolean isInherited()
```




**Returns:**
boolean
