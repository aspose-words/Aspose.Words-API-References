---
title: AxisBound Class
linktitle: AxisBound
articleTitle: AxisBound
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Drawing.Charts.AxisBound 班级. 表示轴值的最小或最大界限 在 C#.
type: docs
weight: 510
url: /zh/net/aspose.words.drawing.charts/axisbound/
---
## AxisBound class

表示轴值的最小或最大界限。

要了解更多信息，请访问[使用图表](https://docs.aspose.com/words/net/working-with-charts/)文档文章。

```csharp
public sealed class AxisBound
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [AxisBound](axisbound/#constructor)() | 创建一个新实例，指示轴边界应由字处理 应用程序自动确定。 |
| [AxisBound](axisbound/#constructor_2)(*DateTime*) | 创建表示为日期时间值的轴边界。 |
| [AxisBound](axisbound/#constructor_1)(*double*) | 创建一个以数字表示的轴边界。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [IsAuto](../../aspose.words.drawing.charts/axisbound/isauto/) { get; } | 返回一个标志，指示应自动确定轴边界。 |
| [Value](../../aspose.words.drawing.charts/axisbound/value/) { get; } | 返回轴边界的数值。 |
| [ValueAsDate](../../aspose.words.drawing.charts/axisbound/valueasdate/) { get; } | 返回表示为日期时间的轴边界值。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Equals](../../aspose.words.drawing.charts/axisbound/equals/)(*object*) | 确定指定对象的值是否等于当前对象。 |
| override [GetHashCode](../../aspose.words.drawing.charts/axisbound/gethashcode/)() | 用作该类型的哈希函数。 |
| override [ToString](../../aspose.words.drawing.charts/axisbound/tostring/)() | 返回一个用户友好的字符串，显示该对象的值。 |

## 评论

绑定可以指定为数字、日期时间或特殊的“自动”值。

该类的实例是不可变的。

## 例子

演示如何插入带有日期/时间值的图表。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;

// 清除图表的演示数据系列以从干净的图表开始。
chart.Series.Clear();

// 添加一个自定义系列，其中包含 X 轴的日期/时间值以及 Y 轴的相应小数值。
chart.Series.Add("Aspose Test Series",
    new[]
    {
        new DateTime(2017, 11, 06), new DateTime(2017, 11, 09), new DateTime(2017, 11, 15),
        new DateTime(2017, 11, 21), new DateTime(2017, 11, 25), new DateTime(2017, 11, 29)
    },
    new[] { 1.2, 0.3, 2.1, 2.9, 4.2, 5.3 });

// 设置 X 轴的下限和上限。
ChartAxis xAxis = chart.AxisX;
xAxis.Scaling.Minimum = new AxisBound(new DateTime(2017, 11, 05).ToOADate());
xAxis.Scaling.Maximum = new AxisBound(new DateTime(2017, 12, 03));

// 将X轴的主要单位设置为周，次要单位设置为天。
xAxis.BaseTimeUnit = AxisTimeUnit.Days;
xAxis.MajorUnit = 7.0d;
xAxis.MajorTickMark = AxisTickMark.Cross;
xAxis.MinorUnit = 1.0d;
xAxis.MinorTickMark = AxisTickMark.Outside;
xAxis.HasMajorGridlines = true;
xAxis.HasMinorGridlines = true;

// 定义小数值的 Y 轴属性。
ChartAxis yAxis = chart.AxisY;
yAxis.TickLabelPosition = AxisTickLabelPosition.High;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 50.0d;
yAxis.DisplayUnit.Unit = AxisBuiltInUnit.Hundreds;
yAxis.Scaling.Minimum = new AxisBound(100);
yAxis.Scaling.Maximum = new AxisBound(700);
yAxis.HasMajorGridlines = true;
yAxis.HasMinorGridlines = true;

doc.Save(ArtifactsDir + "Charts.DateTimeValues.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../)
