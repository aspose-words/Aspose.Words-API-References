---
title: Shape.Stroked
linktitle: Stroked
articleTitle: Stroked
second_title: Aspose.Words für .NET
description: Entdecken Sie die Shape Stroked-Eigenschaft, um Ihre Designs zu verbessern! Steuern Sie die Pfadgestaltung präzise und erzielen Sie beeindruckende visuelle Effekte. Steigern Sie Ihre Kreativität!
type: docs
weight: 210
url: /de/net/aspose.words.drawing/shape/stroked/
---
## Shape.Stroked property

Definiert, ob der Pfad mit Strichen versehen wird.

```csharp
public bool Stroked { get; set; }
```

## Bemerkungen

Dies ist eine Abkürzung zum[`On`](../../stroke/on/) Eigentum.

Der Standardwert ist`WAHR`.

## Beispiele

Zeigt, wie alle Formen in einem Dokument durchlaufen werden.

```csharp
public void VisitShapes()
{
    Document doc = new Document(MyDir + "Revision shape.docx");
    ShapeAppearancePrinter visitor = new ShapeAppearancePrinter();
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Protokolliert erscheinungsbezogene Informationen zu besuchten Formen.
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
    /// Fügt dem StringBuilder eine Zeile mit einem vorangestellten Tabulatorzeichen für jede Einrückungsebene hinzu.
    /// </summary>
    private void AppendLine(string text)
    {
        for (int i = 0; i < mTextIndentLevel; i++) mStringBuilder.Append('\t');

        mStringBuilder.AppendLine(text);
    }

    /// <summary>
    /// Gibt den gesamten Text zurück, den der StringBuilder angesammelt hat.
    /// </summary>
    public string GetText()
    {
        return $"Shapes visited: {mShapesVisited}\n{mStringBuilder}";
    }

    /// <summary>
    /// Wird aufgerufen, wenn dieser Besucher den Anfang eines Shape-Knotens besucht.
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
    /// Wird aufgerufen, wenn dieser Besucher das Ende eines Shape-Knotens besucht.
    /// </summary>
    public override VisitorAction VisitShapeEnd(Shape shape)
    {
        mTextIndentLevel--;
        mShapesVisited++;
        AppendLine($"End of {shape.ShapeType}");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn dieser Besucher den Anfang eines GroupShape-Knotens besucht.
    /// </summary>
    public override VisitorAction VisitGroupShapeStart(GroupShape groupShape)
    {
        AppendLine($"Shape group found: {groupShape.ShapeType}");
        mTextIndentLevel++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Wird aufgerufen, wenn dieser Besucher das Ende eines GroupShape-Knotens besucht.
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

### Siehe auch

* class [Shape](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
