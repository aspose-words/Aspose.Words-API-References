---
title: XamlFlowSaveOptions
second_title: Aspose.Words for .NET API Reference
description: 
type: docs
weight: 10
url: /net/aspose.words.saving/xamlflowsaveoptions/xamlflowsaveoptions/
---
## XamlFlowSaveOptions() {#1}

Initializes a new instance of this class that can be used to save a document in the XamlFlow format.

```csharp
public XamlFlowSaveOptions()
```

### Examples

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

* class [XamlFlowSaveOptions](../../xamlflowsaveoptions)
* namespace [Aspose.Words.Saving](../../xamlflowsaveoptions)
* assembly [Aspose.Words](../../../)

---

## XamlFlowSaveOptions(SaveFormat) {#2}

Initializes a new instance of this class that can be used to save a document in the XamlFlow or XamlFlowPack format.

```csharp
public XamlFlowSaveOptions(SaveFormat saveFormat)
```

| Parameter | Type | Description |
| --- | --- | --- |
| saveFormat | SaveFormat | Can be XamlFlow or XamlFlowPack. |

### Examples

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

* enum [SaveFormat](../../../aspose.words/saveformat)
* class [XamlFlowSaveOptions](../../xamlflowsaveoptions)
* namespace [Aspose.Words.Saving](../../xamlflowsaveoptions)
* assembly [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
