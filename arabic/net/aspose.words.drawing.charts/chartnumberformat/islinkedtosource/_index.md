---
title: ChartNumberFormat.IsLinkedToSource
linktitle: IsLinkedToSource
articleTitle: IsLinkedToSource
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تُحسّن خاصية ChartNumberFormat IsLinkedToSource تصوّر بياناتك من خلال ربط رموز التنسيق بخلايا المصدر. تعرّف على المزيد الآن!
type: docs
weight: 20
url: /ar/net/aspose.words.drawing.charts/chartnumberformat/islinkedtosource/
---
## ChartNumberFormat.IsLinkedToSource property

يحدد ما إذا كان رمز التنسيق مرتبطًا بخلية المصدر. الافتراضي هو true.

```csharp
public bool IsLinkedToSource { get; set; }
```

## ملاحظات

سيتم إعادة تعيين NumberFormat إلى عام إذا تم ربط رمز التنسيق بالمصدر.

## أمثلة

يوضح كيفية تعيين التنسيق لقيم الرسم البياني.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// قم بمسح سلسلة بيانات العرض التوضيحي للرسم البياني للبدء برسم بياني نظيف.
chart.Series.Clear();

// أضف سلسلة مخصصة إلى الرسم البياني مع فئات للمحور X،
 // والقيم الرقمية الكبيرة المقابلة للمحور Y.
chart.Series.Add("Aspose Test Series",
    new[] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 1900000, 850000, 2100000, 600000, 1500000 });

 // قم بتعيين تنسيق الأرقام لعناوين علامات المحور Y لعدم تجميع الأرقام بفاصلات.
chart.AxisY.NumberFormat.FormatCode = "#,##0";

// يمكن لهذا العلم تجاوز القيمة أعلاه ورسم تنسيق الرقم من الخلية المصدر.
Assert.False(chart.AxisY.NumberFormat.IsLinkedToSource);

doc.Save(ArtifactsDir + "Charts.SetNumberFormatToChartAxis.docx");
```

### أنظر أيضا

* class [ChartNumberFormat](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
