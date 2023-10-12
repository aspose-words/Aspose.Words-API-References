---
title: Shape.Chart
second_title: Aspose.Words لمراجع .NET API
description: Shape ملكية. يوفر الوصول إلى خصائص المخطط إذا كان هذا الشكل يحتوي علىChart .
type: docs
weight: 20
url: /ar/net/aspose.words.drawing/shape/chart/
---
## Shape.Chart property

يوفر الوصول إلى خصائص المخطط إذا كان هذا الشكل يحتوي على[`Chart`](../../../aspose.words.drawing.charts/chart/) .

```csharp
public Chart Chart { get; }
```

### ملاحظات

سوف تقوم هذه الخاصية بإرجاع[`Chart`](../../../aspose.words.drawing.charts/chart/) كائن فقط إذا[`HasChart`](../haschart/) الخاصية هي`حقيقي` لهذا[`Shape`](../)، وسوف يطرح استثناءً بخلاف ذلك.

### أمثلة

يوضح كيفية التكرار على كافة الأشكال في المستند.

```csharp
public void VisitShapes()
{
    Document doc = new Document(MyDir + "Revision shape.docx");
    ShapeAppearancePrinter visitor = new ShapeAppearancePrinter();
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// يسجل المعلومات المتعلقة بالمظهر حول الأشكال التي تمت زيارتها.
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
    /// يُلحق سطرًا بـ StringBuilder بحرف جدولة مُسبق لكل مستوى مسافة بادئة.
    /// </summary>
    private void AppendLine(string text)
    {
        for (int i = 0; i < mTextIndentLevel; i++) mStringBuilder.Append('\t');

        mStringBuilder.AppendLine(text);
    }

    /// <summary>
    /// قم بإرجاع كل النص الذي قام StringBuilder بتجميعه.
    /// </summary>
    public string GetText()
    {
        return $"Shapes visited: {mShapesVisited}\n{mStringBuilder}";
    }

    /// <summary>
    /// يتم الاتصال به عندما يزور هذا الزائر بداية عقدة الشكل.
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
    /// يتم الاتصال به عندما يزور هذا الزائر نهاية عقدة الشكل.
    /// </summary>
    public override VisitorAction VisitShapeEnd(Shape shape)
    {
        mTextIndentLevel--;
        mShapesVisited++;
        AppendLine($"End of {shape.ShapeType}");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاتصال به عندما يزور هذا الزائر بداية عقدة GroupShape.
    /// </summary>
    public override VisitorAction VisitGroupShapeStart(GroupShape groupShape)
    {
        AppendLine($"Shape group found: {groupShape.ShapeType}");
        mTextIndentLevel++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// يتم الاتصال به عندما يزور هذا الزائر نهاية عقدة GroupShape.
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

* class [Chart](../../../aspose.words.drawing.charts/chart/)
* class [Shape](../)
* مساحة الاسم [Aspose.Words.Drawing](../../shape/)
* المجسم [Aspose.Words](../../../)


