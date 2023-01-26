---
title: Fill
second_title: Aspose.Words لمراجع .NET API
description: يمثل ملء التنسيق لكائن .
type: docs
weight: 820
url: /ar/net/aspose.words.drawing/fill/
---
## Fill class

يمثل ملء التنسيق لكائن .

```csharp
public class Fill
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [BackColor](../../aspose.words.drawing/fill/backcolor/) { get; set; } | الحصول على أو تعيين كائن اللون الذي يمثل لون الخلفية للتعبئة. |
| [FillType](../../aspose.words.drawing/fill/filltype/) { get; } | يحصل على نوع التعبئة . |
| [ForeColor](../../aspose.words.drawing/fill/forecolor/) { get; set; } | الحصول على أو تعيين كائن اللون الذي يمثل اللون الأمامي للتعبئة. |
| [GradientAngle](../../aspose.words.drawing/fill/gradientangle/) { get; set; } | الحصول على أو تحديد زاوية التعبئة المتدرجة. |
| [GradientStops](../../aspose.words.drawing/fill/gradientstops/) { get; } | يحصل على مجموعة من[`GradientStop`](../gradientstop/) كائنات للتعبئة . |
| [GradientStyle](../../aspose.words.drawing/fill/gradientstyle/) { get; } | يحصل على نمط التدرج[`GradientStyle`](../gradientstyle/) للتعبئة . |
| [GradientVariant](../../aspose.words.drawing/fill/gradientvariant/) { get; } | يحصل على متغير التدرج[`GradientVariant`](../gradientvariant/) للتعبئة . |
| [ImageBytes](../../aspose.words.drawing/fill/imagebytes/) { get; } | الحصول على وحدات البايت الأولية من نسيج أو نموذج التعبئة . |
| [Opacity](../../aspose.words.drawing/fill/opacity/) { get; set; } | الحصول على درجة تعتيم التعبئة المحددة أو تعيينها كقيمة بين 0.0 (واضح) و 1.0 (معتم) . |
| [Pattern](../../aspose.words.drawing/fill/pattern/) { get; } | يحصل على أ[`PatternType`](../patterntype/) للتعبئة . |
| [PresetTexture](../../aspose.words.drawing/fill/presettexture/) { get; } | يحصل على أ[`PresetTexture`](../presettexture/) للتعبئة . |
| [RotateWithObject](../../aspose.words.drawing/fill/rotatewithobject/) { get; set; } | الحصول على أو تحديد ما إذا كانت التعبئة تدور مع الكائن المحدد. |
| [TextureAlignment](../../aspose.words.drawing/fill/texturealignment/) { get; set; } | الحصول على أو تعيين المحاذاة لتعبئة نسيج التجانب. |
| [Transparency](../../aspose.words.drawing/fill/transparency/) { get; set; } | الحصول على درجة شفافية التعبئة المحددة أو تعيينها كقيمة بين 0.0 (معتم) و 1.0 (مسح) . |
| [Visible](../../aspose.words.drawing/fill/visible/) { get; set; } | الحصول على القيمة أو تعيينها`حقيقي` إذا كان التنسيق المطبق على هذا المثال ، يكون مرئيًا. |

## طُرق

| اسم | وصف |
| --- | --- |
| [OneColorGradient](../../aspose.words.drawing/fill/onecolorgradient/#onecolorgradient)(GradientStyle, GradientVariant, double) | يضبط التعبئة المحددة لتدرج لون واحد. |
| [OneColorGradient](../../aspose.words.drawing/fill/onecolorgradient/#onecolorgradient_1)(Color, GradientStyle, GradientVariant, double) | يضبط التعبئة المحددة لتدرج لوني أحادي اللون باستخدام اللون المحدد. |
| [Patterned](../../aspose.words.drawing/fill/patterned/#patterned)(PatternType) | يضبط التعبئة المحددة على نمط . |
| [Patterned](../../aspose.words.drawing/fill/patterned/#patterned_1)(PatternType, Color, Color) | يضبط التعبئة المحددة على نمط . |
| [PresetTextured](../../aspose.words.drawing/fill/presettextured/)(PresetTexture) | يضبط التعبئة على مادة محددة مسبقًا. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage)(byte[]) | يغير نوع التعبئة إلى صورة واحدة. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage_1)(Stream) | يغير نوع التعبئة إلى صورة واحدة. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage_2)(string) | يغير نوع التعبئة إلى صورة واحدة. |
| [Solid](../../aspose.words.drawing/fill/solid/#solid)() | يضبط التعبئة على لون موحد. |
| [Solid](../../aspose.words.drawing/fill/solid/#solid_1)(Color) | يضبط التعبئة على لون موحد محدد. |
| [TwoColorGradient](../../aspose.words.drawing/fill/twocolorgradient/#twocolorgradient)(GradientStyle, GradientVariant) | يضبط التعبئة المحددة لتدرج لوني ثنائي اللون. |
| [TwoColorGradient](../../aspose.words.drawing/fill/twocolorgradient/#twocolorgradient_1)(Color, Color, GradientStyle, GradientVariant) | يضبط التعبئة المحددة لتدرج لوني ثنائي اللون. |

### ملاحظات

استخدم ال[`Fill`](../shapebase/fill/) أو[`Fill`](../../aspose.words/font/fill/) الخاصية للوصول إلى خصائص التعبئة لكائن . لا يمكنك إنشاء مثيلات من`Fill` فئة مباشرة.

### أمثلة

يوضح كيفية تعبئة شكل بلون خالص.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// اكتب بعض النص ، ثم قم بتغطيته بشكل عائم.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// استخدم خاصية "StrokeColor" لتعيين لون المخطط التفصيلي للشكل.
shape.StrokeColor = Color.CadetBlue;

// استخدم خاصية "FillColor" لتعيين لون المنطقة الداخلية للشكل.
shape.FillColor = Color.LightBlue;

// تحدد خاصية "العتامة" مدى شفافية اللون على مقياس من 0-1 ،
// مع كون 1 معتمًا تمامًا ، والصفر غير مرئي.
// يكون ملء الشكل افتراضيًا معتمًا تمامًا ، لذلك لا يمكننا رؤية النص الموجود في أعلى هذا الشكل.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// اضبط عتامة لون تعبئة الشكل على قيمة أقل حتى نتمكن من رؤية النص تحتها.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
