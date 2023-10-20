---
title: Border.TintAndShade
linktitle: TintAndShade
articleTitle: TintAndShade
second_title: Aspose.Words para .NET
description: Border TintAndShade propiedad. Obtiene o establece un valor doble que aclara u oscurece un color en C#.
type: docs
weight: 80
url: /es/net/aspose.words/border/tintandshade/
---
## Border.TintAndShade property

Obtiene o establece un valor doble que aclara u oscurece un color.

```csharp
public double TintAndShade { get; set; }
```

## Observaciones

Los valores permitidos están en el rango de -1 (el más oscuro) a 1 (el más claro) para esta propiedad. Cero (0) es neutral. Intentar establecer esta propiedad en un valor inferior a -1 o superior a 1 da como resultadoArgumentOutOfRangeException.

Establecer esta propiedad para el objeto Borde con colores no temáticos da como resultadoInvalidOperationException.

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

* class [Border](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
