---
title: ParagraphFormat.Borders
second_title: Referencia de API de Aspose.Words para .NET
description: ParagraphFormat propiedad. Obtiene la colección de bordes del párrafo.
type: docs
weight: 60
url: /es/net/aspose.words/paragraphformat/borders/
---
## ParagraphFormat.Borders property

Obtiene la colección de bordes del párrafo.

```csharp
public BorderCollection Borders { get; }
```

### Ejemplos

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

* class [BorderCollection](../../bordercollection/)
* class [ParagraphFormat](../)
* espacio de nombres [Aspose.Words](../../paragraphformat/)
* asamblea [Aspose.Words](../../../)


