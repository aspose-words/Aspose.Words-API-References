---
title: HtmlSaveOptions.ExportOriginalUrlForLinkedImages
second_title: Referencia de API de Aspose.Words para .NET
description: HtmlSaveOptions propiedad. Especifica si la URL original debe usarse como la URL de las imágenes vinculadas. El valor predeterminado esFALSO .
type: docs
weight: 200
url: /es/net/aspose.words.saving/htmlsaveoptions/exportoriginalurlforlinkedimages/
---
## HtmlSaveOptions.ExportOriginalUrlForLinkedImages property

Especifica si la URL original debe usarse como la URL de las imágenes vinculadas. El valor predeterminado es`FALSO` .

```csharp
public bool ExportOriginalUrlForLinkedImages { get; set; }
```

### Observaciones

Si el valor se establece en`verdadero`[`SourceFullName`](../../../aspose.words.drawing/imagedata/sourcefullname/) El valor se utiliza ya que la URL de las imágenes vinculadas y las imágenes vinculadas no se cargan en la carpeta del documento o[`ImagesFolder`](../imagesfolder/).

Si el valor se establece en`FALSO`las imágenes vinculadas se cargan en la carpeta del documento o[`ImagesFolder`](../imagesfolder/) y la URL de cada imagen vinculada se construye dependiendo de la carpeta del documento,[`ImagesFolder`](../imagesfolder/) y[`ImagesFolderAlias`](../imagesfolderalias/) propiedades.

### Ejemplos

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

* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../htmlsaveoptions/)
* asamblea [Aspose.Words](../../../)


