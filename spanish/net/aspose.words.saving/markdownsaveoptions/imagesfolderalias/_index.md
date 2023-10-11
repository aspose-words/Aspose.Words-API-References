---
title: MarkdownSaveOptions.ImagesFolderAlias
second_title: Referencia de API de Aspose.Words para .NET
description: MarkdownSaveOptions propiedad. Especifica el nombre de la carpeta utilizada para construir los URI de imágenes escritos en un documento. El valor predeterminado es una cadena vacía.
type: docs
weight: 50
url: /es/net/aspose.words.saving/markdownsaveoptions/imagesfolderalias/
---
## MarkdownSaveOptions.ImagesFolderAlias property

Especifica el nombre de la carpeta utilizada para construir los URI de imágenes escritos en un documento. El valor predeterminado es una cadena vacía.

```csharp
public string ImagesFolderAlias { get; set; }
```

### Observaciones

Cuando guardas un[`Document`](../../../aspose.words/document/) enMarkdown formato, Aspose.Words necesita guardar todas las imágenes incrustadas en el documento como archivos independientes. [`ImagesFolder`](../imagesfolder/) le permite especificar dónde se guardarán las imágenes y `ImagesFolderAlias` permite especificar cómo se construirán los URI de la imagen.

Si`ImagesFolderAlias` no es una cadena vacía, entonces el URI de la imagen escrito en Markdown seráImagesFolderAlias + &lt;nombre de archivo de imagen&gt;.

Si`ImagesFolderAlias` es una cadena vacía, entonces el URI de la imagen escrito en Markdown seráCarpeta de imágenes + &lt;nombre de archivo de imagen&gt;.

Si`ImagesFolderAlias`se establece en '.' (punto), el archivo de imagen name se escribirá en Markdown sin ruta, independientemente de otras opciones.

### Ejemplos

Muestra cómo especificar el nombre de la carpeta utilizada para construir URI de imágenes.

```csharp
DocumentBuilder builder = new DocumentBuilder();

builder.Writeln("Some image below:");
Image image = Image.FromFile(ImageDir + "Logo.jpg");
builder.InsertImage(image);

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
// Utilice la propiedad "ImagesFolder" para asignar una carpeta en el sistema de archivos local en la que
// Aspose.Words guardará todas las imágenes vinculadas del documento.
saveOptions.ImagesFolder = ArtifactsDir + "ImagesDir/";
// Usa la propiedad "ImagesFolderAlias" para usar esta carpeta
// al construir URI de imágenes en lugar del nombre de la carpeta de imágenes.
saveOptions.ImagesFolderAlias = "http://ejemplo.com/imagenes";

builder.Document.Save(ArtifactsDir + "MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

Muestra cómo especificar el nombre de la carpeta utilizada para construir URI de imágenes (.NetStandard 2.0).

```csharp
DocumentBuilder builder = new DocumentBuilder();

builder.Writeln("Some image below:");
using (SKBitmap bitmap = SKBitmap.Decode(ImageDir + "Logo.jpg"))
    builder.InsertImage(bitmap);

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
// Utilice la propiedad "ImagesFolder" para asignar una carpeta en el sistema de archivos local en la que
// Aspose.Words guardará todas las imágenes vinculadas del documento.
saveOptions.ImagesFolder = ArtifactsDir + "ImagesDir/";
// Usa la propiedad "ImagesFolderAlias" para usar esta carpeta
// al construir URI de imágenes en lugar del nombre de la carpeta de imágenes.
saveOptions.ImagesFolderAlias = "http://ejemplo.com/imagenes";

builder.Document.Save(ArtifactsDir + "MarkdownSaveOptions.ImagesFolder.md", saveOptions);
```

### Ver también

* class [MarkdownSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../markdownsaveoptions/)
* asamblea [Aspose.Words](../../../)


