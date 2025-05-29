---
title: GroupShape.Accept
linktitle: Accept
articleTitle: Accept
second_title: Aspose.Words для .NET
description: Откройте для себя метод GroupShape Accept для беспрепятственного привлечения посетителей и улучшения пользовательского опыта на вашем сайте. Повысьте взаимодействие сегодня!
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
| visitor | DocumentVisitor | Посетитель, который посетит узлы. |

### Возвращаемое значение

True, если все узлы были посещены; false, если[`DocumentVisitor`](../../../aspose.words/documentvisitor/) остановил операцию до посещения всех узлов.

## Примечания

Перечисляет этот узел и всех его потомков. Каждый узел вызывает соответствующий метод на[`DocumentVisitor`](../../../aspose.words/documentvisitor/).

Более подробную информацию см. в шаблоне проектирования «Посетитель».

Звонки[`VisitGroupShapeStart`](../../../aspose.words/documentvisitor/visitgroupshapestart/) , затем звонит[`Accept`](../../../aspose.words/node/accept/) для всех дочерних фигур этой групповой фигуры и вызовов[`VisitGroupShapeEnd`](../../../aspose.words/documentvisitor/visitgroupshapeend/) в конце.

## Примеры

Показывает, как создать группу фигур и распечатать ее содержимое с помощью посетителя документа.

```csharp
public void GroupOfShapes()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    // Если вам нужно создать «непримитивные» фигуры, такие как SingleCornerSnipped, TopCornersSnipped, DiagonalCornersSnipped,
    // ВерхниеУглыОдинЗакругленныйОдинОбрезанный, ОдинЗакругленныйУгол, ВерхниеУглыЗакругленные, ДиагональныеУглыЗакругленные
    // пожалуйста, используйте методы DocumentBuilder.InsertShape.
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
/// Выводит содержимое посещенной группы фигур на консоль.
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
* пространство имен [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* сборка [Aspose.Words](../../../)
