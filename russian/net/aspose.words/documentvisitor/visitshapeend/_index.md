---
title: DocumentVisitor.VisitShapeEnd
linktitle: VisitShapeEnd
articleTitle: VisitShapeEnd
second_title: Aspose.Words для .NET
description: Изучите метод DocumentVisitor VisitShapeEnd, необходимый для управления перечислением фигур в ваших приложениях. Повысьте эффективность кодирования сегодня!
type: docs
weight: 390
url: /ru/net/aspose.words/documentvisitor/visitshapeend/
---
## DocumentVisitor.VisitShapeEnd method

Вызывается, когда перечисление фигуры завершено.

```csharp
public virtual VisitorAction VisitShapeEnd(Shape shape)
```

| Параметр | Тип | Описание |
| --- | --- | --- |
| shape | Shape | Посещаемый объект. |

### Возвращаемое значение

А[`VisitorAction`](../../visitoraction/) значение, указывающее, как продолжить перечисление.

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

* enum [VisitorAction](../../visitoraction/)
* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentVisitor](../)
* пространство имен [Aspose.Words](../../../aspose.words/)
* сборка [Aspose.Words](../../../)
