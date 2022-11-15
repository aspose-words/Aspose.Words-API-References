---
title: IChartDataPoint
second_title: Aspose.Words for Java API 参考
description: 包含图表上单个数据点的属性。
type: docs
weight: 633
url: /zh/java/com.aspose.words/ichartdatapoint/
---
```
public interface IChartDataPoint
```

包含图表上单个数据点的属性。
## 方法

| 方法 | 描述 |
| --- | --- |
| [getBubble3D()](#getBubble3D--) | 指定气泡图中的气泡是否应应用 3-D 效果。 |
| [getExplosion()](#getExplosion--) | 指定数据点应从饼图中心移动的量。 |
| [getInvertIfNegative()](#getInvertIfNegative--) | 指定如果值为负数，父元素是否应反转其颜色。 |
| [getMarker()](#getMarker--) | 指定数据标记。 |
| [setBubble3D(boolean value)](#setBubble3D-boolean-) | 指定气泡图中的气泡是否应应用 3-D 效果。 |
| [setExplosion(int value)](#setExplosion-int-) | 指定数据点应从饼图中心移动的量。 |
| [setInvertIfNegative(boolean value)](#setInvertIfNegative-boolean-) | 指定如果值为负数，父元素是否应反转其颜色。 |
### getBubble3D() {#getBubble3D--}
```
public abstract boolean getBubble3D()
```


指定气泡图中的气泡是否应应用 3-D 效果。

**退货:**
boolean - 对应的布尔值。
### getExplosion() {#getExplosion--}
```
public abstract int getExplosion()
```


指定数据点应从饼图中心移动的量。可以为负数，负数表示未设置属性且不应应用爆炸。仅适用于饼图。

**退货:**
int - 对应的 int 值。
### getInvertIfNegative() {#getInvertIfNegative--}
```
public abstract boolean getInvertIfNegative()
```


指定如果值为负数，父元素是否应反转其颜色。

**退货:**
boolean - 对应的布尔值。
### getMarker() {#getMarker--}
```
public abstract ChartMarker getMarker()
```


指定数据标记。请求时会自动创建标记。

**退货:**
[ChartMarker](../../com.aspose.words/chartmarker) - 相应的[ChartMarker](../../com.aspose.words/chartmarker)价值。
### setBubble3D(boolean value) {#setBubble3D-boolean-}
```
public abstract void setBubble3D(boolean value)
```


指定气泡图中的气泡是否应应用 3-D 效果。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |

### setExplosion(int value) {#setExplosion-int-}
```
public abstract void setExplosion(int value)
```


指定数据点应从饼图中心移动的量。可以为负数，负数表示未设置属性且不应应用爆炸。仅适用于饼图。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | int | 对应的 int 值。 |

### setInvertIfNegative(boolean value) {#setInvertIfNegative-boolean-}
```
public abstract void setInvertIfNegative(boolean value)
```


指定如果值为负数，父元素是否应反转其颜色。

**参数:**
| 范围 | 类型 | 描述 |
| --- | --- | --- |
| value | boolean | 对应的布尔值。 |
