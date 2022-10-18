---
title: AxisScaling
second_title: Aspose.Words for Java API Reference
description: Represents the scaling options of the axis.
type: docs
weight: 22
url: /java/com.aspose.words/axisscaling/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
java.lang.Cloneable
```
public class AxisScaling implements Cloneable
```

Represents the scaling options of the axis.

To learn more, visit the **Working with Charts** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [getType()](#getType--) | Gets scaling type of the axis. |
| [setType(int value)](#setType-int-) | Sets scaling type of the axis. |
| [getLogBase()](#getLogBase--) | Gets the logarithmic base for a logarithmic axis. |
| [setLogBase(double value)](#setLogBase-double-) | Sets the logarithmic base for a logarithmic axis. |
| [getMinimum()](#getMinimum--) | Gets minimum value of the axis. |
| [setMinimum(AxisBound value)](#setMinimum-com.aspose.words.AxisBound-) | Sets minimum value of the axis. |
| [getMaximum()](#getMaximum--) | Gets the maximum value of the axis. |
| [setMaximum(AxisBound value)](#setMaximum-com.aspose.words.AxisBound-) | Sets the maximum value of the axis. |
### getType() {#getType--}
```
public int getType()
```


Gets scaling type of the axis. The [AxisScaleType.LINEAR](../../com.aspose.words/axisscaletype\#LINEAR) value is the only that is allowed in MS Office 2016 new charts.

**Returns:**
int - Scaling type of the axis. The returned value is one of [AxisScaleType](../../com.aspose.words/axisscaletype) constants.
### setType(int value) {#setType-int-}
```
public void setType(int value)
```


Sets scaling type of the axis. The [AxisScaleType.LINEAR](../../com.aspose.words/axisscaletype\#LINEAR) value is the only that is allowed in MS Office 2016 new charts.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | Scaling type of the axis. The value must be one of [AxisScaleType](../../com.aspose.words/axisscaletype) constants. |

### getLogBase() {#getLogBase--}
```
public double getLogBase()
```


Gets the logarithmic base for a logarithmic axis.

The property is not supported by MS Office 2016 new charts.

Valid range of a floating point value is greater than or equal to 2 and less than or equal to 1000. The property has effect only if [getType()](../../com.aspose.words/axisscaling\#getType--) / [setType(int)](../../com.aspose.words/axisscaling\#setType-int-) is set to [AxisScaleType.LOGARITHMIC](../../com.aspose.words/axisscaletype\#LOGARITHMIC).

Setting this property sets the [getType()](../../com.aspose.words/axisscaling\#getType--) / [setType(int)](../../com.aspose.words/axisscaling\#setType-int-) property to [AxisScaleType.LOGARITHMIC](../../com.aspose.words/axisscaletype\#LOGARITHMIC).

**Returns:**
double - The logarithmic base for a logarithmic axis.
### setLogBase(double value) {#setLogBase-double-}
```
public void setLogBase(double value)
```


Sets the logarithmic base for a logarithmic axis.

The property is not supported by MS Office 2016 new charts.

Valid range of a floating point value is greater than or equal to 2 and less than or equal to 1000. The property has effect only if [getType()](../../com.aspose.words/axisscaling\#getType--) / [setType(int)](../../com.aspose.words/axisscaling\#setType-int-) is set to [AxisScaleType.LOGARITHMIC](../../com.aspose.words/axisscaletype\#LOGARITHMIC).

Setting this property sets the [getType()](../../com.aspose.words/axisscaling\#getType--) / [setType(int)](../../com.aspose.words/axisscaling\#setType-int-) property to [AxisScaleType.LOGARITHMIC](../../com.aspose.words/axisscaletype\#LOGARITHMIC).

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | double | The logarithmic base for a logarithmic axis. |

### getMinimum() {#getMinimum--}
```
public AxisBound getMinimum()
```


Gets minimum value of the axis. The default value is "auto".

**Returns:**
[AxisBound](../../com.aspose.words/axisbound) - Minimum value of the axis.
### setMinimum(AxisBound value) {#setMinimum-com.aspose.words.AxisBound-}
```
public void setMinimum(AxisBound value)
```


Sets minimum value of the axis. The default value is "auto".

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [AxisBound](../../com.aspose.words/axisbound) | Minimum value of the axis. |

### getMaximum() {#getMaximum--}
```
public AxisBound getMaximum()
```


Gets the maximum value of the axis. The default value is "auto".

**Returns:**
[AxisBound](../../com.aspose.words/axisbound) - The maximum value of the axis.
### setMaximum(AxisBound value) {#setMaximum-com.aspose.words.AxisBound-}
```
public void setMaximum(AxisBound value)
```


Sets the maximum value of the axis. The default value is "auto".

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | [AxisBound](../../com.aspose.words/axisbound) | The maximum value of the axis. |

