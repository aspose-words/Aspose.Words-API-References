---
title: ChartSeriesType Enum
linktitle: ChartSeriesType
articleTitle: ChartSeriesType
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Drawing.Charts.ChartSeriesType enum لتعزيز سلسلة المخططات الخاصة بك باستخدام خيارات متنوعة لتصور البيانات الديناميكية.
type: docs
weight: 1110
url: /ar/net/aspose.words.drawing.charts/chartseriestype/
---
## ChartSeriesType enumeration

يحدد نوع سلسلة الرسم البياني.

```csharp
public enum ChartSeriesType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Area | `0` | يمثل سلسلة مخططات المساحة. |
| AreaStacked | `1` | يمثل سلسلة مخططات المساحة المكدسة. |
| AreaPercentStacked | `2` | يمثل سلسلة مخططات المساحة المكدسة بنسبة 100%. |
| Area3D | `3` | يمثل سلسلة مخططات المساحة ثلاثية الأبعاد. |
| Area3DStacked | `4` | يمثل سلسلة مخططات المساحة المكدسة ثلاثية الأبعاد. |
| Area3DPercentStacked | `5` | يمثل سلسلة مخططات مساحة مكدسة بنسبة 100% ثلاثية الأبعاد. |
| Bar | `6` | يمثل سلسلة مخططات شريطية. |
| BarStacked | `7` | يمثل سلسلة مخططات الأشرطة المكدسة. |
| BarPercentStacked | `8` | يمثل سلسلة مخططات شريطية مكدسة بنسبة 100%. |
| Bar3D | `9` | يمثل سلسلة مخططات شريطية ثلاثية الأبعاد. |
| Bar3DStacked | `10` | يمثل سلسلة مخططات شريطية مكدسة ثلاثية الأبعاد. |
| Bar3DPercentStacked | `11` | يمثل سلسلة مخططات شريطية مكدسة بنسبة 100% ثلاثية الأبعاد. |
| Bubble | `12` | يمثل سلسلة مخطط الفقاعات. |
| Bubble3D | `13` | يمثل سلسلة مخططات الفقاعات ثلاثية الأبعاد. |
| Column | `14` | يمثل سلسلة مخطط عمودي. |
| ColumnStacked | `15` | يمثل سلسلة مخططات عمودية مكدسة. |
| ColumnPercentStacked | `16` | يمثل سلسلة مخططات عمودية مكدسة بنسبة 100%. |
| Column3D | `17` | يمثل سلسلة مخططات عمودية ثلاثية الأبعاد. |
| Column3DStacked | `18` | يمثل سلسلة مخططات عمودية مكدسة ثلاثية الأبعاد. |
| Column3DPercentStacked | `19` | يمثل سلسلة مخططات عمودية مكدسة بنسبة 100% ثلاثية الأبعاد. |
| Column3DClustered | `20` | يمثل سلسلة مخططات عمودية مجمعة ثلاثية الأبعاد. |
| Doughnut | `21` | يمثل سلسلة مخططات الكعك الدائرية. |
| Line | `22` | يمثل سلسلة مخططات خطية. |
| LineStacked | `23` | يمثل سلسلة مخططات خطية مكدسة. |
| LinePercentStacked | `24` | يمثل سلسلة مخططات خطية مكدسة بنسبة 100%. |
| Line3D | `25` | يمثل سلسلة مخططات خطية ثلاثية الأبعاد. |
| Pie | `26` | يمثل سلسلة مخطط دائري. |
| Pie3D | `27` | يمثل سلسلة مخطط دائري ثلاثي الأبعاد. |
| PieOfBar | `28` | يمثل سلسلة مخططات دائرية للأشرطة. |
| PieOfPie | `29` | يمثل فطيرة من سلسلة مخططات الفطيرة. |
| Radar | `30` | يمثل سلسلة مخططات الرادار. |
| Scatter | `31` | يمثل سلسلة مخططات التشتت. |
| Stock | `32` | يمثل سلسلة مخططات الأسهم. |
| Surface | `33` | يمثل سلسلة مخططات السطح. |
| Surface3D | `34` | يمثل سلسلة مخططات سطحية ثلاثية الأبعاد. |
| Treemap | `35` | يمثل سلسلة مخططات شجرة. |
| Sunburst | `36` | يمثل سلسلة مخططات Sunburst. |
| Histogram | `37` | يمثل سلسلة مخططات الهيستوجرام. |
| Pareto | `38` | يمثل سلسلة مخطط باريتو. |
| ParetoLine | `39` | يمثل سلسلة مخططات خط باريتو. |
| BoxAndWhisker | `40` | يمثل سلسلة مخططات الصندوق والشارب. |
| Waterfall | `41` | يمثل سلسلة مخططات الشلال. |
| Funnel | `42` | يمثل سلسلة مخططات القمع. |
| RegionMap | `43` | يمثل سلسلة مخططات خريطة المنطقة. |

## أمثلة

يوضح كيفية إزالة سلسلة مخطط محددة.

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
