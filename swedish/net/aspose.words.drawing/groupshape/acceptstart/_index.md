---
title: GroupShape.AcceptStart
linktitle: AcceptStart
articleTitle: AcceptStart
second_title: Aspose.Words för .NET
description: Upptäck GroupShape AcceptStart-metoden för att smidigt välkomna besökare och förbättra deras upplevelse från början av din applikation.
type: docs
weight: 50
url: /sv/net/aspose.words.drawing/groupshape/acceptstart/
---
## GroupShape.AcceptStart method

Accepterar en besökare för att besöka början av gruppformen.

```csharp
public override VisitorAction AcceptStart(DocumentVisitor visitor)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| visitor | DocumentVisitor | Dokumentbesökaren. |

### Returvärde

Den åtgärd som besökaren ska vidta.

## Exempel

Visar hur man skapar en grupp med former och skriver ut dess innehåll med hjälp av en dokumentbesökare.

```csharp
public void GroupOfShapes()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Om du behöver skapa "Icke-primitiva" former, till exempel SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
    // ÖvreHörnEttRundatEttBeskärt, EnkeltHörnRundat, ÖvreHörnRundade, DiagonalaHörnRundade
    // använd DocumentBuilder.InsertShape-metoderna.
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
/// Skriver ut innehållet i en besökt formgrupp till konsolen.
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

### Se även

* enum [VisitorAction](../../../aspose.words/visitoraction/)
* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [GroupShape](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
