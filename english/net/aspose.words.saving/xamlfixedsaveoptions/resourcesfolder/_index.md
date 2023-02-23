---
title: XamlFixedSaveOptions.ResourcesFolder
linktitle: ResourcesFolder
second_title: Aspose.Words for .NET API Reference
description: XamlFixedSaveOptions property. Specifies the physical folder where resources images and fonts are saved when exporting a document to fixed page Xaml format. Default is null in C#.
type: docs
weight: 30
url: /net/aspose.words.saving/xamlfixedsaveoptions/resourcesfolder/
---
## XamlFixedSaveOptions.ResourcesFolder property

Specifies the physical folder where resources (images and fonts) are saved when exporting a document to fixed page Xaml format. Default is `null`.

```csharp
public string ResourcesFolder { get; set; }
```

## Remarks

When you save a [`Document`](../../../aspose.words/document/) in fixed page Xaml format, Aspose.Words needs to save all images embedded in the document as standalone files. `ResourcesFolder` allows you to specify where the images will be saved and [`ResourcesFolderAlias`](../resourcesfolderalias/) allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in the same folder where the document file is saved. Use `ResourcesFolder` to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, but still needs to save the images somewhere. In this case, you need to specify an accessible folder by using the `ResourcesFolder` property

## Examples

Shows how to print the URIs of linked resources created while converting a document to fixed-form .xaml.

```csharp
{
    Document doc = new Document(MyDir + "Rendering.docx");
    ResourceUriPrinter callback = new ResourceUriPrinter();

    // Create a "XamlFixedSaveOptions" object, which we can pass to the document's "Save" method
    // to modify how we save the document to the XAML save format.
    XamlFixedSaveOptions options = new XamlFixedSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFixed, options.SaveFormat);

    // Use the "ResourcesFolder" property to assign a folder in the local file system into which
    // Aspose.Words will save all the document's linked resources, such as images and fonts.
    options.ResourcesFolder = ArtifactsDir + "XamlFixedResourceFolder";

    // Use the "ResourcesFolderAlias" property to use this folder
    // when constructing image URIs instead of the resources folder's name.
    options.ResourcesFolderAlias = ArtifactsDir + "XamlFixedFolderAlias";

    options.ResourceSavingCallback = callback;

    // A folder specified by "ResourcesFolderAlias" will need to contain the resources instead of "ResourcesFolder".
    // We must ensure the folder exists before the callback's streams can put their resources into it.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFixedSaveOptions.ResourceFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine(resource);

/// <summary>
/// Counts and prints URIs of resources created during conversion to fixed .xaml.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    public ResourceUriPrinter()
    {
        Resources = new List<string>();
    }

    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        Resources.Add($"Resource \"{args.ResourceFileName}\"\n\t{args.ResourceFileUri}");

        // If we specified a resource folder alias, we would also need
        // to redirect each stream to put its resource in the alias folder.
        args.ResourceStream = new FileStream(args.ResourceFileUri, FileMode.Create);
        args.KeepResourceStreamOpen = false;
    }

    public List<string> Resources { get; }
}
```

### See Also

* class [XamlFixedSaveOptions](../)
* namespace [Aspose.Words.Saving](../../xamlfixedsaveoptions/)
* assembly [Aspose.Words](../../../)
