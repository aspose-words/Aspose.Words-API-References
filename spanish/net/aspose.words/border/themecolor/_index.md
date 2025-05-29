---
title: Border.ThemeColor
linktitle: ThemeColor
articleTitle: ThemeColor
second_title: Aspose.Words para .NET
description: Descubra cómo utilizar la propiedad Border ThemeColor para personalizar su esquema de colores y mejorar su diseño con temas vibrantes y personalizados.
type: docs
weight: 70
url: /es/net/aspose.words/border/themecolor/
---
## Border.ThemeColor property

Obtiene o establece el color del tema en el esquema de color aplicado que está asociado con este objeto Border.

```csharp
public ThemeColor ThemeColor { get; set; }
```

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

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Border](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
