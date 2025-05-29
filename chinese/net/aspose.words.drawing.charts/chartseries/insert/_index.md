---
title: ChartSeries.Insert
linktitle: Insert
articleTitle: Insert
second_title: Aspose.Words for .NET
description: 使用 ChartSeries 的 Insert 方法轻松增强您的图表。在任意索引处插入 X 值，轻松优化您的数据可视化！
type: docs
weight: 200
url: /zh/net/aspose.words.drawing.charts/chartseries/insert/
---
## Insert(*int, [ChartXValue](../../chartxvalue/)*) {#insert}

将指定的 X 值插入图表系列的指定索引处。如果该系列支持 Y 值和气泡大小，则 X 值将为空。

```csharp
public void Insert(int index, ChartXValue xValue)
```

## 评论

相应的数据点将以默认格式插入到数据点集合中。并且， 如果显示数据标签，则相应的数据标签也将以默认格式插入。

## 例子

展示如何将数据插入图表系列。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// 清除第一个系列的 X 和 Y 值。
series1.ClearValues();
// 用数据填充系列。
series1.Insert(0, ChartXValue.FromDouble(3));
series1.Insert(1, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(2, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(3, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### 也可以看看

* class [ChartXValue](../../chartxvalue/)
* class [ChartSeries](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)

---

## Insert(*int, [ChartXValue](../../chartxvalue/), [ChartYValue](../../chartyvalue/)*) {#insert_1}

将指定的 X 和 Y 值插入到指定索引处的图表系列中。

```csharp
public void Insert(int index, ChartXValue xValue, ChartYValue yValue)
```

## 评论

相应的数据点将以默认格式插入到数据点集合中。并且， 如果显示数据标签，则相应的数据标签也将以默认格式插入。

## 例子

展示如何将数据插入图表系列。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// 清除第一个系列的 X 和 Y 值。
series1.ClearValues();
// 用数据填充系列。
series1.Insert(0, ChartXValue.FromDouble(3));
series1.Insert(1, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(2, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(3, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### 也可以看看

* class [ChartXValue](../../chartxvalue/)
* class [ChartYValue](../../chartyvalue/)
* class [ChartSeries](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)

---

## Insert(*int, [ChartXValue](../../chartxvalue/), [ChartYValue](../../chartyvalue/), double*) {#insert_2}

将指定的 X 值、Y 值和气泡大小插入到指定索引处的图表系列中。

```csharp
public void Insert(int index, ChartXValue xValue, ChartYValue yValue, double bubbleSize)
```

## 评论

相应的数据点将以默认格式插入到数据点集合中。并且， 如果显示数据标签，则相应的数据标签也将以默认格式插入。

## 例子

展示如何将数据插入图表系列。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 432, 252);
Chart chart = shape.Chart;
ChartSeries series1 = chart.Series[0];

// 清除第一个系列的 X 和 Y 值。
series1.ClearValues();
// 用数据填充系列。
series1.Insert(0, ChartXValue.FromDouble(3));
series1.Insert(1, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(2, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10));
series1.Insert(3, ChartXValue.FromDouble(3), ChartYValue.FromDouble(10), 10);

doc.Save(ArtifactsDir + "Charts.PopulateChartWithData.docx");
```

### 也可以看看

* class [ChartXValue](../../chartxvalue/)
* class [ChartYValue](../../chartyvalue/)
* class [ChartSeries](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
