---
title: ChartFormat.SetDefaultFill
linktitle: SetDefaultFill
articleTitle: SetDefaultFill
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية استخدام طريقة ChartFormat SetDefaultFill لاستعادة تعبئة عنصر الرسم البياني الخاص بك إلى قيمته الافتراضية الأصلية بسهولة.
type: docs
weight: 50
url: /ar/net/aspose.words.drawing.charts/chartformat/setdefaultfill/
---
## ChartFormat.SetDefaultFill method

إعادة تعيين تعبئة عنصر الرسم البياني للحصول على القيمة الافتراضية.

```csharp
public void SetDefaultFill()
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
