---
title: ShapeBase.HeightRelative
linktitle: HeightRelative
articleTitle: HeightRelative
second_title: Aspose.Words para .NET
description: ShapeBase HeightRelative propiedad. Obtiene o establece el valor que representa el porcentaje de la altura relativa de la forma en C#.
type: docs
weight: 210
url: /es/net/aspose.words.drawing/shapebase/heightrelative/
---
## ShapeBase.HeightRelative property

Obtiene o establece el valor que representa el porcentaje de la altura relativa de la forma.

```csharp
public float HeightRelative { get; set; }
```

## Ejemplos

Muestra cómo establecer el tamaño y la posición relativos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Agregar una forma simple con tamaño y posición absolutos.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 40);
// Establezca WrapType en WrapType.None ya que las formas en línea se convierten automáticamente a unidades absolutas.
shape.WrapType = WrapType.None;

// Comprobando y configurando el tamaño horizontal relativo.
if (shape.RelativeHorizontalSize == RelativeHorizontalSize.Default)
{
    // Establecer el enlace de tamaño horizontal en Margen.
    shape.RelativeHorizontalSize = RelativeHorizontalSize.Margin;
    // Estableciendo el ancho al 50% del ancho del margen.
    shape.WidthRelative = 50;
}

// Comprobando y configurando el tamaño vertical relativo.
if (shape.RelativeVerticalSize == RelativeVerticalSize.Default)
{
    // Establecer el enlace de tamaño vertical en Margen.
    shape.RelativeVerticalSize = RelativeVerticalSize.Margin;
    // Estableciendo la altura al 30% de la altura del margen.
    shape.HeightRelative = 30;
}

// Comprobando y configurando la posición vertical relativa.
if (shape.RelativeVerticalPosition == RelativeVerticalPosition.Paragraph)
{
    // configurando la posición vinculante a TopMargin.
    shape.RelativeVerticalPosition = RelativeVerticalPosition.TopMargin;
    // Estableciendo el Top relativo al 30% de la posición TopMargin.
    shape.TopRelative = 30;
}

// Comprobando y configurando la posición horizontal relativa.
if (shape.RelativeHorizontalPosition == RelativeHorizontalPosition.Default)
{
    // Estableciendo la posición vinculante a RightMargin.
    shape.RelativeHorizontalPosition = RelativeHorizontalPosition.RightMargin;
    // El valor relativo de la posición puede ser negativo.
    shape.LeftRelative = -260;
}

doc.Save(ArtifactsDir + "Shape.RelativeSizeAndPosition.docx");
```

### Ver también

* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
