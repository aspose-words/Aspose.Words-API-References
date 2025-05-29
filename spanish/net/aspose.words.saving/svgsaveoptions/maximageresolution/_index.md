---
title: SvgSaveOptions.MaxImageResolution
linktitle: MaxImageResolution
articleTitle: MaxImageResolution
second_title: Aspose.Words para .NET
description: Controle la calidad de sus imágenes raster exportadas con la opción SvgSaveOptions MaxImageResolution. Configure la densidad de píxeles para obtener resultados óptimos. El valor predeterminado es 0.
type: docs
weight: 50
url: /es/net/aspose.words.saving/svgsaveoptions/maximageresolution/
---
## SvgSaveOptions.MaxImageResolution property

Obtiene o establece un valor en píxeles por pulgada que limita la resolución de las imágenes rasterizadas exportadas. El valor predeterminado es cero.

```csharp
public int MaxImageResolution { get; set; }
```

## Observaciones

Si el valor de esta propiedad no es cero, limita la resolución de las imágenes raster exportadas. Es decir, las imágenes de mayor resolución se remuestrean hasta el límite y las imágenes de menor resolución se exportan tal como están.

Si el valor de esta propiedad es cero, todas las imágenes raster se exportan sin remuestreo.

## Ejemplos

Muestra cómo establecer un límite para la resolución de la imagen.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.MaxImageResolution = 72;

doc.Save(ArtifactsDir + "SvgSaveOptions.MaxImageResolution.svg", saveOptions);
```

### Ver también

* class [SvgSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
