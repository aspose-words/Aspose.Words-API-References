---
title: Shape.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words för .NET
description: Upptäck Shape Accept-metoden, utformad för att öka besökarnas engagemang och effektivisera er acceptansprocess för bättre resultat.
type: docs
weight: 250
url: /sv/net/aspose.words.drawing/shape/accept/
---
## Shape.Accept method

Tar emot en besökare.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| visitor | DocumentVisitor | Besökaren som kommer att besöka noderna. |

### Returvärde

Sant om alla noder besöktes; falskt om[`DocumentVisitor`](../../../aspose.words/documentvisitor/) stoppade operationen innan alla noder besöktes.

## Anmärkningar

Räknar upp denna nod och alla dess underordnade noder. Varje nod anropar en motsvarande metod.[`DocumentVisitor`](../../../aspose.words/documentvisitor/).

För mer information, se designmönstret för besökare.

Samtal[`VisitShapeStart`](../../../aspose.words/documentvisitor/visitshapestart/) , ringer sedan[`Accept`](../../../aspose.words/node/accept/) för alla underordnade noder till formen och anrop[`VisitShapeEnd`](../../../aspose.words/documentvisitor/visitshapeend/) i slutet.

## Exempel

Visar hur man itererar över alla former i ett dokument.

```csharp
public void VisitShapes()
{
    Document doc = new Document(MyDir + "Revision shape.docx");
    ShapeAppearancePrinter visitor = new ShapeAppearancePrinter();
    doc.Accept(visitor);

    Console.WriteLine(visitor.GetText());
}

/// <summary>
/// Loggar information om utseende och besökta former.
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
    /// Lägger till en rad i StringBuilder med ett tabbtecken före varje indragsnivå.
    /// </summary>
    private void AppendLine(string text)
    {
        for (int i = 0; i < mTextIndentLevel; i++) mStringBuilder.Append('\t');

        mStringBuilder.AppendLine(text);
    }

    /// <summary>
    /// Returnerar all text som StringBuilder har ackumulerat.
    /// </summary>
    public string GetText()
    {
        return $"Shapes visited: {mShapesVisited}\n{mStringBuilder}";
    }

    /// <summary>
    /// Anropas när denna besökare besöker början av en Shape-nod.
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
    /// Anropas när denna besökare besöker slutet av en Shape-nod.
    /// </summary>
    public override VisitorAction VisitShapeEnd(Shape shape)
    {
        mTextIndentLevel--;
        mShapesVisited++;
        AppendLine($"End of {shape.ShapeType}");

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när denna besökare besöker början av en GroupShape-nod.
    /// </summary>
    public override VisitorAction VisitGroupShapeStart(GroupShape groupShape)
    {
        AppendLine($"Shape group found: {groupShape.ShapeType}");
        mTextIndentLevel++;

        return VisitorAction.Continue;
    }

    /// <summary>
    /// Anropas när denna besökare besöker slutet av en GroupShape-nod.
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

### Se även

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [Shape](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
