---
title: DocumentPartSavingArgs.DocumentPartFileName
linktitle: DocumentPartFileName
articleTitle: DocumentPartFileName
second_title: Aspose.Words para .NET
description: Descubra la propiedad DocumentPartFileName para DocumentPartSavingArgs. Administre fácilmente los nombres de archivo para guardar partes del documento sin problemas y sin rutas.
type: docs
weight: 20
url: /es/net/aspose.words.saving/documentpartsavingargs/documentpartfilename/
---
## DocumentPartSavingArgs.DocumentPartFileName property

Obtiene o establece el nombre del archivo (sin ruta) donde se guardará la parte del documento.

```csharp
public string DocumentPartFileName { get; set; }
```

## Observaciones

Esta propiedad le permite redefinir cómo se generan los nombres de archivos de partes del documento durante la exportación a HTML o EPUB.

Al invocar la devolución de llamada, esta propiedad contiene el nombre del archivo generado por Aspose.Words. Puede cambiar el valor de esta propiedad para guardar la parte del documento en un archivo diferente. Tenga en cuenta que el nombre de archivo de cada parte debe ser único.

`DocumentPartFileName` Debe contener solo el nombre del archivo sin la ruta. Aspose.Words determina la ruta para guardar usando el nombre del archivo del documento. Si no se especificó el nombre del archivo del documento de salida, por ejemplo, al guardar en una secuencia, este nombre se usa solo para referenciar partes del documento. Lo mismo ocurre al guardar en formato EPUB.

## Ejemplos

Muestra cómo dividir un documento en partes y guardarlas.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // Crea un objeto "HtmlFixedSaveOptions", que podemos pasar al método "Guardar" del documento
    // para modificar la forma en que convertimos el documento a HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Si guardamos el documento normalmente, habrá un HTML de salida
    // documento con todo el contenido del documento fuente.
    // Establezca la propiedad "DocumentSplitCriteria" en "DocumentSplitCriteria.SectionBreak" en
    // guardamos nuestro documento en múltiples archivos HTML: uno para cada sección.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // Asigne una devolución de llamada personalizada a la propiedad "DocumentPartSavingCallback" para alterar la lógica de guardado de partes del documento.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // Si convertimos un documento que contiene imágenes a html, terminaremos con un archivo html que enlaza a varias imágenes.
    //Cada imagen tendrá la forma de un archivo en el sistema de archivos local.
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
        //Podemos acceder al documento fuente completo a través de la propiedad "Documento".
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

        A continuación se muestran dos formas de especificar dónde Aspose.Words guardará cada parte del documento.
        // 1 - Establezca un nombre de archivo para el archivo de la parte de salida:
        args.DocumentPartFileName = partFileName;

        // 2 - Crea una secuencia personalizada para el archivo de la parte de salida:
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

        A continuación se muestran dos formas de especificar dónde Aspose.Words guardará cada parte del documento.
        // 1 - Establezca un nombre de archivo para el archivo de imagen de salida:
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
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
