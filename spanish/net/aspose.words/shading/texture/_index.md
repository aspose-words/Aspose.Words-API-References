---
title: Shading.Texture
linktitle: Texture
articleTitle: Texture
second_title: Aspose.Words para .NET
description: Descubre la propiedad Textura de Sombreado para realzar tus diseños. Personaliza y configura texturas fácilmente para lograr efectos visuales impactantes en tus proyectos.
type: docs
weight: 70
url: /es/net/aspose.words/shading/texture/
---
## Shading.Texture property

Obtiene o establece la textura de sombreado.

```csharp
public TextureIndex Texture { get; set; }
```

## Ejemplos

Muestra cómo decorar texto con bordes y sombreado.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

BorderCollection borders = builder.ParagraphFormat.Borders;
borders.DistanceFromText = 20;
borders[BorderType.Left].LineStyle = LineStyle.Double;
borders[BorderType.Right].LineStyle = LineStyle.Double;
borders[BorderType.Top].LineStyle = LineStyle.Double;
borders[BorderType.Bottom].LineStyle = LineStyle.Double;

Shading shading = builder.ParagraphFormat.Shading;
shading.Texture = TextureIndex.TextureDiagonalCross;
shading.BackgroundPatternColor = Color.LightCoral;
shading.ForegroundPatternColor = Color.LightSalmon;

builder.Write("This paragraph is formatted with a double border and shading.");
doc.Save(ArtifactsDir + "DocumentBuilder.ApplyBordersAndShading.docx");
```

### Ver también

* enum [TextureIndex](../../textureindex/)
* class [Shading](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
