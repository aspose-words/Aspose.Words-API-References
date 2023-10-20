---
title: ImageSavingArgs.IsImageAvailable
linktitle: IsImageAvailable
articleTitle: IsImageAvailable
second_title: Aspose.Words para .NET
description: ImageSavingArgs IsImageAvailable propiedad. Devolucionesverdadero si la imagen actual está disponible para exportar en C#.
type: docs
weight: 50
url: /es/net/aspose.words.saving/imagesavingargs/isimageavailable/
---
## ImageSavingArgs.IsImageAvailable property

Devoluciones`verdadero` si la imagen actual está disponible para exportar.

```csharp
public bool IsImageAvailable { get; }
```

## Observaciones

Algunas imágenes del documento pueden no estar disponibles, por ejemplo, porque image está vinculada y el vínculo es inaccesible o no apunta a una imagen válida. En este caso Aspose.Words exporta un icono con una cruz roja. Esta propiedad devuelve `verdadero` si la imagen original está disponible; devoluciones`FALSO`si la imagen original no está disponible y se ofrecerá un icono de "sin imagen" para guardar.

Al guardar una forma de grupo o una forma que no requiere ninguna imagen, esta propiedad siempre está`verdadero`.

## Ejemplos

Muestra cómo involucrar una devolución de llamada para guardar imágenes en un proceso de conversión HTML.

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

* property [CurrentShape](../currentshape/)
* class [ImageSavingArgs](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
