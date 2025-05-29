---
title: AxisScaleType Enum
linktitle: AxisScaleType
articleTitle: AxisScaleType
second_title: Aspose.Words لـ .NET
description: اكتشف مجموعة Aspose.Words.Drawing.Charts.AxisScaleType، التي تحدد أنواع مقياس المحور متعددة الاستخدامات لتحسين تجربة رسم المخططات الخاصة بك.
type: docs
weight: 810
url: /ar/net/aspose.words.drawing.charts/axisscaletype/
---
## AxisScaleType enumeration

يحدد أنواع المقياس الممكنة للمحور.

```csharp
public enum AxisScaleType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Linear | `0` | التدرج الخطي. |
| Logarithmic | `1` | القياس اللوغاريتمي. |

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
