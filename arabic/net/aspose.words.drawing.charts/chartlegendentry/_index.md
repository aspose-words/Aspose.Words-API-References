---
title: ChartLegendEntry Class
linktitle: ChartLegendEntry
articleTitle: ChartLegendEntry
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.ChartLegendEntry لإنشاء أساطير ديناميكية للمخططات. حسّن تصور بياناتك من خلال التكامل والتخصيص السلس.
type: docs
weight: 1020
url: /ar/net/aspose.words.drawing.charts/chartlegendentry/
---
## ChartLegendEntry class

يمثل إدخال أسطورة الرسم البياني.

لمعرفة المزيد، قم بزيارة[العمل مع الرسوم البيانية](https://docs.aspose.com/words/net/working-with-charts/) مقالة توثيقية.

```csharp
public class ChartLegendEntry
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Font](../../aspose.words.drawing.charts/chartlegendentry/font/) { get; } | يوفر الوصول إلى تنسيق الخط لإدخال الأسطورة هذا. |
| [IsHidden](../../aspose.words.drawing.charts/chartlegendentry/ishidden/) { get; set; } | يحصل على قيمة أو يعينها للإشارة إلى ما إذا كان هذا الإدخال مخفيًا في أسطورة الرسم البياني. القيمة الافتراضية هي**خطأ شنيع** . |

## ملاحظات

يتوافق إدخال الأسطورة مع سلسلة مخطط أو خط اتجاه محدد.

نص الإدخال هو اسم السلسلة أو خط الاتجاه. لا يمكن تغيير النص.

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

* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)
