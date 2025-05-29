---
title: ShapeLineStyle Enum
linktitle: ShapeLineStyle
articleTitle: ShapeLineStyle
second_title: Aspose.Words لـ .NET
description: اكتشف مجموعة Aspose.Words.Drawing.ShapeLineStyle لتعزيز تصميم مستندك باستخدام أنماط الخطوط المركبة القابلة للتخصيص للأشكال.
type: docs
weight: 1660
url: /ar/net/aspose.words.drawing/shapelinestyle/
---
## ShapeLineStyle enumeration

يحدد نمط الخط المركب لـ[`Shape`](../shape/) .

```csharp
public enum ShapeLineStyle
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Single | `0` | سطر واحد. |
| Double | `1` | خطوط مزدوجة متساوية العرض. |
| ThickThin | `2` | خطوط مزدوجة، واحدة سميكة، وأخرى رفيعة. |
| ThinThick | `3` | خطوط مزدوجة، واحدة رفيعة، وأخرى سميكة. |
| Triple | `4` | ثلاثة خطوط، رفيع، سميك، رفيع. |
| Default | `0` | القيمة الافتراضية هيSingle . |

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

* property [LineStyle](../stroke/linestyle/)
* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
