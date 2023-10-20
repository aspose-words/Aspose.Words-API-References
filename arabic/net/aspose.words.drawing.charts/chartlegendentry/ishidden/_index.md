---
title: ChartLegendEntry.IsHidden
linktitle: IsHidden
articleTitle: IsHidden
second_title: Aspose.Words لـ .NET
description: ChartLegendEntry IsHidden ملكية. الحصول على قيمة أو تعيينها تشير إلى ما إذا كان هذا الإدخال مخفيًا في وسيلة إيضاح المخطط. القيمة الافتراضية هيخطأ شنيع  في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing.charts/chartlegendentry/ishidden/
---
## ChartLegendEntry.IsHidden property

الحصول على قيمة أو تعيينها تشير إلى ما إذا كان هذا الإدخال مخفيًا في وسيلة إيضاح المخطط. القيمة الافتراضية هي**خطأ شنيع** .

```csharp
public bool IsHidden { get; set; }
```

## ملاحظات

عندما يتم إخفاء إدخال وسيلة إيضاح المخطط، فإن ذلك لا يؤثر على سلسلة المخطط المقابل أو خط الاتجاه الذي لا يزال معروضًا على المخطط.

## أمثلة

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

* class [ChartLegendEntry](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
