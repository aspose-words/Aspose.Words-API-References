---
title: ImageSavingArgs.CurrentShape
linktitle: CurrentShape
articleTitle: CurrentShape
second_title: Aspose.Words for .NET
description: ImageSavingArgs CurrentShape property. Gets the ShapeBase object corresponding to the shape or group shape that is about to be saved in C#.
type: docs
weight: 10
url: /net/aspose.words.saving/imagesavingargs/currentshape/
---
## ImageSavingArgs.CurrentShape property

Gets the [`ShapeBase`](../../../aspose.words.drawing/shapebase/) object corresponding to the shape or group shape that is about to be saved.

```csharp
public ShapeBase CurrentShape { get; }
```

## Remarks

[`IImageSavingCallback`](../../iimagesavingcallback/) can be fired while saving either a shape or a group shape. That's why the property has [`ShapeBase`](../../../aspose.words.drawing/shapebase/) type. You can check whether it's a group shape comparing [`ShapeType`](../../../aspose.words.drawing/shapebase/shapetype/) with Group or by casting it to one of derived classes: [`Shape`](../../../aspose.words.drawing/shape/) or [`GroupShape`](../../../aspose.words.drawing/groupshape/).

Aspose.Words uses the document file name and a unique number to generate unique file name for each image found in the document. You can use the `CurrentShape` property to generate a "better" file name by examining shape properties such as [`Title`](../../../aspose.words.drawing/imagedata/title/) (Shape only), [`SourceFullName`](../../../aspose.words.drawing/imagedata/sourcefullname/) (Shape only) and [`Name`](../../../aspose.words.drawing/shapebase/name/). Of course you can build file names using any other properties or criteria but note that subsidiary file names must be unique within the export operation.

Some images in the document can be unavailable. To check image availability use the [`IsImageAvailable`](../isimageavailable/) property.

## Examples

Shows how to involve an image saving callback in an HTML conversion process.

```csharp
public void ImageSavingCallback()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // When we save the document to HTML, we can pass a SaveOptions object to designate a callback
    // to customize the image saving process.
    HtmlSaveOptions options = new HtmlSaveOptions();
    options.ImageSavingCallback = new ImageShapePrinter();

    doc.Save(ArtifactsDir + "HtmlSaveOptions.ImageSavingCallback.html", options);
}

/// <summary>
/// Prints the properties of each image as the saving process saves it to an image file in the local file system
/// during the exporting of a document to HTML.
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

### See Also

* class [ShapeBase](../../../aspose.words.drawing/shapebase/)
* class [ImageSavingArgs](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
