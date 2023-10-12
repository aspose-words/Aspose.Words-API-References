---
title: AxisScaling.Type
second_title: Aspose.Words لمراجع .NET API
description: AxisScaling ملكية. الحصول على أو تعيين نوع القياس للمحور.
type: docs
weight: 50
url: /ar/net/aspose.words.drawing.charts/axisscaling/type/
---
## AxisScaling.Type property

الحصول على أو تعيين نوع القياس للمحور.

```csharp
public AxisScaleType Type { get; set; }
```

### ملاحظات

الLinear القيمة هي الوحيدة المسموح بها في مخططات MS Office 2016 الجديدة.

### أمثلة

يوضح كيفية تطبيق القياس اللوغاريتمي على محور المخطط.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape chartShape = builder.InsertChart(ChartType.Scatter, 450, 300);
Chart chart = chartShape.Chart;

// امسح سلسلة البيانات التجريبية للمخطط للبدء بمخطط نظيف.
chart.Series.Clear();

// أدخل سلسلة بإحداثيات X/Y لخمس نقاط.
chart.Series.Add("Series 1", 
    new[] { 1.0, 2.0, 3.0, 4.0, 5.0 }, 
    new[] { 1.0, 20.0, 400.0, 8000.0, 160000.0 });

// يكون تحجيم المحور السيني خطيًا بشكل افتراضي،
// عرض القيم المتزايدة بالتساوي التي تغطي نطاق قيمة X لدينا (0، 1، 2، 3...).
// المحور الخطي ليس مثاليًا لقيم Y لدينا
// نظرًا لأن النقاط ذات قيم Y الأصغر ستكون أكثر صعوبة في القراءة.
// مقياس لوغاريتمي بقاعدة 20 (1، 20، 400، 8000...)
// سوف ينشر النقاط المرسومة، مما يسمح لنا بقراءة قيمها على الرسم البياني بسهولة أكبر.
chart.AxisY.Scaling.Type = AxisScaleType.Logarithmic;
chart.AxisY.Scaling.LogBase = 20;

doc.Save(ArtifactsDir + "Charts.AxisScaling.docx");
```

### أنظر أيضا

* enum [AxisScaleType](../../axisscaletype/)
* class [AxisScaling](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../axisscaling/)
* المجسم [Aspose.Words](../../../)


