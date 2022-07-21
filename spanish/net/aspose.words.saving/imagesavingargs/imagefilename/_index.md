---
title: ImageFileName
second_title: Referencia de API de Aspose.Words para .NET
description: Obtiene o establece el nombre del archivo sin la ruta donde se guardará la imagen.
type: docs
weight: 30
url: /es/net/aspose.words.saving/imagesavingargs/imagefilename/
---
## ImageSavingArgs.ImageFileName property

Obtiene o establece el nombre del archivo (sin la ruta) donde se guardará la imagen.

```csharp
public string ImageFileName { get; set; }
```

### Observaciones

Esta propiedad le permite redefinir cómo se generan los nombres de archivo de imagen durante la exportación a HTML.

Cuando se activa el evento, esta propiedad contiene el nombre de archivo que Aspose.Words generó . Puede cambiar el valor de esta propiedad para guardar la imagen en un archivo diferente. Tenga en cuenta que los nombres de los archivos deben ser únicos.

Aspose.Words genera automáticamente un nombre de archivo único para cada imagen incrustada al exportar a formato HTML. La forma en que se genera el nombre del archivo de imagen depende de si guarda el documento en un archivo o en una secuencia.

Al guardar un documento en un archivo, el nombre del archivo de imagen generado se ve como &lt;nombre de archivo base del documento&gt;.&lt;número de imagen&gt;.&lt;extensión&gt;.

Al guardar un documento en una secuencia, el nombre del archivo de imagen generado se parece a Aspose.Words.&lt;guid del documento&gt;.&lt;número de imagen&gt;.&lt;extensión&gt;.

`ImageFileName` debe contener solo el nombre del archivo sin la ruta. Aspose.Words determina la ruta para guardar y el valor de la`origen`atributo para escribir en HTML usando el nombre de archivo del documento, el[`ImagesFolder`](../../htmlsaveoptions/imagesfolder) y [`ImagesFolderAlias`](../../htmlsaveoptions/imagesfolderalias) propiedades.

### Ejemplos

Muestra cómo dividir un documento en partes y guardarlas.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // Crear un objeto "HtmlFixedSaveOptions", que podemos pasar al método "Guardar" del documento
    // para modificar cómo convertimos el documento a HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Si guardamos el documento normalmente, habrá un HTML de salida
    // documento con todo el contenido del documento fuente.
    // Establecer la propiedad "DocumentSplitCriteria" en "DocumentSplitCriteria.SectionBreak" para
    // guarda nuestro documento en varios archivos HTML: uno para cada sección.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // Asigne una devolución de llamada personalizada a la propiedad "DocumentPartSavingCallback" para modificar la lógica de guardado de la parte del documento.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // Si convertimos un documento que contiene imágenes en html, terminaremos con un archivo html que enlaza con varias imágenes.
    // Cada imagen tendrá la forma de un archivo en el sistema de archivos local.
    // También hay una devolución de llamada que puede personalizar el nombre y la ubicación del sistema de archivos de cada imagen.
    options.ImageSavingCallback = new SavedImageRename(outFileName);

    doc.Save(ArtifactsDir + outFileName, options);
}

/// <summary>
/// Establece nombres de archivo personalizados para los documentos de salida en los que la operación de guardado divide un documento.
/// </summary>
private class SavedDocumentPartRename : IDocumentPartSavingCallback
{
    public SavedDocumentPartRename(string outFileName, DocumentSplitCriteria documentSplitCriteria)
    {
        mOutFileName = outFileName;
        mDocumentSplitCriteria = documentSplitCriteria;
    }

    void IDocumentPartSavingCallback.DocumentPartSaving(DocumentPartSavingArgs args)
    {
        // Podemos acceder a todo el documento de origen a través de la propiedad "Documento".
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        string partType = string.Empty;

        switch (mDocumentSplitCriteria)
        {
            case DocumentSplitCriteria.PageBreak:
                partType = "Page";
                break;
            case DocumentSplitCriteria.ColumnBreak:
                partType = "Column";
                break;
            case DocumentSplitCriteria.SectionBreak:
                partType = "Section";
                break;
            case DocumentSplitCriteria.HeadingParagraph:
                partType = "Paragraph from heading";
                break;
        }

        string partFileName = $"{mOutFileName} part {++mCount}, of type {partType}{Path.GetExtension(args.DocumentPartFileName)}";

        // A continuación hay dos formas de especificar dónde Aspose.Words guardará cada parte del documento.
        // 1 - Establecer un nombre de archivo para el archivo de parte de salida:
        args.DocumentPartFileName = partFileName;

        // 2 - Cree una secuencia personalizada para el archivo de la parte de salida:
        args.DocumentPartStream = new FileStream(ArtifactsDir + partFileName, FileMode.Create);

        Assert.True(args.DocumentPartStream.CanWrite);
        Assert.False(args.KeepDocumentPartStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
    private readonly DocumentSplitCriteria mDocumentSplitCriteria;
}

/// <summary>
/// Establece nombres de archivo personalizados para los archivos de imagen que crea una conversión HTML.
/// </summary>
public class SavedImageRename : IImageSavingCallback
{
    public SavedImageRename(string outFileName)
    {
        mOutFileName = outFileName;
    }

    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        string imageFileName = $"{mOutFileName} shape {++mCount}, of type {args.CurrentShape.ShapeType}{Path.GetExtension(args.ImageFileName)}";

        // A continuación hay dos formas de especificar dónde Aspose.Words guardará cada parte del documento.
        // 1 - Establecer un nombre de archivo para el archivo de imagen de salida:
        args.ImageFileName = imageFileName;

        // 2 - Cree una secuencia personalizada para el archivo de imagen de salida:
        args.ImageStream = new FileStream(ArtifactsDir + imageFileName, FileMode.Create);

        Assert.True(args.ImageStream.CanWrite);
        Assert.True(args.IsImageAvailable);
        Assert.False(args.KeepImageStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
}
```

### Ver también

* class [ImageSavingArgs](../../imagesavingargs)
* espacio de nombres [Aspose.Words.Saving](../../imagesavingargs)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
