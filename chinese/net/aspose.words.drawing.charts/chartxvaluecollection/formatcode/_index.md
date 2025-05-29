---
title: ChartXValueCollection.FormatCode
linktitle: FormatCode
articleTitle: FormatCode
second_title: Aspose.Words for .NET
description: 探索 ChartXValueCollection FormatCode 属性，轻松自定义 X 值格式，以增强图表中的数据可视化和清晰度。
type: docs
weight: 20
url: /zh/net/aspose.words.drawing.charts/chartxvaluecollection/formatcode/
---
## ChartXValueCollection.FormatCode property

获取或设置应用于 X 值的格式代码。

```csharp
public string FormatCode { get; set; }
```

## 评论

数字格式用于更改图表中数值的显示方式。 数字格式示例：

数字 - “#,##0.00”

货币 - "\"$\"#,##0.00"

时间 - “[$-x-systime]h:mm:ss AM/PM”

日期 - “d/mm/yyyy”

百分比 - “0.00%”

分数 - ”＃ ？/？”

科学的——“0.00E+00”

会计 - "_-\"$\"* #,##0.00_-;-\"$\"* #,##0.00_-;_-\"$\"* \"-\"??_-;_-@_-"

自定义颜色 - “[红色]-#,##0.0”

## 例子

展示如何使用图表数据的格式代码。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入气泡图。
Shape shape = builder.InsertChart(ChartType.Bubble, 432, 252);
Chart chart = shape.Chart;

// 删除默认生成的系列。
chart.Series.Clear();

ChartSeries series = chart.Series.Add(
    "Series1",
    new double[] { 1, 1.9, 2.45, 3 },
    new double[] { 1, -0.9, 1.82, 0 },
    new double[] { 2, 1.1, 2.95, 2 });

// 显示数据标签。
series.HasDataLabels = true;
series.DataLabels.ShowCategoryName = true;
series.DataLabels.ShowValue = true;
series.DataLabels.ShowBubbleSize = true;

// 设置数据格式代码。
series.XValues.FormatCode = "#,##0.0#";
series.YValues.FormatCode = "#,##0.0#;[Red]\\-#,##0.0#";
series.BubbleSizes.FormatCode = "#,##0.0#";

doc.Save(ArtifactsDir + "Charts.FormatCode.docx");
```

### 也可以看看

* class [ChartXValueCollection](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
