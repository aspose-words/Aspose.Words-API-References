---
title: ChartSeriesCollection
second_title: Aspose.Words for Java API 参考
description:表示 a 的集合。
type: docs
weight: 69
url: /zh/java/com.aspose.words/chartseriescollection/
---

**遗产:**
java.lang.Object

**All Implemented 界面s:**
java.lang.Iterable
```
public class ChartSeriesCollection implements Iterable
```

代表一个集合[ChartSeries](../../com.aspose.words/chartseries).

要了解更多信息，请访问**Working with Charts**文档文章。
## 方法s

| 方法 | 描述 |
| --- | --- |
| [add(String seriesName, double[] xValues, double[] yValues)](#add-java.lang.String-double---double---) | 添加新的[ChartSeries](../../com.aspose.words/chartseries)到这个集合。 |
| [add(String seriesName, double[] xValues, double[] yValues, double[] bubbleSizes)](#add-java.lang.String-double---double---double---) | 添加新的[ChartSeries](../../com.aspose.words/chartseries)到这个集合。 |
| [add(String seriesName, String[] categories, double[] values)](#add-java.lang.String-java.lang.String---double---) | 添加新的[ChartSeries](../../com.aspose.words/chartseries)到这个集合。 |
| [add(String seriesName, Date[] dates, double[] values)](#add-java.lang.String-java.util.Date---double---) | 添加新的[ChartSeries](../../com.aspose.words/chartseries)到这个集合。 |
| [clear()](#clear--) | 删除所有[ChartSeries](../../com.aspose.words/chartseries)从这个集合。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [get(int index)](#get-int-) | 返回一个[ChartSeries](../../com.aspose.words/chartseries)在指定索引处。 |
| [get班级()](#get班级--) |  |
| [getCount()](#getCount--) | 返回数量[ChartSeries](../../com.aspose.words/chartseries)在这个集合中。 |
| [hashCode()](#hashCode--) |  |
| [iterator()](#iterator--) | 返回一个枚举器对象。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [removeAt(int index)](#removeAt-int-) | 删除一个[ChartSeries](../../com.aspose.words/chartseries)在指定索引处。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### add(String seriesName, double[] xValues, double[] yValues) {#add-java.lang.String-double---double---}
```
public ChartSeries add(String seriesName, double[] xValues, double[] yValues)
```


添加新的[ChartSeries](../../com.aspose.words/chartseries)到这个集合。使用此方法将系列添加到任何类型的散点图。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| seriesName | java.lang.String |  |
| xValues | double[] |  |
| yValues | double[] |  |

**退货:**
[ChartSeries](../../com.aspose.words/chartseries) - 最近添加的[ChartSeries](../../com.aspose.words/chartseries)目的。
### add(String seriesName, double[] xValues, double[] yValues, double[] bubbleSizes) {#add-java.lang.String-double---double---double---}
```
public ChartSeries add(String seriesName, double[] xValues, double[] yValues, double[] bubbleSizes)
```


添加新的[ChartSeries](../../com.aspose.words/chartseries)到这个集合。使用此方法将系列添加到任何类型的气泡图。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| seriesName | java.lang.String |  |
| xValues | double[] |  |
| yValues | double[] |  |
| bubbleSizes | double[] |  |

**退货:**
[ChartSeries](../../com.aspose.words/chartseries) - 最近添加的[ChartSeries](../../com.aspose.words/chartseries)目的。
### add(String seriesName, String[] categories, double[] values) {#add-java.lang.String-java.lang.String---double---}
```
public ChartSeries add(String seriesName, String[] categories, double[] values)
```


添加新的[ChartSeries](../../com.aspose.words/chartseries)到这个集合。使用此方法可将系列添加到任何类型的条形图、柱形图、折线图和曲面图。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| seriesName | java.lang.String |  |
| categories | java.lang.String[] |  |
| values | double[] |  |

**退货:**
[ChartSeries](../../com.aspose.words/chartseries) - 最近添加的[ChartSeries](../../com.aspose.words/chartseries)目的。
### add(String seriesName, Date[] dates, double[] values) {#add-java.lang.String-java.util.Date---double---}
```
public ChartSeries add(String seriesName, Date[] dates, double[] values)
```


添加新的[ChartSeries](../../com.aspose.words/chartseries)到这个集合。使用此方法将系列添加到任何类型的区域、雷达和股票图表。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| seriesName | java.lang.String |  |
| dates | java.util.Date[] |  |
| values | double[] |  |

**退货:**
[ChartSeries](../../com.aspose.words/chartseries)
### clear() {#clear--}
```
public void clear()
```


删除所有[ChartSeries](../../com.aspose.words/chartseries)从这个集合。

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
### get(int index) {#get-int-}
```
public ChartSeries get(int index)
```


返回一个[ChartSeries](../../com.aspose.words/chartseries)在指定索引处。

该索引从零开始。

允许使用负索引并指示从集合的背面进行访问。例如 -1 表示最后一项，-2 表示倒数第二个，依此类推。

如果 index 大于或等于列表中的项目数，则返回空引用。

如果 index 为负且其绝对值大于列表中的项目数，则返回空引用。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 集合中的索引。 |

**退货:**
[ChartSeries](../../com.aspose.words/chartseries) - 一个[ChartSeries](../../com.aspose.words/chartseries)在指定索引处。
### get班级() {#get班级--}
```
public final native 班级<?> get班级()
```




**退货:**
java.lang.班级<?>
### getCount() {#getCount--}
```
public int getCount()
```


返回数量[ChartSeries](../../com.aspose.words/chartseries)在这个集合中。

**退货:**
 int - 的数量[ChartSeries](../../com.aspose.words/chartseries)在这个集合中。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货:**
整数
### iterator() {#iterator--}
```
public Iterator iterator()
```


返回一个枚举器对象。

**退货:**
java.util.Iterator
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### removeAt(int index) {#removeAt-int-}
```
public void removeAt(int index)
```


删除一个[ChartSeries](../../com.aspose.words/chartseries)在指定索引处。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| index | int | 要删除的 ChartSeries 从零开始的索引。 |

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
