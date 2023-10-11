---
title: Enum ShapeLineStyle
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Drawing.ShapeLineStyle تعداد. يحدد نمط الخط المركب لـ aShape .
type: docs
weight: 1270
url: /ar/net/aspose.words.drawing/shapelinestyle/
---
## ShapeLineStyle enumeration

يحدد نمط الخط المركب لـ a[`Shape`](../shape/) .

```csharp
public enum ShapeLineStyle
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Single | `0` | سطر واحد. |
| Double | `1` | خطوط مزدوجة متساوية العرض. |
| ThickThin | `2` | خطوط مزدوجة، واحد سميك والآخر رفيع. |
| ThinThick | `3` | خطوط مزدوجة، واحد رفيع والآخر سميك. |
| Triple | `4` | ثلاثة خطوط رفيعة سميكة رفيعة. |
| Default | `0` | القيمة الافتراضية هيSingle . |

### أمثلة

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

* property [LineStyle](../stroke/linestyle/)
* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)


