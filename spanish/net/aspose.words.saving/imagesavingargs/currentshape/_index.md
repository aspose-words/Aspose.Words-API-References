---
title: ImageSavingArgs.CurrentShape
linktitle: CurrentShape
articleTitle: CurrentShape
second_title: Aspose.Words para .NET
description: ImageSavingArgs CurrentShape propiedad. Obtiene elShapeBase objeto correspondiente a la forma o forma de grupo que está a punto de guardarse en C#.
type: docs
weight: 10
url: /es/net/aspose.words.saving/imagesavingargs/currentshape/
---
## ImageSavingArgs.CurrentShape property

Obtiene el[`ShapeBase`](../../../aspose.words.drawing/shapebase/) objeto correspondiente a la forma o forma de grupo que está a punto de guardarse.

```csharp
public ShapeBase CurrentShape { get; }
```

## Observaciones

[`IImageSavingCallback`](../../iimagesavingcallback/) se puede disparar mientras se guarda una forma o una forma de grupo. Por eso la propiedad tiene[`ShapeBase`](../../../aspose.words.drawing/shapebase/) tipo. Puedes comprobar si es una forma de grupo comparando [`ShapeType`](../../../aspose.words.drawing/shapebase/shapetype/) conGroup o transfiriéndolo a una de las clases derivadas: [`Shape`](../../../aspose.words.drawing/shape/) o[`GroupShape`](../../../aspose.words.drawing/groupshape/).

Aspose.Words utiliza el nombre del archivo del documento y un número único para generar un nombre de archivo único para cada imagen que se encuentra en el documento. Puedes usar el`CurrentShape`propiedad para generar un nombre de archivo "mejor" examinando propiedades de forma como[`Title`](../../../aspose.words.drawing/imagedata/title/) (solo forma),[`SourceFullName`](../../../aspose.words.drawing/imagedata/sourcefullname/) (Solo forma) y[`Name`](../../../aspose.words.drawing/shapebase/name/). Por supuesto, puede crear nombres de archivos utilizando cualquier otra propiedad o criterio , pero tenga en cuenta que los nombres de archivos subsidiarios deben ser únicos dentro de la operación de exportación.

Algunas imágenes del documento pueden no estar disponibles. Para verificar la disponibilidad de la imagen use el[`IsImageAvailable`](../isimageavailable/) propiedad.

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

* class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* class [ImageSavingArgs](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
