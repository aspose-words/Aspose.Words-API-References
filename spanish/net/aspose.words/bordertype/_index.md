---
title: BorderType Enum
linktitle: BorderType
articleTitle: BorderType
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.BorderType para personalizar los bordes. ¡Mejore sus documentos con un control y estilo precisos de los bordes!
type: docs
weight: 290
url: /es/net/aspose.words/bordertype/
---
## BorderType enumeration

Especifica los lados de un borde.

Para obtener más información, visite el[Programación con documentos](https://docs.aspose.com/words/net/programming-with-documents/) Artículo de documentación.

```csharp
public enum BorderType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `-1` | Valor predeterminado. |
| Bottom | `0` | Especifica el borde inferior de un párrafo o una celda de tabla. |
| Left | `1` | Especifica el borde izquierdo de un párrafo o una celda de tabla. |
| Right | `2` | Especifica el borde derecho de un párrafo o de una celda de tabla. |
| Top | `3` | Especifica el borde superior de un párrafo o una celda de tabla. |
| Horizontal | `4` | Especifica el borde horizontal entre celdas de una tabla o entre párrafos conformes. |
| Vertical | `5` | Especifica el borde vertical entre celdas de una tabla. |
| DiagonalDown | `6` | Especifica el borde diagonal en una celda de tabla. |
| DiagonalUp | `7` | Especifica el borde diagonal en una celda de tabla. |

## Ejemplos

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

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
