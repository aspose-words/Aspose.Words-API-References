---
title: AxisScaling.LogBase
linktitle: LogBase
articleTitle: LogBase
second_title: Aspose.Words لـ .NET
description: اضبط القاعدة اللوغاريتمية لخاصية AxisScaling LogBase لعرض دقيق للبيانات ودقة أعلى للرسم البياني. حسّن مخططاتك البيانية اليوم!
type: docs
weight: 20
url: /ar/net/aspose.words.drawing.charts/axisscaling/logbase/
---
## AxisScaling.LogBase property

يحصل على القاعدة اللوغاريتمية للمحور اللوغاريتمي أو يعينها.

```csharp
public double LogBase { get; set; }
```

## ملاحظات

لا يتم دعم الخاصية بواسطة المخططات الجديدة في MS Office 2016.

النطاق الصحيح لقيمة النقطة العائمة أكبر من أو يساوي 2 وأقل من أو يساوي 1000. الخاصية لها تأثير فقط إذا[`Type`](../type/) تم ضبطه على Logarithmic.

يؤدي تعيين هذه الخاصية إلى تعيين[`Type`](../type/) الممتلكات إلىLogarithmic .

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

* class [AxisScaling](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
