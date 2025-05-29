---
title: ChartLegend.Font
linktitle: Font
articleTitle: Font
second_title: Aspose.Words لـ .NET
description: خصّص إعدادات خط ChartLegend بسهولة! تمكّن من الوصول إلى التنسيق الافتراضي وتجاوز إدخالات التسمية التوضيحية المحددة بسهولة للحصول على مظهر أنيق.
type: docs
weight: 10
url: /ar/net/aspose.words.drawing.charts/chartlegend/font/
---
## ChartLegend.Font property

يتيح الوصول إلى تنسيق الخط الافتراضي لإدخالات التسمية التوضيحية. لتجاوز تنسيق الخط لـ إدخال تسمية توضيحية محدد، استخدم[`Font`](../../chartlegendentry/font/) الملكية.

```csharp
public Font Font { get; }
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

* class [Font](../../../aspose.words/font/)
* class [ChartLegend](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
