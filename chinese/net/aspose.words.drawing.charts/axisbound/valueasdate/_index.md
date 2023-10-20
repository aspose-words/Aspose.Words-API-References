---
title: AxisBound.ValueAsDate
linktitle: ValueAsDate
articleTitle: ValueAsDate
second_title: 用于 .NET 的 Aspose.Words
description: AxisBound ValueAsDate 财产. 返回表示为日期时间的轴边界值 在 C#.
type: docs
weight: 40
url: /zh/net/aspose.words.drawing.charts/axisbound/valueasdate/
---
## AxisBound.ValueAsDate property

返回表示为日期时间的轴边界值。

```csharp
public DateTime ValueAsDate { get; }
```

## 例子

展示如何设置自定义轴边界。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape chartShape = builder.InsertChart(ChartType.Scatter, 450, 300);
Chart chart = chartShape.Chart;

// 清除图表的演示数据系列以从干净的图表开始。
chart.Series.Clear();

// 添加具有两个十进制数组的系列。第一个数组包含 X 值，
// 第二个包含散点图中点的相应 Y 值。
chart.Series.Add("Series 1", 
    new[] { 1.1, 5.4, 7.9, 3.5, 2.1, 9.7 }, 
    new[] { 2.1, 0.3, 0.6, 3.3, 1.4, 1.9 });

// 默认情况下，默认缩放应用于图形的 X 轴和 Y 轴，
// 这样它们的范围就足够大以包含每个系列的每个 X 和 Y 值。
Assert.True(chart.AxisX.Scaling.Minimum.IsAuto);

// 我们可以定义自己的轴边界。
// 在本例中，我们将使 X 轴和 Y 轴标尺都显示 0 到 10 的范围。
chart.AxisX.Scaling.Minimum = new AxisBound(0);
chart.AxisX.Scaling.Maximum = new AxisBound(10);
chart.AxisY.Scaling.Minimum = new AxisBound(0);
chart.AxisY.Scaling.Maximum = new AxisBound(10);

Assert.False(chart.AxisX.Scaling.Minimum.IsAuto);
Assert.False(chart.AxisY.Scaling.Minimum.IsAuto);

// 创建一个折线图，其中的系列需要 X 轴上的日期范围和 Y 轴上的小数值。
chartShape = builder.InsertChart(ChartType.Line, 450, 300);
chart = chartShape.Chart;
chart.Series.Clear();

DateTime[] dates = { new DateTime(1973, 5, 11),
    new DateTime(1981, 2, 4),
    new DateTime(1985, 9, 23),
    new DateTime(1989, 6, 28),
    new DateTime(1994, 12, 15)
};

chart.Series.Add("Series 1", dates, new[] { 3.0, 4.7, 5.9, 7.1, 8.9 });

// 我们也可以以日期的形式设置轴边界，将图表限制为一个周期。
// 将范围设置为 1980-1990 将忽略系列值中的两个
// 超出了图表的范围。
chart.AxisX.Scaling.Minimum = new AxisBound(new DateTime(1980, 1, 1));
chart.AxisX.Scaling.Maximum = new AxisBound(new DateTime(1990, 1, 1));

doc.Save(ArtifactsDir + "Charts.AxisBound.docx");
```

### 也可以看看

* class [AxisBound](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
