---
title: Class TextPath
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Drawing.TextPath فصل. يحدد النص وتنسيق مسار النص لكائن WordArt .
type: docs
weight: 1200
url: /ar/net/aspose.words.drawing/textpath/
---
## TextPath class

يحدد النص وتنسيق مسار النص (لكائن WordArt) .

```csharp
public class TextPath
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Bold](../../aspose.words.drawing/textpath/bold/) { get; set; } | True إذا كان تنسيق الخط عريض . |
| [FitPath](../../aspose.words.drawing/textpath/fitpath/) { get; set; } | يحدد ما إذا كان النص يناسب مسار الشكل. |
| [FitShape](../../aspose.words.drawing/textpath/fitshape/) { get; set; } | يحدد ما إذا كان النص يناسب المربع المحيط بالشكل. |
| [FontFamily](../../aspose.words.drawing/textpath/fontfamily/) { get; set; } | يحدد عائلة خط مسار النص. |
| [Italic](../../aspose.words.drawing/textpath/italic/) { get; set; } | True إذا تم تنسيق الخط على أنه مائل. |
| [Kerning](../../aspose.words.drawing/textpath/kerning/) { get; set; } | تحديد ما إذا تم تشغيل تقنين الأحرف . |
| [On](../../aspose.words.drawing/textpath/on/) { get; set; } | يحدد ما إذا كان النص معروضًا أم لا. |
| [ReverseRows](../../aspose.words.drawing/textpath/reverserows/) { get; set; } | لتحديد ما إذا كان ترتيب تخطيط الصفوف معكوسًا. |
| [RotateLetters](../../aspose.words.drawing/textpath/rotateletters/) { get; set; } | لتحديد ما إذا كان سيتم تدوير أحرف النص. |
| [SameLetterHeights](../../aspose.words.drawing/textpath/sameletterheights/) { get; set; } | لتحديد ما إذا كانت جميع الأحرف ستكون بنفس الارتفاع بغض النظر عن الحالة الأولية. |
| [Shadow](../../aspose.words.drawing/textpath/shadow/) { get; set; } | يحدد ما إذا كان يتم تطبيق الظل على النص الموجود على مسار النص. |
| [Size](../../aspose.words.drawing/textpath/size/) { get; set; } | يحدد حجم الخط بالنقاط . |
| [SmallCaps](../../aspose.words.drawing/textpath/smallcaps/) { get; set; } | True إذا تم تنسيق الخط كأحرف كبيرة صغيرة. |
| [Spacing](../../aspose.words.drawing/textpath/spacing/) { get; set; } | يحدد مقدار التباعد للنص. 1 يعني 100٪ . |
| [StrikeThrough](../../aspose.words.drawing/textpath/strikethrough/) { get; set; } | True إذا تم تنسيق الخط كنص يتوسطه خط . |
| [Text](../../aspose.words.drawing/textpath/text/) { get; set; } | يحدد نص مسار النص. |
| [TextPathAlignment](../../aspose.words.drawing/textpath/textpathalignment/) { get; set; } | يحدد محاذاة النص . |
| [Trim](../../aspose.words.drawing/textpath/trim/) { get; set; } | لتحديد ما إذا كانت المساحة الزائدة ستتم إزالتها أعلى النص وأسفله. |
| [Underline](../../aspose.words.drawing/textpath/underline/) { get; set; } | صحيح إذا كان الخط مسطرًا . |
| [XScale](../../aspose.words.drawing/textpath/xscale/) { get; set; } | يحدد ما إذا كان سيتم استخدام مسار نص مستقيم بدلاً من مسار الشكل. |

### ملاحظات

استخدم ال[`TextPath`](../shape/textpath/) للوصول إلى خصائص WordArt لشكل . لا يمكنك إنشاء مثيلات من`TextPath` فئة مباشرة.

### أمثلة

يوضح كيفية استخدام WordArt.

```csharp
{
    Document doc = new Document();

    // أدخل كائن WordArt لعرض النص في شكل يمكننا تغيير حجمه ونقله باستخدام الماوس في Microsoft Word.
    // قم بتوفير "ShapeType" كوسيطة لتعيين شكل لـ WordArt.
    Shape shape = AppendWordArt(doc, "Hello World! This text is bold, and italic.", 
        "Arial", 480, 24, Color.White, Color.Black, ShapeType.TextPlainText);

    // قم بتطبيق إعدادات التنسيق "غامق" و "مائل" على النص باستخدام الخصائص ذات الصلة.
    shape.TextPath.Bold = true;
    shape.TextPath.Italic = true;

    // يوجد أدناه العديد من الخصائص الأخرى المتعلقة بتنسيق النص.
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

    // استخدم خاصية "تشغيل" لإظهار / إخفاء النص.
    shape = AppendWordArt(doc, "On set to \"true\"", "Calibri", 150, 24, Color.Yellow, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.On = true;

    shape = AppendWordArt(doc, "On set to \"false\"", "Calibri", 150, 24, Color.Yellow, Color.Purple, ShapeType.TextPlainText);
    shape.TextPath.On = false;

    // استخدم خاصية "Kerning" لتمكين / تعطيل تباعد المسافات بين أحرف معينة.
    shape = AppendWordArt(doc, "Kerning: VAV", "Times New Roman", 90, 24, Color.Orange, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.Kerning = true;

    shape = AppendWordArt(doc, "No kerning: VAV", "Times New Roman", 100, 24, Color.Orange, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.Kerning = false;

    // استخدم خاصية "التباعد" لتعيين التباعد المخصص بين الأحرف على مقياس من 0.0 (بلا) إلى 1.0 (افتراضي).
    shape = AppendWordArt(doc, "Spacing set to 0.1", "Calibri", 120, 24, Color.BlueViolet, Color.Blue, ShapeType.TextCascadeDown);
    shape.TextPath.Spacing = 0.1;

    // اضبط خاصية "RotateLetters" على "true" لتدوير كل حرف 90 درجة عكس اتجاه عقارب الساعة.
    shape = AppendWordArt(doc, "RotateLetters", "Calibri", 200, 36, Color.GreenYellow, Color.Green, ShapeType.TextWave);
    shape.TextPath.RotateLetters = true;

    // اضبط خاصية "SameLetterHeights" على "true" لجعل ارتفاع x لكل حرف يساوي ارتفاع الحد الأقصى.
    shape = AppendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300, 24, Color.DeepSkyBlue, Color.DodgerBlue, ShapeType.TextSlantUp);
    shape.TextPath.SameLetterHeights = true;

    // بشكل افتراضي ، سيتغير حجم النص دائمًا ليناسب حجم الشكل المحتوي ، متجاوزًا إعداد حجم النص.
    shape = AppendWordArt(doc, "FitShape on", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    Assert.True(shape.TextPath.FitShape);
    shape.TextPath.Size = 24.0;

    // إذا قمنا بتعيين "FitShape: property على" false "، فسيحتفظ النص بالحجم
    // التي تحددها خاصية "الحجم" بغض النظر عن حجم الشكل.
    // استخدم خاصية "TextPathAlignment" أيضًا لمحاذاة النص إلى جانب الشكل.
    shape = AppendWordArt(doc, "FitShape off", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    shape.TextPath.FitShape = false;
    shape.TextPath.Size = 24.0;
    shape.TextPath.TextPathAlignment = TextPathAlignment.Right;

    doc.Save(ArtifactsDir + "Shape.InsertTextPaths.docx");

/// <summary>
/// أدخل فقرة جديدة بداخلها شكل WordArt.
/// </summary>
private static Shape AppendWordArt(Document doc, string text, string textFontFamily, double shapeWidth, double shapeHeight, Color wordArtFill, Color line, ShapeType wordArtShapeType)
{
    // قم بإنشاء شكل مضمن ، والذي سيكون بمثابة حاوية لـ WordArt الخاص بنا.
    // لا يمكن أن يكون الشكل سوى شكل WordArt صالحًا إذا قمنا بتعيين ShapeType معين من WordArt إليه.
    // سيكون لهذه الأنواع "كائن WordArt" في الوصف ،
    // وستبدأ جميع أسماءهم الثابتة في العداد بكلمة "نص".
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


