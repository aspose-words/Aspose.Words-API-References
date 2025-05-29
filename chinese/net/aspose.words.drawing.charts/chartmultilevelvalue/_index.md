---
title: ChartMultilevelValue Class
linktitle: ChartMultilevelValue
articleTitle: ChartMultilevelValue
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.ChartMultilevelValue 类以有效管理图表中的多级数据，增强数据可视化功能。
type: docs
weight: 1050
url: /zh/net/aspose.words.drawing.charts/chartmultilevelvalue/
---
## ChartMultilevelValue class

表示显示多级数据的图表的值。

```csharp
public class ChartMultilevelValue
```

## 构造函数

| 姓名 | 描述 |
| --- | --- |
| [ChartMultilevelValue](chartmultilevelvalue/#constructor)(*string*) | 初始化此类的新实例，表示单级值。 |
| [ChartMultilevelValue](chartmultilevelvalue/#constructor_1)(*string, string*) | 初始化此类的新实例，表示两级值。 |
| [ChartMultilevelValue](chartmultilevelvalue/#constructor_2)(*string, string, string*) | 初始化此类的新实例，表示三级值。 |

## 特性

| 姓名 | 描述 |
| --- | --- |
| [Level1](../../aspose.words.drawing.charts/chartmultilevelvalue/level1/) { get; } | 获取此值所指的图表顶层的名称。 |
| [Level2](../../aspose.words.drawing.charts/chartmultilevelvalue/level2/) { get; } | 获取此值所指的图表中间级别的名称。 |
| [Level3](../../aspose.words.drawing.charts/chartmultilevelvalue/level3/) { get; } | 获取此值所指的图表底层的名称。 |

## 方法

| 姓名 | 描述 |
| --- | --- |
| override [Equals](../../aspose.words.drawing.charts/chartmultilevelvalue/equals/)(*object*) | 获取一个标志，指示指定对象是否等于当前多级数据对象。 |
| override [GetHashCode](../../aspose.words.drawing.charts/chartmultilevelvalue/gethashcode/)() | 获取当前多级数据对象的哈希码。 |

## 例子

展示如何创建树状图。

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// 插入树状图。
Shape shape = builder.InsertChart(ChartType.Treemap, 450, 280);
Chart chart = shape.Chart;
chart.Title.Text = "World Population";

// 删除默认生成的系列。
chart.Series.Clear();

// 添加一个系列。
ChartSeries series = chart.Series.Add(
    "Population by Region",
    new ChartMultilevelValue[]
    {
        new ChartMultilevelValue("Asia", "China"),
        new ChartMultilevelValue("Asia", "India"),
        new ChartMultilevelValue("Asia", "Indonesia"),
        new ChartMultilevelValue("Asia", "Pakistan"),
        new ChartMultilevelValue("Asia", "Bangladesh"),
        new ChartMultilevelValue("Asia", "Japan"),
        new ChartMultilevelValue("Asia", "Philippines"),
        new ChartMultilevelValue("Asia", "Other"),
        new ChartMultilevelValue("Africa", "Nigeria"),
        new ChartMultilevelValue("Africa", "Ethiopia"),
        new ChartMultilevelValue("Africa", "Egypt"),
        new ChartMultilevelValue("Africa", "Other"),
        new ChartMultilevelValue("Europe", "Russia"),
        new ChartMultilevelValue("Europe", "Germany"),
        new ChartMultilevelValue("Europe", "Other"),
        new ChartMultilevelValue("Latin America", "Brazil"),
        new ChartMultilevelValue("Latin America", "Mexico"),
        new ChartMultilevelValue("Latin America", "Other"),
        new ChartMultilevelValue("Northern America", "United States", "Other"),
        new ChartMultilevelValue("Northern America", "Other"),
        new ChartMultilevelValue("Oceania")
    },
    new double[]
    {
        1409670000, 1400744000, 279118866, 241499431, 169828911, 123930000, 112892781, 764000000,
        223800000, 107334000, 105914499, 903000000,
        146150789, 84607016, 516000000,
        203080756, 129713690, 310000000,
        335893238, 35000000,
        42000000
    });

// 显示数据标签。
series.HasDataLabels = true;
series.DataLabels.ShowValue = true;
series.DataLabels.ShowCategoryName = true;
string thousandSeparator = CultureInfo.CurrentCulture.NumberFormat.CurrencyGroupSeparator;
series.DataLabels.NumberFormat.FormatCode = $"#{thousandSeparator}0";

doc.Save(ArtifactsDir + "Charts.Treemap.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* 部件 [Aspose.Words](../../)
