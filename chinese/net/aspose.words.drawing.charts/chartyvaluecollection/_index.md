---
title: ChartYValueCollection Class
linktitle: ChartYValueCollection
articleTitle: ChartYValueCollection
second_title: 用于 .NET 的 Aspose.Words
description: Aspose.Words.Drawing.Charts.ChartYValueCollection 班级. 表示图表系列的 Y 值集合 在 C#.
type: docs
weight: 880
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
| [Item](../../aspose.words.drawing.charts/chartyvaluecollection/item/) { get; set; } | 获取或设置指定索引处的 Y 值。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| [GetEnumerator](../../aspose.words.drawing.charts/chartyvaluecollection/getenumerator/)() | 返回一个枚举器对象。 |

## 评论

除以下以外的所有收藏品**无效的**必须有相同的[`ValueType`](../chartyvalue/valuetype/)。

该集合仅允许更改 Y 值。要向图表系列添加或插入新值，或删除值， 的相应方法[`ChartSeries`](../chartseries/)可以使用类。

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

// 更改最大值和最小值的颜色。
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
