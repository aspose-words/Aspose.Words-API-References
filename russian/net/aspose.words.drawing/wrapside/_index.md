---
title: WrapSide Enum
linktitle: WrapSide
articleTitle: WrapSide
second_title: Aspose.Words для .NET
description: Aspose.Words.Drawing.WrapSide перечисление. Указывает какие стороны фигуры или изображения обтекает текст на С#.
type: docs
weight: 1390
url: /ru/net/aspose.words.drawing/wrapside/
---
## WrapSide enumeration

Указывает, какие стороны фигуры или изображения обтекает текст.

```csharp
public enum WrapSide
```

### Ценности

| Имя | Ценность | Описание |
| --- | --- | --- |
| Both | `0` | Текст документа обтекает обе стороны фигуры. |
| Left | `1` | Текст документа переносится только на левую сторону фигуры. Справа от фигуры есть область без текста. . |
| Right | `2` | Текст документа переносится только на правую сторону фигуры. В левой части фигуры есть область без текста. . |
| Largest | `3` | Текст документа переносится на ту сторону фигуры, которая находится дальше всего от края страницы, оставляя свободную от текста область на другой стороне фигуры. |
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
