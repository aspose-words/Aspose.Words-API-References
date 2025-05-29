---
title: GroupShape.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words för .NET
description: Upptäck GroupShape Accept-metoden för att smidigt engagera besökare och förbättra användarupplevelsen på din webbplats. Öka interaktionen idag!
type: docs
weight: 30
url: /sv/net/aspose.words.drawing/groupshape/accept/
---
## GroupShape.Accept method

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

Samtal[`VisitGroupShapeStart`](../../../aspose.words/documentvisitor/visitgroupshapestart/) , ringer sedan[`Accept`](../../../aspose.words/node/accept/) för alla underformer till denna gruppform och anrop[`VisitGroupShapeEnd`](../../../aspose.words/documentvisitor/visitgroupshapeend/) i slutet.

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

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [GroupShape](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
