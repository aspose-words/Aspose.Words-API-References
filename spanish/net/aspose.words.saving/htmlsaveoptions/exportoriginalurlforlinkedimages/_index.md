---
title: HtmlSaveOptions.ExportOriginalUrlForLinkedImages
linktitle: ExportOriginalUrlForLinkedImages
articleTitle: ExportOriginalUrlForLinkedImages
second_title: Aspose.Words para .NET
description: Descubra la función ExportOriginalUrlForLinkedImages de HtmlSaveOptions, que le permite usar URL originales para las imágenes vinculadas. ¡Mejore la integridad de su documento!
type: docs
weight: 200
url: /es/net/aspose.words.saving/htmlsaveoptions/exportoriginalurlforlinkedimages/
---
## HtmlSaveOptions.ExportOriginalUrlForLinkedImages property

Especifica si se debe utilizar la URL original como URL de las imágenes vinculadas. El valor predeterminado es`FALSO` .

```csharp
public bool ExportOriginalUrlForLinkedImages { get; set; }
```

## Observaciones

Si el valor se establece en`verdadero`[`SourceFullName`](../../../aspose.words.drawing/imagedata/sourcefullname/) El valor se usa como la URL de las imágenes vinculadas y las imágenes vinculadas no se cargan en la carpeta del documento o[`ImagesFolder`](../imagesfolder/).

Si el valor se establece en`FALSO`Las imágenes vinculadas se cargan en la carpeta del documento o[`ImagesFolder`](../imagesfolder/) y la URL de cada imagen vinculada se construye dependiendo de la carpeta del documento,[`ImagesFolder`](../imagesfolder/) y[`ImagesFolderAlias`](../imagesfolderalias/) propiedades.

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

* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
