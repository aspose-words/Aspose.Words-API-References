---
title: ChartAxisTitle.Show
linktitle: Show
articleTitle: Show
second_title: Aspose.Words لـ .NET
description: ChartAxisTitle Show ملكية. تحديد ما إذا كان سيتم عرض العنوان للمحور أم لا. القيمة الافتراضية هيخطأ شنيع  في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing.charts/chartaxistitle/show/
---
## ChartAxisTitle.Show property

تحديد ما إذا كان سيتم عرض العنوان للمحور أم لا. القيمة الافتراضية هي`خطأ شنيع` .

```csharp
public bool Show { get; set; }
```

## أمثلة

يوضح كيفية تعيين عنوان محور المخطط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 432, 252);

Chart chart = shape.Chart;
ChartSeriesCollection seriesColl = chart.Series;
// حذف السلسلة الافتراضية التي تم إنشاؤها.
seriesColl.Clear();

seriesColl.Add("AW Series 1", new string[] { "AW Category 1", "AW Category 2" }, new double[] { 1, 2 });

// تعيين عنوان المحور.
chart.AxisX.Title.Text = "Categories";
chart.AxisX.Title.Show = true;
chart.AxisY.Title.Text = "Values";
chart.AxisY.Title.Show = true;
chart.AxisY.Title.Overlay = true;

doc.Save(ArtifactsDir + "Charts.ChartAxisTitle.docx");
```

### أنظر أيضا

* class [ChartAxisTitle](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
