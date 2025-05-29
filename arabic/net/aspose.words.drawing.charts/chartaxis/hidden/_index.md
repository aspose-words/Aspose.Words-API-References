---
title: ChartAxis.Hidden
linktitle: Hidden
articleTitle: Hidden
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية "إخفاء محور الرسم البياني" لإدارة رؤية المحور بسهولة في مخططاتك. حسّن عرض بياناتك باستخدام هذه الميزة البسيطة!
type: docs
weight: 110
url: /ar/net/aspose.words.drawing.charts/chartaxis/hidden/
---
## ChartAxis.Hidden property

يحصل على علم أو يعينه للإشارة إلى ما إذا كان هذا المحور مخفيًا أم لا.

```csharp
public bool Hidden { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`خطأ شنيع` .

## أمثلة

يوضح كيفية إخفاء محاور الرسم البياني.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Line, 500, 300);
Chart chart = shape.Chart;

// قم بمسح سلسلة بيانات العرض التوضيحي للرسم البياني للبدء برسم بياني نظيف.
chart.Series.Clear();

// أضف سلسلة مخصصة تحتوي على فئات لمحور X، وقيم عشرية مقابلة لمحور Y.
chart.Series.Add("AW Series 1",
    new[] { "Item 1", "Item 2", "Item 3", "Item 4", "Item 5" },
    new[] { 1.2, 0.3, 2.1, 2.9, 4.2 });

 //إخفاء محاور الرسم البياني لتبسيط مظهر الرسم البياني.
chart.AxisX.Hidden = true;
chart.AxisY.Hidden = true;

doc.Save(ArtifactsDir + "Charts.HideChartAxis.docx");
```

### أنظر أيضا

* class [ChartAxis](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
