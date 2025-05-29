---
title: Stroke.Weight
linktitle: Weight
articleTitle: Weight
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية "وزن الفرشاة" لتخصيص سُمك الفرشاة للأشكال. حسّن تصاميمك بضربات مسار دقيقة بالنقاط!
type: docs
weight: 260
url: /ar/net/aspose.words.drawing/stroke/weight/
---
## Stroke.Weight property

يحدد سمك الفرشاة التي ترسم مسار الشكل بالنقاط.

```csharp
public double Weight { get; set; }
```

## ملاحظات

القيمة الافتراضية لـ[`Shape`](../../shape/) هو 0.75.

## أمثلة

يوضح كيفية تغيير خصائص السكتة الدماغية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertShape(ShapeType.Rectangle, RelativeHorizontalPosition.LeftMargin, 100,
    RelativeVerticalPosition.TopMargin, 100, 200, 200, WrapType.None);

//الأشكال الأساسية، مثل المستطيل، تحتوي على جزأين مرئيين.
// 1 - التعبئة، والتي تنطبق على المنطقة داخل مخطط الشكل:
shape.Fill.ForeColor = Color.White;

// 2 - الخط الذي يحدد الخطوط العريضة للشكل:
// تعديل خصائص مختلفة لخط هذا الشكل.
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
