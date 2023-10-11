---
title: ParagraphFormat.Shading
second_title: Referencia de API de Aspose.Words para .NET
description: ParagraphFormat propiedad. Devuelve unShading objeto que hace referencia al formato de sombreado del párrafo.
type: docs
weight: 280
url: /es/net/aspose.words/paragraphformat/shading/
---
## ParagraphFormat.Shading property

Devuelve un[`Shading`](../../shading/) objeto que hace referencia al formato de sombreado del párrafo.

```csharp
public Shading Shading { get; }
```

### Ejemplos

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

* class [Shading](../../shading/)
* class [ParagraphFormat](../)
* espacio de nombres [Aspose.Words](../../paragraphformat/)
* asamblea [Aspose.Words](../../../)


