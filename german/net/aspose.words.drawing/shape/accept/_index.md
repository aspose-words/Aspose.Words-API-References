---
title: Shape.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words für .NET
description: Shape Accept methode. Akzeptiert einen Besucher in C#.
type: docs
weight: 240
url: /de/net/aspose.words.drawing/shape/accept/
---
## Shape.Accept method

Akzeptiert einen Besucher.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| visitor | DocumentVisitor | Der Besucher, der die Knoten besucht. |

### Rückgabewert

True, wenn alle Knoten besucht wurden; falsch wenn[`DocumentVisitor`](../../../aspose.words/documentvisitor/) stoppte den Vorgang, bevor alle Knoten besucht wurden.

## Bemerkungen

Listet diesen Knoten und alle seine untergeordneten Knoten auf. Jeder Knoten ruft eine entsprechende Methode auf[`DocumentVisitor`](../../../aspose.words/documentvisitor/).

Weitere Informationen finden Sie im Visitor-Entwurfsmuster.

Anrufe[`VisitShapeStart`](../../../aspose.words/documentvisitor/visitshapestart/) , dann ruft[`Accept`](../../../aspose.words/node/accept/) für alle untergeordneten Knoten der Form und Aufrufe[`VisitShapeEnd`](../../../aspose.words/documentvisitor/visitshapeend/) am Ende.

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
/// Protokolliert darstellungsbezogene Informationen zu besuchten Formen.
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
    /// Hängt eine Zeile an den StringBuilder an, wobei für jede Einrückungsebene ein Tabulatorzeichen vorangestellt wird.
    /// </summary>
    private void AppendLine(string text)
    {
        for (int i = 0; i < mTextIndentLevel; i++) mStringBuilder.Append('\t');

        mStringBuilder.AppendLine(text);
    }

    /// <summary>
    /// Den gesamten Text zurückgeben, den der StringBuilder gesammelt hat.
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

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [Shape](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
