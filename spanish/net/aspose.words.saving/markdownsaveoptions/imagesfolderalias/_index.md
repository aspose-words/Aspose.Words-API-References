---
title: MarkdownSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: Aspose.Words para .NET
description: Descubre la propiedad ImagesFolderAlias de MarkdownSaveOptions para gestionar fácilmente las URI de imágenes en tus documentos. ¡Optimiza tu flujo de trabajo con esta función esencial!
type: docs
weight: 90
url: /es/net/aspose.words.saving/markdownsaveoptions/imagesfolderalias/
---
## MarkdownSaveOptions.ImagesFolderAlias property

Especifica el nombre de la carpeta utilizada para construir las URI de imágenes escritas en un documento. El valor predeterminado es una cadena vacía.

```csharp
public string ImagesFolderAlias { get; set; }
```

## Observaciones

Cuando guardas un[`Document`](../../../aspose.words/document/) enMarkdown formato, Aspose.Words necesita guardar todas las imágenes incrustadas en el documento como archivos independientes. [`ImagesFolder`](../imagesfolder/) le permite especificar dónde se guardarán las imágenes y `ImagesFolderAlias` permite especificar cómo se construirán las URI de las imágenes.

Si`ImagesFolderAlias` no es una cadena vacía, entonces la URI de la imagen escrita en Markdown seráImagesFolderAlias + &lt;nombre del archivo de imagen&gt;.

Si`ImagesFolderAlias` es una cadena vacía, entonces la URI de la imagen escrita en Markdown seráImagesFolder + &lt;nombre del archivo de imagen&gt;.

Si`ImagesFolderAlias` se establece en '.' (punto), entonces el nombre del archivo de imagen se escribirá en Markdown sin ruta, independientemente de otras opciones.

## Ejemplos

Muestra cómo especificar el nombre de la carpeta utilizada para construir URI de imágenes.

```csharp
DocumentBuilder builder = new DocumentBuilder();

builder.Writeln("Some image below:");
builder.InsertImage(ImageDir + "Logo.jpg");

string imagesFolder = Path.Combine(ArtifactsDir, "ImagesDir");
MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
// Utilice la propiedad "ImagesFolder" para asignar una carpeta en el sistema de archivos local en la que
// Aspose.Words guardará todas las imágenes vinculadas del documento.
saveOptions.ImagesFolder = imagesFolder;
// Utilice la propiedad "ImagesFolderAlias" para usar esta carpeta
// al construir URI de imágenes en lugar del nombre de la carpeta de imágenes.
saveOptions.ImagesFolderAlias = "http://ejemplo.com/imagenes";

builder.Document.Save(ArtifactsDir + "MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

### Ver también

* class [MarkdownSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
