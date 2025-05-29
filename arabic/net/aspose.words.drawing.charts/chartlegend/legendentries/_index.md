---
title: ChartLegend.LegendEntries
linktitle: LegendEntries
articleTitle: LegendEntries
second_title: Aspose.Words لـ .NET
description: استكشف خاصية LegendEntries في ChartLegend للوصول إلى مجموعة شاملة من إدخالات الأسطورة لجميع السلاسل وخطوط الاتجاه في الرسم البياني الخاص بك.
type: docs
weight: 30
url: /ar/net/aspose.words.drawing.charts/chartlegend/legendentries/
---
## ChartLegend.LegendEntries property

يقوم بإرجاع مجموعة من إدخالات الأسطورة لجميع السلاسل وخطوط الاتجاه للرسم البياني الرئيسي.

```csharp
public ChartLegendEntryCollection LegendEntries { get; }
```

## أمثلة

يوضح كيفية العمل مع إدخال الأسطورة لسلسلة الرسم البياني.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection series = chart.Series;
series.Clear();

string[] categories = new string[] { "AW Category 1", "AW Category 2" };

ChartSeries series1 = series.Add("Series 1", categories, new double[] { 1, 2 });
series.Add("Series 2", categories, new double[] { 3, 4 });
series.Add("Series 3", categories, new double[] { 5, 6 });
series.Add("Series 4", categories, new double[] { 0, 0 });

ChartLegendEntryCollection legendEntries = chart.Legend.LegendEntries;
legendEntries[3].IsHidden = true;

doc.Save(ArtifactsDir + "Charts.LegendEntries.docx");
```

### أنظر أيضا

* class [ChartLegendEntryCollection](../../chartlegendentrycollection/)
* class [ChartLegend](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
