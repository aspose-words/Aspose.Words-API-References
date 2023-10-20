---
title: BorderType Enum
linktitle: BorderType
articleTitle: BorderType
second_title: Aspose.Words para .NET
description: Aspose.Words.BorderType enumeración. Especifica los lados de un borde en C#.
type: docs
weight: 100
url: /es/net/aspose.words/bordertype/
---
## BorderType enumeration

Especifica los lados de un borde.

Para obtener más información, visite el[Programación con documentos](https://docs.aspose.com/words/net/programming-with-documents/) artículo de documentación.

```csharp
public enum BorderType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| None | `-1` | Valor predeterminado. |
| Bottom | `0` | Especifica el borde inferior de un párrafo o celda de una tabla. |
| Left | `1` | Especifica el borde izquierdo de un párrafo o celda de una tabla. |
| Right | `2` | Especifica el borde derecho de un párrafo o celda de una tabla. |
| Top | `3` | Especifica el borde superior de un párrafo o celda de una tabla. |
| Horizontal | `4` | Especifica el borde horizontal entre celdas de una tabla o entre párrafos conformes. |
| Vertical | `5` | Especifica el borde vertical entre las celdas de una tabla. |
| DiagonalDown | `6` | Especifica el borde diagonal en una celda de la tabla. |
| DiagonalUp | `7` | Especifica el borde diagonal en una celda de la tabla. |

## Ejemplos

Muestra cómo insertar un párrafo con un borde superior.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Border topBorder = builder.ParagraphFormat.Borders.Top;
topBorder.LineWidth = 4.0d;
topBorder.LineStyle = LineStyle.DashSmallGap;
// Establece ThemeColor solo cuando LineWidth o LineStyle están configurados.
topBorder.ThemeColor = ThemeColor.Accent1;
topBorder.TintAndShade = 0.25d;

builder.Writeln("Text with a top border.");

doc.Save(ArtifactsDir + "Border.ParagraphTopBorder.docx");
```

### Ver también

* espacio de nombres [Aspose.Words](../../aspose.words/)
* asamblea [Aspose.Words](../../)
