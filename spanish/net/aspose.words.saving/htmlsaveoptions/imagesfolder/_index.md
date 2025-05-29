---
title: HtmlSaveOptions.ImagesFolder
linktitle: ImagesFolder
articleTitle: ImagesFolder
second_title: Aspose.Words para .NET
description: Descubra la propiedad ImagesFolder de HtmlSaveOptions. Configure fácilmente la carpeta donde guardar imágenes al exportar documentos a HTML. ¡Optimice su flujo de trabajo hoy mismo!
type: docs
weight: 360
url: /es/net/aspose.words.saving/htmlsaveoptions/imagesfolder/
---
## HtmlSaveOptions.ImagesFolder property

Especifica la carpeta física donde se guardan las imágenes al exportar un documento al formato HTML. El valor predeterminado es una cadena vacía.

```csharp
public string ImagesFolder { get; set; }
```

## Observaciones

Cuando guardas un[`Document`](../../../aspose.words/document/) En formato HTML, Aspose.Words necesita guardar todas las imágenes incrustadas en el documento como archivos independientes.`ImagesFolder` le permite especificar dónde se guardarán las imágenes y[`ImagesFolderAlias`](../imagesfolderalias/) permite especificar cómo se construirán las URI de las imágenes.

Si guarda un documento en un archivo y proporciona un nombre de archivo, Aspose.Words, de forma predeterminada, guarda las imágenes en la misma carpeta donde se guarda el archivo del documento. Utilice`ImagesFolder` para anular este comportamiento.

Si guarda un documento en una secuencia, Aspose.Words no tiene una carpeta donde guardar las imágenes, pero aun así necesita guardarlas en algún lugar. En este caso, debe especificar una carpeta accesible en el archivo.`ImagesFolder` propiedad o proporcionar secuencias personalizadas a través de el[`ImageSavingCallback`](../imagesavingcallback/) controlador de eventos.

Si la carpeta especificada por`ImagesFolder` no existe, se creará automáticamente.

[`ResourceFolder`](../resourcefolder/) Es otra forma de especificar una carpeta donde se deben guardar las imágenes.

## Ejemplos

Muestra cómo especificar la carpeta para almacenar las imágenes vinculadas después de guardarlas en .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// Establezca una opción para exportar los campos de formulario como texto simple en lugar de elementos de entrada HTML.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

### Ver también

* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
