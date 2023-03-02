---
title: XamlFixedSaveOptions.ResourcesFolderAlias
linktitle: ResourcesFolderAlias
second_title: Aspose.Words for .NET API Reference
description: XamlFixedSaveOptions property. Specifies the name of the folder used to construct image URIs written into an fixed page Xaml document. Default is null in C#.
type: docs
weight: 40
url: /net/aspose.words.saving/xamlfixedsaveoptions/resourcesfolderalias/
---
## XamlFixedSaveOptions.ResourcesFolderAlias property

Specifies the name of the folder used to construct image URIs written into an fixed page Xaml document. Default is `null`.

```csharp
public string ResourcesFolderAlias { get; set; }
```

## Remarks

When you save a [`Document`](../../../aspose.words/document/) in fixed page Xaml format, Aspose.Words needs to save all images embedded in the document as standalone files. [`ResourcesFolder`](../resourcesfolder/) allows you to specify where the images will be saved and `ResourcesFolderAlias` allows to specify how the image URIs will be constructed.

## Examples

Shows how to print the URIs of linked resources created while converting a document to fixed-form .xaml.

```csharp
public void ResourceFolder()
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
}

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
