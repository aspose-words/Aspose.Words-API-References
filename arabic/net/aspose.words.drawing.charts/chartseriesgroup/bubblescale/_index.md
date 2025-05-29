---
title: ChartSeriesGroup.BubbleScale
linktitle: BubbleScale
articleTitle: BubbleScale
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ChartSeriesGroup BubbleScale لتخصيص أحجام الفقاعات في الرسوم البيانية الخاصة بك، مما يعزز تصور البيانات وإشراك المستخدم.
type: docs
weight: 40
url: /ar/net/aspose.words.drawing.charts/chartseriesgroup/bubblescale/
---
## ChartSeriesGroup.BubbleScale property

يحصل على حجم الفقاعات أو يعينه كنسبة مئوية من حجمها الافتراضي.

```csharp
public int BubbleScale { get; set; }
```

## ملاحظات

ينطبق فقط على مجموعات السلسلةBubble و Bubble3D أنواع.

يتراوح نطاق القيم المقبولة بين ٠ و٣٠٠. القيمة الافتراضية هي ١٠٠.

## أمثلة

إظهار كيفية ضبط حجم الفقاعات.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

//إدراج مخطط فقاعي ثلاثي الأبعاد.
Shape shape = builder.InsertChart(ChartType.Bubble3D, 450, 250);
ChartSeriesGroup seriesGroup = shape.Chart.SeriesGroups[0];

//ضبط مقياس الفقاعة إلى 200%.
seriesGroup.BubbleScale = 200;

doc.Save(ArtifactsDir + "Charts.BubbleScale.docx");
```

### أنظر أيضا

* class [ChartSeriesGroup](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
