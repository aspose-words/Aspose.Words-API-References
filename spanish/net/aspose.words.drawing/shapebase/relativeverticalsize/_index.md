---
title: ShapeBase.RelativeVerticalSize
linktitle: RelativeVerticalSize
articleTitle: RelativeVerticalSize
second_title: Aspose.Words para .NET
description: ShapeBase RelativeVerticalSize propiedad. Obtiene o establece el valor del tamaño relativo de la forma en dirección vertical en C#.
type: docs
weight: 450
url: /es/net/aspose.words.drawing/shapebase/relativeverticalsize/
---
## ShapeBase.RelativeVerticalSize property

Obtiene o establece el valor del tamaño relativo de la forma en dirección vertical.

```csharp
public RelativeVerticalSize RelativeVerticalSize { get; set; }
```

## Observaciones

El valor predeterminado esMargin.

Tiene efecto sólo si[`HeightRelative`](../heightrelative/) Está establecido.

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

* enum [RelativeVerticalSize](../../relativeverticalsize/)
* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
