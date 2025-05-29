---
title: TextPath Class
linktitle: TextPath
articleTitle: TextPath
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Drawing.TextPath لإنشاء رسومات WordArt رائعة. عرّف النص والتنسيق بسهولة لتحسين مستنداتك.
type: docs
weight: 1760
url: /ar/net/aspose.words.drawing/textpath/
---
## TextPath class

يحدد النص وتنسيق مسار النص (لكائن WordArt).

لمعرفة المزيد، قم بزيارة[العمل مع الأشكال](https://docs.aspose.com/words/net/working-with-shapes/) مقالة توثيقية.

```csharp
public class TextPath
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Bold](../../aspose.words.drawing/textpath/bold/) { get; set; } | صحيح إذا تم تنسيق الخط على أنه غامق. |
| [FitPath](../../aspose.words.drawing/textpath/fitpath/) { get; set; } | يحدد ما إذا كان النص يناسب مسار الشكل. |
| [FitShape](../../aspose.words.drawing/textpath/fitshape/) { get; set; } | يحدد ما إذا كان النص يتناسب مع المربع المحيط بالشكل. |
| [FontFamily](../../aspose.words.drawing/textpath/fontfamily/) { get; set; } | يحدد عائلة خط مسار النص. |
| [Italic](../../aspose.words.drawing/textpath/italic/) { get; set; } | صحيح إذا تم تنسيق الخط على أنه مائل. |
| [Kerning](../../aspose.words.drawing/textpath/kerning/) { get; set; } | يحدد ما إذا كان التباعد بين الأحرف قيد التشغيل. |
| [On](../../aspose.words.drawing/textpath/on/) { get; set; } | يحدد ما إذا كان سيتم عرض النص. |
| [ReverseRows](../../aspose.words.drawing/textpath/reverserows/) { get; set; } | يحدد ما إذا كان ترتيب تخطيط الصفوف معكوسًا. |
| [RotateLetters](../../aspose.words.drawing/textpath/rotateletters/) { get; set; } | يحدد ما إذا كانت أحرف النص تدور أم لا. |
| [SameLetterHeights](../../aspose.words.drawing/textpath/sameletterheights/) { get; set; } | يحدد ما إذا كانت جميع الأحرف ستكون بنفس الارتفاع بغض النظر عن الحالة الأولية. |
| [Shadow](../../aspose.words.drawing/textpath/shadow/) { get; set; } | يحدد ما إذا كان سيتم تطبيق الظل على النص الموجود في مسار النص. |
| [Size](../../aspose.words.drawing/textpath/size/) { get; set; } | يحدد حجم الخط بالنقاط. |
| [SmallCaps](../../aspose.words.drawing/textpath/smallcaps/) { get; set; } | صحيح إذا تم تنسيق الخط بأحرف كبيرة صغيرة. |
| [Spacing](../../aspose.words.drawing/textpath/spacing/) { get; set; } | يحدد مقدار المسافة بين السطور للنص. 1 يعني 100%. |
| [StrikeThrough](../../aspose.words.drawing/textpath/strikethrough/) { get; set; } | صحيح إذا تم تنسيق الخط كنص مشطوب. |
| [Text](../../aspose.words.drawing/textpath/text/) { get; set; } | يحدد نص مسار النص. |
| [TextPathAlignment](../../aspose.words.drawing/textpath/textpathalignment/) { get; set; } | يحدد محاذاة النص. |
| [Trim](../../aspose.words.drawing/textpath/trim/) { get; set; } | يحدد ما إذا كان سيتم إزالة المساحة الزائدة أعلى وأسفل النص. |
| [Underline](../../aspose.words.drawing/textpath/underline/) { get; set; } | صحيح إذا كان الخط مسطرًا. |
| [XScale](../../aspose.words.drawing/textpath/xscale/) { get; set; } | يحدد ما إذا كان سيتم استخدام مسار نص مستقيم بدلاً من مسار الشكل. |

## ملاحظات

استخدم[`TextPath`](../shape/textpath/) الخاصية للوصول إلى خصائص WordArt الخاصة بالشكل. لا تقم بإنشاء مثيلات من`TextPath` الصف مباشرة.

## أمثلة

يوضح كيفية العمل مع WordArt.

```csharp
public void InsertTextPaths()
{
    Document doc = new Document();

    // قم بإدراج كائن WordArt لعرض النص في شكل يمكننا تغيير حجمه وتحريكه باستخدام الماوس في Microsoft Word.
    // قم بتوفير "ShapeType" كحجة لتعيين شكل لـ WordArt.
    Shape shape = AppendWordArt(doc, "Hello World! This text is bold, and italic.",
        "Arial", 480, 24, Color.White, Color.Black, ShapeType.TextPlainText);

    // قم بتطبيق إعدادات التنسيق "غامق" و"مائل" على النص باستخدام الخصائص الخاصة بكل منها.
    shape.TextPath.Bold = true;
    shape.TextPath.Italic = true;

    // فيما يلي خصائص أخرى مختلفة متعلقة بتنسيق النص.
    Assert.False(shape.TextPath.Underline);
    Assert.False(shape.TextPath.Shadow);
    Assert.False(shape.TextPath.StrikeThrough);
    Assert.False(shape.TextPath.ReverseRows);
    Assert.False(shape.TextPath.XScale);
    Assert.False(shape.TextPath.Trim);
    Assert.False(shape.TextPath.SmallCaps);

    Assert.AreEqual(36.0, shape.TextPath.Size);
    Assert.AreEqual("Hello World! This text is bold, and italic.", shape.TextPath.Text);
    Assert.AreEqual(ShapeType.TextPlainText, shape.ShapeType);

    //استخدم خاصية "تشغيل" لإظهار/إخفاء النص.
    shape = AppendWordArt(doc, "On set to \"true\"", "Calibri", 150, 24, Color.Yellow, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.On = true;

    shape = AppendWordArt(doc, "On set to \"false\"", "Calibri", 150, 24, Color.Yellow, Color.Purple, ShapeType.TextPlainText);
    shape.TextPath.On = false;

    // استخدم خاصية "التباعد بين الأحرف" لتمكين/تعطيل التباعد بين الأحرف المحددة.
    shape = AppendWordArt(doc, "Kerning: VAV", "Times New Roman", 90, 24, Color.Orange, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.Kerning = true;

    shape = AppendWordArt(doc, "No kerning: VAV", "Times New Roman", 100, 24, Color.Orange, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.Kerning = false;

    // استخدم خاصية "التباعد" لتعيين التباعد المخصص بين الأحرف على مقياس من 0.0 (لا شيء) إلى 1.0 (افتراضي).
    shape = AppendWordArt(doc, "Spacing set to 0.1", "Calibri", 120, 24, Color.BlueViolet, Color.Blue, ShapeType.TextCascadeDown);
    shape.TextPath.Spacing = 0.1;

    // اضبط خاصية "RotateLetters" على "true" لتدوير كل حرف بمقدار 90 درجة عكس اتجاه عقارب الساعة.
    shape = AppendWordArt(doc, "RotateLetters", "Calibri", 200, 36, Color.GreenYellow, Color.Green, ShapeType.TextWave);
    shape.TextPath.RotateLetters = true;

    // اضبط خاصية "SameLetterHeights" على "true" لجعل ارتفاع x لكل حرف مساويًا لارتفاع الحرف الكبير.
    shape = AppendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300, 24, Color.DeepSkyBlue, Color.DodgerBlue, ShapeType.TextSlantUp);
    shape.TextPath.SameLetterHeights = true;

    // بشكل افتراضي، سيتم دائمًا تعديل حجم النص ليناسب حجم الشكل المحتوي، متجاوزًا إعداد حجم النص.
    shape = AppendWordArt(doc, "FitShape on", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    Assert.True(shape.TextPath.FitShape);
    shape.TextPath.Size = 24.0;

    // إذا قمنا بتعيين خاصية "FitShape:" إلى "false"، سيحتفظ النص بالحجم
    // الذي تحدده خاصية "الحجم" بغض النظر عن حجم الشكل.
    //استخدم خاصية "TextPathAlignment" أيضًا لمحاذاة النص إلى أحد جانبي الشكل.
    shape = AppendWordArt(doc, "FitShape off", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    shape.TextPath.FitShape = false;
    shape.TextPath.Size = 24.0;
    shape.TextPath.TextPathAlignment = TextPathAlignment.Right;

    doc.Save(ArtifactsDir + "Shape.InsertTextPaths.docx");
}

/// <summary>
/// قم بإدراج فقرة جديدة تحتوي على شكل WordArt بداخلها.
/// </summary>
private static Shape AppendWordArt(Document doc, string text, string textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, ShapeType wordArtShapeType)
{
    // قم بإنشاء شكل مضمن، والذي سيعمل كحاوية لـ WordArt الخاص بنا.
    // لا يمكن أن يكون الشكل شكل WordArt صالحًا إلا إذا قمنا بتعيين ShapeType مخصص لـ WordArt له.
    // ستحتوي هذه الأنواع على "كائن WordArt" في الوصف،
    // وستبدأ جميع أسماء الثوابت العددية الخاصة بهم بـ "نص".
    Shape shape = new Shape(doc, wordArtShapeType)
    {
        WrapType = WrapType.Inline,
        Width = shapeWidth,
        Height = shapeHeight,
        FillColor = wordArtFill,
        StrokeColor = line
    };

    shape.TextPath.Text = text;
    shape.TextPath.FontFamily = textFontFamily;

    Paragraph para = (Paragraph)doc.FirstSection.Body.AppendChild(new Paragraph(doc));
    para.AppendChild(shape);
    return shape;
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Drawing](../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../)
