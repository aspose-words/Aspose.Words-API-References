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
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBubble3D()](#getBubble3D--) |  |
| [getClass()](#getClass--) |  |
| [getExplosion()](#getExplosion--) |  |
| [getFormat()](#getFormat--) | Provides access to fill and line formatting of this data point. |
| [getIndex()](#getIndex--) | Index of the data point this object applies formatting to. |
| [getInvertIfNegative()](#getInvertIfNegative--) |  |
| [getMarker()](#getMarker--) |  |
| [hashCode()](#hashCode--) |  |
| [materializeSpPr()](#materializeSpPr--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setBubble3D(boolean value)](#setBubble3D-boolean-) |  |
| [setExplosion(int value)](#setExplosion-int-) |  |
| [setInvertIfNegative(boolean value)](#setInvertIfNegative-boolean-) |  |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clearFormat() {#clearFormat--}
```
public void clearFormat()
```


Clears format of this data point. The properties are set to the default values defined in the parent series.

### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**Returns:**
boolean
### getBubble3D() {#getBubble3D--}
```
public boolean getBubble3D()
```


Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them.

**Returns:**
boolean
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**Returns:**
java.lang.Class<?>
### getExplosion() {#getExplosion--}
```
public int getExplosion()
```


Specifies the amount the data point shall be moved from the center of the pie. Can be negative, negative means that property is not set and no explosion should be applied. Applies only to Pie charts.

**Returns:**
int
### getFormat() {#getFormat--}
```
public ChartFormat getFormat()
```


Provides access to fill and line formatting of this data point.

**Returns:**
[ChartFormat](../../com.aspose.words/chartformat) - The corresponding [ChartFormat](../../com.aspose.words/chartformat) value.
### getIndex() {#getIndex--}
```
public int getIndex()
```


Index of the data point this object applies formatting to.

**Returns:**
int - The corresponding  int  value.
### getInvertIfNegative() {#getInvertIfNegative--}
```
public boolean getInvertIfNegative()
```


Specifies whether the parent element shall inverts its colors if the value is negative.

**Returns:**
boolean
### getMarker() {#getMarker--}
```
public ChartMarker getMarker()
```


Specifies a data marker. Marker is automatically created when requested.

**Returns:**
[ChartMarker](../../com.aspose.words/chartmarker)
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Returns:**
int
### materializeSpPr() {#materializeSpPr--}
```
public void materializeSpPr()
```




### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setBubble3D(boolean value) {#setBubble3D-boolean-}
```
public void setBubble3D(boolean value)
```


Specifies whether the bubbles in Bubble chart should have a 3-D effect applied to them.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean |  |

### setExplosion(int value) {#setExplosion-int-}
```
public void setExplosion(int value)
```


Specifies the amount the data point shall be moved from the center of the pie. Can be negative, negative means that property is not set and no explosion should be applied. Applies only to Pie charts.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | int |  |

### setInvertIfNegative(boolean value) {#setInvertIfNegative-boolean-}
```
public void setInvertIfNegative(boolean value)
```


Specifies whether the parent element shall inverts its colors if the value is negative.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean |  |

### toString() {#toString--}
```
public String toString()
```




**Returns:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |

