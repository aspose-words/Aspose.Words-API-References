---
title: ImageSavingArgs.ImageStream
linktitle: ImageStream
articleTitle: ImageStream
second_title: Aspose.Words for .NET
description: Discover the ImageStream property in ImageSavingArgs to easily specify where to save your images, enhancing your workflow and efficiency.
type: docs
weight: 40
url: /net/aspose.words.saving/imagesavingargs/imagestream/
---
## ImageSavingArgs.ImageStream property

Allows to specify the stream where the image will be saved to.

```csharp
public Stream ImageStream { get; set; }
```

## Remarks

This property allows you to save images to streams instead of files during HTML.

The default value is `null`. When this property is `null`, the image will be saved to a file specified in the [`ImageFileName`](../imagefilename/) property.

Using [`IImageSavingCallback`](../../iimagesavingcallback/) you cannot substitute one image with another. It is intended only for control over location where to save images.

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
        Assert.That(args.IsImageAvailable, Is.True);

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

* class [ImageSavingArgs](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
