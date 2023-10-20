---
title: HtmlSaveOptions.ImageResolution
linktitle: ImageResolution
articleTitle: ImageResolution
second_title: Aspose.Words para .NET
description: HtmlSaveOptions ImageResolution propiedad. Especifica la resolución de salida de las imágenes al exportar a HTML MHTML o EPUB. El valor predeterminado es96 ppp  en C#.
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

Esta propiedad afecta a las imágenes rasterizadas cuando[`ScaleImageToShapeSize`](../scaleimagetoshapesize/) es`verdadero` y metarchivos de efectos exportados como imágenes rasterizadas. Algunas propiedades de la imagen, como cropping o rotación, requieren guardar imágenes transformadas y, en este caso, las imágenes transformadas se crean con la resolución dada .

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
    FontsFolderAlias = "http://ejemplo.com/fonts",
    ImagesFolderAlias = "http://ejemplo.com/imagenes",
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
