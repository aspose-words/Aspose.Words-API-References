---
title: GroupShape.AcceptStart
linktitle: AcceptStart
articleTitle: AcceptStart
second_title: Aspose.Words für .NET
description: Entdecken Sie die GroupShape AcceptStart-Methode, um Besucher nahtlos willkommen zu heißen und ihr Erlebnis vom ersten Moment Ihrer Anwendung an zu verbessern.
type: docs
weight: 50
url: /de/net/aspose.words.drawing/groupshape/acceptstart/
---
## GroupShape.AcceptStart method

Akzeptiert einen Besucher für den Besuch des Anfangs des GroupShape.

```csharp
public override VisitorAction AcceptStart(DocumentVisitor visitor)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| visitor | DocumentVisitor | Der Dokumentbesucher. |

### Rückgabewert

Die vom Besucher auszuführende Aktion.

## Beispiele

Zeigt, wie Sie eine Gruppe von Formen erstellen und deren Inhalt mithilfe eines Dokumentbetrachters drucken.

```csharp
public void GroupOfShapes()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Wenn Sie „nicht-primitive“ Formen erstellen müssen, wie z. B. SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
    // Eine abgerundete obere Ecke, eine abgeschnittene Ecke, eine abgerundete obere Ecke, abgerundete diagonale Ecke
    // Bitte verwenden Sie DocumentBuilder.InsertShape-Methoden.
    Shape balloon = new Shape(doc, ShapeType.Balloon)
    {
        Width = 200,
        Height = 200,
        Stroke = { Color = Color.Red }
    };

    Shape cube = new Shape(doc, ShapeType.Cube)
    {
        Width = 100,
        Height = 100,
        Stroke = { Color = Color.Blue }
    };

    GroupShape group = new GroupShape(doc);
    group.AppendChild(balloon);
    group.AppendChild(cube);

    Assert.True(group.IsGroup);

    builder.InsertNode(group);

    ShapeGroupPrinter printer = new ShapeGroupPrinter();
    group.Accept(printer);

    Console.WriteLine(printer.GetText());
}

/// <summary>
/// Gibt den Inhalt einer besuchten Formgruppe auf der Konsole aus.
/// </summary>
public class ShapeGroupPrinter : DocumentVisitor
{
    public ShapeGroupPrinter()
    {
        mBuilder = new StringBuilder();
    }

    public string GetText()
    {
        return mBuilder.ToString();
    }

    public override VisitorAction VisitGroupShapeStart(GroupShape groupShape)
    {
        mBuilder.AppendLine("Shape group started:");
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitGroupShapeEnd(GroupShape groupShape)
    {
        mBuilder.AppendLine("End of shape group");
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitShapeStart(Shape shape)
    {
        mBuilder.AppendLine("\tShape - " + shape.ShapeType + ":");
        mBuilder.AppendLine("\t\tWidth: " + shape.Width);
        mBuilder.AppendLine("\t\tHeight: " + shape.Height);
        mBuilder.AppendLine("\t\tStroke color: " + shape.Stroke.Color);
        mBuilder.AppendLine("\t\tFill color: " + shape.Fill.ForeColor);
        return VisitorAction.Continue;
    }

    public override VisitorAction VisitShapeEnd(Shape shape)
    {
        mBuilder.AppendLine("\tEnd of shape");
        return VisitorAction.Continue;
    }

    private readonly StringBuilder mBuilder;
}
```

### Siehe auch

* enum [VisitorAction](../../../aspose.words/visitoraction/)
* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [GroupShape](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
