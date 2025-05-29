---
title: ChartDataLabelPosition Enum
linktitle: ChartDataLabelPosition
articleTitle: ChartDataLabelPosition
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.ChartDataLabelPosition 枚举，轻松自定义图表数据标签，以增强清晰度和呈现效果。
type: docs
weight: 960
url: /zh/net/aspose.words.drawing.charts/chartdatalabelposition/
---
## ChartDataLabelPosition enumeration

指定图表数据标签的位置。

```csharp
public enum ChartDataLabelPosition
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Center | `0` | 指定数据标签应显示在数据标记的中心。 |
| Left | `1` | 指定数据标签应显示在数据标记的左侧。 |
| Right | `2` | 指定数据标签应显示在数据标记的右侧。 |
| Above | `3` | 指定数据标签应显示在数据标记上方。 |
| Below | `4` | 指定数据标签应显示在数据标记下方。 |
| InsideBase | `5` | 指定数据标签应显示在数据标记的底部。 |
| InsideEnd | `6` | 指定数据标签应显示在数据标记的末尾。 |
| OutsideEnd | `7` | 指定数据标签应显示在数据标记的末尾之外。 |
| BestFit | `8` | 指定数据标签应显示在最合适的位置。 |

## 评论

并非所有系列类型都允许指定标签位置。即使允许，也并非所有值都支持。

## 例子

显示如何设置数据标签的位置。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入柱状图。
Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;

// 删除默认生成的系列。
seriesColl.Clear();

// 添加系列。
ChartSeries series = seriesColl.Add(
    "Series 1",
    new string[] { "Category 1", "Category 2", "Category 3" },
    new double[] { 4, 5, 6 });

// 显示数据标签并设置字体颜色。
series.HasDataLabels = true;
ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowValue = true;
dataLabels.Font.Color = Color.White;

// 设置数据标签位置。
dataLabels.Position = ChartDataLabelPosition.InsideBase;
dataLabels[0].Position = ChartDataLabelPosition.OutsideEnd;
dataLabels[0].Font.Color = Color.DarkRed;

doc.Save(ArtifactsDir + "Charts.LabelPosition.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../)
