---
title: DocumentVisitor.VisitGroupShapeEnd
second_title: Aspose.Words för .NET API Referens
description: DocumentVisitor metod. Anropas när uppräkningen av en gruppform har avslutats.
type: docs
weight: 260
url: /sv/net/aspose.words/documentvisitor/visitgroupshapeend/
---
## DocumentVisitor.VisitGroupShapeEnd method

Anropas när uppräkningen av en gruppform har avslutats.

```csharp
public virtual VisitorAction VisitGroupShapeEnd(GroupShape groupShape)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| groupShape | GroupShape | Objektet som besöks. |

### Returvärde

A[`VisitorAction`](../../visitoraction/) värde som anger hur uppräkningen ska fortsätta.

### Exempel

Visar hur man skapar en grupp av former och skriver ut dess innehåll med hjälp av en dokumentbesökare.

```csharp
public void GroupOfShapes()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Om du behöver skapa "NonPrimitive" former, som SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
    // TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, DiagonalCornersRounded
    // använd DocumentBuilder.InsertShape metoder.
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

* enum [VisitorAction](../../visitoraction/)
* class [GroupShape](../../../aspose.words.drawing/groupshape/)
* class [DocumentVisitor](../)
* namnutrymme [Aspose.Words](../../documentvisitor/)
* hopsättning [Aspose.Words](../../../)


