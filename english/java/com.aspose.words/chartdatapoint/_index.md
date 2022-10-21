---
title: ChartDataPoint
second_title: Aspose.Words for Java API Reference
description: Allows to specify formatting of a single data point on the chart.
type: docs
weight: 60
url: /java/com.aspose.words/chartdatapoint/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
[com.aspose.words.IChartDataPoint](../../com.aspose.words/ichartdatapoint), java.lang.Cloneable
```
public class ChartDataPoint implements IChartDataPoint, Cloneable
```

Allows to specify formatting of a single data point on the chart.

To learn more, visit the **Working with Charts** documentation article.

On a series, the [ChartDataPoint](../../com.aspose.words/chartdatapoint) object is a member of the [ChartDataPointCollection](../../com.aspose.words/chartdatapointcollection). The [ChartDataPointCollection](../../com.aspose.words/chartdatapointcollection) contains a [ChartDataPoint](../../com.aspose.words/chartdatapoint) object for each point.
## Methods

| Method | Description |
| --- | --- |
| [clearFormat()](#clearFormat--) | Clears format of this data point. |
| [materializeSpPr()](#materializeSpPr--) |  |
| [getIndex()](#getIndex--) | Index of the data point this object applies formatting to. |
| [getExplosion()](#getExplosion--) |  |
| [setExplosion(int value)](#setExplosion-int-) |  |
| [getInvertIfNegative()](#getInvertIfNegative--) |  |
| [setInvertIfNegative(boolean value)](#setInvertIfNegative-boolean-) |  |
| [getBubble3D()](#getBubble3D--) |  |
| [setBubble3D(boolean value)](#setBubble3D-boolean-) |  |
| [getFormat()](#getFormat--) | Provides access to fill and line formatting of this data point. |
| [getMarker()](#getMarker--) |  |
### clearFormat() {#clearFormat--}
```
public void clearFormat()
```


Clears format of this data point. The properties are set to the default values defined in the parent series.

### materializeSpPr() {#materializeSpPr--}
```
public void materializeSpPr()
```




### getIndex() {#getIndex--}
```
public int getIndex()
```


Index of the data point this object applies formatting to.

**Returns:**
int - The corresponding  int  value.
### getExplosion() {#getExplosion--}
```
public int getExplosion()
```


Specifies the amount the data point shall be moved from the center of the pie. Can be negative, negative means that property is not set and no explosion should be applied. Applies only to Pie charts.

**Returns:**
int
### setExplosion(int value) {#setExplosion-int-}
```
public void setExplosion(int value)
```


Specifies the amount the data point shall be moved from the center of the pie. Can be negative, negative means that property is not set and no explosion should be applied. Applies only to Pie charts.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### getInvertIfNegative() {#getInvertIfNegative--}
```
public boolean getInvertIfNegative()
```


Specifies whether the parent element shall inverts its colors if the value is negative.

**Returns:**
boolean
### setInvertIfNegative(boolean value) {#setInvertIfNegative-boolean-}
```
public void setInvertIfNegative(boolean value)
```


Specifies whether the parent element shall inverts its colors if the value is negative.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean |  |

### getBubble3D() {#getBubble3D--}
```
public boolean getBubble3D()
```


Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them.

**Returns:**
boolean
### setBubble3D(boolean value) {#setBubble3D-boolean-}
```
public void setBubble3D(boolean value)
```


Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean |  |

### getFormat() {#getFormat--}
```
public ChartFormat getFormat()
```


Provides access to fill and line formatting of this data point.

**Returns:**
[ChartFormat](../../com.aspose.words/chartformat) - The corresponding [ChartFormat](../../com.aspose.words/chartformat) value.
### getMarker() {#getMarker--}
```
public ChartMarker getMarker()
```


Specifies a data marker. Marker is automatically created when requested.

**Returns:**
[ChartMarker](../../com.aspose.words/chartmarker)
