---
title: ChartSeriesGroup.FirstSliceAngle
linktitle: FirstSliceAngle
articleTitle: FirstSliceAngle
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ChartSeriesGroup FirstSliceAngle لتخصيص زاوية الشريحة الأولى لمخططك الدائري بالدرجات لتحسين تصور البيانات.
type: docs
weight: 60
url: /ar/net/aspose.words.drawing.charts/chartseriesgroup/firstsliceangle/
---
## ChartSeriesGroup.FirstSliceAngle property

يحصل على الزاوية، بالدرجات، للشريحة الأولى من مخطط الفطيرة الرئيسي أو يعينها.

```csharp
public int FirstSliceAngle { get; set; }
```

## ملاحظات

ينطبق على مجموعات السلسلةPie ،Pie3D وDoughnut أنواع.

يتراوح نطاق القيم المقبولة بين ٠ و٣٦٠ درجة. القيمة الافتراضية هي ٠.

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
