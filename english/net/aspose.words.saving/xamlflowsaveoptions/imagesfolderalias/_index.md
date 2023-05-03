---
title: XamlFlowSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
second_title: Aspose.Words for .NET API Reference
description: XamlFlowSaveOptions ImagesFolderAlias property. Specifies the name of the folder used to construct image URIs written into an XAML document. Default is an empty string in C#.
type: docs
weight: 40
url: /net/aspose.words.saving/xamlflowsaveoptions/imagesfolderalias/
---
## ImagesFolderAlias property

Specifies the name of the folder used to construct image URIs written into an XAML document. Default is an empty string.

```csharp
public string ImagesFolderAlias { get; set; }
```

## Remarks

When you save a [`Document`](../../../aspose.words/document/) in XAML format, Aspose.Words needs to save all images embedded in the document as standalone files. [`ImagesFolder`](../imagesfolder/) allows you to specify where the images will be saved and `ImagesFolderAlias` allows to specify how the image URIs will be constructed.

If `ImagesFolderAlias` is not an empty string, then the image URI written to XAML will be ImagesFolderAlias + &lt;image file name&gt;.

If `ImagesFolderAlias` is an empty string, then the image URI written to XAML will be ImagesFolder + &lt;image file name&gt;.

If `ImagesFolderAlias` is set to '.' (dot), then the image file name will be written to XAML without path regardless of other options.

## Examples

Shows how to print the filenames of linked images created while converting a document to flow-form .xaml.

```csharp
public void ImageFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ImageUriPrinter callback = new ImageUriPrinter(ArtifactsDir + "XamlFlowImageFolderAlias");

    // Create a "XamlFlowSaveOptions" object, which we can pass to the document's "Save" method
    // to modify how we save the document to the XAML save format.
    XamlFlowSaveOptions options = new XamlFlowSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFlow, options.SaveFormat);

    // Use the "ImagesFolder" property to assign a folder in the local file system into which
    // Aspose.Words will save all the document's linked images.
    options.ImagesFolder = ArtifactsDir + "XamlFlowImageFolder";

    // Use the "ImagesFolderAlias" property to use this folder
    // when constructing image URIs instead of the images folder's name.
    options.ImagesFolderAlias = ArtifactsDir + "XamlFlowImageFolderAlias";

    options.ImageSavingCallback = callback;

    // A folder specified by "ImagesFolderAlias" will need to contain the resources instead of "ImagesFolder".
    // We must ensure the folder exists before the callback's streams can put their resources into it.
    Directory.CreateDirectory(options.ImagesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFlowSaveOptions.ImageFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine($"{callback.ImagesFolderAlias}/{resource}");
}

/// <summary>
/// Counts and prints filenames of images while their parent document is converted to flow-form .xaml.
/// </summary>
private class ImageUriPrinter : IImageSavingCallback
{
    public ImageUriPrinter(string imagesFolderAlias)
    {
        ImagesFolderAlias = imagesFolderAlias;
        Resources = new List<string>();
    }

    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        Resources.Add(args.ImageFileName);

        // If we specified an image folder alias, we would also need
        // to redirect each stream to put its image in the alias folder.
        args.ImageStream = new FileStream($"{ImagesFolderAlias}/{args.ImageFileName}", FileMode.Create);
        args.KeepImageStreamOpen = false;
    }

    public string ImagesFolderAlias { get; }
    public List<string> Resources { get; }
}
```

### See Also

* class [XamlFlowSaveOptions](../)
* namespace [Aspose.Words.Saving](../../xamlflowsaveoptions/)
* assembly [Aspose.Words](../../../)
