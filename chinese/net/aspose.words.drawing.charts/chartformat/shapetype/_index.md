---
title: ChartFormat.ShapeType
linktitle: ShapeType
articleTitle: ShapeType
second_title: 用于 .NET 的 Aspose.Words
description: ChartFormat ShapeType 财产. 获取或设置父图表元素的形状类型 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.drawing.charts/chartformat/shapetype/
---
## ChartFormat.ShapeType property

获取或设置父图表元素的形状类型。

```csharp
public ChartShapeType ShapeType { get; set; }
```

## 评论

目前，该属性只能用于数据标签。

## 例子

演示如何设置图表数据标签的填充、描边和标注格式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// 删除默认生成的系列。
chart.Series.Clear();

// 添加新系列。
ChartSeries series = chart.Series.Add("AW Series 1",
    new string[] { "AW Category 1", "AW Category 2", "AW Category 3", "AW Category 4" },
    new double[] { 100, 200, 300, 400 });

// 显示数据标签。
series.HasDataLabels = true;
series.DataLabels.ShowValue = true;

// 将数据标签格式化为标注。
ChartFormat format = series.DataLabels.Format;
format.ShapeType = ChartShapeType.WedgeRectCallout;
format.Stroke.Color = Color.DarkGreen;
format.Fill.Solid(Color.Green);
series.DataLabels.Font.Color = Color.Yellow;

// 更改单个数据标签的填充和描边。
ChartFormat labelFormat = series.DataLabels[0].Format;
labelFormat.Stroke.Color = Color.DarkBlue;
labelFormat.Fill.Solid(Color.Blue);

doc.Save(ArtifactsDir + "Charts.FormatDataLables.docx");
```

### 也可以看看

* enum [ChartShapeType](../../chartshapetype/)
* class [ChartFormat](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
