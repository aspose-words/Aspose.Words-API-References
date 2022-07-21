---
title: TextPathAlignment
second_title: Aspose.Words لمراجع .NET API
description: يحدد محاذاة النص .
type: docs
weight: 170
url: /ar/net/aspose.words.drawing/textpath/textpathalignment/
---
## TextPath.TextPathAlignment property

يحدد محاذاة النص .

```csharp
public TextPathAlignment TextPathAlignment { get; set; }
```

### ملاحظات

النظام الأساسيCenter.

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

* enum [TextPathAlignment](../../textpathalignment)
* class [TextPath](../../textpath)
* مساحة الاسم [Aspose.Words.Drawing](../../textpath)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
