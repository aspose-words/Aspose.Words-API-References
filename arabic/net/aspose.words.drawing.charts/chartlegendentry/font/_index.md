---
title: ChartLegendEntry.Font
second_title: Aspose.Words لمراجع .NET API
description: ChartLegendEntry ملكية. يوفر الوصول إلى تنسيق الخط لإدخال وسيلة الإيضاح هذا.
type: docs
weight: 10
url: /ar/net/aspose.words.drawing.charts/chartlegendentry/font/
---
## ChartLegendEntry.Font property

يوفر الوصول إلى تنسيق الخط لإدخال وسيلة الإيضاح هذا.

```csharp
public Font Font { get; }
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

* class [Font](../../../aspose.words/font/)
* class [ChartLegendEntry](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../chartlegendentry/)
* المجسم [Aspose.Words](../../../)


