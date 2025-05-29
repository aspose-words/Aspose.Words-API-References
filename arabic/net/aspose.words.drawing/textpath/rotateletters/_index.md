---
title: TextPath.RotateLetters
linktitle: RotateLetters
articleTitle: RotateLetters
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية تدوير الحروف في TextPath لتحسين تصميماتك من خلال التحكم في تدوير النص للحصول على تأثير بصري ديناميكي. أطلق العنان لإبداعك!
type: docs
weight: 90
url: /ar/net/aspose.words.drawing/textpath/rotateletters/
---
## TextPath.RotateLetters property

يحدد ما إذا كانت أحرف النص تدور أم لا.

```csharp
public bool RotateLetters { get; set; }
```

## ملاحظات

القيمة الافتراضية هي`خطأ شنيع`.

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

* class [TextPath](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
