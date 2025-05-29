---
title: AxisScaling Class
linktitle: AxisScaling
articleTitle: AxisScaling
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Drawing.Charts.AxisScaling للحصول على خيارات تخصيص مقياس المحور، مما يعزز عروض المخططات الخاصة بك بسهولة.
type: docs
weight: 820
url: /ar/net/aspose.words.drawing.charts/axisscaling/
---
## AxisScaling class

يمثل خيارات قياس المحور.

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
| [LogBase](../../aspose.words.drawing.charts/axisscaling/logbase/) { get; set; } | يحصل على القاعدة اللوغاريتمية للمحور اللوغاريتمي أو يعينها. |
| [Maximum](../../aspose.words.drawing.charts/axisscaling/maximum/) { get; set; } | يحصل على القيمة القصوى للمحور أو يعينها. |
| [Minimum](../../aspose.words.drawing.charts/axisscaling/minimum/) { get; set; } | يحصل على الحد الأدنى لقيمة المحور أو يعينها. |
| [Type](../../aspose.words.drawing.charts/axisscaling/type/) { get; set; } | يحصل على نوع مقياس المحور أو يعينه. |

## أمثلة

يوضح كيفية تطبيق المقياس اللوغاريتمي على محور الرسم البياني.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape chartShape = builder.InsertChart(ChartType.Scatter, 450, 300);
Chart chart = chartShape.Chart;

// قم بمسح سلسلة بيانات العرض التوضيحي للرسم البياني للبدء برسم بياني نظيف.
chart.Series.Clear();

// أدخل سلسلة تحتوي على إحداثيات X/Y لخمس نقاط.
chart.Series.Add("Series 1",
    new[] { 1.0, 2.0, 3.0, 4.0, 5.0 },
    new[] { 1.0, 20.0, 400.0, 8000.0, 160000.0 });

// يكون مقياس المحور X خطيًا بشكل افتراضي،
// عرض قيم متزايدة بالتساوي تغطي نطاق قيمة X (0، 1، 2، 3...).
// المحور الخطي ليس مثاليًا لقيم Y الخاصة بنا
// نظرًا لأن النقاط ذات قيم Y الأصغر ستكون أصعب في القراءة.
// مقياس لوغاريتمي بقاعدة 20 (1، 20، 400، 8000...)
// سوف يقوم بتوزيع النقاط المرسومة، مما يسمح لنا بقراءة قيمها على الرسم البياني بسهولة أكبر.
chart.AxisY.Scaling.Type = AxisScaleType.Logarithmic;
chart.AxisY.Scaling.LogBase = 20;

doc.Save(ArtifactsDir + "Charts.AxisScaling.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing.Charts](../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../)
