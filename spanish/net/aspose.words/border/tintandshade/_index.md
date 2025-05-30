---
title: Border.TintAndShade
linktitle: TintAndShade
articleTitle: TintAndShade
second_title: Aspose.Words para .NET
description: Descubre Border TintAndShade ajusta fácilmente el brillo del color con un simple valor doble para lograr impresionantes mejoras de diseño. ¡Perfecto para tus proyectos creativos!
type: docs
weight: 80
url: /es/net/aspose.words/border/tintandshade/
---
## Border.TintAndShade property

Obtiene o establece un valor doble que aclara u oscurece un color.

```csharp
public double TintAndShade { get; set; }
```

### Excepciones

| excepción | condición |
| --- | --- |
| ArgumentOutOfRangeException | Se lanza si intenta establecer esta propiedad en un valor menor que -1 o mayor que 1. |
| InvalidOperationException | Se lanza si se establece esta propiedad para un objeto Border con colores que no sean del tema. |

## Observaciones

Los valores permitidos están en el rango de -1 (el más oscuro) a 1 (el más claro) para esta propiedad. Cero (0) es neutral.

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

* class [Border](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
