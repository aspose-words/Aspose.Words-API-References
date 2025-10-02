---
title: ResourceSavingArgs Class
linktitle: ResourceSavingArgs
articleTitle: ResourceSavingArgs
second_title: Aspose.Words for .NET
description: Discover the Aspose.Words.Saving.ResourceSavingArgs class, which enhances your document processing by providing essential data for the ResourceSaving event.
type: docs
weight: 6400
url: /net/aspose.words.saving/resourcesavingargs/
---
## ResourceSavingArgs class

Provides data for the [`ResourceSaving`](../iresourcesavingcallback/resourcesaving/) event.

To learn more, visit the [Save a Document](https://docs.aspose.com/words/net/save-a-document/) documentation article.

```csharp
public class ResourceSavingArgs
```

## Properties

| Name | Description |
| --- | --- |
| [Document](../../aspose.words.saving/resourcesavingargs/document/) { get; } | Gets the document object that is currently being saved. |
| [KeepResourceStreamOpen](../../aspose.words.saving/resourcesavingargs/keepresourcestreamopen/) { get; set; } | Specifies whether Aspose.Words should keep the stream open or close it after saving a resource. |
| [ResourceFileName](../../aspose.words.saving/resourcesavingargs/resourcefilename/) { get; set; } | Gets or sets the file name (without path) where the resource will be saved to. |
| [ResourceFileUri](../../aspose.words.saving/resourcesavingargs/resourcefileuri/) { get; set; } | Gets or sets the uniform resource identifier (URI) used to reference the resource file from the document. |
| [ResourceStream](../../aspose.words.saving/resourcesavingargs/resourcestream/) { get; set; } | Allows to specify the stream where the resource will be saved to. |

## Remarks

By default, when Aspose.Words saves a document to fixed page HTML, SVG or Markdown, it saves each resource into a separate file. Aspose.Words uses the document file name and a unique number to generate unique file name for each resource found in the document.

`ResourceSavingArgs` allows to redefine how resource file names are generated or to completely circumvent saving of resources into files by providing your own stream objects.

To apply your own logic for generating resource file names use the [`ResourceFileName`](./resourcefilename/) property.

To save resources into streams instead of files, use the [`ResourceStream`](./resourcestream/) property.

## Examples

Shows how to use a callback to track external resources created while converting a document to HTML.

```csharp
public void ResourceSavingCallback()
{
    Document doc = new Document(MyDir + "Bullet points with alternative font.docx");

    FontSavingCallback callback = new FontSavingCallback();

    HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions
    {
        ResourceSavingCallback = callback
    };

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

    Console.WriteLine(callback.GetText());
}

private class FontSavingCallback : IResourceSavingCallback
{
    /// <summary>
    /// Called when Aspose.Words saves an external resource to fixed page HTML or SVG.
    /// </summary>
    public void ResourceSaving(ResourceSavingArgs args)
    {
        mText.AppendLine($"Original document URI:\t{args.Document.OriginalFileName}");
        mText.AppendLine($"Resource being saved:\t{args.ResourceFileName}");
        mText.AppendLine($"Full uri after saving:\t{args.ResourceFileUri}\n");
    }

    public string GetText()
    {
        return mText.ToString();
    }

    private readonly StringBuilder mText = new StringBuilder();
}
```

### See Also

* namespace [Aspose.Words.Saving](../../aspose.words.saving/)
* assembly [Aspose.Words](../../)
