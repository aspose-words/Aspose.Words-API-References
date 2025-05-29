---
title: RelativeVerticalSize Enum
linktitle: RelativeVerticalSize
articleTitle: RelativeVerticalSize
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Drawing.RelativeVerticalSize, que define los cálculos de altura vertical para formas y marcos de texto, mejorando la precisión del diseño del documento.
type: docs
weight: 1610
url: /es/net/aspose.words.drawing/relativeverticalsize/
---
## RelativeVerticalSize enumeration

Especifica con relación a qué se calcula verticalmente la altura de una forma o un marco de texto.

```csharp
public enum RelativeVerticalSize
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Margin | `0` | Especifica que la altura se calcula en relación con el espacio entre los márgenes superior e inferior. |
| Page | `1` | Especifica que la altura se calcula en relación con la altura de la página. |
| TopMargin | `2` | Especifica que la altura se calcula en relación con el tamaño del área del margen superior. |
| BottomMargin | `3` | Especifica que la altura se calcula en relación con el tamaño del área del margen inferior. |
| InnerMargin | `4` | Especifica que la altura se calcula en relación con el tamaño del área del margen interior, con el tamaño del área del margen superior para las páginas impares y con el tamaño del área del margen inferior para las páginas pares. |
| OuterMargin | `5` | Especifica que la altura se calcula en relación con el tamaño del área del margen exterior, con el tamaño del área del margen inferior para las páginas impares y con el tamaño del área del margen superior para las páginas pares. |
| Default | `1` | El valor predeterminado esMargin . |

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

* property [RelativeVerticalSize](../shapebase/relativeverticalsize/)
* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)
