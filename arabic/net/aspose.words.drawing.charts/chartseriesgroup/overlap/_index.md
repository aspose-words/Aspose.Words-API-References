---
title: ChartSeriesGroup.Overlap
linktitle: Overlap
articleTitle: Overlap
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Overlap في ChartSeriesGroup لضبط نسبة التداخل لأشرطة أو أعمدة السلسلة بسهولة لتحسين تصور البيانات.
type: docs
weight: 80
url: /ar/net/aspose.words.drawing.charts/chartseriesgroup/overlap/
---
## ChartSeriesGroup.Overlap property

يحصل على النسبة المئوية لمدى تداخل أشرطة أو أعمدة السلسلة أو يعينها.

```csharp
public int Overlap { get; set; }
```

## ملاحظات

ينطبق على مجموعات السلاسل من جميع أنواع الأعمدة والأشرطة.

يتراوح نطاق القيم المقبولة بين -١٠٠ و١٠٠ شاملةً. تشير القيمة ٠ إلى عدم وجود مسافة x000d_ بين الأعمدة/الأشرطة. إذا كانت القيمة -١٠٠، فإن المسافة بين الأعمدة/الأشرطة تساوي عرضها. تعني القيمة ١٠٠ أن الأعمدة/الأشرطة متداخلة تمامًا.

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
