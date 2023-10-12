---
title: Class Fill
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Drawing.Fill فصل. يمثل تنسيق التعبئة للكائن.
type: docs
weight: 950
url: /ar/net/aspose.words.drawing/fill/
---
## Fill class

يمثل تنسيق التعبئة للكائن.

لمعرفة المزيد، قم بزيارة[العمل مع العناصر الرسومية](https://docs.aspose.com/words/net/working-with-graphic-elements/) مقالة توثيقية.

```csharp
public class Fill
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [BackColor](../../aspose.words.drawing/fill/backcolor/) { get; set; } | الحصول على أو تعيين كائن اللون الذي يمثل لون الخلفية للتعبئة. |
| [BackThemeColor](../../aspose.words.drawing/fill/backthemecolor/) { get; set; } | الحصول على أو تعيين كائن ThemeColor الذي يمثل لون الخلفية للتعبئة. |
| [BackTintAndShade](../../aspose.words.drawing/fill/backtintandshade/) { get; set; } | الحصول على أو تعيين قيمة مزدوجة تؤدي إلى تفتيح أو تغميق لون الخلفية. |
| [BaseForeColor](../../aspose.words.drawing/fill/baseforecolor/) { get; } |  |
| [Color](../../aspose.words.drawing/fill/color/) { get; set; } | الحصول على أو تعيين كائن اللون الذي يمثل اللون الأمامي للتعبئة. |
| [FillType](../../aspose.words.drawing/fill/filltype/) { get; } | الحصول على نوع التعبئة. |
| [ForeColor](../../aspose.words.drawing/fill/forecolor/) { get; set; } | الحصول على أو تعيين كائن اللون الذي يمثل اللون الأمامي للتعبئة. |
| [ForeThemeColor](../../aspose.words.drawing/fill/forethemecolor/) { get; set; } | الحصول على أو تعيين كائن ThemeColor الذي يمثل اللون الأمامي للتعبئة. |
| [ForeTintAndShade](../../aspose.words.drawing/fill/foretintandshade/) { get; set; } | الحصول على أو تعيين قيمة مزدوجة تعمل على تفتيح أو تغميق اللون الأمامي. |
| [GradientAngle](../../aspose.words.drawing/fill/gradientangle/) { get; set; } | الحصول على أو تعيين زاوية التعبئة المتدرجة. |
| [GradientStops](../../aspose.words.drawing/fill/gradientstops/) { get; } | يحصل على مجموعة من[`GradientStop`](../gradientstop/) كائنات للتعبئة. |
| [GradientStyle](../../aspose.words.drawing/fill/gradientstyle/) { get; } | الحصول على نمط التدرج[`GradientStyle`](../gradientstyle/) للتعبئة. |
| [GradientVariant](../../aspose.words.drawing/fill/gradientvariant/) { get; } | يحصل على متغير التدرج[`GradientVariant`](../gradientvariant/) للتعبئة. |
| [ImageBytes](../../aspose.words.drawing/fill/imagebytes/) { get; } | الحصول على البايتات الأولية لملمس التعبئة أو النمط. |
| [Opacity](../../aspose.words.drawing/fill/opacity/) { get; set; } | الحصول على أو تعيين درجة عتامة التعبئة المحددة كقيمة تتراوح بين 0.0 (واضح) و1.0 (معتم). |
| [Pattern](../../aspose.words.drawing/fill/pattern/) { get; } | يحصل على[`PatternType`](../patterntype/) للتعبئة. |
| [PresetTexture](../../aspose.words.drawing/fill/presettexture/) { get; } | يحصل على[`PresetTexture`](../presettexture/) للتعبئة. |
| [RotateWithObject](../../aspose.words.drawing/fill/rotatewithobject/) { get; set; } | الحصول على أو تحديد ما إذا كان سيتم تدوير التعبئة مع الكائن المحدد. |
| [TextureAlignment](../../aspose.words.drawing/fill/texturealignment/) { get; set; } | الحصول على أو تعيين المحاذاة لملء نسيج التجانب. |
| [Transparency](../../aspose.words.drawing/fill/transparency/) { get; set; } | الحصول على أو تعيين درجة شفافية التعبئة المحددة كقيمة تتراوح بين 0.0 (معتم) و1.0 (واضح). |
| [Visible](../../aspose.words.drawing/fill/visible/) { get; set; } | الحصول على القيمة أو تحديدها`حقيقي` إذا كان التنسيق المطبق على هذه الحالة مرئيًا. |

## طُرق

| اسم | وصف |
| --- | --- |
| [OneColorGradient](../../aspose.words.drawing/fill/onecolorgradient/#onecolorgradient)(GradientStyle, GradientVariant, double) | يضبط التعبئة المحددة على تدرج لوني واحد. |
| [OneColorGradient](../../aspose.words.drawing/fill/onecolorgradient/#onecolorgradient_1)(Color, GradientStyle, GradientVariant, double) | يضبط التعبئة المحددة على تدرج لوني واحد باستخدام اللون المحدد. |
| [Patterned](../../aspose.words.drawing/fill/patterned/#patterned)(PatternType) | يضبط التعبئة المحددة على النمط. |
| [Patterned](../../aspose.words.drawing/fill/patterned/#patterned_1)(PatternType, Color, Color) | يضبط التعبئة المحددة على النمط. |
| [PresetTextured](../../aspose.words.drawing/fill/presettextured/)(PresetTexture) | يضبط التعبئة على مادة محددة مسبقًا. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage)(byte[]) | تغيير نوع التعبئة إلى صورة واحدة. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage_1)(Stream) | تغيير نوع التعبئة إلى صورة واحدة. |
| [SetImage](../../aspose.words.drawing/fill/setimage/#setimage_2)(string) | تغيير نوع التعبئة إلى صورة واحدة. |
| [Solid](../../aspose.words.drawing/fill/solid/#solid)() | يضبط التعبئة على لون موحد. |
| [Solid](../../aspose.words.drawing/fill/solid/#solid_1)(Color) | يضبط التعبئة على لون موحد محدد. |
| [TwoColorGradient](../../aspose.words.drawing/fill/twocolorgradient/#twocolorgradient)(GradientStyle, GradientVariant) | يضبط التعبئة المحددة على تدرج لونين. |
| [TwoColorGradient](../../aspose.words.drawing/fill/twocolorgradient/#twocolorgradient_1)(Color, Color, GradientStyle, GradientVariant) | يضبط التعبئة المحددة على تدرج لونين. |

### ملاحظات

استخدم ال[`Fill`](../shapebase/fill/) أو[`Fill`](../../aspose.words/font/fill/) الخاصية للوصول إلى خصائص تعبئة الكائن. لا تقم بإنشاء مثيلات للكائن`Fill` الصف مباشرة.

### أمثلة

يوضح كيفية تعبئة الشكل بلون خالص.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// اكتب بعض النص، ثم قم بتغطيته بشكل عائم.
builder.Font.Size = 32;
builder.Writeln("Hello world!");

Shape shape = builder.InsertShape(ShapeType.CloudCallout, RelativeHorizontalPosition.LeftMargin, 25,
    RelativeVerticalPosition.TopMargin, 25, 250, 150, WrapType.None);

// استخدم خاصية "StrokeColor" لتعيين لون المخطط التفصيلي للشكل.
shape.StrokeColor = Color.CadetBlue;

// استخدم خاصية "FillColor" لتعيين لون المنطقة الداخلية من الشكل.
shape.FillColor = Color.LightBlue;

// تحدد خاصية "العتامة" مدى شفافية اللون على مقياس من 0 إلى 1،
// مع كون 1 معتمًا تمامًا، و0 غير مرئي.
// تكون تعبئة الشكل معتمة تمامًا بشكل افتراضي، لذا لا يمكننا رؤية النص الذي يوجد هذا الشكل فوقه.
Assert.AreEqual(1.0d, shape.Fill.Opacity);

// اضبط عتامة لون تعبئة الشكل على قيمة أقل حتى نتمكن من رؤية النص الموجود أسفله.
shape.Fill.Opacity = 0.3;

doc.Save(ArtifactsDir + "Shape.Fill.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)


