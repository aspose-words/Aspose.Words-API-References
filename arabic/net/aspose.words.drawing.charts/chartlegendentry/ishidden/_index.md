---
title: ChartLegendEntry.IsHidden
linktitle: IsHidden
articleTitle: IsHidden
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ChartLegendEntry IsHidden، وتحكّم في رؤية أسطورة الرسم البياني بسهولة. حسّن عرض بياناتك باستخدام هذه الميزة البسيطة!
type: docs
weight: 20
url: /ar/net/aspose.words.drawing.charts/chartlegendentry/ishidden/
---
## ChartLegendEntry.IsHidden property

يحصل على قيمة أو يعينها للإشارة إلى ما إذا كان هذا الإدخال مخفيًا في أسطورة الرسم البياني. القيمة الافتراضية هي**خطأ شنيع** .

```csharp
public bool IsHidden { get; set; }
```

## ملاحظات

عندما يتم إخفاء إدخال أسطورة الرسم البياني، فإن ذلك لا يؤثر على سلسلة الرسم البياني المقابلة أو خط الاتجاه الذي لا يزال معروضًا على الرسم البياني.

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

* class [ChartLegendEntry](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
