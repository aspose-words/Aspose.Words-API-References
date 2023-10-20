---
title: Stroke Class
linktitle: Stroke
articleTitle: Stroke
second_title: Aspose.Words لـ .NET
description: Aspose.Words.Drawing.Stroke فصل. يحدد حد الشكل في C#.
type: docs
weight: 1310
url: /ar/net/aspose.words.drawing/stroke/
---
## Stroke class

يحدد حد الشكل.

لمعرفة المزيد، قم بزيارة[العمل مع الأشكال](https://docs.aspose.com/words/net/working-with-shapes/) مقالة توثيقية.

```csharp
public class Stroke
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [BackColor](../../aspose.words.drawing/stroke/backcolor/) { get; set; } | الحصول على أو تعيين لون خلفية الحد. |
| [Color](../../aspose.words.drawing/stroke/color/) { get; set; } | يحدد لون الحد. |
| [Color2](../../aspose.words.drawing/stroke/color2/) { get; set; } | يحدد اللون الثاني للحد. |
| [DashStyle](../../aspose.words.drawing/stroke/dashstyle/) { get; set; } | يحدد نمط النقطة والشرطة للحد. |
| [EndArrowLength](../../aspose.words.drawing/stroke/endarrowlength/) { get; set; } | يحدد طول رأس السهم لنهاية الحد. |
| [EndArrowType](../../aspose.words.drawing/stroke/endarrowtype/) { get; set; } | يحدد رأس السهم لنهاية الخط. |
| [EndArrowWidth](../../aspose.words.drawing/stroke/endarrowwidth/) { get; set; } | يحدد عرض رأس السهم لنهاية الحد. |
| [EndCap](../../aspose.words.drawing/stroke/endcap/) { get; set; } | يحدد نمط الغطاء لنهاية الخط. |
| [Fill](../../aspose.words.drawing/stroke/fill/) { get; } | يحصل على تنسيق التعبئة لـ`Stroke` . |
| [ForeColor](../../aspose.words.drawing/stroke/forecolor/) { get; set; } | الحصول على أو تعيين اللون الأمامي للحد. |
| [ImageBytes](../../aspose.words.drawing/stroke/imagebytes/) { get; } | يحدد الصورة لصورة الحد أو تعبئة النمط. |
| [JoinStyle](../../aspose.words.drawing/stroke/joinstyle/) { get; set; } | يحدد نمط ربط الخطوط المتعددة. |
| [LineStyle](../../aspose.words.drawing/stroke/linestyle/) { get; set; } | يحدد نمط الخط للحد. |
| [On](../../aspose.words.drawing/stroke/on/) { get; set; } | يحدد ما إذا كان سيتم تحديد المسار أم لا. |
| [Opacity](../../aspose.words.drawing/stroke/opacity/) { get; set; } | يحدد مقدار شفافية الحد. النطاق الصالح هو من 0 إلى 1. |
| [StartArrowLength](../../aspose.words.drawing/stroke/startarrowlength/) { get; set; } | يحدد طول رأس السهم لبداية السكتة الدماغية. |
| [StartArrowType](../../aspose.words.drawing/stroke/startarrowtype/) { get; set; } | يحدد رأس السهم لبداية السكتة الدماغية. |
| [StartArrowWidth](../../aspose.words.drawing/stroke/startarrowwidth/) { get; set; } | يحدد عرض رأس السهم لبداية السكتة الدماغية. |
| [Transparency](../../aspose.words.drawing/stroke/transparency/) { get; set; } | الحصول على أو تعيين قيمة بين 0.0 (معتم) و1.0 (واضح) تمثل درجة الشفافية للحد. |
| [Visible](../../aspose.words.drawing/stroke/visible/) { get; set; } | الحصول على أو تعيين علامة تشير إلى ما إذا كانت الحدود مرئية أم لا. |
| [Weight](../../aspose.words.drawing/stroke/weight/) { get; set; } | يحدد سمك الفرشاة الذي يحدد مسار الشكل بالنقاط. |

## ملاحظات

استخدم ال[`Stroke`](../shape/stroke/) الخاصية للوصول إلى خصائص حد الشكل. لا تقم بإنشاء مثيلات لل`Stroke` الصف مباشرة.

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

* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
