---
title: Shape.Chart
linktitle: Chart
articleTitle: Chart
second_title: Aspose.Words für .NET
description: Schalten Sie Diagrammeigenschaften mit Shape Chart frei. Verbessern Sie mühelos Ihre visuelle Datenpräsentation und maximieren Sie Ihre Erkenntnisse noch heute!
type: docs
weight: 30
url: /de/net/aspose.words.drawing/shape/chart/
---
## Shape.Chart property

Bietet Zugriff auf die Diagrammeigenschaften, wenn diese Form eine[`Chart`](../../../aspose.words.drawing.charts/chart/) .

```csharp
public Chart Chart { get; }
```

## Bemerkungen

Diese Eigenschaft gibt die[`Chart`](../../../aspose.words.drawing.charts/chart/) Objekt nur, wenn[`HasChart`](../haschart/) Eigenschaft ist`WAHR` dafür[`Shape`](../), und löst andernfalls eine Ausnahme aus.

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

* class [Chart](../../../aspose.words.drawing.charts/chart/)
* class [Shape](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
