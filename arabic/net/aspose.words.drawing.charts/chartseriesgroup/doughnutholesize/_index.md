---
title: ChartSeriesGroup.DoughnutHoleSize
linktitle: DoughnutHoleSize
articleTitle: DoughnutHoleSize
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ChartSeriesGroup DoughnutHoleSize لتخصيص نسبة حجم الثقب في مخطط الدونات الخاص بك بسهولة لتحسين تصور البيانات.
type: docs
weight: 50
url: /ar/net/aspose.words.drawing.charts/chartseriesgroup/doughnutholesize/
---
## ChartSeriesGroup.DoughnutHoleSize property

يحصل على حجم ثقب مخطط الدونات الرئيسي أو يعينه كنسبة مئوية.

```csharp
public int DoughnutHoleSize { get; set; }
```

## ملاحظات

ينطبق فقط على مجموعات السلسلةDoughnut يكتب.

يتراوح نطاق القيم المقبولة بين ٠ و٩٠. القيمة الافتراضية هي ٧٥.

## أمثلة

يوضح كيفية إنشاء مخطط دائري وتنسيقه.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Doughnut, 400, 400);
Chart chart = shape.Chart;
//حذف السلسلة المولدة افتراضيًا.
chart.Series.Clear();

string[] categories = new string[] { "Category 1", "Category 2", "Category 3" };
chart.Series.Add("Series 1", categories, new double[] { 4, 2, 5 });

//تنسيق مخطط الكعكة.
ChartSeriesGroup seriesGroup = chart.SeriesGroups[0];
seriesGroup.DoughnutHoleSize = 10;
seriesGroup.FirstSliceAngle = 270;

doc.Save(ArtifactsDir + "Charts.DoughnutChart.docx");
```

### أنظر أيضا

* class [ChartSeriesGroup](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
