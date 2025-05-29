---
title: GraphicsQualityOptions.CompositingMode
linktitle: CompositingMode
articleTitle: CompositingMode
second_title: Aspose.Words para .NET
description: Descubra la propiedad GraphicsQualityOptions CompositingMode para optimizar la forma en que se renderizan las imágenes, mejorando el rendimiento y la calidad de sus gráficos.
type: docs
weight: 20
url: /es/net/aspose.words.saving/graphicsqualityoptions/compositingmode/
---
## GraphicsQualityOptions.CompositingMode property

Obtiene o establece un valor que especifica cómo se dibujan las imágenes compuestas en este Graphics.

```csharp
public CompositingMode? CompositingMode { get; set; }
```

## Ejemplos

Muestra cómo configurar las opciones de calidad de renderizado al convertir documentos a formatos de imagen.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

GraphicsQualityOptions qualityOptions = new GraphicsQualityOptions
{
    SmoothingMode = SmoothingMode.AntiAlias,
    TextRenderingHint = TextRenderingHint.ClearTypeGridFit,
    CompositingMode = CompositingMode.SourceOver,
    CompositingQuality = CompositingQuality.HighQuality,
    InterpolationMode = InterpolationMode.High,
    StringFormat = StringFormat.GenericTypographic
};

ImageSaveOptions saveOptions = new ImageSaveOptions(SaveFormat.Jpeg);
saveOptions.GraphicsQualityOptions = qualityOptions;

doc.Save(ArtifactsDir + "ImageSaveOptions.GraphicsQuality.jpg", saveOptions);
```

### Ver también

* class [GraphicsQualityOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
