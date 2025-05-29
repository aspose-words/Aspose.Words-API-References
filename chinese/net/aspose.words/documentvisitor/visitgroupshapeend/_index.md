---
title: DocumentVisitor.VisitGroupShapeEnd
linktitle: VisitGroupShapeEnd
articleTitle: VisitGroupShapeEnd
second_title: Aspose.Words for .NET
description: 探索 DocumentVisitor VisitGroupShapeEnd 方法，该方法有效地发出组形状枚举结束的信号，从而实现无缝文档处理。
type: docs
weight: 260
url: /zh/net/aspose.words/documentvisitor/visitgroupshapeend/
---
## DocumentVisitor.VisitGroupShapeEnd method

当组形状的枚举结束时调用。

```csharp
public virtual VisitorAction VisitGroupShapeEnd(GroupShape groupShape)
```

| 范围 | 类型 | 描述 |
| --- | --- | --- |
| groupShape | GroupShape | 正在访问的对象。 |

### 返回值

一个[`VisitorAction`](../../visitoraction/)指定如何继续枚举的值。

## 例子

展示如何创建一组形状，并使用文档访问器打印其内容。

```csharp
public void GroupOfShapes()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // 如果需要创建“非原始”形状，例如 SingleCornerSnipped、TopCornersSnipped、DiagonalCornersSnipped，
    // 顶角一个圆角一个截角、单角圆角、顶角圆角、对角角圆角
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
* 命名空间 [Aspose.Words](../../../aspose.words/)
* 部件 [Aspose.Words](../../../)
