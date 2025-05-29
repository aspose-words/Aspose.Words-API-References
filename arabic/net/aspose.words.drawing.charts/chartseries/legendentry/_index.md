---
title: ChartSeries.LegendEntry
linktitle: LegendEntry
articleTitle: LegendEntry
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ChartSeries LegendEntry للوصول بسهولة إلى إدخالات الأسطورة وتخصيصها لمخططاتك، مما يعزز تصور البيانات لديك.
type: docs
weight: 90
url: /ar/net/aspose.words.drawing.charts/chartseries/legendentry/
---
## ChartSeries.LegendEntry property

يحصل على إدخال أسطورة لسلسلة الرسم البياني هذه.

```csharp
public ChartLegendEntry LegendEntry { get; }
```

## أمثلة

يوضح كيفية العمل مع خط الأسطورة.

```csharp
Document doc = new Document(MyDir + "Reporting engine template - Chart series.docx");
Chart chart = ((Shape)doc.GetChild(NodeType.Shape, 0, true)).Chart;

ChartLegend chartLegend = chart.Legend;
// تعيين حجم الخط الافتراضي لجميع إدخالات الأسطورة.
chartLegend.Font.Size = 14;
// تغيير الخط لإدخال الأسطورة المحددة.
chartLegend.LegendEntries[1].Font.Italic = true;
chartLegend.LegendEntries[1].Font.Size = 12;
// الحصول على إدخال الأسطورة لسلسلة الرسم البياني.
ChartLegendEntry legendEntry = chart.Series[0].LegendEntry;

doc.Save(ArtifactsDir + "Charts.LegendFont.docx");
```

### أنظر أيضا

* class [ChartLegendEntry](../../chartlegendentry/)
* class [ChartSeries](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
