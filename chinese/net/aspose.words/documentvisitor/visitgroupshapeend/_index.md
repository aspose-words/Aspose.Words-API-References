---
title: DocumentVisitor.VisitGroupShapeEnd
second_title: Aspose.Words for .NET API 参考
description: DocumentVisitor 方法. 当组形状枚举结束时调用
type: docs
weight: 260
url: /zh/net/aspose.words/documentvisitor/visitgroupshapeend/
---
## DocumentVisitor.VisitGroupShapeEnd method

当组形状枚举结束时调用。

```csharp
public virtual VisitorAction VisitGroupShapeEnd(GroupShape groupShape)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| groupShape | GroupShape | 正在访问的对象。 |

### 返回值

A[`VisitorAction`](../../visitoraction/)指定如何继续枚举的值。

### 例子

演示如何创建一组形状，并使用文档访问者打印其内容。

```csharp
public void GroupOfShapes()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // 如果需要创建“NonPrimitive”形状，例如 SingleCornerSnipped、TopCornersSnipped、DiagonalCornersSnipped，
    // TopCornersOneRoundedOneSnipped、SingleCornerRounded、TopCornersRounded、DiagonalCornersRounded
    // 请使用 DocumentBuilder.InsertShape 方法。
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
/// 将访问过的形状组的内容打印到控制台。
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

### 也可以看看

* enum [VisitorAction](../../visitoraction/)
* class [GroupShape](../../../aspose.words.drawing/groupshape/)
* class [DocumentVisitor](../)
* 命名空间 [Aspose.Words](../../documentvisitor/)
* 部件 [Aspose.Words](../../../)


