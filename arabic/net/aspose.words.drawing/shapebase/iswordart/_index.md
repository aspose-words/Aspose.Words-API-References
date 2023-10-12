---
title: ShapeBase.IsWordArt
second_title: Aspose.Words لمراجع .NET API
description: ShapeBase ملكية. إرجاعحقيقي إذا كان هذا الشكل عبارة عن كائن WordArt.
type: docs
weight: 360
url: /ar/net/aspose.words.drawing/shapebase/iswordart/
---
## ShapeBase.IsWordArt property

إرجاع`حقيقي` إذا كان هذا الشكل عبارة عن كائن WordArt.

```csharp
public bool IsWordArt { get; }
```

### ملاحظات

يعمل حتى وضع التوافق 2007. في 2010 ووضع التوافق الأعلى، يعد WordArt مجرد مربع نص يحتوي على خطوط فاخرة.

### أمثلة

يوضح كيفية العمل مع WordArt.

```csharp
public void InsertTextPaths()
{
    Document doc = new Document();

    // قم بإدراج كائن WordArt لعرض النص في شكل يمكننا تغيير حجمه وتحريكه باستخدام الماوس في Microsoft Word.
    // قم بتوفير "ShapeType" كوسيطة لتعيين شكل لـ WordArt.
    Shape shape = AppendWordArt(doc, "Hello World! This text is bold, and italic.", 
        "Arial", 480, 24, Color.White, Color.Black, ShapeType.TextPlainText);

    // قم بتطبيق إعدادات التنسيق "غامق" و"مائل" على النص باستخدام الخصائص المعنية.
    shape.TextPath.Bold = true;
    shape.TextPath.Italic = true;

    // فيما يلي العديد من الخصائص الأخرى المتعلقة بتنسيق النص.
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

    // استخدم خاصية "تشغيل" لإظهار/إخفاء النص.
    shape = AppendWordArt(doc, "On set to \"true\"", "Calibri", 150, 24, Color.Yellow, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.On = true;

    shape = AppendWordArt(doc, "On set to \"false\"", "Calibri", 150, 24, Color.Yellow, Color.Purple, ShapeType.TextPlainText);
    shape.TextPath.On = false;

    // استخدم خاصية "تقنين الأحرف" لتمكين/تعطيل تباعد المسافات بين أحرف معينة.
    shape = AppendWordArt(doc, "Kerning: VAV", "Times New Roman", 90, 24, Color.Orange, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.Kerning = true;

    shape = AppendWordArt(doc, "No kerning: VAV", "Times New Roman", 100, 24, Color.Orange, Color.Red, ShapeType.TextPlainText);
    shape.TextPath.Kerning = false;

    // استخدم خاصية "التباعد" لتعيين التباعد المخصص بين الأحرف على مقياس من 0.0 (لا شيء) إلى 1.0 (افتراضي).
    shape = AppendWordArt(doc, "Spacing set to 0.1", "Calibri", 120, 24, Color.BlueViolet, Color.Blue, ShapeType.TextCascadeDown);
    shape.TextPath.Spacing = 0.1;

    // اضبط خاصية "RotateLetters" على "صحيح" لتدوير كل حرف بمقدار 90 درجة عكس اتجاه عقارب الساعة.
    shape = AppendWordArt(doc, "RotateLetters", "Calibri", 200, 36, Color.GreenYellow, Color.Green, ShapeType.TextWave);
    shape.TextPath.RotateLetters = true;

    // اضبط خاصية "SameLetterHeights" على "صحيح" للحصول على ارتفاع x لكل حرف يساوي ارتفاع الحد الأقصى.
    shape = AppendWordArt(doc, "Same character height for lower and UPPER case", "Calibri", 300, 24, Color.DeepSkyBlue, Color.DodgerBlue, ShapeType.TextSlantUp);
    shape.TextPath.SameLetterHeights = true;

    // افتراضيًا، سيتم دائمًا تغيير حجم النص ليناسب حجم الشكل الذي يحتوي عليه، مما يؤدي إلى تجاوز إعداد حجم النص.
    shape = AppendWordArt(doc, "FitShape on", "Calibri", 160, 24, Color.LightBlue, Color.Blue, ShapeType.TextPlainText);
    Assert.True(shape.TextPath.FitShape);
    shape.TextPath.Size = 24.0;

    // إذا قمنا بتعيين خاصية "FitShape: على "خطأ"، فسيحتفظ النص بالحجم
    // الذي تحدده خاصية "الحجم" بغض النظر عن حجم الشكل.
    // استخدم خاصية "TextPathAlignment" أيضًا لمحاذاة النص إلى جانب الشكل.
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
    // قم بإنشاء شكل مضمن، والذي سيكون بمثابة حاوية لـ WordArt الخاص بنا.
    // يمكن أن يكون الشكل شكل WordArt صالحًا فقط إذا قمنا بتعيين ShapeType مخصص لـ WordArt له.
    // ستحتوي هذه الأنواع على "كائن WordArt" في الوصف،
    // وستبدأ جميع أسماء عداداتها الثابتة بـ "نص".
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

* class [ShapeBase](../)
* مساحة الاسم [Aspose.Words.Drawing](../../shapebase/)
* المجسم [Aspose.Words](../../../)


