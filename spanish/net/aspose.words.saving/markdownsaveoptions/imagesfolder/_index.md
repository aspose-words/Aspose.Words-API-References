---
title: MarkdownSaveOptions.ImagesFolder
linktitle: ImagesFolder
articleTitle: ImagesFolder
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad ImagesFolder de MarkdownSaveOptions mejora las exportaciones de sus documentos al especificar la carpeta ideal para guardar imágenes en formato Markdown.
type: docs
weight: 80
url: /es/net/aspose.words.saving/markdownsaveoptions/imagesfolder/
---
## MarkdownSaveOptions.ImagesFolder property

Especifica la carpeta física donde se guardan las imágenes al exportar un documento a Markdown Formato. El valor predeterminado es una cadena vacía.

```csharp
public string ImagesFolder { get; set; }
```

## Observaciones

Cuando guardas un[`Document`](../../../aspose.words/document/) enMarkdownformato, Aspose.Words necesita guardar todas las imágenes incrustadas en el documento como archivos independientes. `ImagesFolder` le permite especificar dónde se guardarán las imágenes.

Si guarda un documento en un archivo y proporciona un nombre de archivo, Aspose.Words, de forma predeterminada, guarda las imágenes en la misma carpeta donde se guarda el documento.`ImagesFolder` para anular este comportamiento.

Si guarda un documento en una secuencia, Aspose.Words no tiene una carpeta donde guardar las imágenes, pero aun así necesita guardarlas en algún lugar. En este caso, debe especificar una carpeta accesible en el`ImagesFolder` propiedad.

Si la carpeta especificada por`ImagesFolder` no existe, se creará automáticamente.

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
