---
title: HtmlSaveOptions.ResourceFolderAlias
linktitle: ResourceFolderAlias
articleTitle: ResourceFolderAlias
second_title: Aspose.Words para .NET
description: Optimice sus documentos HTML con la propiedad HtmlSaveOptions ResourceFolderAlias, que define nombres de carpetas para una construcción URI eficiente de los recursos.
type: docs
weight: 450
url: /es/net/aspose.words.saving/htmlsaveoptions/resourcefolderalias/
---
## HtmlSaveOptions.ResourceFolderAlias property

Especifica el nombre de la carpeta utilizada para construir las URI de todos los recursos escritos en un documento HTML. El valor predeterminado es una cadena vacía.

```csharp
public string ResourceFolderAlias { get; set; }
```

## Observaciones

`ResourceFolderAlias` Es la forma más sencilla de especificar cómo se deben construir las URI de todos los archivos de recursos. La misma información se puede especificar para imágenes y fuentes por separado mediante[`ImagesFolderAlias`](../imagesfolderalias/) y[`FontsFolderAlias`](../fontsfolderalias/) propiedades, respectivamente. Sin embargo, no existe ninguna propiedad individual para CSS.

`ResourceFolderAlias` tiene menor prioridad que[`FontsFolderAlias`](../fontsfolderalias/) y[`ImagesFolderAlias`](../imagesfolderalias/) . Por ejemplo, si ambos`ResourceFolderAlias` y[`FontsFolderAlias`](../fontsfolderalias/) se especifican, las URI de las fuentes se construirán utilizando [`FontsFolderAlias`](../fontsfolderalias/) mientras que las URI de las imágenes y CSS se construirán utilizando `ResourceFolderAlias`.

Si`ResourceFolderAlias` está vacío, el[`ResourceFolder`](../resourcefolder/) El valor de la propiedad se utilizará para construir URI de recursos.

Si`ResourceFolderAlias` se establece en '.' (punto), las URI de recursos contendrán solo nombres de archivos, sin ninguna ruta.

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
