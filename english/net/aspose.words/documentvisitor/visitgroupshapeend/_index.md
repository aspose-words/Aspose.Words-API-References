---
title: DocumentVisitor.VisitGroupShapeEnd
linktitle: VisitGroupShapeEnd
second_title: Aspose.Words for .NET API Reference
description: DocumentVisitor VisitGroupShapeEnd method. Called when enumeration of a group shape has ended in C#.
type: docs
weight: 260
url: /net/aspose.words/documentvisitor/visitgroupshapeend/
---
## VisitGroupShapeEnd method

Called when enumeration of a group shape has ended.

```csharp
public virtual VisitorAction VisitGroupShapeEnd(GroupShape groupShape)
```

| Parameter | Type | Description |
| --- | --- | --- |
| groupShape | GroupShape | The object that is being visited. |

### Return Value

A [`VisitorAction`](../../visitoraction/) value that specifies how to continue the enumeration.

## Examples

Shows how to create a group of shapes, and print its contents using a document visitor.

```csharp
public void GroupOfShapes()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // If you need to create "NonPrimitive" shapes, such as SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
    // TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, DiagonalCornersRounded
    // please use DocumentBuilder.InsertShape methods.
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
/// Prints the contents of a visited shape group to the console.
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

### See Also

* enum [VisitorAction](../../visitoraction/)
* class [GroupShape](../../../aspose.words.drawing/groupshape/)
* class [DocumentVisitor](../)
* namespace [Aspose.Words](../../documentvisitor/)
* assembly [Aspose.Words](../../../)
