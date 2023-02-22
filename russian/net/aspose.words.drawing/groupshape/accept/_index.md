---
title: GroupShape.Accept
second_title: Справочник по API Aspose.Words для .NET
description: GroupShape метод. Принимает посетителя.
type: docs
weight: 30
url: /ru/net/aspose.words.drawing/groupshape/accept/
---
## GroupShape.Accept method

Принимает посетителя.

```csharp
public override bool Accept(DocumentVisitor visitor)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| visitor | DocumentVisitor | Посетитель, который будет посещать узлы. |

### Возвращаемое значение

Истинно, если все узлы были посещены; false, если DocumentVisitor остановил операцию перед посещением всех узлов.

### Примечания

Перечисляет этот узел и все его дочерние элементы. Каждый узел вызывает соответствующий метод в DocumentVisitor.

Дополнительные сведения см. в шаблоне проектирования «Посетитель».

звонки[`VisitGroupShapeStart`](../../../aspose.words/documentvisitor/visitgroupshapestart/) , затем звонит[`Accept`](../../../aspose.words/node/accept/) для всех дочерних форм этой групповой формы и вызовов[`VisitGroupShapeEnd`](../../../aspose.words/documentvisitor/visitgroupshapeend/) в конце.

### Примеры

Показывает, как создать группу фигур и распечатать ее содержимое с помощью посетителя документа.

```csharp
public void GroupOfShapes()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Если вам нужно создать "непримитивные" фигуры, такие как SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
    // TopCornersOneRoundedOneSnipped, SingleCornerRounded, TopCornersRounded, DiagonalCornersRounded
    // используйте методы DocumentBuilder.InsertShape.
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
/// Выводит содержимое посещенной группы форм на консоль.
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

### Смотрите также

* class [DocumentVisitor](../../../aspose.words/documentvisitor/)
* class [GroupShape](../)
* пространство имен [Aspose.Words.Drawing](../../groupshape/)
* сборка [Aspose.Words](../../../)


