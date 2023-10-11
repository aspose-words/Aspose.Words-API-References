---
title: Shading.BackgroundPatternColor
second_title: Referencia de API de Aspose.Words para .NET
description: Shading propiedad. Obtiene o establece el color que se aplica al fondo delShading objeto.
type: docs
weight: 10
url: /es/net/aspose.words/shading/backgroundpatterncolor/
---
## Shading.BackgroundPatternColor property

Obtiene o establece el color que se aplica al fondo del[`Shading`](../) objeto.

```csharp
public Color BackgroundPatternColor { get; set; }
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

* class [Shading](../)
* espacio de nombres [Aspose.Words](../../shading/)
* asamblea [Aspose.Words](../../../)


