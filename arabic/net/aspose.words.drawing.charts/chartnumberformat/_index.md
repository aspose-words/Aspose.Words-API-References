---
title: ChartNumberFormat Class
linktitle: ChartNumberFormat
articleTitle: ChartNumberFormat
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Drawing.Charts.ChartNumberFormat فصل. يمثل تنسيق الأرقام للعنصر الأصلي في C#.
type: docs
weight: 770
url: /ar/net/aspose.words.drawing.charts/chartnumberformat/
---
## ChartNumberFormat class

يمثل تنسيق الأرقام للعنصر الأصلي.

لمعرفة المزيد، قم بزيارة[العمل مع الرسوم البيانية](https://docs.aspose.com/words/net/working-with-charts/) مقالة توثيقية.

```csharp
public class ChartNumberFormat
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [FormatCode](../../aspose.words.drawing.charts/chartnumberformat/formatcode/) { get; set; } | الحصول على رمز التنسيق المطبق على تسمية البيانات أو تعيينه. |
| [IsLinkedToSource](../../aspose.words.drawing.charts/chartnumberformat/islinkedtosource/) { get; set; } | يحدد ما إذا كان رمز التنسيق مرتبطًا بخلية مصدر أم لا. الافتراضي هو صحيح. |

## أمثلة

يوضح كيفية تعيين التنسيق لقيم المخطط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// امسح سلسلة البيانات التجريبية للمخطط للبدء بمخطط نظيف.
chart.Series.Clear();

// أضف سلسلة مخصصة إلى المخطط مع فئات المحور السيني،
 // وقيم رقمية كبيرة خاصة بالمحور Y.
chart.Series.Add("Aspose Test Series",
    new [] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 1900000, 850000, 2100000, 600000, 1500000 });

 // قم بتعيين تنسيق الأرقام لتسميات تحديد المحور Y بحيث لا يتم تجميع الأرقام بفواصل.
chart.AxisY.NumberFormat.FormatCode = "#,##0";

// يمكن لهذه العلامة تجاوز القيمة المذكورة أعلاه ورسم تنسيق الأرقام من الخلية المصدر.
Assert.False(chart.AxisY.NumberFormat.IsLinkedToSource);

doc.Save(ArtifactsDir + "Charts.SetNumberFormatToChartAxis.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)
