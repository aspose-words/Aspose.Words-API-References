---
title: HtmlSaveOptions.ResourceFolderAlias
linktitle: ResourceFolderAlias
articleTitle: ResourceFolderAlias
second_title: Aspose.Words para .NET
description: HtmlSaveOptions ResourceFolderAlias propiedad. Especifica el nombre de la carpeta utilizada para construir los URI de todos los recursos escritos en un documento HTML. El valor predeterminado es una cadena vacía en C#.
type: docs
weight: 430
url: /es/net/aspose.words.saving/htmlsaveoptions/resourcefolderalias/
---
## HtmlSaveOptions.ResourceFolderAlias property

Especifica el nombre de la carpeta utilizada para construir los URI de todos los recursos escritos en un documento HTML. El valor predeterminado es una cadena vacía.

```csharp
public string ResourceFolderAlias { get; set; }
```

## Observaciones

`ResourceFolderAlias` es la forma más sencilla de especificar cómo se deben construir los URI para todos los archivos de recursos. Se puede especificar la misma información para imágenes y fuentes por separado a través de[`ImagesFolderAlias`](../imagesfolderalias/) y[`FontsFolderAlias`](../fontsfolderalias/) propiedades, respectivamente. Sin embargo, no existe ninguna propiedad individual para CSS.

`ResourceFolderAlias` tiene menor prioridad que[`FontsFolderAlias`](../fontsfolderalias/) y[`ImagesFolderAlias`](../imagesfolderalias/) . Por ejemplo, si ambos`ResourceFolderAlias` y[`FontsFolderAlias`](../fontsfolderalias/) se especifican, los URI de las fuentes se construirán usando [`FontsFolderAlias`](../fontsfolderalias/) , mientras que los URI de imágenes y CSS se construirán usando `ResourceFolderAlias`.

Si`ResourceFolderAlias` está vacío, el[`ResourceFolder`](../resourcefolder/)El valor de la propiedad se utilizará para construir URI de recursos.

Si`ResourceFolderAlias` se establece en '.' (punto), los URI de recursos contendrán solo nombres de archivos, sin ninguna ruta.

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
