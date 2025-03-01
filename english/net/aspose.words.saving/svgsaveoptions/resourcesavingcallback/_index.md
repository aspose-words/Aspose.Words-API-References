---
title: SvgSaveOptions.ResourceSavingCallback
linktitle: ResourceSavingCallback
articleTitle: ResourceSavingCallback
second_title: Aspose.Words for .NET
description: Control image resource saving with SvgSaveOptions' ResourceSavingCallback. Optimize SVG exports for better quality and efficiency.
type: docs
weight: 70
url: /net/aspose.words.saving/svgsaveoptions/resourcesavingcallback/
---
## SvgSaveOptions.ResourceSavingCallback property

Allows to control how resources (images) are saved when a document is exported to SVG format.

```csharp
public IResourceSavingCallback ResourceSavingCallback { get; set; }
```

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

* interface [IResourceSavingCallback](../../iresourcesavingcallback/)
* class [SvgSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
