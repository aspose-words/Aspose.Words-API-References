---
title: AxisTickLabels.Orientation
linktitle: Orientation
articleTitle: Orientation
second_title: Aspose.Words لـ .NET
description: خصّص اتجاه علامات AxisTickLabels لتحسين قابلية القراءة. عدّل بسهولة اتجاه نص علامات التجزئة لتحسين عرض بياناتك!
type: docs
weight: 50
url: /ar/net/aspose.words.drawing.charts/axisticklabels/orientation/
---
## AxisTickLabels.Orientation property

يحصل على اتجاه نص علامة التجزئة أو يعينه.

```csharp
public ShapeTextOrientation Orientation { get; set; }
```

## ملاحظات

القيمة الافتراضية هيHorizontal.

لاحظ أن بعض[`ShapeTextOrientation`](../../../aspose.words.drawing/shapetextorientation/) لا تؤثر القيم على اتجاه text في محاور القيمة.

## أمثلة

يوضح كيفية تغيير الاتجاه والدوران لملصقات علامات المحور.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// إدراج مخطط عمودي.
Shape shape = builder.InsertChart(ChartType.Column, 432, 252);
AxisTickLabels xTickLabels = shape.Chart.AxisX.TickLabels;
AxisTickLabels yTickLabels = shape.Chart.AxisY.TickLabels;

// تعيين اتجاه علامة محور الدوران.
xTickLabels.Orientation = ShapeTextOrientation.VerticalFarEast;
xTickLabels.Rotation = -30;
yTickLabels.Orientation = ShapeTextOrientation.Horizontal;
yTickLabels.Rotation = 45;

doc.Save(ArtifactsDir + "Charts.TickLabelsOrientationRotation.docx");
```

### أنظر أيضا

* enum [ShapeTextOrientation](../../../aspose.words.drawing/shapetextorientation/)
* class [AxisTickLabels](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
