---
title: WrapSide Enum
linktitle: WrapSide
articleTitle: WrapSide
second_title: Aspose.Words для .NET
description: Откройте для себя перечисление Aspose.Words.Drawing.WrapSide для управления обтеканием текстом фигур и изображений, что улучшает компоновку документа и его читабельность.
type: docs
weight: 1800
url: /ru/net/aspose.words.drawing/wrapside/
---
## WrapSide enumeration

Указывает, вокруг какой стороны(сторон) фигуры или изображения будет обтекаться текст.

```csharp
public enum WrapSide
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Both | `0` | Текст документа обтекает обе стороны фигуры. |
| Left | `1` | Текст документа обтекает только левую сторону фигуры. Справа от фигуры есть область, свободная от текста. |
| Right | `2` | Текст документа обтекает только правую сторону фигуры. С левой стороны фигуры есть область, свободная от текста. |
| Largest | `3` | Текст документа обтекает ту сторону фигуры, которая находится дальше всего от поля страницы, оставляя свободную от текста область с другой стороны фигуры. |
| Default | `0` | Значение по умолчанию:Both . |

## Примеры

Показывает, как заменить все фигуры текстовых полей фигурами изображений.

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

* property [WrapSide](../shapebase/wrapside/)
* пространство имен [Aspose.Words.Drawing](../../aspose.words.drawing/)
* сборка [Aspose.Words](../../)
