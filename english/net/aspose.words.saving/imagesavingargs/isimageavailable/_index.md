---
title: ImageSavingArgs.IsImageAvailable
second_title: Aspose.Words for .NET API Reference
description: ImageSavingArgs property. Returns true if the current image is available for export in C#.
type: docs
weight: 50
url: /net/aspose.words.saving/imagesavingargs/isimageavailable/
---
## ImageSavingArgs.IsImageAvailable property

Returns `true` if the current image is available for export.

```csharp
public bool IsImageAvailable { get; }
```

## Remarks

Some images in the document can be unavailable, for example, because the image is linked and the link is inaccessible or does not point to a valid image. In this case Aspose.Words exports an icon with a red cross. This property returns `true` if the original image is available; returns `false` if the original image is not available and a "no image" icon will be offered for save.

When saving a group shape or a shape that doesn't require any image this property is always `true`.

## Examples

Shows how to involve an image saving callback in an HTML conversion process.

```csharp
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

* property [CurrentShape](../currentshape/)
* class [ImageSavingArgs](../)
* namespace [Aspose.Words.Saving](../../imagesavingargs/)
* assembly [Aspose.Words](../../../)
