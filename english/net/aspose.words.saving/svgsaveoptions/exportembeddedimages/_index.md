---
title: SvgSaveOptions.ExportEmbeddedImages
second_title: Aspose.Words for .NET API Reference
description: SvgSaveOptions property. Specified whether images should be embedded into SVG document as base64. Note setting this flag can significantly increase size of output SVG file in C#.
type: docs
weight: 20
url: /net/aspose.words.saving/svgsaveoptions/exportembeddedimages/
---
## SvgSaveOptions.ExportEmbeddedImages property

Specified whether images should be embedded into SVG document as base64. Note setting this flag can significantly increase size of output SVG file.

```csharp
public bool ExportEmbeddedImages { get; set; }
```

## Examples

Shows how to manipulate and print the URIs of linked resources created while converting a document to .svg.

```csharp
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
* namespace [Aspose.Words.Saving](../../svgsaveoptions/)
* assembly [Aspose.Words](../../../)
