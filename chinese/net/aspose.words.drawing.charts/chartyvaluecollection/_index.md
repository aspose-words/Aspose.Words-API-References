---
title: ChartYValueCollection Class
linktitle: ChartYValueCollection
articleTitle: ChartYValueCollection
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.Charts.ChartYValueCollection 类，这是高效管理图表系列中 Y 值的首选解决方案。
type: docs
weight: 1200
url: /zh/net/aspose.words.drawing.charts/chartyvaluecollection/
---
## ChartYValueCollection class

表示图表系列的 Y 值集合。

```csharp
public class ChartYValueCollection : IEnumerable<ChartYValue>
```

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Count](../../aspose.words.drawing.charts/chartyvaluecollection/count/) { get; } | 获取此集合中的项目数。 |
| [FormatCode](../../aspose.words.drawing.charts/chartyvaluecollection/formatcode/) { get; set; } | 获取或设置应用于 Y 值的格式代码。 |
| [Item](../../aspose.words.drawing.charts/chartyvaluecollection/item/) { get; set; } | 获取或设置指定索引处的 Y 值。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartyvaluecollection/getenumerator/)() | 返回一个枚举器对象。 |

## 评论

除以下物品外的所有藏品**无效的**必须有相同的[`ValueType`](../chartyvalue/valuetype/)。

该集合仅允许更改 Y 值。要向图表系列添加或插入新值，或者删除值，请使用[`ChartSeries`](../chartseries/)可以使用类。

## 例子

展示如何获取图表系列数据。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder();

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
Chart chart = shape.Chart;
ChartSeries series = chart.Series[0];

double minValue = double.MaxValue;
int minValueIndex = 0;
double maxValue = double.MinValue;
int maxValueIndex = 0;

for (int i = 0; i < series.YValues.Count; i++)
{
    // 清除所有数据点的单独格式。
    // 柱形图中数据点和数据值是一一对应的。
    series.DataPoints[i].ClearFormat();

    // 获取 Y 值。
    double yValue = series.YValues[i].DoubleValue;

    if (yValue < minValue)
    {
        minValue = yValue;
        minValueIndex = i;
    }

    if (yValue > maxValue)
    {
        maxValue = yValue;
        maxValueIndex = i;
    }
}

// 改变最大值和最小值的颜色。
series.DataPoints[minValueIndex].Format.Fill.ForeColor = Color.Red;
series.DataPoints[maxValueIndex].Format.Fill.ForeColor = Color.Green;

doc.Save(ArtifactsDir + "Charts.GetChartSeriesData.docx");
```

### 也可以看看

* method [Add](../chartseries/add/)
* method [Add](../chartseries/add/)
* method [Add](../chartseries/add/)
* method [Insert](../chartseries/insert/)
* method [Insert](../chartseries/insert/)
* method [Insert](../chartseries/insert/)
* method [Remove](../chartseries/remove/)
* class [ChartYValue](../chartyvalue/)
* 命名空间 [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../)
