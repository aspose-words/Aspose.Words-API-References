---
title: IChartDataPoint
second_title: Aspose.Words for Java API Reference
description: Contains properties of a single data point on the chart.
type: docs
weight: 637
url: /java/com.aspose.words/ichartdatapoint/
---
```
public interface IChartDataPoint
```

Contains properties of a single data point on the chart.
## Methods

| Method | Description |
| --- | --- |
| [getBubble3D()](#getBubble3D) | Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them. |
| [getExplosion()](#getExplosion) | Specifies the amount the data point shall be moved from the center of the pie. |
| [getInvertIfNegative()](#getInvertIfNegative) | Specifies whether the parent element shall inverts its colors if the value is negative. |
| [getMarker()](#getMarker) | Specifies a data marker. |
| [setBubble3D(boolean value)](#setBubble3D-boolean) | Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them. |
| [setExplosion(int value)](#setExplosion-int) | Specifies the amount the data point shall be moved from the center of the pie. |
| [setInvertIfNegative(boolean value)](#setInvertIfNegative-boolean) | Specifies whether the parent element shall inverts its colors if the value is negative. |
### getBubble3D() {#getBubble3D}
```
public abstract boolean getBubble3D()
```


Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them.

**Returns:**
boolean - The corresponding  boolean  value.
### getExplosion() {#getExplosion}
```
public abstract int getExplosion()
```


Specifies the amount the data point shall be moved from the center of the pie. Can be negative, negative means that property is not set and no explosion should be applied. Applies only to Pie charts.

**Returns:**
int - The corresponding  int  value.
### getInvertIfNegative() {#getInvertIfNegative}
```
public abstract boolean getInvertIfNegative()
```


Specifies whether the parent element shall inverts its colors if the value is negative.

**Returns:**
boolean - The corresponding  boolean  value.
### getMarker() {#getMarker}
```
public abstract ChartMarker getMarker()
```


Specifies a data marker. Marker is automatically created when requested.

**Returns:**
[ChartMarker](../../com.aspose.words/chartmarker) - The corresponding [ChartMarker](../../com.aspose.words/chartmarker) value.
### setBubble3D(boolean value) {#setBubble3D-boolean}
```
public abstract void setBubble3D(boolean value)
```


Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

### setExplosion(int value) {#setExplosion-int}
```
public abstract void setExplosion(int value)
```


Specifies the amount the data point shall be moved from the center of the pie. Can be negative, negative means that property is not set and no explosion should be applied. Applies only to Pie charts.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int | The corresponding  int  value. |

### setInvertIfNegative(boolean value) {#setInvertIfNegative-boolean}
```
public abstract void setInvertIfNegative(boolean value)
```


Specifies whether the parent element shall inverts its colors if the value is negative.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

