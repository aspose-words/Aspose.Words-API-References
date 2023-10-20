---
title: ChartXValue Class
linktitle: ChartXValue
articleTitle: ChartXValue
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Drawing.Charts.ChartXValue 班级. 表示图表系列的 X 值 在 C#.
type: docs
weight: 840
url: /zh/net/aspose.words.drawing.charts/chartxvalue/
---
## ChartXValue class

表示图表系列的 X 值。

```csharp
public class ChartXValue
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [DateTimeValue](../../aspose.words.drawing.charts/chartxvalue/datetimevalue/) { get; } | 获取存储的日期时间值。 |
| [DoubleValue](../../aspose.words.drawing.charts/chartxvalue/doublevalue/) { get; } | 获取存储的数值。 |
| [MultilevelValue](../../aspose.words.drawing.charts/chartxvalue/multilevelvalue/) { get; } | 获取存储的多级值。 |
| [StringValue](../../aspose.words.drawing.charts/chartxvalue/stringvalue/) { get; } | 获取存储的字符串值。 |
| [TimeValue](../../aspose.words.drawing.charts/chartxvalue/timevalue/) { get; } | 获取存储的时间值。 |
| [ValueType](../../aspose.words.drawing.charts/chartxvalue/valuetype/) { get; } | 获取存储在对象中的 X 值的类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| static [FromDateTime](../../aspose.words.drawing.charts/chartxvalue/fromdatetime/)(*DateTime*) | 创建一个`ChartXValue`的实例DateTime类型. |
| static [FromDouble](../../aspose.words.drawing.charts/chartxvalue/fromdouble/)(*double*) | 创建一个`ChartXValue`的实例Double类型. |
| static [FromMultilevelValue](../../aspose.words.drawing.charts/chartxvalue/frommultilevelvalue/)(*[ChartMultilevelValue](../chartmultilevelvalue/)*) | 创建一个`ChartXValue`的实例Multilevel类型. |
| static [FromString](../../aspose.words.drawing.charts/chartxvalue/fromstring/)(*string*) | 创建一个`ChartXValue`的实例String类型. |
| static [FromTimeSpan](../../aspose.words.drawing.charts/chartxvalue/fromtimespan/)(*TimeSpan*) | 创建一个`ChartXValue`的实例Time类型. |
| override [Equals](../../aspose.words.drawing.charts/chartxvalue/equals/)(*object*) | 获取一个标志，指示指定对象是否等于当前 X 值对象。 |
| override [GetHashCode](../../aspose.words.drawing.charts/chartxvalue/gethashcode/)() | 获取当前 X 值对象的哈希码。 |

## 评论

此类包含许多用于创建特定类型的 X 值的静态方法。 The [`ValueType`](./valuetype/)属性允许您确定现有 X 值的类型。

图表系列的所有非空 X 值必须相同[`ChartXValueType`](../chartxvaluetype/)类型。

### 也可以看看

* 命名空间 [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../)
