---
title: ChartDataLabel
second_title: Aspose.Words for Java API 参考
description: 表示图表点或趋势线上的数据标签。
type: docs
weight: 58
url: /zh/java/com.aspose.words/chartdatalabel/
---

**遗产：**
java.lang.Object

**所有已实现的接口：**
java.lang.Cloneable
```
public class ChartDataLabel implements Cloneable
```

表示图表点或趋势线上的数据标签。

要了解更多信息，请访问**Working with Charts**文档文章。

在一个系列中，[ChartDataLabel](../../com.aspose.words/chartdatalabel)对象是[ChartDataLabelCollection](../../com.aspose.words/chartdatalabelcollection).这[ChartDataLabelCollection](../../com.aspose.words/chartdatalabelcollection)包含一个[ChartDataLabel](../../com.aspose.words/chartdatalabel)每个点的对象。
## 方法

| 方法 | 描述 |
| --- | --- |
| [clearFormat()](#clearFormat--) | 清除此数据标签的格式。 |
| [equals(Object arg0)](#equals-java.lang.Object-) |  |
| [getClass()](#getClass--) |  |
| [getIndex()](#getIndex--) | 指定包含元素的索引。 |
| [getNumberFormat()](#getNumberFormat--) | 返回父元素的数字格式。 |
| [getSeparator()](#getSeparator--) | 获取用于图表上数据标签的字符串分隔符。 |
| [getShowBubbleSize()](#getShowBubbleSize--) | 允许指定是否要为图表上的数据标签显示气泡大小。 |
| [getShowCategoryName()](#getShowCategoryName--) | 允许指定是否要为图表上的数据标签显示类别名称。 |
| [getShowDataLabelsRange()](#getShowDataLabelsRange--) | 允许指定数据标签中的值是否显示在数据标签中。 |
| [getShowLeaderLines()](#getShowLeaderLines--) | 允许指定是否需要显示数据标签引导线。 |
| [getShowLegendKey()](#getShowLegendKey--) | 允许指定是否为图表上的数据标签显示图例键。 |
| [getShowPercentage()](#getShowPercentage--) | 允许指定是否要为图表上的数据标签显示百分比值。 |
| [getShowSeriesName()](#getShowSeriesName--) | 获取一个布尔值以指示图表上数据标签的系列名称显示行为。 |
| [getShowValue()](#getShowValue--) | 允许指定值是否要显示在数据标签中。 |
| [hashCode()](#hashCode--) |  |
| [isHidden()](#isHidden--) | 获取/设置一个标志，指示此标签是否隐藏。 |
| [isHidden(boolean value)](#isHidden-boolean-) | 获取/设置一个标志，指示此标签是否隐藏。 |
| [isInherited()](#isInherited--) |  |
| [isVisible()](#isVisible--) | 如果此数据标签有要显示的内容，则返回 true。 |
| [notify()](#notify--) |  |
| [notifyAll()](#notifyAll--) |  |
| [setSeparator(String value)](#setSeparator-java.lang.String-) | 设置用于图表上数据标签的字符串分隔符。 |
| [setShowBubbleSize(boolean value)](#setShowBubbleSize-boolean-) | 允许指定是否要为图表上的数据标签显示气泡大小。 |
| [setShowCategoryName(boolean value)](#setShowCategoryName-boolean-) | 允许指定是否要为图表上的数据标签显示类别名称。 |
| [setShowDataLabelsRange(boolean value)](#setShowDataLabelsRange-boolean-) | 允许指定数据标签中的值是否显示在数据标签中。 |
| [setShowLeaderLines(boolean value)](#setShowLeaderLines-boolean-) | 允许指定是否需要显示数据标签引导线。 |
| [setShowLegendKey(boolean value)](#setShowLegendKey-boolean-) | 允许指定是否为图表上的数据标签显示图例键。 |
| [setShowPercentage(boolean value)](#setShowPercentage-boolean-) | 允许指定是否要为图表上的数据标签显示百分比值。 |
| [setShowSeriesName(boolean value)](#setShowSeriesName-boolean-) | 设置一个布尔值以指示图表上数据标签的系列名称显示行为。 |
| [setShowValue(boolean value)](#setShowValue-boolean-) | 允许指定值是否要显示在数据标签中。 |
| [toString()](#toString--) |  |
| [wait()](#wait--) |  |
| [wait(long arg0)](#wait-long-) |  |
| [wait(long arg0, int arg1)](#wait-long-int-) |  |
### clearFormat() {#clearFormat--}
```
public void clearFormat()
```


清除此数据标签的格式。属性设置为父数据标签集合中定义的默认值。

### equals(Object arg0) {#equals-java.lang.Object-}
```
public boolean equals(Object arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | java.lang.Object |  |

**退货：**
布尔值
### getClass() {#getClass--}
```
public final native Class<?> getClass()
```




**退货：**
java.lang.Class<?>
### getIndex() {#getIndex--}
```
public int getIndex()
```


指定包含元素的索引。该索引应确定该元素适用于哪个父子集合。默认值为 0。

**退货：**
int - 相应的 int 值。
### getNumberFormat() {#getNumberFormat--}
```
public ChartNumberFormat getNumberFormat()
```


返回父元素的数字格式。

**退货：**
[ChartNumberFormat](../../com.aspose.words/chartnumberformat) - 父元素的数字格式。
### getSeparator() {#getSeparator--}
```
public String getSeparator()
```


获取用于图表上数据标签的字符串分隔符。默认为逗号，但仅显示类别名称和百分比的饼图除外，此时应使用换行符。

**退货：**
java.lang.String - 用于图表上数据标签的字符串分隔符。
### getShowBubbleSize() {#getShowBubbleSize--}
```
public boolean getShowBubbleSize()
```


允许指定是否要为图表上的数据标签显示气泡大小。仅适用于气泡图。默认值为假。

**退货：**
boolean - 相应的布尔值。
### getShowCategoryName() {#getShowCategoryName--}
```
public boolean getShowCategoryName()
```


允许指定是否要为图表上的数据标签显示类别名称。默认值为假。

**退货：**
boolean - 相应的布尔值。
### getShowDataLabelsRange() {#getShowDataLabelsRange--}
```
public boolean getShowDataLabelsRange()
```


允许指定数据标签中的值是否显示在数据标签中。默认值为假。

**退货：**
boolean - 相应的布尔值。
### getShowLeaderLines() {#getShowLeaderLines--}
```
public boolean getShowLeaderLines()
```


允许指定是否需要显示数据标签引导线。默认值为假。仅适用于饼图。引导线在数据标签和相应的数据点之间创建视觉连接。

**退货：**
boolean - 相应的布尔值。
### getShowLegendKey() {#getShowLegendKey--}
```
public boolean getShowLegendKey()
```


允许指定是否为图表上的数据标签显示图例键。默认值为假。

**退货：**
boolean - 相应的布尔值。
### getShowPercentage() {#getShowPercentage--}
```
public boolean getShowPercentage()
```


允许指定是否要为图表上的数据标签显示百分比值。默认值为假。

**退货：**
boolean - 相应的布尔值。
### getShowSeriesName() {#getShowSeriesName--}
```
public boolean getShowSeriesName()
```


获取一个布尔值以指示图表上数据标签的系列名称显示行为。 True 显示系列名称。假以掩饰。默认为假。

**退货：**
boolean - 一个布尔值，用于指示图表上数据标签的系列名称显示行为。
### getShowValue() {#getShowValue--}
```
public boolean getShowValue()
```


允许指定值是否要显示在数据标签中。默认值为假。

**退货：**
boolean - 相应的布尔值。
### hashCode() {#hashCode--}
```
public native int hashCode()
```




**退货：**
整数
### isHidden() {#isHidden--}
```
public boolean isHidden()
```


获取/设置一个标志，指示此标签是否隐藏。默认值为**false**.

**退货：**
boolean - 相应的布尔值。
### isHidden(boolean value) {#isHidden-boolean-}
```
public void isHidden(boolean value)
```


获取/设置一个标志，指示此标签是否隐藏。默认值为**false**.

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### isInherited() {#isInherited--}
```
public boolean isInherited()
```




**退货：**
布尔值
### isVisible() {#isVisible--}
```
public boolean isVisible()
```


如果此数据标签有要显示的内容，则返回 true。

**退货：**
boolean - 如果此数据标签有要显示的内容，则为 True。
### notify() {#notify--}
```
public final native void notify()
```




### notifyAll() {#notifyAll--}
```
public final native void notifyAll()
```




### setSeparator(String value) {#setSeparator-java.lang.String-}
```
public void setSeparator(String value)
```


设置用于图表上数据标签的字符串分隔符。默认为逗号，但仅显示类别名称和百分比的饼图除外，此时应使用换行符。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | java.lang.String | 用于图表上数据标签的字符串分隔符。 |

### setShowBubbleSize(boolean value) {#setShowBubbleSize-boolean-}
```
public void setShowBubbleSize(boolean value)
```


允许指定是否要为图表上的数据标签显示气泡大小。仅适用于气泡图。默认值为假。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setShowCategoryName(boolean value) {#setShowCategoryName-boolean-}
```
public void setShowCategoryName(boolean value)
```


允许指定是否要为图表上的数据标签显示类别名称。默认值为假。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setShowDataLabelsRange(boolean value) {#setShowDataLabelsRange-boolean-}
```
public void setShowDataLabelsRange(boolean value)
```


允许指定数据标签中的值是否显示在数据标签中。默认值为假。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setShowLeaderLines(boolean value) {#setShowLeaderLines-boolean-}
```
public void setShowLeaderLines(boolean value)
```


允许指定是否需要显示数据标签引导线。默认值为假。仅适用于饼图。引导线在数据标签和相应的数据点之间创建视觉连接。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setShowLegendKey(boolean value) {#setShowLegendKey-boolean-}
```
public void setShowLegendKey(boolean value)
```


允许指定是否为图表上的数据标签显示图例键。默认值为假。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setShowPercentage(boolean value) {#setShowPercentage-boolean-}
```
public void setShowPercentage(boolean value)
```


允许指定是否要为图表上的数据标签显示百分比值。默认值为假。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setShowSeriesName(boolean value) {#setShowSeriesName-boolean-}
```
public void setShowSeriesName(boolean value)
```


设置一个布尔值以指示图表上数据标签的系列名称显示行为。 True 显示系列名称。假以掩饰。默认为假。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 一个布尔值，用于指示图表上数据标签的系列名称显示行为。 |

### setShowValue(boolean value) {#setShowValue-boolean-}
```
public void setShowValue(boolean value)
```


允许指定值是否要显示在数据标签中。默认值为假。

**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### toString() {#toString--}
```
public String toString()
```




**退货：**
java.lang.字符串
### wait() {#wait--}
```
public final void wait()
```




### wait(long arg0) {#wait-long-}
```
public final native void wait(long arg0)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |

### wait(long arg0, int arg1) {#wait-long-int-}
```
public final void wait(long arg0, int arg1)
```




**参数：**

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| arg0 | long |  |
| arg1 | int |  |
