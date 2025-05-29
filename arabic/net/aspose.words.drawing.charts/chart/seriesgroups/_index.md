---
title: Chart.SeriesGroups
linktitle: SeriesGroups
articleTitle: SeriesGroups
second_title: Aspose.Words لـ .NET
description: استكشف خاصية Chart SeriesGroups للوصول بسهولة إلى مجموعة غنية من مجموعات السلاسل، مما يعزز تجربة تصور البيانات لديك.
type: docs
weight: 90
url: /ar/net/aspose.words.drawing.charts/chart/seriesgroups/
---
## Chart.SeriesGroups property

يوفر الوصول إلى مجموعة تسلسلية من هذا الرسم البياني.

```csharp
public ChartSeriesGroupCollection SeriesGroups { get; }
```

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

* class [ChartSeriesGroupCollection](../../chartseriesgroupcollection/)
* class [Chart](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
