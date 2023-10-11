---
title: ChartLegend.LegendEntries
second_title: Aspose.Words لمراجع .NET API
description: ChartLegend ملكية. إرجاع مجموعة من إدخالات وسيلة الإيضاح لجميع السلاسل وخطوط الاتجاه للمخطط الأصلي.
type: docs
weight: 10
url: /ar/net/aspose.words.drawing.charts/chartlegend/legendentries/
---
## ChartLegend.LegendEntries property

إرجاع مجموعة من إدخالات وسيلة الإيضاح لجميع السلاسل وخطوط الاتجاه للمخطط الأصلي.

```csharp
public ChartLegendEntryCollection LegendEntries { get; }
```

### أمثلة

يوضح كيفية العمل مع إدخال وسيلة الإيضاح لسلسلة المخططات.

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

foreach (ChartLegendEntry legendEntry in legendEntries)
    legendEntry.Font.Size = 12;

series1.LegendEntry.Font.Italic = true;

doc.Save(ArtifactsDir + "Charts.LegendEntries.docx");
```

### أنظر أيضا

* class [ChartLegendEntryCollection](../../chartlegendentrycollection/)
* class [ChartLegend](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../chartlegend/)
* المجسم [Aspose.Words](../../../)


