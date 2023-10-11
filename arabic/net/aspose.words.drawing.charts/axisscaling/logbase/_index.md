---
title: AxisScaling.LogBase
second_title: Aspose.Words لمراجع .NET API
description: AxisScaling ملكية. الحصول على أو تعيين الأساس اللوغاريتمي لمحور لوغاريتمي.
type: docs
weight: 20
url: /ar/net/aspose.words.drawing.charts/axisscaling/logbase/
---
## AxisScaling.LogBase property

الحصول على أو تعيين الأساس اللوغاريتمي لمحور لوغاريتمي.

```csharp
public double LogBase { get; set; }
```

### ملاحظات

الخاصية غير مدعومة بمخططات MS Office 2016 الجديدة.

النطاق الصالح لقيمة النقطة العائمة أكبر من أو يساوي 2 وأقل من أو يساوي 1000. الخاصية لها تأثير فقط إذا[`Type`](../type/) تم ضبطه على Logarithmic.

يؤدي تعيين هذه الخاصية إلى تعيين[`Type`](../type/) الملكية لLogarithmic .

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

* class [AxisScaling](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../axisscaling/)
* المجسم [Aspose.Words](../../../)


