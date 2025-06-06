---
title: Shape.StrokeColor
linktitle: StrokeColor
articleTitle: StrokeColor
second_title: Aspose.Words لـ .NET
description: قم بتخصيص التصميم الخاص بك باستخدام خاصية Shape StrokeColor، مما يسمح لك بتحديد ألوان حدود نابضة بالحياة للحصول على تأثير بصري مذهل.
type: docs
weight: 200
url: /ar/net/aspose.words.drawing/shape/strokecolor/
---
## Shape.StrokeColor property

يحدد لون الخط.

```csharp
public Color StrokeColor { get; set; }
```

## ملاحظات

هذا اختصار لـ[`Color`](../../stroke/color/) ملكية.

القيمة الافتراضية هي Black .

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

يوضح كيفية تكرار جميع الأشكال في مستند.

```csharp
public void VisitShapes()
{
    Document doc = new Document(MyDir + "Revision shape.docx");
    ShapeAppearancePrinter visitor = new ShapeAppearancePrinter();
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// يسجل معلومات متعلقة بالمظهر حول الأشكال التي تمت زيارتها.
/// </summary>
private class ShapeAppearancePrinter : DocumentVisitor
{
    public ShapeAppearancePrinter()
    {
        mShapesVisited = 0;
        mTextIndentLevel = 0;
        mStringBuilder = new StringBuilder();
    }

    /// <summary>
    /// يضيف سطرًا إلى StringBuilder بإضافة حرف تبويب واحد لكل مستوى مسافة بادئة.
    /// </summary>
    private void AppendLine(string text)
    {
        for (int i = 0; i < mTextIndentLevel; i++) mStringBuilder.Append('\t');

        mStringBuilder.AppendLine(text);
    }

    /// <summary>
    /// إرجاع كل النص الذي قام StringBuilder بتجميعه.
    /// </summary>
    public string GetText()
    {
        return $"Shapes visited: {mShapesVisited}\n{mStringBuilder}";
    }

    /// <summary>
    /// يتم استدعاؤها عندما يزور هذا الزائر بداية عقدة الشكل.
    /// </summary>
    public override VisitorAction VisitShapeStart(Shape shape)
    {
        AppendLine($"Shape found: {shape.ShapeType}");

        mTextIndentLevel++;

        if (shape.HasChart)
            AppendLine($"Has chart: {shape.Chart.Title.Text}");

        AppendLine($"Extrusion enabled: {shape.ExtrusionEnabled}");
        AppendLine($"Shadow enabled: {shape.ShadowEnabled}");
        AppendLine($"StoryType: {shape.StoryType}");

        if (shape.Stroked)
        {
            Assert.AreEqual(shape.Stroke.Color, shape.StrokeColor);
            AppendLine($"Stroke colors: {shape.Stroke.Color}, {shape.Stroke.Color2}");
            AppendLine($"Stroke weight: {shape.StrokeWeight}");
        }

        if (shape.Filled)
            AppendLine($"Filled: {shape.FillColor}");

        if (shape.OleFormat != null)
            AppendLine($"Ole found of type: {shape.OleFormat.ProgId}");

        if (shape.SignatureLine != null)
            AppendLine($"Found signature line for: {shape.SignatureLine.Signer}, {shape.SignatureLine.SignerTitle}");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عندما يقوم هذا الزائر بزيارة نهاية عقدة الشكل.
    /// </summary>
    public override VisitorAction VisitShapeEnd(Shape shape)
    {
        mTextIndentLevel--;
        mShapesVisited++;
        AppendLine($"End of {shape.ShapeType}");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عندما يزور هذا الزائر بداية عقدة GroupShape.
    /// </summary>
    public override VisitorAction VisitGroupShapeStart(GroupShape groupShape)
    {
        AppendLine($"Shape group found: {groupShape.ShapeType}");
        mTextIndentLevel++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم استدعاؤها عندما يزور هذا الزائر نهاية عقدة GroupShape.
    /// </summary>
    public override VisitorAction VisitGroupShapeEnd(GroupShape groupShape)
    {
        mTextIndentLevel--;
        AppendLine($"End of {groupShape.ShapeType}");

        return VisitorAction.Continue;
    }

    private int mShapesVisited;
    private int mTextIndentLevel;
    private readonly StringBuilder mStringBuilder;
}
```

### أنظر أيضا

* class [Shape](../)
* مساحة الاسم [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* المجسم [Aspose.Words](../../../)
