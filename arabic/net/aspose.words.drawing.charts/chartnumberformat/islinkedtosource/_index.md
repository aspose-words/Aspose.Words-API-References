---
title: ChartNumberFormat.IsLinkedToSource
second_title: Aspose.Words لمراجع .NET API
description: ChartNumberFormat ملكية. يحدد ما إذا كان رمز التنسيق مرتبطًا بخلية مصدر أم لا. الافتراضي هو صحيح.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing.charts/chartnumberformat/islinkedtosource/
---
## ChartNumberFormat.IsLinkedToSource property

يحدد ما إذا كان رمز التنسيق مرتبطًا بخلية مصدر أم لا. الافتراضي هو صحيح.

```csharp
public bool IsLinkedToSource { get; set; }
```

### ملاحظات

سيتم إعادة تعيين NumberFormat إلى الوضع العام إذا كان رمز التنسيق مرتبطًا بالمصدر.

### أمثلة

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

* class [ChartNumberFormat](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../chartnumberformat/)
* المجسم [Aspose.Words](../../../)


