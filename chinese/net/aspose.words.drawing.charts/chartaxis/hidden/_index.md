---
title: ChartAxis.Hidden
second_title: Aspose.Words for .NET API 参考
description: ChartAxis 财产. 获取或设置一个标志指示该轴是否隐藏
type: docs
weight: 100
url: /zh/net/aspose.words.drawing.charts/chartaxis/hidden/
---
## ChartAxis.Hidden property

获取或设置一个标志，指示该轴是否隐藏。

```csharp
public bool Hidden { get; set; }
```

### 评论

默认值为`错误的`.

### 例子

展示如何隐藏图表轴。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;

// 清除图表的演示数据系列以从干净的图表开始。
chart.Series.Clear();

// 添加一个自定义系列，其中 X 轴为类别，Y 轴为相应的小数值。
chart.Series.Add("AW Series 1",
    new[] { "Item 1", "Item 2", "Item 3", "Item 4", "Item 5" },
    new[] { 1.2, 0.3, 2.1, 2.9, 4.2 });

 // 隐藏图表轴以简化图表的外观。
chart.AxisX.Hidden = true;
chart.AxisY.Hidden = true;

doc.Save(ArtifactsDir + "Charts.HideChartAxis.docx");
```

### 也可以看看

* class [ChartAxis](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../chartaxis/)
* 部件 [Aspose.Words](../../../)


