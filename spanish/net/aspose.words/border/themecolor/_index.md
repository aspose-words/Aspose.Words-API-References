---
title: Border.ThemeColor
second_title: Referencia de API de Aspose.Words para .NET
description: Border propiedad. Obtiene o establece el color del tema en el esquema de color aplicado asociado con este objeto Borde.
type: docs
weight: 70
url: /es/net/aspose.words/border/themecolor/
---
## Border.ThemeColor property

Obtiene o establece el color del tema en el esquema de color aplicado asociado con este objeto Borde.

```csharp
public ThemeColor ThemeColor { get; set; }
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

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Border](../)
* espacio de nombres [Aspose.Words](../../border/)
* asamblea [Aspose.Words](../../../)


