---
title: Stroke.On
linktitle: On
articleTitle: On
second_title: Aspose.Words لـ .NET
description: Stroke On ملكية. يحدد ما إذا كان سيتم تحديد المسار أم لا في C#.
type: docs
weight: 140
url: /ar/net/aspose.words.drawing/stroke/on/
---
## Stroke.On property

يحدد ما إذا كان سيتم تحديد المسار أم لا.

```csharp
public bool On { get; set; }
```

## ملاحظات

القيمة الافتراضية ل[`Shape`](../../shape/) يكون`حقيقي`.

## أمثلة

يوضح كيفية تغيير خصائص السكتة الدماغية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 200, 200, WrapType.None);

// الأشكال الأساسية، مثل المستطيل، لها جزأين مرئيين.
// 1 - التعبئة، والتي تنطبق على المساحة الموجودة داخل المخطط التفصيلي للشكل:
shape.Fill.ForeColor = Color.White;

// 2 - الحد الذي يحدد الخطوط العريضة للشكل:
// تعديل الخصائص المختلفة لحد هذا الشكل.
Stroke stroke = shape.Stroke;
stroke.On = true;
stroke.Weight = 5;
stroke.Color = Color.Red;
stroke.DashStyle = DashStyle.ShortDashDotDot;
stroke.JoinStyle = JoinStyle.Miter;
stroke.EndCap = EndCap.Square;
stroke.LineStyle = ShapeLineStyle.Triple;
stroke.Fill.TwoColorGradient(Color.Red, Color.Blue, GradientStyle.Vertical, GradientVariant.Variant1);

doc.Save(ArtifactsDir + "Shape.Stroke.docx");
```

### أنظر أيضا

* class [Stroke](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
