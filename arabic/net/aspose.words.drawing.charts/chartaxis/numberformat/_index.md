---
title: ChartAxis.NumberFormat
second_title: Aspose.Words لمراجع .NET API
description: ChartAxis ملكية. إرجاع أChartNumberFormat كائن يسمح بتعريف تنسيقات الأرقام للمحور.
type: docs
weight: 170
url: /ar/net/aspose.words.drawing.charts/chartaxis/numberformat/
---
## ChartAxis.NumberFormat property

إرجاع أ[`ChartNumberFormat`](../../chartnumberformat/) كائن يسمح بتعريف تنسيقات الأرقام للمحور.

```csharp
public ChartNumberFormat NumberFormat { get; }
```

### أمثلة

يوضح كيفية تعيين التنسيق لقيم المخطط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertChart(ChartType.Column, 500, 300);
Chart chart = shape.Chart;

// امسح سلسلة بيانات العرض التوضيحي للرسم البياني لتبدأ بمخطط نظيف.
chart.Series.Clear();

// أضف سلسلة مخصصة إلى الرسم البياني بفئات للمحور السيني ،
 // والقيم الرقمية الكبيرة الخاصة بالمحور ص.
chart.Series.Add("Aspose Test Series",
    new [] { "Word", "PDF", "Excel", "GoogleDocs", "Note" },
    new double[] { 1900000, 850000, 2100000, 600000, 1500000 });

 // قم بتعيين تنسيق الأرقام الخاص بعلامات تحديد المحور Y على عدم تجميع الأرقام بفاصلات.
chart.AxisY.NumberFormat.FormatCode = "#,##0";

// يمكن لهذه العلامة تجاوز القيمة أعلاه ورسم تنسيق الأرقام من الخلية المصدر.
Assert.False(chart.AxisY.NumberFormat.IsLinkedToSource);

doc.Save(ArtifactsDir + "Charts.SetNumberFormatToChartAxis.docx");
```

### أنظر أيضا

* class [ChartNumberFormat](../../chartnumberformat/)
* class [ChartAxis](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../chartaxis/)
* المجسم [Aspose.Words](../../../)


