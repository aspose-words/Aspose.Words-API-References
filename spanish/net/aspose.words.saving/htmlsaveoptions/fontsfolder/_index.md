---
title: HtmlSaveOptions.FontsFolder
linktitle: FontsFolder
articleTitle: FontsFolder
second_title: Aspose.Words para .NET
description: HtmlSaveOptions FontsFolder propiedad. Especifica la carpeta física donde se guardan las fuentes al exportar un documento a HTML. El valor predeterminado es una cadena vacía en C#.
type: docs
weight: 310
url: /es/net/aspose.words.saving/htmlsaveoptions/fontsfolder/
---
## HtmlSaveOptions.FontsFolder property

Especifica la carpeta física donde se guardan las fuentes al exportar un documento a HTML. El valor predeterminado es una cadena vacía.

```csharp
public string FontsFolder { get; set; }
```

## Observaciones

Cuando guardas un[`Document`](../../../aspose.words/document/) en formato HTML y[`ExportFontResources`](../exportfontresources/) está configurado en`verdadero` , Aspose.Words necesita guardar las fuentes utilizadas en el documento como archivos independientes. `FontsFolder` le permite especificar dónde se guardarán las fuentes y [`FontsFolderAlias`](../fontsfolderalias/) permite especificar cómo se construirán los URI de fuente.

Si guarda un documento en un archivo y proporciona un nombre de archivo, Aspose.Words, de forma predeterminada, guarda las fuentes en la misma carpeta donde se guarda el archivo del documento. Usar`FontsFolder` para anular este comportamiento.

Si guarda un documento en una secuencia, Aspose.Words no tiene una carpeta donde guardar las fuentes, pero aún necesita guardar las fuentes en algún lugar. En este caso, debe especificar una carpeta accesible en el`FontsFolder` propiedad o proporcionar secuencias personalizadas a través de el[`FontSavingCallback`](../fontsavingcallback/) controlador de eventos.

Si la carpeta especificada por`FontsFolder` no existe, se creará automáticamente.

[`ResourceFolder`](../resourcefolder/) es otra forma de especificar una carpeta donde se deben guardar las fuentes.

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
