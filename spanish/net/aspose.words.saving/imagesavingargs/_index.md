---
title: Class ImageSavingArgs
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Saving.ImageSavingArgs clase. Proporciona datos para elImageSaving evento.
type: docs
weight: 4980
url: /es/net/aspose.words.saving/imagesavingargs/
---
## ImageSavingArgs class

Proporciona datos para el[`ImageSaving`](../iimagesavingcallback/imagesaving/) evento.

```csharp
public class ImageSavingArgs
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [CurrentShape](../../aspose.words.saving/imagesavingargs/currentshape/) { get; } | Obtiene el[`ShapeBase`](../../aspose.words.drawing/shapebase/) objeto correspondiente a la forma o grupo de formas que se va a guardar. |
| [Document](../../aspose.words.saving/imagesavingargs/document/) { get; } | Obtiene el objeto de documento que se está guardando actualmente. |
| [ImageFileName](../../aspose.words.saving/imagesavingargs/imagefilename/) { get; set; } | Obtiene o establece el nombre del archivo (sin la ruta) donde se guardará la imagen. |
| [ImageStream](../../aspose.words.saving/imagesavingargs/imagestream/) { get; set; } | Permite especificar el flujo donde se guardará la imagen. |
| [IsImageAvailable](../../aspose.words.saving/imagesavingargs/isimageavailable/) { get; } | Devoluciones`verdadero` si la imagen actual está disponible para exportar. |
| [KeepImageStreamOpen](../../aspose.words.saving/imagesavingargs/keepimagestreamopen/) { get; set; } | Especifica si Aspose.Words debe mantener la transmisión abierta o cerrarla después de guardar una imagen. |

### Observaciones

De manera predeterminada, cuando Aspose.Words guarda un documento en HTML, guarda cada imagen en en un archivo separado. Aspose.Words usa el nombre de archivo del documento y un número único para generar un nombre de archivo único para cada imagen encontrada en el documento.

`ImageSavingArgs` permite redefinir cómo se generan los nombres de archivo de imagen o eludir por completo el guardado de imágenes en archivos proporcionando sus propios objetos de flujo.

Para aplicar su propia lógica para generar nombres de archivo de imagen, use [`ImageFileName`](./imagefilename/) ,[`CurrentShape`](./currentshape/) y[`IsImageAvailable`](./isimageavailable/) propiedades.

Para guardar imágenes en secuencias en lugar de archivos, utilice el[`ImageStream`](./imagestream/) propiedad.

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

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)


