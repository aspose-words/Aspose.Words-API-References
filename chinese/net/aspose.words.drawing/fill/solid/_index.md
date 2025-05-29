---
title: Fill.Solid
linktitle: Solid
articleTitle: Solid
second_title: Aspose.Words for .NET
description: 探索填充实心方法，实现一致的颜色填充，轻松增强设计的视觉吸引力和统一性。
type: docs
weight: 260
url: /zh/net/aspose.words.drawing/fill/solid/
---
## Solid() {#solid}

将填充设置为统一颜色。

```csharp
public void Solid()
```

## 评论

使用此方法将任何填充转换回实心填充。

## 例子

展示如何将任何填充转换回实心填充。

```csharp
Document doc = new Document(MyDir + "Two color gradient.docx");

// 获取第一个 Run 的 Font 的 Fill 对象。
Fill fill = doc.FirstSection.Body.Paragraphs[0].Runs[0].Font.Fill;

// 检查字体的填充属性。
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill is transparent at {0}%", fill.Transparency * 100);

// 将填充类型更改为均匀的绿色实心。
fill.Solid();
Console.WriteLine("\nThe fill is changed:");
Console.WriteLine("The type of the fill is: {0}", fill.FillType);
Console.WriteLine("The foreground color of the fill is: {0}", fill.ForeColor);
Console.WriteLine("The fill transparency is {0}%", fill.Transparency * 100);

doc.Save(ArtifactsDir + "Drawing.FillSolid.docx");
```

### 也可以看看

* class [Fill](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)

---

## Solid(*Color*) {#solid_1}

将填充设置为指定的统一颜色。

```csharp
public void Solid(Color color)
```

## 评论

使用此方法将任何填充转换回实心填充。

## 例子

展示如何使用图表格式。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;

// 删除默认生成的系列。
ChartSeriesCollection series = chart.Series;
series.Clear();

string[] categories = new string[] { "Category 1", "Category 2" };
series.Add("Series 1", categories, new double[] { 1, 2 });
series.Add("Series 2", categories, new double[] { 3, 4 });

// 格式化图表背景。
chart.Format.Fill.Solid(Color.DarkSlateGray);

// 隐藏轴刻度标签。
chart.AxisX.TickLabels.Position = AxisTickLabelPosition.None;
chart.AxisY.TickLabels.Position = AxisTickLabelPosition.None;

// 格式化图表标题。
chart.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

// 格式化轴标题。
chart.AxisX.Title.Show = true;
chart.AxisX.Title.Format.Fill.Solid(Color.LightGoldenrodYellow);

// 格式化图例。
chart.Legend.Format.Fill.Solid(Color.LightGoldenrodYellow);

doc.Save(ArtifactsDir + "Charts.ChartFormat.docx");
```

### 也可以看看

* class [Fill](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
