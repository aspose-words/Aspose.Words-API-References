---
title: NodeCollection.ToArray
second_title: Справочник по API Aspose.Words для .NET
description: NodeCollection метод. Копирует все узлы из коллекции в новый массив узлов.
type: docs
weight: 110
url: /ru/net/aspose.words/nodecollection/toarray/
---
## NodeCollection.ToArray method

Копирует все узлы из коллекции в новый массив узлов.

```csharp
public Node[] ToArray()
```

### Возвращаемое значение

Массив узлов.

### Примечания

Вы не должны добавлять/удалять узлы при переборе коллекции узлов, потому что это делает итератор недействительным и требует обновления для живых коллекций.

Чтобы иметь возможность добавлять/удалять узлы во время итерации, используйте этот метод для копирования узлов в массив фиксированного размера, а затем выполните итерацию по массиву.

### Примеры

Показывает, как заменить все фигуры текстового поля фигурами изображения.

```csharp
Document doc = new Document(MyDir + "Textboxes in drawing canvas.docx");

Shape[] shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(3, shapes.Count(s => s.ShapeType == ShapeType.TextBox));
Assert.AreEqual(1, shapes.Count(s => s.ShapeType == ShapeType.Image));

foreach (Shape shape in shapes)
{
    if (shape.ShapeType == ShapeType.TextBox)
    {
        Shape replacementShape = new Shape(doc, ShapeType.Image);
        replacementShape.ImageData.SetImage(ImageDir + "Logo.jpg");
        replacementShape.Left = shape.Left;
        replacementShape.Top = shape.Top;
        replacementShape.Width = shape.Width;
        replacementShape.Height = shape.Height;
        replacementShape.RelativeHorizontalPosition = shape.RelativeHorizontalPosition;
        replacementShape.RelativeVerticalPosition = shape.RelativeVerticalPosition;
        replacementShape.HorizontalAlignment = shape.HorizontalAlignment;
        replacementShape.VerticalAlignment = shape.VerticalAlignment;
        replacementShape.WrapType = shape.WrapType;
        replacementShape.WrapSide = shape.WrapSide;

        shape.ParentNode.InsertAfter(replacementShape, shape);
        shape.Remove();
    }
}

shapes = doc.GetChildNodes(NodeType.Shape, true).OfType<Shape>().ToArray();

Assert.AreEqual(0, shapes.Count(s => s.ShapeType == ShapeType.TextBox));
Assert.AreEqual(4, shapes.Count(s => s.ShapeType == ShapeType.Image));

doc.Save(ArtifactsDir + "Shape.ReplaceTextboxesWithImages.docx");
```

### Смотрите также

* class [Node](../../node/)
* class [NodeCollection](../)
* пространство имен [Aspose.Words](../../nodecollection/)
* сборка [Aspose.Words](../../../)


