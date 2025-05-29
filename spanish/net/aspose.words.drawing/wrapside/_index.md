---
title: WrapSide Enum
linktitle: WrapSide
articleTitle: WrapSide
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Drawing.WrapSide para controlar el ajuste del texto alrededor de formas e imágenes, mejorando el diseño y la legibilidad del documento.
type: docs
weight: 1800
url: /es/net/aspose.words.drawing/wrapside/
---
## WrapSide enumeration

Especifica en qué lado(s) de la forma o imagen se ajusta el texto.

```csharp
public enum WrapSide
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Both | `0` | El texto del documento se ajusta en ambos lados de la forma. |
| Left | `1` | El texto del documento se ajusta solo al lado izquierdo de la forma. Hay un área libre de texto a la derecha. |
| Right | `2` | El texto del documento se ajusta solo al lado derecho de la forma. Hay un área libre de texto a la izquierda. |
| Largest | `3` | El texto del documento se ajusta en el lado de la forma que está más alejado del margen de la página, dejando un área libre de texto en el otro lado de la forma. |
| Default | `0` | El valor predeterminado esBoth . |

## Ejemplos

Muestra cómo reemplazar todas las formas de cuadro de texto con formas de imagen.

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

### Ver también

* property [WrapSide](../shapebase/wrapside/)
* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
