---
title: ChartDataPoint
second_title: Aspose.Words for Java API 参考
description: 允许指定图表上单个数据点的格式。
type: docs
weight: 60
url: /zh/java/com.aspose.words/chartdatapoint/
---

**遗产:**
java.lang.Object

**All Implemented 界面s:**
[com.aspose.words.IChartDataPoint](../../com.aspose.words/ichartdatapoint), java.lang.Cloneable
```
public class ChartDataPoint implements IChartDataPoint, Cloneable
```

允许指定图表上单个数据点的格式。

要了解更多信息，请访问**Working with Charts**文档文章。

在一个系列中，[ChartDataPoint](../../com.aspose.words/chartdatapoint)对象是[ChartDataPointCollection](../../com.aspose.words/chartdatapointcollection).这[ChartDataPointCollection](../../com.aspose.words/chartdatapointcollection)包含一个[ChartDataPoint](../../com.aspose.words/chartdatapoint)每个点的对象。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [clearFormat()](#clearFormat--) | 清除此数据点的格式。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBubble3D()](#getBubble3D--) |  |
| [get班级()](#get班级--) |  |
| [getExplosion()](#getExplosion--) |  |
| [getFormat()](#getFormat--) | 提供对此数据点的填充和线条格式的访问。 |
| [getIndex()](#getIndex--) | 此对象对其应用格式设置的数据点的索引。 |
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


清除此数据点的格式。属性设置为父系列中定义的默认值。

### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货:**
布尔值
### getBubble3D() {#getBubble3D--}
```
public boolean getBubble3D()
```


指定气泡图中的气泡是否应应用 3-D 效果。

**退货:**
布尔值
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getExplosion() {#getExplosion--}
```
public int getExplosion()
```


指定数据点应从饼图中心移动的量。可以为负数，负数表示未设置属性且不应应用爆炸。仅适用于饼图。

**退货:**
整数
### getFormat() {#getFormat--}
```
public ChartFormat getFormat()
```


提供对此数据点的填充和线条格式的访问。

**退货:**
[ChartFormat](../../com.aspose.words/chartformat) - 相应的[ChartFormat](../../com.aspose.words/chartformat)价值。
### getIndex() {#getIndex--}
```
public int getIndex()
```


此对象对其应用格式设置的数据点的索引。

**退货:**
int - 对应的 int 值。
### getInvertIfNegative() {#getInvertIfNegative--}
```
public boolean getInvertIfNegative()
```


指定如果值为负数，父元素是否应反转其颜色。

**退货:**
布尔值
### getMarker() {#getMarker--}
```
public ChartMarker getMarker()
```


指定数据标记。请求时会自动创建标记。

**退货:**
[ChartMarker](../../com.aspose.words/chartmarker)
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
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


指定气泡图中的气泡是否应应用 3-D 效果。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean |  |

### setExplosion(int value) {#setExplosion-int-}
```
public void setExplosion(int value)
```


指定数据点应从饼图中心移动的量。可以为负数，负数表示未设置属性且不应应用爆炸。仅适用于饼图。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int |  |

### setInvertIfNegative(boolean value) {#setInvertIfNegative-boolean-}
```
public void setInvertIfNegative(boolean value)
```


指定如果值为负数，父元素是否应反转其颜色。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean |  |

### toString() {#toString--}
```
public String toString()
```




**退货:**
java.lang.String
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
