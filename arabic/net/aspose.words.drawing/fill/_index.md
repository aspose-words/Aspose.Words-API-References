---
title: Fill Class
linktitle: Fill
articleTitle: Fill
second_title: Aspose.Words لـ .NET
description: استكشف فئة Aspose.Words.Drawing.Fill للحصول على خيارات تنسيق التعبئة المتقدمة، مما يعزز تصميم مستندك وجاذبيته البصرية بسهولة.
type: docs
weight: 1270
url: /ar/net/aspose.words.drawing/fill/
---
## Fill class

يمثل تنسيق التعبئة لكائن.

لمعرفة المزيد، قم بزيارة[العمل مع العناصر الرسومية](https://docs.aspose.com/words/net/working-with-graphic-elements/) مقالة توثيقية.

```csharp
public class Fill
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [BackColor](../../aspose.words.drawing/fill/backcolor/) { get; set; } | يحصل على كائن اللون الذي يمثل لون الخلفية للتعبئة أو يعينه. |
| [BackThemeColor](../../aspose.words.drawing/fill/backthemecolor/) { get; set; } | يحصل على كائن ThemeColor أو يعينه، والذي يمثل لون الخلفية للتعبئة. |
| [BackTintAndShade](../../aspose.words.drawing/fill/backtintandshade/) { get; set; } | يحصل على قيمة مزدوجة لتفتيح أو تعتيم لون الخلفية أو تعيينها. |
| [BaseForeColor](../../aspose.words.drawing/fill/baseforecolor/) { get; } | يحصل على كائن لون يمثل لون المقدمة الأساسي لـ fill بدون أي تعديلات. |
| [Color](../../aspose.words.drawing/fill/color/) { get; set; } | يحصل على كائن اللون الذي يمثل لون المقدمة للتعبئة أو يعينه. |
| [FillType](../../aspose.words.drawing/fill/filltype/) { get; } | يحصل على نوع التعبئة. |
| [ForeColor](../../aspose.words.drawing/fill/forecolor/) { get; set; } | يحصل على كائن اللون الذي يمثل لون المقدمة للتعبئة أو يعينه. |
| [ForeThemeColor](../../aspose.words.drawing/fill/forethemecolor/) { get; set; } | يحصل على كائن ThemeColor أو يعينه، والذي يمثل لون المقدمة للتعبئة. |
| [ForeTintAndShade](../../aspose.words.drawing/fill/foretintandshade/) { get; set; } | يحصل على قيمة مزدوجة أو يعينها لتفتيح أو تعتيم لون المقدمة. |
| [GradientAngle](../../aspose.words.drawing/fill/gradientangle/) { get; set; } | يحصل على زاوية التعبئة المتدرجة أو يعينها. |
| [GradientStops](../../aspose.words.drawing/fill/gradientstops/) { get; } | يحصل على مجموعة من[`GradientStop`](../gradientstop/) أشياء للتعبئة. |
| [GradientStyle](../../aspose.words.drawing/fill/gradientstyle/) { get; } | يحصل على نمط التدرج[`GradientStyle`](../gradientstyle/) للتعبئة. |
| [GradientVariant](../../aspose.words.drawing/fill/gradientvariant/) { get; } | يحصل على متغير التدرج[`GradientVariant`](../gradientvariant/) للتعبئة. |
| [ImageBytes](../../aspose.words.drawing/fill/imagebytes/) { get; } | يحصل على البايتات الخام من نسيج التعبئة أو النمط. |
| [Opacity](../../aspose.words.drawing/fill/opacity/) { get; set; } | يحصل على درجة تعتيم التعبئة المحددة أو يضبطها كقيمة بين 0.0 (واضح) و1.0 (غير شفاف). |
| [Pattern](../../aspose.words.drawing/fill/pattern/) { get; } | يحصل على[`PatternType`](../patterntype/) للتعبئة. |
| [PresetTexture](../../aspose.words.drawing/fill/presettexture/) { get; } | يحصل على[`PresetTexture`](../presettexture/) للتعبئة. |
| [RotateWithObject](../../aspose.words.drawing/fill/rotatewithobject/) { get; set; } | يحصل على أو يعين ما إذا كان التعبئة تدور مع الكائن المحدد. |
| [TextureAlignment](../../aspose.words.drawing/fill/texturealignment/) { get; set; } | يحصل على محاذاة تعبئة نسيج البلاط أو يعينها. |
| [Transparency](../../aspose.words.drawing/fill/transparency/) { get; set; } | يحصل على درجة شفافية التعبئة المحددة أو يعينها كقيمة بين 0.0 (غير شفاف) و1.0 (واضح). |
| [Visible](../../aspose.words.drawing/fill/visible/) { get; set; } | يحصل على القيمة أو يعينها`حقيقي` إذا تم تطبيق التنسيق على هذه الحالة، فسيكون مرئيًا. |

## طُرق

| اسم | وصف |
| --- | --- |
| [OneColorGradient](../../aspose.words.drawing/fill/onecolorgradient/#onecolorgradient)(*[GradientStyle](../gradientstyle/), [GradientVariant](../gradientvariant/), double*) | يضبط التعبئة المحددة إلى تدرج لوني أحادي اللون. |
| [OneColorGradient](../../aspose.words.drawing/fill/onecolorgradient/#onecolorgradient_1)(*Color, [GradientStyle](../gradientstyle/), [GradientVariant](../gradientvariant/), double*) | يضبط التعبئة المحددة لتدرج لوني أحادي اللون باستخدام اللون المحدد. |
| [Patterned](../../aspose.words.drawing/fill/patterned/#patterned)(*[PatternType](../patterntype/)*) | يضبط التعبئة المحددة إلى نمط. |
| [Patterned](../../aspose.words.drawing/fill/patterned/#patterned_1)(*[PatternType](../patterntype/), Color, Color*) | يضبط التعبئة المحددة إلى نمط. |
| [PresetTextured](../../aspose.words.drawing/fill/presettextured/)(*[PresetTexture](../presettexture/)*) | يضبط التعبئة إلى نسيج محدد مسبقًا. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage)(*byte[]*) | يغير نوع التعبئة إلى صورة واحدة. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage_1)(*Stream*) | يغير نوع التعبئة إلى صورة واحدة. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage_2)(*string*) | يغير نوع التعبئة إلى صورة واحدة. |
| [Solid](../../aspose.words.drawing/fill/solid/#solid)() | يضبط التعبئة على لون موحد. |
| [Solid](../../aspose.words.drawing/fill/solid/#solid_1)(*Color*) | يضبط التعبئة إلى لون موحد محدد. |
| [TwoColorGradient](../../aspose.words.drawing/fill/twocolorgradient/#twocolorgradient)(*[GradientStyle](../gradientstyle/), [GradientVariant](../gradientvariant/)*) | يضبط التعبئة المحددة إلى تدرج لوني ثنائي اللون. |
| [TwoColorGradient](../../aspose.words.drawing/fill/twocolorgradient/#twocolorgradient_1)(*Color, Color, [GradientStyle](../gradientstyle/), [GradientVariant](../gradientvariant/)*) | يضبط التعبئة المحددة إلى تدرج لوني ثنائي اللون. |

## ملاحظات

استخدم[`Fill`](../shapebase/fill/) أو[`Fill`](../../aspose.words/font/fill/) الخاصية للوصول إلى خصائص التعبئة الخاصة بالكائن. لا تقم بإنشاء مثيلات من`Fill` الصف مباشرة.

## أمثلة

يوضح كيفية ملء الشكل بلون ثابت.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// اكتب بعض النص، ثم قم بتغطيته بشكل عائم.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

//استخدم خاصية "StrokeColor" لتعيين لون الخطوط العريضة للشكل.
shape.StrokeColor = Color.CadetBlue;

//استخدم خاصية "FillColor" لتعيين لون المنطقة الداخلية للشكل.
shape.FillColor = Color.LightBlue;

// تحدد خاصية "الشفافية" مدى شفافية اللون على مقياس من 0 إلى 1،
// حيث 1 يكون معتمًا تمامًا، و0 يكون غير مرئي.
// يتم تعبئة الشكل بشكل افتراضي بشكل معتم بالكامل، وبالتالي لا يمكننا رؤية النص الموجود أعلى هذا الشكل.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// قم بضبط تعتيم لون تعبئة الشكل إلى قيمة أقل حتى نتمكن من رؤية النص الموجود أسفله.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
