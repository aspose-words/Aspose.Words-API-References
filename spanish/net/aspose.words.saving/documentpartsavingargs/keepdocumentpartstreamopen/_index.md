---
title: DocumentPartSavingArgs.KeepDocumentPartStreamOpen
second_title: Referencia de API de Aspose.Words para .NET
description: DocumentPartSavingArgs propiedad. Especifica si Aspose.Words debe mantener el flujo abierto o cerrarlo después de guardar una parte del documento.
type: docs
weight: 40
url: /es/net/aspose.words.saving/documentpartsavingargs/keepdocumentpartstreamopen/
---
## DocumentPartSavingArgs.KeepDocumentPartStreamOpen property

Especifica si Aspose.Words debe mantener el flujo abierto o cerrarlo después de guardar una parte del documento.

```csharp
public bool KeepDocumentPartStreamOpen { get; set; }
```

### Observaciones

El valor predeterminado es`falso` y Aspose.Words cerrará la transmisión que proporcionó en el[`DocumentPartStream`](../documentpartstream/) propiedad después de escribir una parte del documento en ella. Especificar`verdadero` para mantener la corriente abierta. Tenga en cuenta que el flujo de salida principal proporcionado en la llamada a[`Save`](../../../aspose.words/document/save/)[`Save`](../../../aspose.words/document/save/) nunca será cerrado por Aspose.Words incluso si`KeepDocumentPartStreamOpen` se establece en`falso`.

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

* class [DocumentPartSavingArgs](../)
* espacio de nombres [Aspose.Words.Saving](../../documentpartsavingargs/)
* asamblea [Aspose.Words](../../../)


