---
title: AxisGroup Enum
linktitle: AxisGroup
articleTitle: AxisGroup
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.Charts.AxisGroup 枚举，这是有效管理图表轴组以增强数据可视化的关键。
type: docs
weight: 800
url: /zh/net/aspose.words.drawing.charts/axisgroup/
---
## AxisGroup enumeration

表示图表轴组的类型。

```csharp
public enum AxisGroup
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Primary | `0` | 指定主轴组。 |
| Secondary | `1` | 指定次轴组。 |

## 例子

展示如何使用图表的次轴。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 450, 250);
Chart chart = shape.Chart;
ChartSeriesCollection series = chart.Series;

// 删除默认生成的系列。
series.Clear();

string[] categories = new string[] { "Category 1", "Category 2", "Category 3" };
series.Add("Series 1 of primary series group", categories, new double[] { 2, 3, 4 });
series.Add("Series 2 of primary series group", categories, new double[] { 5, 2, 3 });

// 创建一个额外的系列组，也是线类型。
ChartSeriesGroup newSeriesGroup = chart.SeriesGroups.Add(ChartSeriesType.Line);
// 指定新系列组使用次坐标轴。
newSeriesGroup.AxisGroup = AxisGroup.Secondary;
// 隐藏次要 X 轴。
newSeriesGroup.AxisX.Hidden = true;
// 定义次要 Y 轴的标题。
newSeriesGroup.AxisY.Title.Show = true;
newSeriesGroup.AxisY.Title.Text = "Secondary Y axis";

Assert.AreEqual(ChartSeriesType.Line, newSeriesGroup.SeriesType);

// 将系列添加到新的系列组。
ChartSeries series3 =
    newSeriesGroup.Series.Add("Series of secondary series group", categories, new double[] { 13, 11, 16 });
series3.Format.Stroke.Weight = 3.5;

doc.Save(ArtifactsDir + "Charts.SecondaryAxis.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../)
