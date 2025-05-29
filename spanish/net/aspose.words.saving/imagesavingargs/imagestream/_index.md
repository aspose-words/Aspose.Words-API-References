---
title: ImageSavingArgs.ImageStream
linktitle: ImageStream
articleTitle: ImageStream
second_title: Aspose.Words para .NET
description: Descubra la propiedad ImageStream en ImageSavingArgs para especificar fácilmente dónde guardar sus imágenes, mejorando su flujo de trabajo y eficiencia.
type: docs
weight: 40
url: /es/net/aspose.words.saving/imagesavingargs/imagestream/
---
## ImageSavingArgs.ImageStream property

Permite especificar la secuencia donde se guardará la imagen.

```csharp
public Stream ImageStream { get; set; }
```

## Observaciones

Esta propiedad le permite guardar imágenes en secuencias en lugar de archivos durante el HTML.

El valor predeterminado es`nulo` . Cuando esta propiedad es`nulo` , la imagen se guardará en un archivo especificado en el[`ImageFileName`](../imagefilename/) propiedad.

Usando[`IImageSavingCallback`](../../iimagesavingcallback/) No se puede sustituir una imagen por otra . Su propósito es únicamente controlar la ubicación donde se guardan las imágenes.

## Ejemplos

Muestra cómo involucrar una devolución de llamada de guardado de imágenes en un proceso de conversión HTML.

```csharp
public void ImageSavingCallback()
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

* class [ImageSavingArgs](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
