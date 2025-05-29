---
title: ShapeBase.TopRelative
linktitle: TopRelative
articleTitle: TopRelative
second_title: Aspose.Words para .NET
description: Descubra la propiedad ShapeBase TopRelative para gestionar fácilmente la posición de las formas. Ajuste su diseño con valores porcentuales superiores precisos para una distribución óptima.
type: docs
weight: 590
url: /es/net/aspose.words.drawing/shapebase/toprelative/
---
## ShapeBase.TopRelative property

Obtiene o establece el valor que representa la posición superior relativa de la forma en porcentaje.

```csharp
public float TopRelative { get; set; }
```

## Ejemplos

Muestra cómo establecer el tamaño y la posición relativos.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Agregar una forma simple con tamaño y posición absolutos.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 100, 40);
// Establezca WrapType en WrapType.None ya que las formas en línea se convierten automáticamente en unidades absolutas.
shape.WrapType = WrapType.None;

// Comprobación y configuración del tamaño horizontal relativo.
if (shape.RelativeHorizontalSize == RelativeHorizontalSize.Default)
{
    // Establecer el tamaño de encuadernación horizontal en Margen.
    shape.RelativeHorizontalSize = RelativeHorizontalSize.Margin;
    // Establecer el ancho al 50% del ancho del margen.
    shape.WidthRelative = 50;
}

// Comprobación y configuración del tamaño vertical relativo.
if (shape.RelativeVerticalSize == RelativeVerticalSize.Default)
{
    // Establecer el tamaño de encuadernación vertical en Margen.
    shape.RelativeVerticalSize = RelativeVerticalSize.Margin;
    // Establecer la altura al 30% de la altura del margen.
    shape.HeightRelative = 30;
}

// Comprobación y configuración de la posición vertical relativa.
if (shape.RelativeVerticalPosition == RelativeVerticalPosition.Paragraph)
{
    // estableciendo la vinculación de posición a TopMargin.
    shape.RelativeVerticalPosition = RelativeVerticalPosition.TopMargin;
    // Establecer el Top relativo al 30% de la posición TopMargin.
    shape.TopRelative = 30;
}

// Comprobación y ajuste de la posición horizontal relativa.
if (shape.RelativeHorizontalPosition == RelativeHorizontalPosition.Default)
{
    // Establecer la vinculación de posición a RightMargin.
    shape.RelativeHorizontalPosition = RelativeHorizontalPosition.RightMargin;
    //El valor relativo de la posición puede ser negativo.
    shape.LeftRelative = -260;
}

doc.Save(ArtifactsDir + "Shape.RelativeSizeAndPosition.docx");
```

### Ver también

* class [ShapeBase](../)
* espacio de nombres [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../../)
