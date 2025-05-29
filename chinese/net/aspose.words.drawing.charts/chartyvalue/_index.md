---
title: ChartYValue Class
linktitle: ChartYValue
articleTitle: ChartYValue
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.Charts.ChartYValue 类，以便在图表系列中精确表示 Y 值，增强数据可视化。
type: docs
weight: 1190
url: /zh/net/aspose.words.drawing.charts/chartyvalue/
---
## ChartYValue class

表示图表系列的 Y 值。

```csharp
public class ChartYValue
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [DateTimeValue](../../aspose.words.drawing.charts/chartyvalue/datetimevalue/) { get; } | 获取存储的日期时间值。 |
| [DoubleValue](../../aspose.words.drawing.charts/chartyvalue/doublevalue/) { get; } | 获取存储的数值。 |
| [TimeValue](../../aspose.words.drawing.charts/chartyvalue/timevalue/) { get; } | 获取存储的时间值。 |
| [ValueType](../../aspose.words.drawing.charts/chartyvalue/valuetype/) { get; } | 获取对象中存储的 Y 值的类型。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| static [FromDateTime](../../aspose.words.drawing.charts/chartyvalue/fromdatetime/)(*DateTime*) | 创建一个`ChartYValue`的实例DateTime类型. |
| static [FromDouble](../../aspose.words.drawing.charts/chartyvalue/fromdouble/)(*double*) | 创建一个`ChartYValue`的实例Double类型. |
| static [FromTimeSpan](../../aspose.words.drawing.charts/chartyvalue/fromtimespan/)(*TimeSpan*) | 创建一个`ChartYValue`的实例Time类型. |
| override [Equals](../../aspose.words.drawing.charts/chartyvalue/equals/)(*object*) | 获取一个标志，指示指定对象是否等于当前 Y 值对象。 |
| override [GetHashCode](../../aspose.words.drawing.charts/chartyvalue/gethashcode/)() | 获取当前 Y 值对象的哈希码。 |

## 评论

此类包含许多用于创建特定类型的 Y 值的静态方法。[`ValueType`](./valuetype/)属性允许您确定现有 Y 值的类型。

图表系列的所有非空 Y 值必须相同[`ChartYValueType`](../chartyvaluetype/)类型。

### 也可以看看

* 命名空间 [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../)
