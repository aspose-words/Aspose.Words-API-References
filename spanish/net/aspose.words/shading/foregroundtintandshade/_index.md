---
title: Shading.ForegroundTintAndShade
second_title: Referencia de API de Aspose.Words para .NET
description: Shading propiedad. Obtiene o establece un valor doble que aclara u oscurece el color de un tema de primer plano.
type: docs
weight: 60
url: /es/net/aspose.words/shading/foregroundtintandshade/
---
## Shading.ForegroundTintAndShade property

Obtiene o establece un valor doble que aclara u oscurece el color de un tema de primer plano.

```csharp
public double ForegroundTintAndShade { get; set; }
```

### Observaciones

Los valores permitidos están en el rango de -1 (el más oscuro) a 1 (el más claro) para esta propiedad. Cero (0) es neutral. Intentar establecer esta propiedad en un valor inferior a -1 o superior a 1 da como resultadoArgumentOutOfRangeException.

Establecer esta propiedad para el objeto Sombreado con colores no temáticos da como resultadoInvalidOperationException.

### Ejemplos

Muestra cómo configurar los colores de primer plano y de fondo para sombrear la textura.

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
* espacio de nombres [Aspose.Words](../../shading/)
* asamblea [Aspose.Words](../../../)


