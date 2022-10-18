---
title: AxisDisplayUnit
second_title: Aspose.Words for Java API Reference
description: Provides access to the scaling options of the display units for the value axis.
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

To learn more, visit the **Working with Charts** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getUnit()](#getUnit--) | Gets the scaling value of the display units as one of the predefined values. |
| [setUnit(int value)](#setUnit-int-) | Sets the scaling value of the display units as one of the predefined values. |
| [getCustomUnit()](#getCustomUnit--) | Gets a user-defined divisor to scale display units on the value axis. |
| [setCustomUnit(double value)](#setCustomUnit-double-) | Sets a user-defined divisor to scale display units on the value axis. |
| [getTitle()](#getTitle--) |  |
| [setTitle(ChartTitle value)](#setTitle-com.aspose.words.ChartTitle-) |  |
| [getTitlePosition()](#getTitlePosition--) |  |
| [getDocument()](#getDocument--) | Returns the Document the title holder belongs. |
| [getTitleDeleted()](#getTitleDeleted--) |  |
| [setTitleDeleted(boolean value)](#setTitleDeleted-boolean-) |  |
| [isVisible()](#isVisible--) |  |
### getUnit() {#getUnit--}
```
public int getUnit()
```


Gets the scaling value of the display units as one of the predefined values. Default value is [AxisBuiltInUnit.NONE](../../com.aspose.words/axisbuiltinunit\#NONE). The [AxisBuiltInUnit.CUSTOM](../../com.aspose.words/axisbuiltinunit\#CUSTOM) and [AxisBuiltInUnit.PERCENTAGE](../../com.aspose.words/axisbuiltinunit\#PERCENTAGE) values are not available in some chart types; see [AxisBuiltInUnit](../../com.aspose.words/axisbuiltinunit) for more information.

**Returns:**
int - The scaling value of the display units as one of the predefined values. The returned value is one of [AxisBuiltInUnit](../../com.aspose.words/axisbuiltinunit) constants.
### setUnit(int value) {#setUnit-int-}
```
public void setUnit(int value)
```


Sets the scaling value of the display units as one of the predefined values. Default value is [AxisBuiltInUnit.NONE](../../com.aspose.words/axisbuiltinunit\#NONE). The [AxisBuiltInUnit.CUSTOM](../../com.aspose.words/axisbuiltinunit\#CUSTOM) and [AxisBuiltInUnit.PERCENTAGE](../../com.aspose.words/axisbuiltinunit\#PERCENTAGE) values are not available in some chart types; see [AxisBuiltInUnit](../../com.aspose.words/axisbuiltinunit) for more information.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The scaling value of the display units as one of the predefined values. The value must be one of [AxisBuiltInUnit](../../com.aspose.words/axisbuiltinunit) constants. |

### getCustomUnit() {#getCustomUnit--}
```
public double getCustomUnit()
```


Gets a user-defined divisor to scale display units on the value axis.

The property is not supported by MS Office 2016 new charts. Default value is 1.

Setting this property sets the [getUnit()](../../com.aspose.words/axisdisplayunit\#getUnit--) / [setUnit(int)](../../com.aspose.words/axisdisplayunit\#setUnit-int-) property to [AxisBuiltInUnit.CUSTOM](../../com.aspose.words/axisbuiltinunit\#CUSTOM).

**Returns:**
double - A user-defined divisor to scale display units on the value axis.
### setCustomUnit(double value) {#setCustomUnit-double-}
```
public void setCustomUnit(double value)
```


Sets a user-defined divisor to scale display units on the value axis.

The property is not supported by MS Office 2016 new charts. Default value is 1.

Setting this property sets the [getUnit()](../../com.aspose.words/axisdisplayunit\#getUnit--) / [setUnit(int)](../../com.aspose.words/axisdisplayunit\#setUnit-int-) property to [AxisBuiltInUnit.CUSTOM](../../com.aspose.words/axisbuiltinunit\#CUSTOM).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | A user-defined divisor to scale display units on the value axis. |

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
