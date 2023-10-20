---
title: AxisScaling Class
linktitle: AxisScaling
articleTitle: AxisScaling
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Drawing.Charts.AxisScaling فصل. يمثل خيارات القياس للمحور في C#.
type: docs
weight: 570
url: /ar/net/aspose.words.drawing.charts/axisscaling/
---
## AxisScaling class

يمثل خيارات القياس للمحور.

لمعرفة المزيد، قم بزيارة[العمل مع الرسوم البيانية](https://docs.aspose.com/words/net/working-with-charts/) مقالة توثيقية.

```csharp
public class AxisScaling
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [AxisScaling](axisscaling/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [LogBase](../../aspose.words.drawing.charts/axisscaling/logbase/) { get; set; } | الحصول على أو تعيين الأساس اللوغاريتمي لمحور لوغاريتمي. |
| [Maximum](../../aspose.words.drawing.charts/axisscaling/maximum/) { get; set; } | الحصول على أو تعيين القيمة القصوى للمحور. |
| [Minimum](../../aspose.words.drawing.charts/axisscaling/minimum/) { get; set; } | الحصول على أو تعيين الحد الأدنى لقيمة المحور. |
| [Type](../../aspose.words.drawing.charts/axisscaling/type/) { get; set; } | الحصول على أو تعيين نوع القياس للمحور. |

## أمثلة

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

* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)
