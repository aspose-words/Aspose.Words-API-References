---
title: HtmlSaveOptions.ResourceFolder
linktitle: ResourceFolder
articleTitle: ResourceFolder
second_title: Aspose.Words para .NET
description: HtmlSaveOptions ResourceFolder propiedad. Especifica una carpeta física donde se guardan todos los recursos como imágenes fuentes y CSS externo cuando se exporta un documento a HTML. El valor predeterminado es una cadena vacía en C#.
type: docs
weight: 420
url: /es/net/aspose.words.saving/htmlsaveoptions/resourcefolder/
---
## HtmlSaveOptions.ResourceFolder property

Especifica una carpeta física donde se guardan todos los recursos como imágenes, fuentes y CSS externo cuando se exporta un documento a HTML. El valor predeterminado es una cadena vacía.

```csharp
public string ResourceFolder { get; set; }
```

## Observaciones

`ResourceFolder` es la forma más sencilla de especificar una carpeta donde se deben escribir todos los recursos. Otra forma es utilizar propiedades individuales[`FontsFolder`](../fontsfolder/) ,[`ImagesFolder`](../imagesfolder/) , y[`CssStyleSheetFileName`](../cssstylesheetfilename/).

`ResourceFolder` tiene una prioridad más baja que las carpetas especificadas mediante[`FontsFolder`](../fontsfolder/) , [`ImagesFolder`](../imagesfolder/) , y[`CssStyleSheetFileName`](../cssstylesheetfilename/) . Por ejemplo, si ambos `ResourceFolder` y[`FontsFolder`](../fontsfolder/)se especifican, las fuentes se guardarán en[`FontsFolder`](../fontsfolder/) , mientras que las imágenes y CSS se guardarán en`ResourceFolder`.

Si la carpeta especificada por`ResourceFolder` no existe, se creará automáticamente.

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

* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
