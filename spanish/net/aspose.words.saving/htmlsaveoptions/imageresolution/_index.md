---
title: HtmlSaveOptions.ImageResolution
linktitle: ImageResolution
articleTitle: ImageResolution
second_title: Aspose.Words para .NET
description: Ajuste la resolución de la imagen fácilmente con HtmlSaveOptions. Optimice sus exportaciones HTML, MHTML o EPUB con configuraciones personalizables para obtener imágenes impactantes.
type: docs
weight: 340
url: /es/net/aspose.words.saving/htmlsaveoptions/imageresolution/
---
## HtmlSaveOptions.ImageResolution property

Especifica la resolución de salida de las imágenes al exportar a HTML, MHTML o EPUB. El valor predeterminado es`96 ppp` .

```csharp
public int ImageResolution { get; set; }
```

## Observaciones

Esta propiedad afecta a las imágenes rasterizadas cuando[`ScaleImageToShapeSize`](../scaleimagetoshapesize/) es`verdadero` Y metarchivos de efectos exportados como imágenes rasterizadas. Algunas propiedades de imagen, como cropping o rotación, requieren guardar las imágenes transformadas; en este caso, las imágenes transformadas se crean con la resolución dada .

## Ejemplos

Muestra cómo configurar carpetas y alias de carpetas para recursos guardados externamente que Aspose.Words creará al guardar un documento en HTML.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlSaveOptions options = new HtmlSaveOptions
{
    CssStyleSheetType = CssStyleSheetType.External,
    ExportFontResources = true,
    ImageResolution = 72,
    FontResourcesSubsettingSizeThreshold = 0,
    FontsFolder = ArtifactsDir + "Fonts",
    ImagesFolder = ArtifactsDir + "Images",
    ResourceFolder = ArtifactsDir + "Resources",
    FontsFolderAlias = "http://ejemplo.com/fuentes",
    ImagesFolderAlias = "http://ejemplo.com/imágenes",
    ResourceFolderAlias = "http://ejemplo.com/recursos",
    ExportOriginalUrlForLinkedImages = true
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.FolderAlias.html", options);
```

### Ver también

* property [ScaleImageToShapeSize](../scaleimagetoshapesize/)
* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
