---
title: Enum AxisTimeUnit
second_title: Aspose.Words for .NET API 参考
description: Aspose.Words.Drawing.Charts.AxisTimeUnit 枚举. 指定坐标轴的时间单位
type: docs
weight: 590
url: /zh/net/aspose.words.drawing.charts/axistimeunit/
---
## AxisTimeUnit enumeration

指定坐标轴的时间单位。

```csharp
public enum AxisTimeUnit
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Automatic | `0` | 指定未明确设置单位，应使用默认值。 |
| Days | `1` | 指定图表数据应以天为单位显示。 |
| Months | `2` | 指定图表数据应以月显示。 |
| Years | `3` | 指定图表数据应以年显示。 |

### 例子

显示如何插入带有日期/时间值的图表。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;

// 清除图表的演示数据系列以从干净的图表开始。
chart.Series.Clear();

// 添加一个自定义系列，其中包含 X 轴的日期/时间值和 Y 轴的相应十进制值。
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

// 设置 X 轴的主要单位为周，次要单位为天。
xAxis.BaseTimeUnit = AxisTimeUnit.Days;
xAxis.MajorUnit = 7.0d;
xAxis.MajorTickMark = AxisTickMark.Cross;
xAxis.MinorUnit = 1.0d;
xAxis.MinorTickMark = AxisTickMark.Outside;

// 定义十进制值的 Y 轴属性。
ChartAxis yAxis = chart.AxisY;
yAxis.TickLabelPosition = AxisTickLabelPosition.High;
yAxis.MajorUnit = 100.0d;
yAxis.MinorUnit = 50.0d;
yAxis.DisplayUnit.Unit = AxisBuiltInUnit.Hundreds;
yAxis.Scaling.Minimum = new AxisBound(100);
yAxis.Scaling.Maximum = new AxisBound(700);

doc.Save(ArtifactsDir + "Charts.DateTimeValues.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../)


