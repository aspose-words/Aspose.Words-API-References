---
title: ChartFormat.IsDefined
linktitle: IsDefined
articleTitle: IsDefined
second_title: Aspose.Words لـ .NET
description: اكتشف ما إذا كان التنسيق مُعرّفًا باستخدام خاصية ChartFormat IsDefined. تمتع بتحكم سلس في تنسيق مخططاتك اليوم!
type: docs
weight: 20
url: /ar/net/aspose.words.drawing.charts/chartformat/isdefined/
---
## ChartFormat.IsDefined property

يحصل على علم يشير إلى ما إذا كان قد تم تعريف أي تنسيق.

```csharp
public bool IsDefined { get; }
```

## أمثلة

يوضح كيفية إعادة تعيين التعبئة إلى القيمة الافتراضية المحددة في السلسلة.

```csharp
Document doc = new Document(MyDir + "DataPoint format.docx");

Shape shape = (Shape)doc.GetChild(NodeType.Shape, 0, true);
ChartSeries series = shape.Chart.Series[0];
ChartDataPoint dataPoint = series.DataPoints[1];

Assert.IsTrue(dataPoint.Format.IsDefined);

dataPoint.Format.SetDefaultFill();

doc.Save(ArtifactsDir + "Charts.ResetDataPointFill.docx");
```

### أنظر أيضا

* class [ChartFormat](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
