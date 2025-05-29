---
title: Shading.ForegroundTintAndShade
linktitle: ForegroundTintAndShade
articleTitle: ForegroundTintAndShade
second_title: Aspose.Words para .NET
description: Ajuste la propiedad ForegroundTintAndShade para aclarar u oscurecer sin esfuerzo los colores de su tema, mejorando el atractivo visual de su diseño.
type: docs
weight: 60
url: /es/net/aspose.words/shading/foregroundtintandshade/
---
## Shading.ForegroundTintAndShade property

Obtiene o establece un valor doble que aclara u oscurece un color de tema de primer plano.

```csharp
public double ForegroundTintAndShade { get; set; }
```

### Excepciones

| excepción | condición |
| --- | --- |
| ArgumentOutOfRangeException | Se lanza si se establece esta propiedad en un valor menor que -1 o mayor que 1. |
| InvalidOperationException | Se lanza si se establece esta propiedad para el objeto de sombreado con colores que no sean del tema. |

## Observaciones

Los valores permitidos están en el rango de -1 (el más oscuro) a 1 (el más claro) para esta propiedad.

Cero (0) es neutral.

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

* class [Shading](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
