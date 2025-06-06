---
title: HtmlSaveOptions.FontsFolderAlias
linktitle: FontsFolderAlias
articleTitle: FontsFolderAlias
second_title: Aspose.Words para .NET
description: Descubre la propiedad HtmlSaveOptions FontsFolderAlias para personalizar las URI de fuentes en tus documentos HTML. ¡Mejora tu diseño web fácilmente!
type: docs
weight: 320
url: /es/net/aspose.words.saving/htmlsaveoptions/fontsfolderalias/
---
## HtmlSaveOptions.FontsFolderAlias property

Especifica el nombre de la carpeta utilizada para construir las URI de fuentes escritas en un documento HTML. El valor predeterminado es una cadena vacía.

```csharp
public string FontsFolderAlias { get; set; }
```

## Observaciones

Cuando guardas un[`Document`](../../../aspose.words/document/) en formato HTML y[`ExportFontResources`](../exportfontresources/) está configurado en`verdadero` Aspose.Words necesita guardar las fuentes utilizadas en el documento como archivos independientes. [`FontsFolder`](../fontsfolder/) le permite especificar dónde se guardarán las fuentes y `FontsFolderAlias` permite especificar cómo se construirán las URI de fuentes.

Si`FontsFolderAlias` no es una cadena vacía, entonces el URI de fuente escrito en HTML seráFontsFolderAlias + &lt;nombre del archivo de fuente&gt;.

Si`FontsFolderAlias` es una cadena vacía, entonces el URI de fuente escrito en HTML seráFontsFolder + &lt;nombre del archivo de fuente&gt;.

Si`FontsFolderAlias`se establece en '.' (punto), entonces el nombre del archivo de fuente se escribirá en HTML sin ruta, independientemente de otras opciones.

Una forma alternativa de especificar el nombre de la carpeta para construir la fuente URIs es usar[`ResourceFolderAlias`](../resourcefolderalias/).

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
