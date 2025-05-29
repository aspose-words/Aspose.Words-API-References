---
title: AxisTickLabels.Rotation
linktitle: Rotation
articleTitle: Rotation
second_title: Aspose.Words لـ .NET
description: اضبط دوران علامات AxisTickLabels لتحسين سهولة القراءة. خصص زوايا علامات التجزئة بالدرجات لتحسين وضوح مخططك وجاذبيته البصرية.
type: docs
weight: 70
url: /ar/net/aspose.words.drawing.charts/axisticklabels/rotation/
---
## AxisTickLabels.Rotation property

يحصل على أو يضبط دوران علامات التجزئة بالدرجات.

```csharp
public int Rotation { get; set; }
```

## ملاحظات

نطاق القيم المقبولة يتراوح من -180 إلى 180 شاملةً. القيمة الافتراضية هي 0.

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

* class [AxisTickLabels](../)
* مساحة الاسم [Aspose.Words.Drawing.Charts](../../../aspose.words.drawing.charts/)
* المجسم [Aspose.Words](../../../)
