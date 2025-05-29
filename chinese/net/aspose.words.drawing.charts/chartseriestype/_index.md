---
title: ChartSeriesType Enum
linktitle: ChartSeriesType
articleTitle: ChartSeriesType
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Drawing.Charts.ChartSeriesType 枚举，使用多种动态数据可视化选项增强您的图表系列。
type: docs
weight: 1110
url: /zh/net/aspose.words.drawing.charts/chartseriestype/
---
## ChartSeriesType enumeration

指定图表系列的类型。

```csharp
public enum ChartSeriesType
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Area | `0` | 表示面积图系列。 |
| AreaStacked | `1` | 表示堆积面积图系列。 |
| AreaPercentStacked | `2` | 表示 100% 堆积面积图系列。 |
| Area3D | `3` | 表示 3D 面积图系列。 |
| Area3DStacked | `4` | 表示 3D 堆积面积图系列。 |
| Area3DPercentStacked | `5` | 表示 3D 100% 堆积面积图系列。 |
| Bar | `6` | 表示条形图系列。 |
| BarStacked | `7` | 表示堆积条形图系列。 |
| BarPercentStacked | `8` | 表示 100% 堆积条形图系列。 |
| Bar3D | `9` | 表示 3D 条形图系列。 |
| Bar3DStacked | `10` | 表示 3D 堆积条形图系列。 |
| Bar3DPercentStacked | `11` | 表示 3D 100% 堆积条形图系列。 |
| Bubble | `12` | 表示气泡图系列。 |
| Bubble3D | `13` | 表示 3D 气泡图系列。 |
| Column | `14` | 表示柱形图系列。 |
| ColumnStacked | `15` | 表示堆积柱形图系列。 |
| ColumnPercentStacked | `16` | 表示 100% 堆积柱形图系列。 |
| Column3D | `17` | 表示 3D 柱形图系列。 |
| Column3DStacked | `18` | 表示 3D 堆积柱形图系列。 |
| Column3DPercentStacked | `19` | 表示 3D 100% 堆积柱形图系列。 |
| Column3DClustered | `20` | 表示 3D 簇状柱形图系列。 |
| Doughnut | `21` | 表示甜甜圈图系列。 |
| Line | `22` | 表示折线图系列。 |
| LineStacked | `23` | 表示堆积折线图系列。 |
| LinePercentStacked | `24` | 表示 100% 堆积折线图系列。 |
| Line3D | `25` | 表示 3D 折线图系列。 |
| Pie | `26` | 表示饼图系列。 |
| Pie3D | `27` | 表示 3D 饼图系列。 |
| PieOfBar | `28` | 表示饼图或条形图系列。 |
| PieOfPie | `29` | 表示饼图中的饼图系列。 |
| Radar | `30` | 代表雷达图系列。 |
| Scatter | `31` | 表示散点图系列。 |
| Stock | `32` | 代表股票图表系列。 |
| Surface | `33` | 表示曲面图系列。 |
| Surface3D | `34` | 表示 3D 曲面图表系列。 |
| Treemap | `35` | 表示树状图系列。 |
| Sunburst | `36` | 代表旭日图表系列。 |
| Histogram | `37` | 表示直方图系列。 |
| Pareto | `38` | 表示帕累托图系列。 |
| ParetoLine | `39` | 表示帕累托线图系列。 |
| BoxAndWhisker | `40` | 代表箱线图系列。 |
| Waterfall | `41` | 表示瀑布图系列。 |
| Funnel | `42` | 表示漏斗图系列。 |
| RegionMap | `43` | 代表区域地图图表系列。 |

## 例子

显示如何删除特定图表系列。

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

// 删除所有列类型的系列。
for (int i = chart.Series.Count - 1; i >= 0; i--)
{
    if (chart.Series[i].SeriesType == ChartSeriesType.Column)
        chart.Series.RemoveAt(i);
}

chart.Series.Add(
    "Aspose Series",
    new string[] { "Category 1", "Category 2", "Category 3", "Category 4" },
    new double[] { 5.6, 7.1, 2.9, 8.9 });

doc.Save(ArtifactsDir + "Charts.RemoveSpecificChartSeries.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../)
