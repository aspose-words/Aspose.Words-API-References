---
title: GroupShape.Accept
linktitle: Accept
articleTitle: Accept
second_title: 用于 .NET 的 Aspose.Words
description: GroupShape Accept 方法. 接受访客 在 C#.
type: docs
weight: 30
url: /zh/net/aspose.words.drawing/groupshape/accept/
---
## GroupShape.Accept method

接受访客。

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| visitor | DocumentVisitor | 将访问节点的访问者。 |

### 返回值

如果访问了所有节点，则为 True；假如果[`DocumentVisitor`](../../../aspose.words/documentvisitor/)在访问所有节点之前停止操作。

## 评论

枚举该节点及其所有子节点。每个节点调用相应的方法[`DocumentVisitor`](../../../aspose.words/documentvisitor/)。

有关更多信息，请参阅访客设计模式。

通话[`VisitGroupShapeStart`](../../../aspose.words/documentvisitor/visitgroupshapestart/)，然后调用[`Accept`](../../../aspose.words/node/accept/)对于该组形状的所有 子形状并调用[`VisitGroupShapeEnd`](../../../aspose.words/documentvisitor/visitgroupshapeend/)最后.

## 例子

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

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [GroupShape](../)
* 命名空间 [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* 部件 [Aspose.Words](../../../)
