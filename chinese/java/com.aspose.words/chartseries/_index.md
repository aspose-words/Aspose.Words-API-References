---
title: ChartSeries
second_title: Aspose.Words for Java API 参考
description:表示图表系列属性。
type: docs
weight: 68
url: /zh/java/com.aspose.words/chartseries/
---

**遗产:**
java.lang.Object

**All Implemented 界面s:**
[com.aspose.words.IChartDataPoint](../../com.aspose.words/ichartdatapoint), java.lang.Cloneable
```
public class ChartSeries implements IChartDataPoint, Cloneable
```

表示图表系列属性。

要了解更多信息，请访问**Working with Charts**文档文章。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getBubble3D()](#getBubble3D--) |  |
| [get班级()](#get班级--) |  |
| [getDataLabels()](#getDataLabels--) | 指定整个系列的数据标签设置。 |
| [getDataPoints()](#getDataPoints--) | 返回此系列中所有数据点的格式化对象的集合。 |
| [getExplosion()](#getExplosion--) |  |
| [getFormat()](#getFormat--) | 提供对系列的填充和线条格式的访问。 |
| [getInvertIfNegative()](#getInvertIfNegative--) |  |
| [getLegendEntry()](#getLegendEntry--) | 获取此图表系列的图例条目。 |
| [getMarker()](#getMarker--) |  |
| [getName()](#getName--) | 获取系列的名称，如果未明确设置名称，则使用索引生成。 |
| [getSmooth()](#getSmooth--) | 允许指定连接图表上的点的线是否应使用 Catmull-Rom 样条进行平滑。 |
| [hasDataLabels()](#hasDataLabels--) | 获取一个标志，该标志指示是否为系列显示数据标签。 |
| [hasDataLabels(boolean value)](#hasDataLabels-boolean-) | 设置一个标志，指示是否为系列显示数据标签。 |
| [hashCode()](#hashCode--) |  |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setBubble3D(boolean value)](#setBubble3D-boolean-) |  |
| [setExplosion(int value)](#setExplosion-int-) |  |
| [setInvertIfNegative(boolean value)](#setInvertIfNegative-boolean-) |  |
| [setName(String value)](#setName-java.lang.String-) | 设置系列的名称，如果未明确设置名称，则使用索引生成。 |
| [setSmooth(boolean value)](#setSmooth-boolean-) | 允许指定连接图表上的点的线是否应使用 Catmull-Rom 样条进行平滑。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
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
### getDataLabels() {#getDataLabels--}
```
public ChartDataLabelCollection getDataLabels()
```


指定整个系列的数据标签设置。

**退货:**
[ChartDataLabelCollection](../../com.aspose.words/chartdatalabelcollection) - 相应的[ChartDataLabelCollection](../../com.aspose.words/chartdatalabelcollection)价值。
### getDataPoints() {#getDataPoints--}
```
public ChartDataPointCollection getDataPoints()
```


返回此系列中所有数据点的格式化对象的集合。

**退货:**
[ChartDataPointCollection](../../com.aspose.words/chartdatapointcollection) - 本系列中所有数据点的格式化对象集合。
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


提供对系列的填充和线条格式的访问。

**退货:**
[ChartFormat](../../com.aspose.words/chartformat) - 相应的[ChartFormat](../../com.aspose.words/chartformat)价值。
### getInvertIfNegative() {#getInvertIfNegative--}
```
public boolean getInvertIfNegative()
```


指定如果值为负数，父元素是否应反转其颜色。

**退货:**
布尔值
### getLegendEntry() {#getLegendEntry--}
```
public ChartLegendEntry getLegendEntry()
```


获取此图表系列的图例条目。

**退货:**
[ChartLegendEntry](../../com.aspose.words/chartlegendentry) - 此图表系列的图例条目。
### getMarker() {#getMarker--}
```
public ChartMarker getMarker()
```


指定数据标记。请求时会自动创建标记。

**退货:**
[ChartMarker](../../com.aspose.words/chartmarker)
### getName() {#getName--}
```
public String getName()
```


获取系列的名称，如果未明确设置名称，则使用索引生成。默认情况下返回 Series 加一个基于索引的索引。

**退货:**
java.lang.String - 系列的名称，如果未明确设置名称，则使用索引生成。
### getSmooth() {#getSmooth--}
```
public boolean getSmooth()
```


允许指定连接图表上的点的线是否应使用 Catmull-Rom 样条进行平滑。

**退货:**
boolean - 对应的布尔值。
### hasDataLabels() {#hasDataLabels--}
```
public boolean hasDataLabels()
```


获取一个标志，该标志指示是否为系列显示数据标签。

**退货:**
boolean - 指示是否为系列显示数据标签的标志。
### hasDataLabels(boolean value) {#hasDataLabels-boolean-}
```
public void hasDataLabels(boolean value)
```


设置一个标志，指示是否为系列显示数据标签。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 指示是否为系列显示数据标签的标志。 |

### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
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

### setName(String value) {#setName-java.lang.String-}
```
public void setName(String value)
```


设置系列的名称，如果未明确设置名称，则使用索引生成。默认情况下返回 Series 加一个基于索引的索引。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 系列的名称，如果未明确设置名称，则使用索引生成。 |

### setSmooth(boolean value) {#setSmooth-boolean-}
```
public void setSmooth(boolean value)
```


允许指定连接图表上的点的线是否应使用 Catmull-Rom 样条进行平滑。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

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
