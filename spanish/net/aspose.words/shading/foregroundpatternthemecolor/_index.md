---
title: Shading.ForegroundPatternThemeColor
linktitle: ForegroundPatternThemeColor
articleTitle: ForegroundPatternThemeColor
second_title: Aspose.Words para .NET
description: Descubra cómo personalizar la propiedad Shading ForegroundPatternThemeColor para mejorar el esquema de colores de su diseño y elevar su atractivo visual.
type: docs
weight: 50
url: /es/net/aspose.words/shading/foregroundpatternthemecolor/
---
## Shading.ForegroundPatternThemeColor property

Obtiene o establece el color del tema del patrón de primer plano en el esquema de color aplicado que está asociado con este[`Shading`](../) objeto.

```csharp
public ThemeColor ForegroundPatternThemeColor { get; set; }
```

## Ejemplos

Muestra cómo establecer los colores de primer plano y de fondo para la textura de sombreado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shading shading = doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Shading;
shading.Texture = TextureIndex.Texture12Pt5Percent;
shading.ForegroundPatternThemeColor = ThemeColor.Dark1;
shading.BackgroundPatternThemeColor = ThemeColor.Dark2;

shading.ForegroundTintAndShade = 0.5;
shading.BackgroundTintAndShade = -0.2;

builder.Font.Border.Color = Color.Green;
builder.Font.Border.LineWidth = 2.5d;
builder.Font.Border.LineStyle = LineStyle.DashDotStroker;

builder.Writeln("Foreground and background pattern colors for shading texture.");

doc.Save(ArtifactsDir + "Font.ForegroundAndBackground.docx");
```

### Ver también

* enum [ThemeColor](../../../aspose.words.themes/themecolor/)
* class [Shading](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
