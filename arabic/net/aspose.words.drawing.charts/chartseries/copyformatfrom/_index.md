---
title: ChartSeries.CopyFormatFrom
linktitle: CopyFormatFrom
articleTitle: CopyFormatFrom
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة ChartSeries CopyFormatFrom لتكرار تنسيقات نقاط البيانات بسهولة حسب الفهرس، مما يعزز كفاءة الرسم البياني وتناسقه.
type: docs
weight: 190
url: /ar/net/aspose.words.drawing.charts/chartseries/copyformatfrom/
---
## ChartSeries.CopyFormatFrom method

نسخ تنسيق نقطة البيانات الافتراضية من نقطة البيانات ذات الفهرس المحدد.

```csharp
public void CopyFormatFrom(int dataPointIndex)
```

## أمثلة

يوضح كيفية نسخ تنسيق نقطة البيانات.

```csharp
Document doc = new Document(MyDir + "DataPoint format.docx");

// احصل على الرسم البياني والسلسلة لتحديث التنسيق.
Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ChartSeries series = shape.Chart.Series[0];
ChartDataPointCollection dataPoints = series.DataPoints;

Assert.IsTrue(dataPoints.HasDefaultFormat(0));
Assert.IsFalse(dataPoints.HasDefaultFormat(1));

// نسخ تنسيق نقطة البيانات ذات الفهرس 1 إلى نقطة البيانات ذات الفهرس 2
// بحيث تبدو نقطة البيانات 2 مماثلة لنقطة البيانات 1.
dataPoints.CopyFormat(0, 1);

Assert.IsTrue(dataPoints.HasDefaultFormat(0));
Assert.IsTrue(dataPoints.HasDefaultFormat(1));

// نسخ تنسيق نقطة البيانات ذات الفهرس 0 إلى الإعدادات الافتراضية للسلسلة بحيث يتم نسخ جميع نقاط البيانات
// في السلسلة التي لها التنسيق الافتراضي تبدو بنفس شكل نقطة البيانات 0.
series.CopyFormatFrom(1);

Assert.IsTrue(dataPoints.HasDefaultFormat(0));
Assert.IsTrue(dataPoints.HasDefaultFormat(1));

doc.Save(ArtifactsDir + "Charts.CopyDataPointFormat.docx");
```

### أنظر أيضا

* class [ChartSeries](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
