---
title: DocumentPartSavingArgs.DocumentPartStream
second_title: Referencia de API de Aspose.Words para .NET
description: DocumentPartSavingArgs propiedad. Permite especificar la secuencia donde se guardará la parte del documento.
type: docs
weight: 30
url: /es/net/aspose.words.saving/documentpartsavingargs/documentpartstream/
---
## DocumentPartSavingArgs.DocumentPartStream property

Permite especificar la secuencia donde se guardará la parte del documento.

```csharp
public Stream DocumentPartStream { get; set; }
```

### Observaciones

Esta propiedad le permite guardar partes del documento en secuencias en lugar de archivos durante la exportación HTML.

El valor predeterminado es`nulo` . Cuando esta propiedad es`nulo` , la parte del documento se guardará en un archivo especificado en el[`DocumentPartFileName`](../documentpartfilename/) propiedad.

Cuando se solicita guardar en una secuencia en formato HTML[`Save`](../../../aspose.words/document/save/) o[`Save`](../../../aspose.words/document/save/) y la primera parte del documento está a punto de guardarse, Aspose.Words sugiere aquí el flujo de salida principal pasado inicialmente por la persona que llama.

Al guardar en formato EPUB, que es un formato contenedor basado en HTML,`DocumentPartStream` No se puede especificar porque todas las partes subsidiarias se encapsularán en un único paquete de salida.

### Ejemplos

Muestra cómo dividir un documento en partes y guardarlas.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // Crea un objeto "HtmlFixedSaveOptions", que podemos pasar al método "Guardar" del documento
    // para modificar cómo convertimos el documento a HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Si guardamos el documento normalmente, habrá un HTML de salida
    // documento con todo el contenido del documento fuente.
    // Establece la propiedad "DocumentSplitCriteria" en "DocumentSplitCriteria.SectionBreak" para
    // guarda nuestro documento en varios archivos HTML: uno para cada sección.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // Asigne una devolución de llamada personalizada a la propiedad "DocumentPartSavingCallback" para modificar la lógica de guardado de partes del documento.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // Si convertimos un documento que contiene imágenes a html, terminaremos con un archivo html que enlaza con varias imágenes.
    // Cada imagen tendrá la forma de un archivo en el sistema de archivos local.
    // También hay una devolución de llamada que puede personalizar el nombre y la ubicación del sistema de archivos de cada imagen.
    options.ImageSavingCallback = new SavedImageRename(outFileName);

    doc.Save(ArtifactsDir + outFileName, options);
}

/// <summary>
/// Establece nombres de archivos personalizados para los documentos de salida en los que la operación de guardado divide un documento.
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
        // Podemos acceder al documento fuente completo a través de la propiedad "Documento".
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

        // A continuación se muestran dos formas de especificar dónde Aspose.Words guardará cada parte del documento.
        // 1 - Establece un nombre de archivo para el archivo de pieza de salida:
        args.DocumentPartFileName = partFileName;

        // 2 - Crea una secuencia personalizada para el archivo de pieza de salida:
        args.DocumentPartStream = new FileStream(ArtifactsDir + partFileName, FileMode.Create);

        Assert.True(args.DocumentPartStream.CanWrite);
        Assert.False(args.KeepDocumentPartStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
    private readonly DocumentSplitCriteria mDocumentSplitCriteria;
}

/// <summary>
/// Establece nombres de archivos personalizados para los archivos de imagen que crea una conversión HTML.
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

        // A continuación se muestran dos formas de especificar dónde Aspose.Words guardará cada parte del documento.
        // 1 - Establece un nombre de archivo para el archivo de imagen de salida:
        args.ImageFileName = imageFileName;

        // 2 - Crea una secuencia personalizada para el archivo de imagen de salida:
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

* class [DocumentPartSavingArgs](../)
* espacio de nombres [Aspose.Words.Saving](../../documentpartsavingargs/)
* asamblea [Aspose.Words](../../../)


