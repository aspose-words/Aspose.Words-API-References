---
title: Enum RelativeVerticalSize
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Drawing.RelativeVerticalSize enumeración. Especifica en relación con qué altura de una forma o un marco de texto se calcula verticalmente.
type: docs
weight: 1220
url: /es/net/aspose.words.drawing/relativeverticalsize/
---
## RelativeVerticalSize enumeration

Especifica en relación con qué altura de una forma o un marco de texto se calcula verticalmente.

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
| InnerMargin | `4` | Especifica que la altura se calcula en relación con el tamaño del área del margen interior, con el tamaño del área del margen superior para páginas impares y con el tamaño del área del margen inferior para páginas pares. |
| OuterMargin | `5` | Especifica que la altura se calcula en relación con el tamaño del área del margen exterior, con el tamaño del área del margen inferior para páginas impares y con el tamaño del área del margen superior para páginas pares. |
| Default | `1` | El valor predeterminado esMargin . |

### Ejemplos

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

* property [RelativeVerticalSize](../shapebase/relativeverticalsize/)
* espacio de nombres [Aspose.Words.Drawing](../../aspose.words.drawing/)
* asamblea [Aspose.Words](../../)


