---
title: DocumentVisitor.VisitShapeEnd
linktitle: VisitShapeEnd
articleTitle: VisitShapeEnd
second_title: Aspose.Words für .NET
description: Entdecken Sie die DocumentVisitor VisitShapeEnd-Methode, die für die Verwaltung der Shape-Enumeration in Ihren Anwendungen unerlässlich ist. Steigern Sie noch heute Ihre Programmiereffizienz!
type: docs
weight: 390
url: /de/net/aspose.words/documentvisitor/visitshapeend/
---
## DocumentVisitor.VisitShapeEnd method

Wird aufgerufen, wenn die Aufzählung einer Form beendet ist.

```csharp
public virtual VisitorAction VisitShapeEnd(Shape shape)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| shape | Shape | Das Objekt, das besucht wird. |

### Rückgabewert

A[`VisitorAction`](../../visitoraction/) Wert, der angibt, wie die Aufzählung fortgesetzt werden soll.

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

* enum [VisitorAction](../../visitoraction/)
* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentVisitor](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
