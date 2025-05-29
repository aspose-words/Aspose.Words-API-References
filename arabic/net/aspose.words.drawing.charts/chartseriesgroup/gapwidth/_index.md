---
title: ChartSeriesGroup.GapWidth
linktitle: GapWidth
articleTitle: GapWidth
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ChartSeriesGroup GapWidth لضبط نسبة الفجوة بين عناصر الرسم البياني بسهولة لتحسين تصور البيانات.
type: docs
weight: 70
url: /ar/net/aspose.words.drawing.charts/chartseriesgroup/gapwidth/
---
## ChartSeriesGroup.GapWidth property

يحصل على النسبة المئوية لعرض الفجوة بين عناصر الرسم البياني أو يعينها.

```csharp
public int GapWidth { get; set; }
```

## ملاحظات

ينطبق فقط على مجموعات السلاسل من أنواع الشريط، والعمود، وفطيرة الشريط، وفطيرة الفطيرة، والرسم البياني، والصندوق والشارب، والشلال، والقمع.

يتراوح نطاق القيم المقبولة بين ٠ و٥٠٠. بالنسبة لمجموعات السلاسل الشريطية/العمودية، تُمثل الخاصية المسافة بين مجموعات الأشرطة كنسبة مئوية من عرضها. أما بالنسبة لمخططات "فطيرة من فطيرة" و"x000d_ شريط من فطيرة"، فهي المسافة بين القسمين الرئيسي والثانوي من المخطط.

## أمثلة

إظهار كيفية تكوين عرض الفجوة والتداخل.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 450, 250);
ChartSeriesGroup seriesGroup = shape.Chart.SeriesGroups[0];

// تعيين عرض فجوة العمود والتداخل.
seriesGroup.GapWidth = 450;
seriesGroup.Overlap = -75;

doc.Save(ArtifactsDir + "Charts.ConfigureGapOverlap.docx");
```

### أنظر أيضا

* class [ChartSeriesGroup](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
