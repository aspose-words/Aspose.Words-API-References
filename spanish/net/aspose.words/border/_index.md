---
title: Border Class
linktitle: Border
articleTitle: Border
second_title: Aspose.Words para .NET
description: Descubre la clase Aspose.Words.Border, tu solución ideal para personalizar los bordes de objetos en tus documentos. ¡Mejora tus proyectos con precisión y estilo!
type: docs
weight: 270
url: /es/net/aspose.words/border/
---
## Border class

Representa un borde de un objeto.

Para obtener más información, visite el[Programación con documentos](https://docs.aspose.com/words/net/programming-with-documents/) Artículo de documentación.

```csharp
public class Border : InternableComplexAttr
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Color](../../aspose.words/border/color/) { get; set; } | Obtiene o establece el color del borde. |
| [DistanceFromText](../../aspose.words/border/distancefromtext/) { get; set; } | Obtiene o establece la distancia del borde desde el texto o desde el borde de la página en puntos. |
| [IsVisible](../../aspose.words/border/isvisible/) { get; } | Devuelve`verdadero` Si el[`LineStyle`](./linestyle/) no esNone . |
| [LineStyle](../../aspose.words/border/linestyle/) { get; set; } | Obtiene o establece el estilo del borde. |
| [LineWidth](../../aspose.words/border/linewidth/) { get; set; } | Obtiene o establece el ancho del borde en puntos. |
| [Shadow](../../aspose.words/border/shadow/) { get; set; } | Obtiene o establece un valor que indica si el borde tiene sombra. |
| [ThemeColor](../../aspose.words/border/themecolor/) { get; set; } | Obtiene o establece el color del tema en el esquema de color aplicado que está asociado con este objeto Border. |
| [TintAndShade](../../aspose.words/border/tintandshade/) { get; set; } | Obtiene o establece un valor doble que aclara u oscurece un color. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [ClearFormatting](../../aspose.words/border/clearformatting/)() | Restablece las propiedades del borde a los valores predeterminados. |
| [Equals](../../aspose.words/border/equals/#equals)(*Border*) | Determina si el borde especificado tiene el mismo valor que el borde actual. |
| override [Equals](../../aspose.words/border/equals/#equals_1)(*object*) | Determina si el objeto especificado es igual en valor al objeto actual. |
| override [GetHashCode](../../aspose.words/border/gethashcode/)() | Sirve como una función hash para este tipo. |

## Observaciones

Los bordes se pueden aplicar a varios elementos del documento, incluidos párrafos, secciones de texto dentro de un párrafo o una celda de una tabla.

## Ejemplos

Muestra cómo insertar una cadena rodeada por un borde en un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Write("Text surrounded by green border.");

doc.Save(ArtifactsDir + "Border.FontBorder.docx");
```

Muestra cómo insertar un párrafo con un borde superior.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders.Top;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;
// Establezca ThemeColor solo cuando se configure LineWidth o LineStyle.
topBorder.ThemeColor = ThemeColor.Accent1;
topBorder.TintAndShade = 0.25d;

builder.Writeln("Text with a top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Ver también

* class [InternableComplexAttr](../internablecomplexattr/)
* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
