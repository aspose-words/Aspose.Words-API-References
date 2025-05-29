---
title: ChartAxis.NumberFormat
linktitle: NumberFormat
articleTitle: NumberFormat
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ChartAxis NumberFormat لتخصيص تنسيقات أرقام الرسم البياني الخاص بك بسهولة باستخدام كائن ChartNumberFormat لتحسين تصور البيانات.
type: docs
weight: 200
url: /ar/net/aspose.words.drawing.charts/chartaxis/numberformat/
---
## ChartAxis.NumberFormat property

يعيد[`ChartNumberFormat`](../../chartnumberformat/) كائن يسمح بتحديد تنسيقات الأرقام للمحور.

```csharp
public ChartNumberFormat NumberFormat { get; }
```

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

* class [ChartNumberFormat](../../chartnumberformat/)
* class [ChartAxis](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
