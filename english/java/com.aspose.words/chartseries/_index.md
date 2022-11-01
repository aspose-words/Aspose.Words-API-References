---
title: ChartSeries
second_title: Aspose.Words for Java API Reference
description: Represents chart series properties.
type: docs
weight: 68
url: /java/com.aspose.words/chartseries/
---

**Inheritance:**
java.lang.Object

**All Implemented Interfaces:**
[com.aspose.words.IChartDataPoint](../../com.aspose.words/ichartdatapoint), java.lang.Cloneable
```
public class ChartSeries implements IChartDataPoint, Cloneable
```

Represents chart series properties.

To learn more, visit the **Working with Charts** documentation article.
## Methods

| Method | Description |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBubble3D()](#getBubble3D--) |  |
| [getClass()](#getClass--) |  |
| [getDataLabels()](#getDataLabels--) | Specifies the settings for the data labels for the entire series. |
| [getDataPoints()](#getDataPoints--) | Returns a collection of formatting objects for all data points in this series. |
| [getExplosion()](#getExplosion--) |  |
| [getFormat()](#getFormat--) | Provides access to fill and line formatting of the series. |
| [getInvertIfNegative()](#getInvertIfNegative--) |  |
| [getLegendEntry()](#getLegendEntry--) | Gets a legend entry for this chart series. |
| [getMarker()](#getMarker--) |  |
| [getName()](#getName--) | Gets the name of the series, if name is not set explicitly it is generated using index. |
| [getSmooth()](#getSmooth--) | Allows to specify whether the line connecting the points on the chart shall be smoothed using Catmull-Rom splines. |
| [hasDataLabels()](#hasDataLabels--) | Gets a flag indicating whether data labels are displayed for the series. |
| [hasDataLabels(boolean value)](#hasDataLabels-boolean-) | Sets a flag indicating whether data labels are displayed for the series. |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setBubble3D(boolean value)](#setBubble3D-boolean-) |  |
| [setExplosion(int value)](#setExplosion-int-) |  |
| [setInvertIfNegative(boolean value)](#setInvertIfNegative-boolean-) |  |
| [setName(String value)](#setName-java.lang.String-) | Sets the name of the series, if name is not set explicitly it is generated using index. |
| [setSmooth(boolean value)](#setSmooth-boolean-) | Allows to specify whether the line connecting the points on the chart shall be smoothed using Catmull-Rom splines. |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
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
### getDataLabels() {#getDataLabels--}
```
public ChartDataLabelCollection getDataLabels()
```


Specifies the settings for the data labels for the entire series.

**Returns:**
[ChartDataLabelCollection](../../com.aspose.words/chartdatalabelcollection) - The corresponding [ChartDataLabelCollection](../../com.aspose.words/chartdatalabelcollection) value.
### getDataPoints() {#getDataPoints--}
```
public ChartDataPointCollection getDataPoints()
```


Returns a collection of formatting objects for all data points in this series.

**Returns:**
[ChartDataPointCollection](../../com.aspose.words/chartdatapointcollection) - A collection of formatting objects for all data points in this series.
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


Provides access to fill and line formatting of the series.

**Returns:**
[ChartFormat](../../com.aspose.words/chartformat) - The corresponding [ChartFormat](../../com.aspose.words/chartformat) value.
### getInvertIfNegative() {#getInvertIfNegative--}
```
public boolean getInvertIfNegative()
```


Specifies whether the parent element shall inverts its colors if the value is negative.

**Returns:**
boolean
### getLegendEntry() {#getLegendEntry--}
```
public ChartLegendEntry getLegendEntry()
```


Gets a legend entry for this chart series.

**Returns:**
[ChartLegendEntry](../../com.aspose.words/chartlegendentry) - A legend entry for this chart series.
### getMarker() {#getMarker--}
```
public ChartMarker getMarker()
```


Specifies a data marker. Marker is automatically created when requested.

**Returns:**
[ChartMarker](../../com.aspose.words/chartmarker)
### getName() {#getName--}
```
public String getName()
```


Gets the name of the series, if name is not set explicitly it is generated using index. By default returns Series plus one based index.

**Returns:**
java.lang.String - The name of the series, if name is not set explicitly it is generated using index.
### getSmooth() {#getSmooth--}
```
public boolean getSmooth()
```


Allows to specify whether the line connecting the points on the chart shall be smoothed using Catmull-Rom splines.

**Returns:**
boolean - The corresponding  boolean  value.
### hasDataLabels() {#hasDataLabels--}
```
public boolean hasDataLabels()
```


Gets a flag indicating whether data labels are displayed for the series.

**Returns:**
boolean - A flag indicating whether data labels are displayed for the series.
### hasDataLabels(boolean value) {#hasDataLabels-boolean-}
```
public void hasDataLabels(boolean value)
```


Sets a flag indicating whether data labels are displayed for the series.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | A flag indicating whether data labels are displayed for the series. |

### hashCode() {#hashCode--}
```
public native int hashCode()
```




**Returns:**
int
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

### setName(String value) {#setName-java.lang.String-}
```
public void setName(String value)
```


Sets the name of the series, if name is not set explicitly it is generated using index. By default returns Series plus one based index.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | java.lang.String | The name of the series, if name is not set explicitly it is generated using index. |

### setSmooth(boolean value) {#setSmooth-boolean-}
```
public void setSmooth(boolean value)
```


Allows to specify whether the line connecting the points on the chart shall be smoothed using Catmull-Rom splines.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| value | boolean | The corresponding  boolean  value. |

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

