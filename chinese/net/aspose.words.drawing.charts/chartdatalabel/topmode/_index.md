---
title: ChartDataLabel.TopMode
linktitle: TopMode
articleTitle: TopMode
second_title: Aspose.Words for .NET
description: 探索 ChartDataLabel TopMode 属性，自定义图表上数据标签的位置。提升可视化数据呈现的清晰度和精准度！
type: docs
weight: 220
url: /zh/net/aspose.words.drawing.charts/chartdatalabel/topmode/
---
## ChartDataLabel.TopMode property

获取或设置[`Top`](../top/)属性值：是否设置数据标签的 location 距离图表顶部边缘或距离其指定的位置[`Position`](../position/) 属性.

```csharp
public ChartDataLabelLocationMode TopMode { get; set; }
```

## 评论

无法在 Word 2016 图表中设置该属性。

## 例子

展示如何将圆环图的数据标签放置在圆环图外面。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

const int chartWidth = 432;
const int chartHeight = 252;
Shape shape = builder.InsertChart(ChartType.Doughnut, chartWidth, chartHeight);
Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
// 删除默认生成的系列。
seriesColl.Clear();

// 隐藏图例。
chart.Legend.Position = LegendPosition.None;

// 生成数据。
const int dataLength = 20;
double totalValue = 0;
string[] categories = new string[dataLength];
double[] values = new double[dataLength];

for (int i = 0; i < dataLength; i++)
{
    categories[i] = $"Category {i}";
    values[i] = dataLength - i;
    totalValue = totalValue + values[i];
}

ChartSeries series = seriesColl.Add("Series 1", categories, values);
series.HasDataLabels = true;

ChartDataLabelCollection dataLabels = series.DataLabels;
dataLabels.ShowValue = true;
dataLabels.ShowLeaderLines = true;

// Position 属性不适用于圆环图。让我们使用 Left 和 Top 属性来放置数据标签
// 图表甜甜圈外面圆圈周围的属性。
// 原点位于图表的左上角。

const double titleAreaHeight = 25.5; // 这可以使用标题文本和字体来计算。
const double doughnutCenterY = titleAreaHeight + (chartHeight - titleAreaHeight) / 2;
const double doughnutCenterX = chartWidth / 2d;
const double labelHeight = 16.5; // 这可以使用标签字体来计算。
const double oneCharLabelWidth = 12.75; // 可以使用每个标签的文本和字体来计算。
const double twoCharLabelWidth = 17.25; // 可以使用每个标签的文本和字体来计算。
const double yMargin = 0.75;
const double labelMargin = 1.5;
const double labelCircleRadius = chartHeight - doughnutCenterY - yMargin - labelHeight / 2;

// 因为数据点从顶部开始，所以 Left 和 Top 属性中使用的 X 坐标
// 数据标签指向右侧，Y 坐标指向下方，起始角度为 -PI/2。
double totalAngle = -System.Math.PI / 2;
ChartDataLabel previousLabel = null;

for (int i = 0; i < series.YValues.Count; i++)
{
    ChartDataLabel dataLabel = dataLabels[i];

    double value = series.YValues[i].DoubleValue;
    double labelWidth;
    if (value < 10)
        labelWidth = oneCharLabelWidth;
    else
        labelWidth = twoCharLabelWidth;
    double labelSegmentAngle = value / totalValue * 2 * System.Math.PI;
    double labelAngle = labelSegmentAngle / 2 + totalAngle;
    double labelCenterX = labelCircleRadius * System.Math.Cos(labelAngle) + doughnutCenterX;
    double labelCenterY = labelCircleRadius * System.Math.Sin(labelAngle) + doughnutCenterY;
    double labelLeft = labelCenterX - labelWidth / 2;
    double labelTop = labelCenterY - labelHeight / 2;

    // 如果当前数据标签与其他标签重叠，则水平移动它。
    if ((previousLabel != null) &&
        (System.Math.Abs(previousLabel.Top - labelTop) < labelHeight) &&
        (System.Math.Abs(previousLabel.Left - labelLeft) < labelWidth))
    {
        // 在顶部向右移动，在底部向左移动。
        bool isOnTop = (totalAngle < 0) || (totalAngle >= System.Math.PI);
        int factor;
        if (isOnTop)
            factor = 1;
        else
            factor = -1;

        labelLeft = previousLabel.Left + labelWidth * factor + labelMargin;
    }

    dataLabel.Left = labelLeft;
    dataLabel.LeftMode = ChartDataLabelLocationMode.Absolute;
    dataLabel.Top = labelTop;
    dataLabel.TopMode = ChartDataLabelLocationMode.Absolute;

    totalAngle = totalAngle + labelSegmentAngle;
    previousLabel = dataLabel;
}

doc.Save(ArtifactsDir + "Charts.DoughnutChartLabelPosition.docx");
```

### 也可以看看

* enum [ChartDataLabelLocationMode](../../chartdatalabellocationmode/)
* class [ChartDataLabel](../)
* 命名空间 [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../../)
