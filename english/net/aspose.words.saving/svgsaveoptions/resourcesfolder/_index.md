---
title: SvgSaveOptions.ResourcesFolder
linktitle: ResourcesFolder
articleTitle: ResourcesFolder
second_title: Aspose.Words for .NET
description: Discover how to set the ResourcesFolder in SvgSaveOptions for efficient image storage when exporting documents to SVG format. Optimize your workflow today!
type: docs
weight: 80
url: /net/aspose.words.saving/svgsaveoptions/resourcesfolder/
---
## SvgSaveOptions.ResourcesFolder property

Specifies the physical folder where resources (images) are saved when exporting a document to Svg format. Default is `null`.

```csharp
public string ResourcesFolder { get; set; }
```

## Remarks

Has effect only if [`ExportEmbeddedImages`](../exportembeddedimages/) property is `false`.

When you save a [`Document`](../../../aspose.words/document/) in SVG format, Aspose.Words needs to save all images embedded in the document as standalone files. `ResourcesFolder` allows you to specify where the images will be saved and [`ResourcesFolderAlias`](../resourcesfolderalias/) allows to specify how the image URIs will be constructed.

If you save a document into a file and provide a file name, Aspose.Words, by default, saves the images in the same folder where the document file is saved. Use `ResourcesFolder` to override this behavior.

If you save a document into a stream, Aspose.Words does not have a folder where to save the images, but still needs to save the images somewhere. In this case, you need to specify an accessible folder in the `ResourcesFolder` property

## Examples

Shows how to manipulate and print the URIs of linked resources created while converting a document to .svg.

```csharp
public void SvgResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    SvgSaveOptions options = new SvgSaveOptions
    {
        SaveFormat = SaveFormat.Svg,
        ExportEmbeddedImages = false,
        ResourcesFolder = ArtifactsDir + "SvgResourceFolder",
        ResourcesFolderAlias = ArtifactsDir + "SvgResourceFolderAlias",
        ShowPageBorder = false,

        ResourceSavingCallback = new ResourceUriPrinter()
    };

    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "SvgSaveOptions.SvgResourceFolder.svg", options);
}

/// <summary>
/// Counts and prints URIs of resources contained by as they are converted to .svg.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        Console.WriteLine($"Resource #{++mSavedResourceCount} \"{args.ResourceFileName}\"");
        Console.WriteLine("\t" + args.ResourceFileUri);
    }

    private int mSavedResourceCount;
}
```

### See Also

* class [SvgSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
