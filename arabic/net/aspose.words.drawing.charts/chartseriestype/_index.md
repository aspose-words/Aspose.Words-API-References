---
title: ChartSeriesType Enum
linktitle: ChartSeriesType
articleTitle: ChartSeriesType
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Drawing.Charts.ChartSeriesType تعداد. يحدد نوع سلسلة المخططات في C#.
type: docs
weight: 800
url: /ar/net/aspose.words.drawing.charts/chartseriestype/
---
## ChartSeriesType enumeration

يحدد نوع سلسلة المخططات.

```csharp
public enum ChartSeriesType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Area | `0` | يمثل سلسلة من المخططات المساحية. |
| AreaStacked | `1` | يمثل سلسلة مخططات مساحية مكدسة. |
| AreaPercentStacked | `2` | يمثل سلسلة مخططات مساحية مكدسة بنسبة 100%. |
| Area3D | `3` | يمثل سلسلة مخططات مساحية ثلاثية الأبعاد. |
| Area3DStacked | `4` | يمثل سلسلة مخططات مساحية مكدسة ثلاثية الأبعاد. |
| Area3DPercentStacked | `5` | يمثل سلسلة مخططات مساحية مكدسة ثلاثية الأبعاد بنسبة 100%. |
| Bar | `6` | يمثل سلسلة من المخططات الشريطية. |
| BarStacked | `7` | يمثل سلسلة مخططات شريطية مكدسة. |
| BarPercentStacked | `8` | يمثل سلسلة مخططات شريطية مكدسة بنسبة 100%. |
| Bar3D | `9` | يمثل سلسلة مخططات شريطية ثلاثية الأبعاد. |
| Bar3DStacked | `10` | يمثل سلسلة مخططات شريطية مكدسة ثلاثية الأبعاد. |
| Bar3DPercentStacked | `11` | يمثل سلسلة مخططات شريطية مكدسة ثلاثية الأبعاد بنسبة 100%. |
| Bubble | `12` | يمثل سلسلة من المخططات الفقاعية. |
| Bubble3D | `13` | يمثل سلسلة مخططات فقاعية ثلاثية الأبعاد. |
| Column | `14` | يمثل سلسلة من المخططات العمودية. |
| ColumnStacked | `15` | يمثل سلسلة من المخططات ذات الأعمدة المكدسة. |
| ColumnPercentStacked | `16` | يمثل سلسلة من المخططات ذات الأعمدة المكدسة بنسبة 100%. |
| Column3D | `17` | يمثل سلسلة مخططات عمودية ثلاثية الأبعاد. |
| Column3DStacked | `18` | يمثل سلسلة مخططات ثلاثية الأبعاد ذات أعمدة مكدسة. |
| Column3DPercentStacked | `19` | يمثل سلسلة من المخططات العمودية المكدسة ثلاثية الأبعاد بنسبة 100%. |
| Column3DClustered | `20` | يمثل سلسلة مخططات أعمدة متفاوتة المسافات ثلاثية الأبعاد. |
| Doughnut | `21` | يمثل سلسلة من المخططات الدائرية. |
| Line | `22` | يمثل سلسلة مخططات خطية. |
| LineStacked | `23` | يمثل سلسلة من المخططات الخطية المكدسة. |
| LinePercentStacked | `24` | يمثل سلسلة من المخططات الخطية المكدسة بنسبة 100%. |
| Line3D | `25` | يمثل سلسلة مخططات خطية ثلاثية الأبعاد. |
| Pie | `26` | يمثل سلسلة من المخططات الدائرية. |
| Pie3D | `27` | يمثل سلسلة مخططات دائرية ثلاثية الأبعاد. |
| PieOfBar | `28` | يمثل سلسلة المخططات الدائرية للأعمدة. |
| PieOfPie | `29` | يمثل سلسلة المخططات الدائرية الدائرية. |
| Radar | `30` | يمثل سلسلة من المخططات الرادارية. |
| Scatter | `31` | يمثل سلسلة من المخططات المبعثرة. |
| Stock | `32` | يمثل سلسلة مخططات الأسهم. |
| Surface | `33` | يمثل سلسلة من المخططات السطحية. |
| Surface3D | `34` | يمثل سلسلة مخططات سطحية ثلاثية الأبعاد. |
| Treemap | `35` | يمثل سلسلة مخططات هيكلية. |
| Sunburst | `36` | يمثل سلسلة مخططات Sunburst. |
| Histogram | `37` | يمثل سلسلة من الرسوم البيانية. |
| Pareto | `38` | يمثل سلسلة مخططات باريتو. |
| ParetoLine | `39` | يمثل سلسلة مخططات خط باريتو. |
| BoxAndWhisker | `40` | يمثل سلسلة من المخططات المربعة والطرفية. |
| Waterfall | `41` | يمثل سلسلة مخططات انحدارية. |
| Funnel | `42` | يمثل سلسلة من المخططات القمعية. |
| RegionMap | `43` | يمثل سلسلة من مخططات خريطة المنطقة. |

## أمثلة

يبين كيفية

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

// قم بإزالة كافة سلاسل نوع العمود.
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

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)
