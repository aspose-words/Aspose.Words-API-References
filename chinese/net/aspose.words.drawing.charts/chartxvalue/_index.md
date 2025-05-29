---
title: ChartXValue Class
linktitle: ChartXValue
articleTitle: ChartXValue
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.Charts.ChartXValue 类，这是定义图表系列中的 X 值的解决方案，可轻松增强数据可视化。
type: docs
weight: 1160
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
| [ValueType](../../aspose.words.drawing.charts/chartxvalue/valuetype/) { get; } | 获取对象中存储的 X 值的类型。 |

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

此类包含许多用于创建特定类型的 X 值的静态方法。[`ValueType`](./valuetype/)属性允许您确定现有 X 值的类型。

图表系列的所有非空 X 值必须相同[`ChartXValueType`](../chartxvaluetype/)类型。

## 例子

展示如何用数据填充图表系列。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// 清除第一个系列的 X 和 Y 值。
series1.ClearValues();

// 用数据填充系列。
series1.Add(ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);
series1.Add(ChartXValue.FromDouble(5), ChartYValue.FromDouble(5));
series1.Add(ChartXValue.FromDouble(7), ChartYValue.FromDouble(11));
series1.Add(ChartXValue.FromDouble(9));

ChartSeries series2 = chart.Series[1];
// 清除第二个系列的 X 和 Y 值。
series2.Clear();

// 用数据填充系列。
series2.Add(ChartXValue.FromDouble(2), ChartYValue.FromDouble(4));
series2.Add(ChartXValue.FromDouble(4), ChartYValue.FromDouble(7));
series2.Add(ChartXValue.FromDouble(6), ChartYValue.FromDouble(14));
series2.Add(ChartXValue.FromDouble(8), ChartYValue.FromDouble(7));

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../)
