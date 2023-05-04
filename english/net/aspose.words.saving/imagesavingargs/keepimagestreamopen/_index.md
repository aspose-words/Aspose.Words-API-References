---
title: ImageSavingArgs.KeepImageStreamOpen
linktitle: KeepImageStreamOpen
articleTitle: KeepImageStreamOpen
second_title: Aspose.Words for .NET
description: ImageSavingArgs KeepImageStreamOpen property. Specifies whether Aspose.Words should keep the stream open or close it after saving an image in C#.
type: docs
weight: 60
url: /net/aspose.words.saving/imagesavingargs/keepimagestreamopen/
---
## ImageSavingArgs.KeepImageStreamOpen property

Specifies whether Aspose.Words should keep the stream open or close it after saving an image.

```csharp
public bool KeepImageStreamOpen { get; set; }
```

## Remarks

Default is `false` and Aspose.Words will close the stream you provided in the [`ImageStream`](../imagestream/) property after writing an image into it. Specify `true` to keep the stream open.

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

* class [ImageSavingArgs](../)
* namespace [Aspose.Words.Saving](../../imagesavingargs/)
* assembly [Aspose.Words](../../../)
