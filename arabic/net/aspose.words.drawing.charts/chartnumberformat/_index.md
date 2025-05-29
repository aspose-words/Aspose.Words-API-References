---
title: ChartNumberFormat Class
linktitle: ChartNumberFormat
articleTitle: ChartNumberFormat
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Drawing.Charts.ChartNumberFormat لتنسيق الأرقام المتقدم في المخططات. حسّن مظهر مستندك!
type: docs
weight: 1060
url: /ar/net/aspose.words.drawing.charts/chartnumberformat/
---
## ChartNumberFormat class

يمثل تنسيق الأرقام للعنصر الرئيسي.

لمعرفة المزيد، قم بزيارة[العمل مع الرسوم البيانية](https://docs.aspose.com/words/net/working-with-charts/) مقالة توثيقية.

```csharp
public class ChartNumberFormat
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [FormatCode](../../aspose.words.drawing.charts/chartnumberformat/formatcode/) { get; set; } | يحصل على رمز التنسيق المطبق على تسمية البيانات أو يعينه. |
| [IsLinkedToSource](../../aspose.words.drawing.charts/chartnumberformat/islinkedtosource/) { get; set; } | يحدد ما إذا كان رمز التنسيق مرتبطًا بخلية المصدر. الافتراضي هو true. |

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

* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)
