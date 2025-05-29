---
title: HtmlSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: Aspose.Words para .NET
description: Descubra la propiedad HtmlSaveOptions ImagesFolderAlias para gestionar fácilmente las URI de imágenes en sus documentos HTML. ¡Simplifique su flujo de trabajo con esta función esencial!
type: docs
weight: 370
url: /es/net/aspose.words.saving/htmlsaveoptions/imagesfolderalias/
---
## HtmlSaveOptions.ImagesFolderAlias property

Especifica el nombre de la carpeta utilizada para construir las URI de imágenes escritas en un documento HTML. El valor predeterminado es una cadena vacía.

```csharp
public string ImagesFolderAlias { get; set; }
```

## Observaciones

Cuando guardas un[`Document`](../../../aspose.words/document/) En formato HTML, Aspose.Words necesita guardar todas las imágenes incrustadas en el documento como archivos independientes.[`ImagesFolder`](../imagesfolder/) le permite especificar dónde se guardarán las imágenes y`ImagesFolderAlias` permite especificar cómo se construirán las URI de las imágenes.

Si`ImagesFolderAlias` no es una cadena vacía, entonces la URI de la imagen escrita en HTML seráImagesFolderAlias + &lt;nombre del archivo de imagen&gt;.

Si`ImagesFolderAlias`es una cadena vacía, entonces la URI de la imagen escrita en HTML seráImagesFolder + &lt;nombre del archivo de imagen&gt;.

Si`ImagesFolderAlias` se establece en '.' (punto), entonces el nombre del archivo de imagen se escribirá en HTML sin ruta, independientemente de otras opciones.

Una forma alternativa de especificar el nombre de la carpeta para construir la imagen URIs es usar[`ResourceFolderAlias`](../resourcefolderalias/).

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
