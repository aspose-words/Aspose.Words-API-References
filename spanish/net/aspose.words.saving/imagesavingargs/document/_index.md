---
title: ImageSavingArgs.Document
second_title: Referencia de API de Aspose.Words para .NET
description: ImageSavingArgs propiedad. Obtiene el objeto de documento que se está guardando actualmente.
type: docs
weight: 20
url: /es/net/aspose.words.saving/imagesavingargs/document/
---
## ImageSavingArgs.Document property

Obtiene el objeto de documento que se está guardando actualmente.

```csharp
public Document Document { get; }
```

### Ejemplos

Muestra cómo involucrar una devolución de llamada para guardar imágenes en un proceso de conversión de HTML.

```csharp
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Cuando guardamos el documento en HTML, podemos pasar un objeto SaveOptions para designar una devolución de llamada
    // para personalizar el proceso de guardado de imágenes.
    HtmlSaveOptions options = new HtmlSaveOptions();
    options.ImageSavingCallback = new ImageShapePrinter();

    doc.Save(ArtifactsDir + "HtmlSaveOptions.ImageSavingCallback.html", options);
}

/// <summary>
/// Imprime las propiedades de cada imagen a medida que el proceso de guardado la guarda en un archivo de imagen en el sistema de archivos local
/// durante la exportación de un documento a HTML.
/// </summary>
private class ImageShapePrinter : IImageSavingCallback
{
    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        args.KeepImageStreamOpen = false;
        Assert.True(args.IsImageAvailable);

        Console.WriteLine($"{args.Document.OriginalFileName.Split('\\').Last()} Image #{++mImageCount}");

        LayoutCollector layoutCollector = new LayoutCollector(args.Document);

        Console.WriteLine($"\tOn page:\t{layoutCollector.GetStartPageIndex(args.CurrentShape)}");
        Console.WriteLine($"\tDimensions:\t{args.CurrentShape.Bounds}");
        Console.WriteLine($"\tAlignment:\t{args.CurrentShape.VerticalAlignment}");
        Console.WriteLine($"\tWrap type:\t{args.CurrentShape.WrapType}");
        Console.WriteLine($"Output filename:\t{args.ImageFileName}\n");
    }

    private int mImageCount;
}
```

### Ver también

* class [Document](../../../aspose.words/document/)
* class [ImageSavingArgs](../)
* espacio de nombres [Aspose.Words.Saving](../../imagesavingargs/)
* asamblea [Aspose.Words](../../../)


