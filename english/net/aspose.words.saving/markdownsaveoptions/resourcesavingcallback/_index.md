---
title: MarkdownSaveOptions.ResourceSavingCallback
linktitle: ResourceSavingCallback
articleTitle: ResourceSavingCallback
second_title: Aspose.Words for .NET
description: Control how images and resources are saved when exporting Word to Markdown with ResourceSavingCallback for flexible document output.
type: docs
weight: 130
url: /net/aspose.words.saving/markdownsaveoptions/resourcesavingcallback/
---
## MarkdownSaveOptions.ResourceSavingCallback property

Allows to control how resources are saved when a document is exported to Markdown format.

```csharp
public IResourceSavingCallback ResourceSavingCallback { get; set; }
```

## Remarks

Note, there is only one type of resources in Markdown. These are images. When you specify both [`ImageSavingCallback`](../imagesavingcallback/) and `ResourceSavingCallback`, then first is called `ResourceSavingCallback`. However, note it is not necessary to have both implementations, as [`ImageSavingArgs`](../../imagesavingargs/) is actually a subset of [`ResourceSavingArgs`](../../resourcesavingargs/).

## Examples

Shows how to use a callback to change the resource URI.

```csharp
public void ResourceSavingCallback()
{
    string outputPath = ArtifactsDir + "MarkdownSaveOptions.ResourceSavingCallback.md";

    Document doc = new Document(MyDir + "Rendering.docx");

    MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
    saveOptions.ResourceSavingCallback = new ChangeUriPath();

    doc.Save(outputPath, saveOptions);

    DocumentHelper.FindTextInFile(outputPath, "/uri/for/");
}

/// <summary>
/// Class implementing <see cref="IResourceSavingCallback"/>.
/// </summary>
private class ChangeUriPath : IResourceSavingCallback
{
    public void ResourceSaving(ResourceSavingArgs args)
    {
        args.ResourceFileUri = string.Format("/uri/for/{0}", args.ResourceFileName);
    }
}
```

### See Also

* interface [IResourceSavingCallback](../../iresourcesavingcallback/)
* class [MarkdownSaveOptions](../)
* namespace [Aspose.Words.Saving](../../../aspose.words.saving/)
* assembly [Aspose.Words](../../../)
